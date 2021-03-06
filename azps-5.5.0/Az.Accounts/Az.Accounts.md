---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 6be8097fb649b6ebdec1c6dc5f28f2a06c572d35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159891"
---
# Az.Accounts modul
## Leírás
Kezeli az összes Azure-modul hitelesítő adatait és közös konfigurációját.

## Az.Accounts parancsmagok
### [Add-AzEnvironment](Add-AzEnvironment.md)
Végpontokat és metaadatokat ad hozzá az Azure Resource Manager egy példányához.

### [Clear-AzContext](Clear-AzContext.md)
Távolítsa el az Összes Azure-hitelesítő adatokat, fiókot és előfizetési információt.

### [Clear-AzDefault](Clear-AzDefault.md)
Törli a felhasználó által az aktuális környezetben beállított alapértelmezett értékeket.

### [Connect-AzAccount](Connect-AzAccount.md)
Csatlakozzon az Azure-hoz egy hitelesített fiókkal az Az PowerShell-modulok parancsmagjaival való használathoz.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Kapcsolja ki az Azure-beli hitelesítő adatok automatikus mentését.  A bejelentkezési adatok a PowerShell-ablak következő megnyitásakor elfelejtkednek

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
Az Azure PowerShell-parancsmagok fejlesztése érdekében leiratkozás az adatgyűjtésről. Az adatokat alapértelmezés szerint gyűjtjük, hacsak Ön kifejezetten nem tiltja le.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Letiltja az AzureRm előtag-aliasokat az Az modulokhoz.

### [Disconnect-AzAccount](Disconnect-AzAccount.md)
Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja a fiókkal társított összes hitelesítő adatokat és kontextust.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
A PowerShell-ablak megnyitásakor a rendszer menti és automatikusan betölti az Azure-beli hitelesítő adatokat, fiók- és előfizetésadatokat. 

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Lehetővé teszi, hogy az Azure PowerShell adatokat gyűjtsön az Azure PowerShell-parancsmagok felhasználói élményének javításához. A parancsmag végrehajtása az aktuális gép aktuális felhasználója számára is be fog jelentkezni az adatgyűjtésbe. Az adatokat alapértelmezés szerint gyűjtjük, hacsak Ön kifejezetten nem tiltja le.

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
Engedélyezi az AzureRm előtag-aliasokat az Az-modulokhoz.

### [Get-AzAccessToken](Get-AzAccessToken.md)
Nyers hozzáférési jogkivonat beszerzése.

### [Get-AzContext](Get-AzContext.md)
Az Azure Resource Manager-kérelmek hitelesítéséhez használt metaadatok bekérése.

### [Get-AzContextAutosaveSetting](Get-AzContextAutosaveSetting.md)
A környezet automatikus mentésének funkciójának metaadatainak megjelenítése, beleértve a környezet automatikus mentésének és a mentett környezet és hitelesítő adatok helyének megjelenítését.

### [Get-AzDefault](Get-AzDefault.md)
Szerezze be a felhasználó által az aktuális környezetben beállított alapértelmezett értékeket.

### [Get-AzEnvironment](Get-AzEnvironment.md)
Végpontok és metaadatok lekérte az Azure-szolgáltatások egy példányát.

### [Get-AzSubscription](Get-AzSubscription.md)
Szerezze be az aktuális fiók által elérhető előfizetéseket.

### [Get-AzTenant](Get-AzTenant.md)
Az aktuális felhasználóhoz engedélyezett bérlőket kapja meg.

### [Import-AzContext](Import-AzContext.md)
Egy fájlból betölti az Azure-hitelesítési adatokat.

### [Invoke-AzRestMethod](Invoke-AzRestMethod.md)
Kizárólag Azure-erőforrás-kezelési végpontra vonatkozó HTTP-kérések építése és végrehajtása

### [Register-AzModule](Register-AzModule.md)
CSAK BELSŐ HASZNÁLAT ESETÉN – Futásidejű támogatás az AutoRest által létrehozott parancsmagok számára

### [Remove-AzContext](Remove-AzContext.md)
Környezet eltávolítása az elérhető környezetek készletből

### [Remove-AzEnvironment](Remove-AzEnvironment.md)
Eltávolítja az adott Azure-példányhoz való csatlakozás végpontját és metaadatait.

### [Átnevezés-AzContext](Rename-AzContext.md)
Azure-környezet átnevezése  Az alapértelmezett környezetek neve felhasználói fiók és előfizetés szerint van elnevezve.

### [Resolve-AzError](Resolve-AzError.md)
Részletes információkat jelenít meg a PowerShell-hibákról, az Azure PowerShell-hibák részletes adataival együtt.

### [Save-AzContext](Save-AzContext.md)
Menti az aktuális hitelesítési adatokat más PowerShell-munkamenetekben való használatra.

### [Select-AzContext](Select-AzContext.md)
Válassza ki a megcél kívánt előfizetést és fiókot az Azure PowerShell-parancsmagokkal

### [Visszajelzés küldése](Send-Feedback.md)
Visszajelzést küld az Azure PowerShell-csapatnak interaktív üzenetekkel.

### [Set-AzContext](Set-AzContext.md)
Beállítja a parancsmagok bérlői, előfizetési és környezetét az aktuális munkamenetben való használatra.

### [Set-AzDefault](Set-AzDefault.md)
Alapértelmezett beállítás az aktuális környezetben

### [Set-AzEnvironment](Set-AzEnvironment.md)
Beállítja egy Azure-környezet tulajdonságait.

### [Uninstall-AzureRm](Uninstall-AzureRm.md)
Eltávolítja az összes AzureRm-modult egy gépről.

