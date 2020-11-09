---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302951"
---
# Az. StorageSync modul
## Leírás
A tárterület-szinkronizálási modulban lévő parancsmagok segítségével kezelheti az Azure-fájlok szinkronizálásához használható műveleteket a PowerShellben.

## Az. StorageSync parancsmagok
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Ez a parancs felsorolja az összes Felhőbeli végpontot egy adott szinkronizálási csoporton belül.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Ez a parancs felsorolja az összes szinkronizálási csoportot egy adott tárterület-szinkronizálási szolgáltatáson belül.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Ez a parancs felsorolja az összes olyan kiszolgálót, amely egy adott tárterület-szinkronizálási szolgáltatáshoz van regisztrálva.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Ez a parancs felsorolja az összes kiszolgáló-végpontot egy adott szinkronizálási csoporton belül.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Ez a parancs felsorolja az összes tárterület-szinkronizálási szolgáltatást az előfizetés/erőforrás csoport adott hatókörén belül.

### [Meghívó-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Ez a parancs segítségével manuálisan indíthatja el a névterek változásainak észlelését. A cél a teljes megosztás, az almappa vagy a fájlok halmaza lehet. A 10 000-es módosítások maximális száma észlelhető. Ha a változtatások köre ismert Önnek, akkor korlátozhatja a parancs végrehajtását a névtér részeire, így a változtatások észlelése gyorsan elvégezhető, és egy 10 000-módosítási korláton belül.

### [Meghívó-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Ellenőrzi, hogy milyen kompatibilitási problémákat tapasztal a rendszer és az Azure-fájlok szinkronizálása között.

### [Meghívó-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Ez a parancs visszahívja az összes többszintű fájlt a helyi merevlemezre.

### [Új – AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Ez a parancs Azure-szinkronizálási Felhőbeli végpontot hoz létre a szinkronizálási csoportban.

### [Új – AzStorageSyncGroup](New-AzStorageSyncGroup.md)
A parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.

### [Új – AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Ez a parancs létrehoz egy új kiszolgálói végpontot egy regisztrált kiszolgálón. Ez a beállítás lehetővé teszi a kiszolgálón megadott elérési út szinkronizálását a fájlok más végpontokkal való szinkronizálásának megkezdéséhez a szinkronizálás csoportban.

### [Új – AzStorageSyncService](New-AzStorageSyncService.md)
A parancs új tárterület-szinkronizálási szolgáltatást hoz létre egy erőforráscsoportben.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Ez a parancs egy erőforrás-csoportban tárol egy tárterület-szinkronizálási szolgáltatást.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Ez a parancs a kiszolgálót egy olyan tárterület-szinkronizáló szolgáltatáshoz regisztrálja, amely bizalmi kapcsolatot hoz létre. Ezt követően a PowerShell vagy az Azure portál segítségével konfigurálhatja a szinkronizálást a kiszolgálón.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Ez a parancs a megadott Felhőbeli végpontot fogja törölni egy szinkronizálási csoportból. Ha nincs legalább egy felhő végpontja, a szinkronizálási csoportban nem lehet más kiszolgálói végpontokat szinkronizálni.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Ezzel a paranccsal törlődik a megadott szinkronizálási csoport.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Ez a parancs törli a megadott kiszolgálói végpontot. A szinkronizálás erre a helyre beállítás azonnal megszűnik.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Ezzel a paranccsal törlődik a megadott tárterület-szinkronizálási szolgáltatás.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Csak hibaelhárítás esetén használható. Ez a parancs a tárterület-szinkronizálási kiszolgáló tanúsítványát fogja használni a kiszolgáló identitásának a tárterület-szinkronizálási szolgáltatáshoz való leírásához.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Ez a parancs lehetővé teszi a kiszolgálói végpontok állítható paramétereinek módosítását.

### [Regisztráció törlése – AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Figyelmeztetés: a kiszolgálók regisztrációjának megszüntetése a kiszolgálón futó összes kiszolgáló-végpontok lépcsőzetes törlését eredményezi. Ez a parancs töröl egy kiszolgálót a tárterület-szinkronizálási szolgáltatásból.

