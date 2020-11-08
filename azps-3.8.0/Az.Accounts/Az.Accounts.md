---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 7eb19dfc45a954a9e23a3cc6c04190c3a1388547
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013041"
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
Csatlakozás az Azure-hoz hitelesített fiókkal az Azure Resource Manager parancsmag-kérésekkel való használathoz.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Kapcsolja ki az automatikus mentés Azure hitelesítő adatait.  A rendszer a PowerShell-ablak legközelebbi megnyitásakor elfelejti a bejelentkezési adatait

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
A AzurePowerShell-parancsmagok fejlesztéséhez kimarad az adatok gyűjtése. Az adatokat csak akkor gyűjti össze, ha kifejezetten bejelöli.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Letiltja a AzureRm előtag-aliasát az as modulokhoz.

### [Disconnect-AzAccount](Disconnect-AzAccount.md)
Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókkal társított összes hitelesítő adatot és kontextust.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
A PowerShell-ablak megnyitásakor az Azure-hitelesítő adatok, a fiók és az előfizetési adatok menthetők és automatikusan betölthetők. 

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Lehetővé teszi az Azure PowerShell számára az adatok gyűjtését az AzurePowerShell-parancsmagokkal való felhasználói élmény fokozása érdekében.
A parancsmag végrehajtásával az aktuális számítógépen az aktuális felhasználó adatgyűjtési funkciója látható.
Csak akkor gyűjtünk adatokat, ha kifejezetten bekapcsolta.

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

### [Register-AzModule](Register-AzModule.md)
CSAK belső használatra – futásidejű támogatás nyújtása az autorest bővítmények által generált parancsmagok számára.

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

