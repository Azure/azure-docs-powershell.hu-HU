---
title: Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között
description: A cikkből megismerheti, hogyan használhatók fel újra az Azure-beli hitelesítő és egyéb adatok több PowerShell-munkamenet során.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 8702de48429482748939fb1a43ff911bed15f6c0
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153799"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a>Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között

Az Azure PowerShell új, **Azure-környezet automatikus mentése** nevű funkciója a következő szolgáltatásokat nyújtja:

- A bejelentkezési adatok megőrzése és ismételt használata az új PowerShell-munkamenetekben.
- A háttérfeladatok egyszerűbb használata a hosszú ideig futó parancsmagok végrehajtásához.
- Váltás a fiókok, előfizetések és környezet között külön bejelentkezés nélkül.
- Feladatok egyidejű végrehajtása több bejelentkezés és előfizetés használatával ugyanabból a PowerShell-munkamenetből.

## <a name="azure-contexts-defined"></a>Az Azure-környezetek

Az *Azure-környezet* az Azure PowerShell-parancsmagok célját meghatározó adatok halmaza. A környezet öt részből áll:

- A *Fiók* – Az Azure-beli kommunikáció hitelesítéséhez használt felhasználónév vagy szolgáltatásnév
- Az *előfizetés* – Az adott erőforrásokat tartalmazó Azure-előfizetés, amelyre a műveletek irányulnak.
- A *bérlő* – Az előfizetést tartalmazó Azure Active Directory-bérlő. A bérlők a szolgáltatásnévvel való hitelesítés során fontosabbak.
- A *környezet* – A célzott Azure-felhő, általában az Azure globális felhője.
  A környezetbeállításban azonban megadhat országos, kormányzati és helyszíni (Azure Stack) felhőket is.
- A *hitelesítő adatok* – Az Azure által az identitás és az Azure-erőforrások hozzáférési jogosultságának ellenőrzéséhez használt adatok.

Az Azure PowerShell legújabb verziójában új PowerShell-munkamenet megnyitásakor beállítható az Azure-környezetek automatikus mentése.

## <a name="automatically-save-the-context-for-the-next-sign-in"></a>A környezet automatikus mentése a következő bejelentkezéshez

Az Azure PowerShell automatikusan megőrzi a környezet adatait a munkamenetek között. Ha szeretné beállítani, hogy a PowerShell elfelejtse a környezetet és a hitelesítő adatokat, használja a `Disable-AzContextAutoSave` parancsmagot. Ha le van tiltva a környezet mentése, minden alkalommal be kell jelentkeznie az Azure-ba, amikor megnyit egy PowerShell-munkamenetet.

Ha szeretné engedélyezni, hogy az Azure PowerShell megjegyezze a környezet adatait a PowerShell-munkamenetek bezárásakor, használja az `Enable-AzContextAutosave` parancsmagot. A rendszer automatikusan menti a környezet adatait és a hitelesítő adatokat egy speciális rejtett mappába a felhasználó könyvtárában (`$env:USERPROFILE\.Azure` Windows rendszeren és `$HOME/.Azure` más platformokon). Minden egyes új PowerShell-munkamenet az utolsó munkamenet során használt környezetre irányul.

Az Azure-környezetek kezeléséhez használt parancsmagokkal pontosan szabályozható a működés. Például megadhatja, hogy a módosítások csak az aktuális PowerShell-munkamenetre (`Process` hatókör) vagy minden PowerShell-munkamenetre (`CurrentUser` hatókör) érvényesek legyenek. Ezeket a beállításokat részletesebben a [Környezeti hatókörök használata](#Using-Context-Scopes) című szakasz tárgyalja.

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Azure PowerShell-parancsmagok futtatása háttérfeladatként

Az **Azure-környezet automatikus mentése** funkcióval megoszthatja a környezetet a PowerShell-háttérfeladatokkal. A PowerShell segítségével a hosszú lefutású feladatokat indíthatja és monitorozhatja háttérfeladatokként is, így nem kell megvárnia, amíg ezek befejeződnek. A hitelesítő adatokat kétféleképpen oszthatja meg a háttérfeladatokkal:

- A környezet átadása argumentumként

  A legtöbb AzureRM-parancsmagba a környezet átadható a parancsmag paramétereként. A környezet a háttérfeladat számára az alábbi példában látható módon adható át:

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- Az alapértelmezett környezet használata működő automatikus mentés mellett

  Ha engedélyezte a **Környezet automatikus mentése** funkciót, a háttérfeladatok automatikusan az alapértelmezett mentett környezetet használják.

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

Ha tájékozódni szeretne egy háttérfeladat kimeneteléről, a `Get-Job` parancsmaggal ellenőrizheti le a feladat állapotát, és a `Wait-Job` parancsmaggal várhatja meg a feladat befejezését. A `Receive-Job` parancsmaggal rögzítheti és jelenítheti meg a háttérfeladat kimenetét. További információkért lásd a [feladatokat ismertető szakaszt](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Környezetek létrehozása, kiválasztása, átnevezése és eltávolítása

Környezetek létrehozásához be kell jelentkeznie az Azure-ba. Az `Connect-AzAccount` parancsmag (vagy az aliasa, a `Login-AzAccount` parancsmag) beállítja az Azure PowerShell-parancsmagok által használt alapértelmezett környezetet, valamint lehetővé teszi a bejelentkezési hitelesítő adatai számára engedélyezett bérlők vagy előfizetések elérését.

A bejelentkezés után új környezet hozzáadásához használja a `Set-AzContext` parancsmagot (vagy az aliasát, a `Select-AzSubscription` parancsmagot).

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

Az előző példa hozzáad egy új környezetet, amely a „Contoso Subscription 1” nevű előfizetést célozza az aktuális hitelesítő adatokkal. Az új környezet neve „Contoso1”. Ha nem ad meg nevet a környezetnek, a rendszer egy alapértelmezett nevet ad a használt fiók- és előfizetés-azonosító alapján.

Meglévő környezetek átnevezéséhez használja a `Rename-AzContext` parancsmagot. Például:

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

A példa az automatikusan elnevezett `[user1@contoso.org; 123456-7890-1234-564321]` környezetet átnevezi az egyszerű „Contoso2” névre. A környezetek kezelésére szolgáló parancsmagok parancssori kiegészítés funkcióval rendelkeznek, így a beírásukkor gyorsan kiválasztható a környezet.

A környezet a `Remove-AzContext` parancsmaggal távolítható el.  Például:

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

Elfelejti a „Contoso2” nevű környezetet. A környezet a `Set-AzContext` parancsmaggal hozható újra létre

## <a name="removing-credentials"></a>Hitelesítő adatok eltávolítása

Egy adott felhasználó vagy szolgáltatásnév összes hitelesítő adatát és társított környezetét a `Disconnect-AzAccount` (vagy más néven `Logout-AzAccount`) parancsmaggal távolíthatja el. Paraméterek nélkül a `Disconnect-AzAccount` parancsmag az aktuális környezetben bejelentkezett felhasználó vagy szolgáltatásnév összes társított hitelesítő adatát és környezetét eltávolítja. A parancsmagnak átadható egy felhasználónév, egyszerű szolgáltatásnév vagy egy környezet is, ha egy adott szolgáltatást kíván megcélozni.

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Környezeti hatókörök használata

Előfordulhat, hogy úgy szeretné kiválasztani, módosítani vagy eltávolítani egy PowerShell-munkamenet valamely környezetét, hogy a többi munkamenetet ne érintse a módosítás. A környezeti parancsmagok alapértelmezett viselkedésének módosításához használja a `Scope` paramétert. A `Process` hatókör felülírja az alapértelmezett viselkedést, hogy csak az aktuális munkamenetre vonatkozzon. A `CurrentUser` hatókör ezzel szemben nemcsak az aktuális, hanem minden munkamenetben módosítja a környezetet.

Ha például anélkül szeretné módosítani az aktuális PowerShell-munkamenet alapértelmezett környezetét, hogy a módosítás a többi ablakot vagy a munkamenet következő megnyitásakor használt környezetet is érintené, használja a következő parancsmagot:

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>A környezet automatikus mentési beállításainak megőrzése

A rendszer a felhasználó Azure PowerShell-könyvtárába (`$env:USERPROFILE\.Azure` Windows rendszeren és `$HOME/.Azure` más platformokon) menti a környezet automatikus mentési beállításait. Előfordulhat, hogy egyes számítógépfiókok nem rendelkeznek hozzáféréshez ehhez a könyvtárhoz. Ilyen esetekben használhatja a következő környezeti változót:

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

Ha a változó értéke „true”, a rendszer automatikusan menti a környezetet. Ha az érték „false”, a rendszer nem menti a környezetet.

## <a name="context-management-cmdlets"></a>Környezet kezelésének parancsmagjai

- [Enable-AzContextAutosave][enable] – A környezet mentésének engedélyezése a PowerShell-munkamenetek között.
  Minden változás módosítja a globális környezetet.
- [Disable-AzContextAutosave][disable] – A környezet automatikus mentésének letiltása. Minden egyes új PowerShell-munkamenetnek újra be kell jelentkeznie.
- [Select-AzContext][select] – Az alapértelmezett környezet kiválasztása. Az összes parancsmag ennek a környezetnek a hitelesítő adatait használja.
- [Disconnect-AzAccount][remove-cred] – Egy fiókhoz tartozó összes hitelesítő adat és környezet eltávolítása.
- [Remove-AzContext][remove-context] – Egy elnevezett környezet eltávolítása.
- [Rename-AzContext][rename] – Meglévő környezet átnevezése.
- [Add-AzAccount][login] – Lehetővé teszi a bejelentkezés hatókörének beállítását a folyamatra vagy az aktuális felhasználóra.
  Lehetővé teszi az alapértelmezett környezet elnevezését a bejelentkezés után.
- [Import-AzContext][import] – Lehetővé teszi a bejelentkezés hatókörének beállítását a folyamatra vagy az aktuális felhasználóra.
- [Set-AzContext][set-context] – Lehetővé teszi meglévő elnevezett környezetek kiválasztását, valamint a hatókör módosítását a folyamatra vagy az aktuális felhasználóra.

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
