---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325481"
---
# Az.StorageSync modul
## Leírás
A Tárterület-szinkronizálás modul parancsmagja lehetővé teszi az Azure File Syncre vonatkozó műveletek kezelését a PowerShellben.

## Az.StorageSync-parancsmagok
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Ez a parancs felsorolja egy adott szinkronizálási csoport összes felhőbeli végpontját.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Ez a parancs felsorolja az adott tár szinkronizálási szolgáltatásában található összes szinkronizálási csoportot.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Ez a parancs felsorolja az adott tárhelyszinkronizálási szolgáltatáshoz regisztrált összes kiszolgálót.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Ez a parancs felsorolja egy adott szinkronizálási csoport összes kiszolgálói végpontját.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Ez a parancs felsorolja az adott előfizetési/erőforráscsoporton belüli összes tárterület-szinkronizálási szolgáltatást.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Ezzel a paranccsal manuálisan elindítható a névterek változásainak észlelése. Meg lehet célzottan a teljes megosztásra, almappára vagy fájlkészletre. Legfeljebb 10 000 módosítás észlelhető. Ha ön ismeri a módosítások hatókörét, a parancs végrehajtását a névtér bizonyos részeire korlátozhatja, így a változások észlelése gyorsan befejeződhet, és a 10 000 módosítási korláton belülre eshet.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
A rendszer és az Azure File Sync közötti esetleges kompatibilitási problémákat ellenőrzi.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Ez a parancs visszahívja az összes réteges fájlt a helyi lemezre.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Ez a parancs egy Azure File Sync felhőbeli végpontot hoz létre egy szinkronizálási csoportban.

### [New-AzstorageSyncGroup](New-AzStorageSyncGroup.md)
Ez a parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Ez a parancs új kiszolgáló végpontot hoz létre egy regisztrált kiszolgálón. Ez lehetővé teszi, hogy a kiszolgálón megadott elérési út elindítsa a fájlok szinkronizálását a szinkronizálási csoport más végpontjaival.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Ez a parancs új tárterület-szinkronizálási szolgáltatást hoz létre egy erőforráscsoportban.

### [Set-AzstorageSyncService](New-AzStorageSyncService.md)
Ez a parancs egy tárterület-szinkronizálási szolgáltatást állít be egy erőforráscsoportban.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Ez a parancs regisztrál egy kiszolgálót egy tárterület-szinkronizálási szolgáltatásban, amely megbízhatósági kapcsolatot hoz létre. Ezután a PowerShell vagy az Azure Portal segítségével konfigurálhatja a szinkronizálást ezen a kiszolgálón.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Ez a parancs törli a megadott felhőbeli végpontot egy szinkronizálási csoportból. Legalább egy felhőbeli végpont nélkül a szinkronizálási csoport egyetlen másik kiszolgálói végpontja sem tud szinkronizálni.

### [Remove-AzstorageSyncGroup](Remove-AzStorageSyncGroup.md)
Ez a parancs törli a megadott szinkronizálási csoportot.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Ez a parancs törli a megadott kiszolgálóvégpontot. Az erre a helyre való szinkronizálás azonnal leáll.

### [Remove-AzstorageSyncService](Remove-AzStorageSyncService.md)
Ez a parancs törli a megadott tárterület-szinkronizálási szolgáltatást.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Csak hibaelhárításhoz használható. Ez a parancs roll the storage sync server certificate used to describe the server identity to the storage sync service.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Ez a parancs lehetővé teszi a kiszolgáló végpontjának módosítható paramétereinek módosításait.

### [Unregister-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Figyelmeztetés: A kiszolgáló regisztrációjának törlése kaszkádolt törlést eredményez a kiszolgáló összes kiszolgálói végpontjának. Ez a parancs a kiszolgáló tárhelyszinkronizálási szolgáltatásában való regisztrációját is visszaveszi.

