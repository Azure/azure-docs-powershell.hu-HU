---
title: Azure-környezetek és bejelentkezési hitelesítő adatok
description: A cikkből megismerheti, hogyan használhatók fel újra az Azure-beli hitelesítő és egyéb adatok több PowerShell-munkamenet során.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: c79d1d634d5b76b2c6ab6b6ab309c2d49f9f7678
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/14/2020
ms.locfileid: "86382066"
---
# <a name="azure-powershell-context-objects"></a>Azure PowerShell környezeti objektumok

Az Azure PowerShell _Azure PowerShell környezeti objektumokat_ (Azure-környezeteket) használ az előfizetési és a hitelesítési információk tárolására. Ha több előfizetéssel is rendelkezik, az Azure-környezetekben kiválaszthatja azt az előfizetést, amelyben futtatni szeretné az Azure PowerShell-parancsmagokat. Az Azure-környezetek a bejelentkezési adatok több PowerShell-munkamenetre kiterjedő tárolására, illetve a háttérfeladatok futtatására is használhatók.

Ez a cikk az Azure-környezetek kezelését ismerteti, az előfizetések és a fiókok kezelésére nem tér ki. Ha felhasználók, előfizetések, bérlők vagy más fiókadatok kezelése iránt érdeklődik, tekintse át az [Azure Active Directory](/azure/active-directory) dokumentációját. A környezetek háttér- vagy párhuzamos feladatok futtatására való használatával kapcsolatban tekintse meg [az Azure PowerShell-parancsmagok PowerShell-feladatokban való használatát](using-psjobs.md) ismertető cikket, miután megismerkedett az Azure-környezetekkel.

## <a name="overview-of-azure-context-objects"></a>Az Azure-beli környezeti objektumok áttekintése

Az Azure-környezetek olyan PowerShell-objektumok, amelyek a parancsok futtatásához kiválasztott aktív előfizetést, illetve az Azure-felhőkhöz való csatlakozáshoz szükséges hitelesítő adatokat képviselik. Az Azure-környezeteknek köszönhetően az Azure PowerShellnek nem kell az előfizetések közötti váltáskor újból és újból hitelesítenie a fiókját. Az Azure-környezetek a következőkből állnak:

* A _fiókból_, amelyet az Azure-ba való bejelentkezéshez használt a [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) parancsmaggal. Az Azure-környezetek a fiókok szempontjából ugyanúgy kezelik a felhasználókat, az alkalmazásazonosítókat és a szolgáltatásneveket.
* Az aktív _előfizetésből_, azaz egy adott _bérlőhöz_ társított Azure-erőforrások létrehozására és futtatására vonatkozó, Microsofttal kötött szolgáltatási szerződésből. A bérlőket gyakran _szervezeteknek_ is nevezik a dokumentációkban vagy az Active Directory használata során.
* Egy _jogkivonat-gyorsítótárra_, azaz egy, az Azure-felhők elérésére használt, tárolt hitelesítési jogkivonatra mutató hivatkozásból. A [környezet automatikus mentésére vonatkozó beállítások](#save-azure-contexts-across-powershell-sessions) határozzák meg, hogy a rendszer hol tárolja és mennyi ideig őrzi meg a jogkivonatot.

A kifejezésekkel kapcsolatos további információkért lásd [az Azure Active Directory terminológiáját](/azure/active-directory/fundamentals/active-directory-whatis#terminology). Az Azure-környezetek által használt hitelesítési jogkivonatok ugyanolyanok, mint az állandó munkamenet részét képező többi tárolt jogkivonat. 

Amikor bejelentkezik a `Connect-AzAccount` parancsmaggal, a rendszer legalább egy Azure-környezetet létrehoz az alapértelmezett előfizetéshez. A `Connect-AzAccount` által visszaadott objektum a PowerShell-munkamenet hátralévő részéhez használt alapértelmezett Azure-környezet.

## <a name="get-azure-contexts"></a>Azure-környezetek lekérése

Az elérhető Azure-környezeteket a [Get-AzContext](/powershell/module/az.accounts/get-azcontext) parancsmaggal lehet lekérni. Az összes elérhető környezetet a `-ListAvailable` argumentummal lehet megjeleníteni:

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

Azt is megteheti, hogy név alapján kér le egy környezetet:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

A környezetek nevei eltérhetnek a társított előfizetés nevétől.

> [!IMPORTANT]
> Az elérhető Azure-környezetek __nem__ mindig azonosak az elérhető előfizetésekkel. Az Azure-környezetek csak a helyben tárolt adatokat jelölik. Az előfizetéseit a [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) parancsmaggal kérheti le.

## <a name="create-a-new-azure-context-from-subscription-information"></a>Új Azure-környezet létrehozása előfizetési adatokból

A [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) parancsmaggal új Azure-környezeteket hozhat létre, és be is állíthatja őket aktív környezetként.
Az új Azure-környezetek létrehozásának legegyszerűbb módja a meglévő előfizetési adatok használata. A parancsmagot arra tervezték, hogy átirányított értékként kivegye a `Get-AzSubscription` kimeneti objektumát, és konfiguráljon egy új Azure-környezetet:

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

Azt is megteheti, hogy megadja az előfizetés nevét vagy azonosítóját, és szükség esetén a bérlőazonosítót:

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

Ha a `-Name` argumentum kimarad, a rendszer az előfizetés nevét és azonosítóját használja a környezet neveként, `Subscription Name (subscription-id)` formátumban.

## <a name="change-the-active-azure-context"></a>Az aktív Azure-környezet módosítása

Az aktív Azure-környezetet a `Set-AzContext` és a [Select-AzContext](/powershell/module/az.accounts/set-azcontext) parancsmaggal is meg lehet változtatni. Az [új Azure-környezet létrehozásával](#create-a-new-azure-context-from-subscription-information) foglalkozó szakaszban leírtak szerint a `Set-AzContext` létrehoz egy új Azure-környezetet egy előfizetéshez, ha annak még nincs környezete, majd beállítja aktívként.

A `Select-AzContext` csak a meglévő Azure-környezetekkel használható. Hasonlóan működik, mint a `Set-AzContext -Context`, de átadáshoz tervezték:

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

Az Azure PowerShell számos más fiók- és környezetkezelési parancsához hasonlóan a `Set-AzContext` és a `Select-AzContext` támogatja a `-Scope` argumentumot, így Ön szabályozhatja, hogy mennyi ideig legyen aktív a környezet. A `-Scope` argumentummal meg lehet változtatni egyetlen munkamenet aktív környezetét, az alapértelmezett érték módosítása nélkül:

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

Ha el szeretné kerülni, hogy a rendszer a teljes PowerShell-munkamenetre vonatkozóan lecserélje a környezetet, az Azure PowerShell-parancsokat egy adott környezetben is futtathatja az `-AzContext` argumentummal:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

A környezetek Azure PowerShell-parancsmagokkal való használatának másik fő felhasználási módja a parancsok háttérbeli futtatása. A PowerShell-feladatok Azure PowerShell-lel történő futtatásával kapcsolatos további információkért lásd: [Azure PowerShell-parancsmagok futtatása PowerShell-feladatokban](using-psjobs.md).

## <a name="save-azure-contexts-across-powershell-sessions"></a>Azure-környezetek több PowerShell-munkamenetre kiterjedő mentése

A rendszer alapértelmezés szerint menti az Azure-környezeteket, hogy több PowerShell-munkamenetben is használhatók legyenek. Az alábbiak szerint módosíthatja ezt a viselkedést:

* Jelentkezzen be a `-Scope Process` és a `Connect-AzAccount` használatával.

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  A bejelentkezés részeként visszaadott Azure-környezet _csak_ az aktuális munkamenetre érvényes, és a rendszer az Azure PowerShell-környezet automatikus mentési beállításától függetlenül nem fogja automatikusan menteni.
* Tiltsa le az Azure PowerShell környezeteinek automatikus mentését a [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) parancsmaggal.
  A környezet automatikus mentésének letiltása __nem__ törli a tárolt jogkivonatokat. A tárolt Azure-beli környezeti adatok törlésével kapcsolatban lásd az [Azure-környezetek és hitelesítő adatok eltávolításával](#remove-azure-contexts-and-stored-credentials) foglalkozó szakaszt.
* Explicit módon engedélyezze az Azure-környezet automatikus mentését. Ezt az [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) parancsmaggal teheti meg. Ha engedélyezte az automatikus mentést, a rendszer helyben fogja tárolni a felhasználó környezeteit a későbbi PowerShell-munkamenetek számára.
* Mentse manuálisan a környezeteket a [Save-AzContext](/powershell/module/az.accounts/save-azcontext) parancsmaggal a későbbi PowerShell-munkamenetekben való használathoz, amelyekbe az [Import-AzContext](/powershell/module/az.accounts/import-azcontext) parancsmaggal tölthetők be:

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> A környezet automatikus mentésének letiltása __nem__ törli a mentett környezeti adatokat. A tárolt adatok eltávolításához használja a [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) parancsmagot. A mentett környezetek eltávolításával kapcsolatos további információkért lásd a [környezetek és hitelesítő adatok eltávolításával](#remove-azure-contexts-and-stored-credentials) foglalkozó szakaszt.

Mindegyik parancs támogatja a `-Scope` paramétert, ami fel tudja venni a `Process` értéket, hogy csak a jelenleg futó folyamatra vonatkozzon. Adja meg például a következőt, ha gondoskodni szeretne róla, hogy a rendszer ne mentse az újonnan létrehozott környezeteket a PowerShell-munkamenetből való kilépés után:

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

A Windows az `$env:USERPROFILE\.Azure` könyvtárban tárolja a környezetek adatait és a jogkivonatokat, más platformok pedig a `$HOME/.Azure` könyvtárban. Előfordulhat, hogy a tárolt adatok között megtalálható bizalmas adatokat, például az előfizetési azonosítókat és bérlőazonosítókat továbbra is el lehet érni a naplókon vagy a mentett környezeteken keresztül. A tárolt adatok törlésével kapcsolatban tekintse meg a [környezetek és hitelesítő adatok eltávolítását](#remove-azure-contexts-and-stored-credentials) ismertető szakaszt.

## <a name="remove-azure-contexts-and-stored-credentials"></a>Az Azure-környezetek és a tárolt hitelesítő adatok eltávolítása

Azure-környezetek és hitelesítő adatok törlése:

* Jelentkezzen ki a fiókból a [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount) parancsmaggal.
  Bármely fiókból kijelentkezhet a fiók vagy a környezet megadásával:

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  A kapcsolat bontásakor a rendszer mindig eltávolítja a tárolt hitelesítési jogkivonatokat, és törli a leválasztott felhasználóhoz vagy környezethez társított mentett környezeteket.
* Használja a [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) parancsmagot. Ez a parancsmag garantáltan mindig eltávolítja a tárolt környezeteket és hitelesítési jogkivonatokat, és a felhasználót is kilépteti.
* Távolítson el egy környezetet a [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext) parancsmaggal:
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  Ha eltávolítja az aktív környezetet, a rendszer bontja a kapcsolatot az Azure-ral, és Önnek újból hitelesítenie kell magát a `Connect-AzAccount` parancsmaggal.

## <a name="see-also"></a>Lásd még

* [Azure PowerShell-parancsmagok futtatása PowerShell-feladatokban](using-psjobs.md)
* [Az Azure Active Directory terminológiája](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Az.Accounts referencia](/powershell/module/az.accounts)
