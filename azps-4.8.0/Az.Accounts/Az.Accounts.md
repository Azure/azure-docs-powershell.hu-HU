---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: d15e053e8801c292add5a80e04726f1eeb1181fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180700"
---
# Az Accounts (fiókok) modul
## Leírás
Minden Azure-modul hitelesítő adatait és általános konfigurációját kezeli.

## Az. accounts parancsmagok
### [Add-AzEnvironment](Add-AzEnvironment.md)
Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.

### [Clear-AzContext](Clear-AzContext.md)
Az összes Azure-hitelesítőadat,-fiók és-előfizetés adatainak eltávolítása

### [Clear-AzDefault](Clear-AzDefault.md)
Törli a felhasználó által az aktuális környezetben beállított alapértékeket.

### [Connect-AzAccount](Connect-AzAccount.md)
Csatlakozás az Azure-hoz hitelesített fiókkal a PowerShell-modulokból származó parancsmagokkal való használathoz.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.  A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
Az Azure PowerShell-parancsmagok fejlesztésére az adatok gyűjtésének kijavítása. Az adatokat alapértelmezés szerint gyűjtjük, hacsak nem kifejezetten kikapcsolja.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Letiltja a AzureRm előtag-aliasát az as modulokhoz.

### [Disconnect-AzAccount](Disconnect-AzAccount.md)
Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókkal társított összes hitelesítő adatot és kontextust.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők. 

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az Azure PowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében. A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható. Az adatokat alapértelmezés szerint gyűjtjük, hacsak nem kifejezetten kikapcsolja.

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
Engedélyezi a AzureRm előtag-aliasát az as modulokhoz.

### [Get-AzContext](Get-AzContext.md)
Az Azure Resource Manager-kérések hitelesítéséhez használt metaadatot kapja meg.

### [Get-AzContextAutosaveSetting](Get-AzContextAutosaveSetting.md)
Metaadatok megjelenítése a környezeti mentés funkcióról, például hogy a környezet automatikusan mentve van-e, illetve hogy hol találhatók a mentett környezet-és hitelesítőadat-adatok.

### [Get-AzDefault](Get-AzDefault.md)
A felhasználó által az aktuális környezetben beállított alapértékek beszerzése.

### [Get-AzEnvironment](Get-AzEnvironment.md)
Az Azure Services egy példányának végpontját és metaadatait kapja meg.

### [Get-AzProfile](Get-AzProfile.md)
A telepített modulok által támogatott szolgáltatásprofilok beszerzése.

### [Get-AzSubscription](Get-AzSubscription.md)
Az aktuális fiók által elérhető előfizetések beszerzése.

### [Get-AzTenant](Get-AzTenant.md)
Az aktuális felhasználótól kapott bérlői fiókokat kapja.

### [Importálás – AzContext](Import-AzContext.md)
Azure-hitelesítési adatok betöltése egy fájlból.

### [Meghívó-AzRestMethod](Invoke-AzRestMethod.md)
HTTP-kérés létesítése és végrehajtása csak az Azure erőforrás-kezelési végponttal

### [Register-AzModule](Register-AzModule.md)
CSAK belső használatra – futásidejű támogatás nyújtása az autorest bővítmények által generált parancsmagokhoz

### [Remove-AzContext](Remove-AzContext.md)
Környezet eltávolítása az elérhető környezetek halmazból

### [Remove-AzEnvironment](Remove-AzEnvironment.md)
Eltávolítja az adott Azure-példányhoz való csatlakozáshoz szükséges végpontokat és metaadatokat.

### [Rename-AzContext](Rename-AzContext.md)
Azure-környezet átnevezése  Alapértelmezés szerint a kontextusokat felhasználói fiók és előfizetés szerint nevezi el a program.

### [Feloldás – AzError](Resolve-AzError.md)
Részletes információk megjelenítése a PowerShell-hibákról, az Azure PowerShell hibáinak meghosszabbításával.

### [Mentés-AzContext](Save-AzContext.md)
Az aktuális hitelesítési adatokat menti a többi PowerShell-munkamenetben való használatra.

### [Select-AzContext](Select-AzContext.md)
Előfizetés és fiók kiválasztása az Azure PowerShell-parancsmagokban

### [Select-AzProfile](Select-AzProfile.md)
Több szolgáltatásprofilt támogató modulok esetén – a megadott szolgáltatásprofil megfelelő parancsmagok behelyezése.

### [Visszajelzés küldése](Send-Feedback.md)
Visszajelzést küld az Azure PowerShell-csoportnak egy sor interaktív utasítással.

### [Set-AzContext](Set-AzContext.md)
A bérlői fiók, az előfizetés és a környezet beállítása az aktuális munkamenetben használható parancsmagok esetében.

### [Set-AzDefault](Set-AzDefault.md)
Alapértelmezett érték beállítása az aktuális környezetben

### [Set-AzEnvironment](Set-AzEnvironment.md)
Az Azure-környezet tulajdonságainak beállítása.

### [Eltávolítás – AzureRm](Uninstall-AzureRm.md)
Eltávolítja az összes AzureRm-modult egy gépről.

