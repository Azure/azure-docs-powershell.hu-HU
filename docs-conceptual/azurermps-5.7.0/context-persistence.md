---
title: Felhasználói bejelentkezések megőrzése a PowerShell-munkamenetek között
description: A cikk az Azure PowerShell új funkcióit ismerteti, amellyel újra felhasználhatók a felhasználók hitelesítési és egyéb adatai az egymást követő PowerShell-munkamenetek során.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 4b2b3b690a8c5d6951b24d49091154c6fb479fe3
ms.sourcegitcommit: 5f0013981fcea1d689649b9a2b2ffe84ae842e56
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2018
---
# <a name="persisting-user-logins-across-powershell-sessions"></a>Felhasználói bejelentkezések megőrzése a PowerShell-munkamenetek között

Az Azure PowerShell 2017. szeptemberi kiadásában az Azure Resource Manager parancsmagjaival bevezettünk egy új szolgáltatást, az **Azure-környezet automatikus mentését**. A szolgáltatás számos új felhasználói forgatókönyvet kínál, a következőket beleértve:

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

A korábbi kiadásokban az új PowerShell-munkamenetek megnyitásakor minden egyes alkalommal létre kellett hozni az Azure-környezetet. Az Azure PowerShell 4.4.0-s verziójától azonban engedélyezheti az Azure-környezet automatikus mentését és egy új PowerShell-munkamenet megnyitásakor való újbóli használatát.

## <a name="automatically-saving-the-context-for-the-next-login"></a>A környezet automatikus mentése a következő bejelentkezéshez

Az Azure PowerShell alapértelmezés szerint a munkamenetek bezárásakor elveti a környezet adatait.

Ha szeretné engedélyezni, hogy az Azure PowerShell megjegyezze a környezet adatait a PowerShell-munkamenetek bezárásakor, használja az `Enable-AzureRmContextAutosave` parancsmagot. A rendszer automatikusan menti a környezet adatait és a hitelesítő adatokat egy speciális rejtett mappába a felhasználó könyvtárában (`%AppData%\Roaming\Windows Azure PowerShell`).
Ezután minden egyes új PowerShell-munkamenet az utolsó munkamenet során használt környezetre irányul majd.

Ha szeretné beállítani, hogy a PowerShell elfelejtse a környezetet és a hitelesítő adatokat, használja a `Disable-AzureRmContextAutoSave` parancsmagot. Ekkor minden alkalommal újra be kell majd jelentkeznie az Azure-ba, amikor megnyit egy PowerShell-munkamenetet.

Az Azure-környezetek kezeléséhez használt parancsmagokkal pontosan szabályozható a működés. Például megadhatja, hogy a módosítások csak az aktuális PowerShell-munkamenetre (`Process` hatókör) vagy minden PowerShell-munkamenetre (`CurrentUser` hatókör) érvényesek legyenek. Ezeket a beállításokat a részletesebben a [Környezeti hatókörök használata](#Using-Context-Scopes) című szakasz tárgyalja.

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Azure PowerShell-parancsmagok futtatása háttérfeladatként

Az **Azure-környezet automatikus mentése** funkcióval megoszthatja a környezetet a PowerShell-háttérfeladatokkal. A PowerShell segítségével a hosszú lefutású feladatokat indíthatja és monitorozhatja háttérfeladatokként is, így nem kell megvárnia, amíg ezek befejeződnek. A hitelesítő adatokat kétféleképpen oszthatja meg a háttérfeladatokkal:

- A környezet átadása argumentumként

  A legtöbb AzureRM-parancsmagba a környezet átadható a parancsmag paramétereként. A környezet a háttérfeladat számára az alábbi példában látható módon adható át:

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- Az alapértelmezett környezet használata működő automatikus mentés mellett

  Ha engedélyezte a **Környezet automatikus mentése** funkciót, a háttérfeladatok automatikusan az alapértelmezett mentett környezetet használják.

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

Ha tájékozódni szeretne egy háttérfeladat kimeneteléről, a `Get-Job` parancsmaggal ellenőrizheti le a feladat állapotát, és a `Wait-Job` parancsmaggal várhatja meg a feladat befejezését. A `Receive-Job` parancsmaggal rögzítheti és jelenítheti meg a háttérfeladat kimenetét. További információkért lásd a [feladatokat ismertető szakaszt](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Környezetek létrehozása, kiválasztása, átnevezése és eltávolítása

Környezetek létrehozásához be kell jelentkeznie az Azure-ba. Az `Connect-AzureRmAccount` parancsmaggal (vagy az aliasával, a `Login-AzureRmAccount` parancsmaggal) állítható be a későbbiekben futtatott Azure PowerShell-parancsmagok által használt alapértelmezett környezet, valamint lehetővé teszi a bejelentkezési hitelesítő adatai számára engedélyezett bérlők vagy előfizetések elérését.

A bejelentkezés után új környezet hozzáadásához használja a `Set-AzureRmContext` parancsmagot (vagy az aliasát, a `Select-AzureRmSubscription` parancsmagot).

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

Az előző példa hozzáad egy új környezetet, amely a „Contoso Subscription 1” nevű előfizetést célozza az aktuális hitelesítő adatokkal. Az új környezet neve „Contoso1”. Ha nem ad meg nevet a környezetnek, a rendszer egy alapértelmezett nevet ad a használt fiók- és előfizetés-azonosító alapján.

Meglévő környezetek átnevezéséhez használja a `Rename-AzureRmContext` parancsmagot. Például:

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

A példa az automatikusan elnevezett `[user1@contoso.org; 123456-7890-1234-564321]` környezetet átnevezi az egyszerű „Contoso2” névre. A környezetek kezelésére szolgáló parancsmagok parancssori kiegészítés funkcióval rendelkeznek, így a beírásukkor gyorsan kiválasztható a környezet.

A környezet a `Remove-AzureRmContext` parancsmaggal távolítható el.  Például:

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

Elfelejti a „Contoso2” nevű környezetet. A környezet ezután a `Set-AzureRmContext` parancsmaggal hozható újra létre

## <a name="removing-credentials"></a>Hitelesítő adatok eltávolítása

Egy adott felhasználó vagy szolgáltatásnév összes hitelesítő adatát és társított környezetét a `Remove-AzureRmAccount` (vagy más néven `Logout-AzureRmAccount`) parancsmaggal távolíthatja el. Paraméterek nélkül a `Remove-AzureRmAccount` parancsmag az aktuális környezetben bejelentkezett felhasználó vagy szolgáltatásnév összes társított hitelesítő adatát és környezetét eltávolítja. A parancsmagnak átadható egy felhasználónév, egyszerű szolgáltatásnév vagy egy környezet is, ha egy adott szolgáltatást kíván megcélozni.

```powershell
Remove-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Környezeti hatókörök használata

Előfordulhat, hogy úgy szeretné kiválasztani, módosítani vagy eltávolítani egy PowerShell-munkamenet valamely környezetét, hogy a többi munkamenetet ne érintse a módosítás. A környezeti parancsmagok alapértelmezett viselkedésének módosításához használja a `Scope` paramétert. A `Process` hatókör felülírja az alapértelmezett viselkedést, hogy csak az aktuális munkamenetre vonatkozzon. A `CurrentUser` hatókör ezzel szemben nemcsak az aktuális, hanem minden munkamenetben módosítja a környezetet.

Ha például anélkül szeretné módosítani az aktuális PowerShell-munkamenet alapértelmezett környezetét, hogy a módosítás a többi ablakot vagy a munkamenet következő megnyitásakor használt környezetet is érintené, használja a következő parancsmagot:

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>A környezet automatikus mentési beállításainak megőrzése

A rendszer a felhasználó Azure PowerShell-könyvtárába (`%AppData%\Roaming\Windows Azure PowerShell`) menti a környezet automatikus mentési beállításait. Előfordulhat, hogy egyes számítógépfiókok nem rendelkeznek hozzáféréshez ehhez a könyvtárhoz. Ilyen esetekben használhatja a következő környezeti változót:

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

Ha a változó értéke „true”, a rendszer automatikusan menti a környezetet. Ha az érték „false”, a rendszer nem menti a környezetet.

## <a name="changes-to-the-azurermprofile-module"></a>Az AzureRM.Profile modul változásai

Új parancsmagok a környezetek kezeléséhez

- [Enable-AzureRmContextAutosave][enable] – A környezet mentésének engedélyezése a PowerShell-munkamenetek között.
  Minden változás módosítja a globális környezetet.
- [Disable-AzureRmContextAutosave][disable] – A környezet automatikus mentésének letiltása. Minden egyes új PowerShell-munkamenetnek újra be kell jelentkeznie.
- [Select-AzureRmContext][select] – Az alapértelmezett környezet kiválasztása. Az ezt követő parancsmagok ennek a környezetnek a hitelesítő adatait használják.
- [Remove-AzureRmAccount][remove-cred] – Adott fiókkal társított összes hitelesítő adat és környezet eltávolítása.
- [Remove-AzureRmContext][remove-context] – A megnevezett környezet eltávolítása.
- [Rename-AzureRmContext][rename] – Meglévő környezet eltávolítása.

Meglévő profilparancsmagok változásai

- [Add-AzureRmAccount][login] – Lehetővé teszi a bejelentkezés hatókörének beállítását a folyamatra vagy az aktuális felhasználóra.
  Lehetővé teszi az alapértelmezett környezet elnevezését a bejelentkezés után.
- [Import-AzureRmContext][import] – Lehetővé teszi a bejelentkezés hatókörének beállítását a folyamatra vagy az aktuális felhasználóra.
- [Set-AzureRmContext][set-context] – Lehetővé teszi meglévő megnevezett környezetek kiválasztását, valamint a hatókör beállítását a folyamatra vagy az aktuális felhasználóra.

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Remove-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Add-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
