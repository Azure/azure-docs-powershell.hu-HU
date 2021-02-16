---
Module Name: Az.CloudService
Module Guid: a41eb61d-c5a1-4e9b-81a7-b8905fff7f2c
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Az.CloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Az.CloudService.md
ms.openlocfilehash: c9ab8aaefc7d97c7d1082b76b1dcef1546fe96d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145090"
---
# Az.CloudService modul
## Leírás
Microsoft Azure PowerShell: CloudService parancsmagok

## Az.CloudService parancsmagok
### [Get-AzCloudService](Get-AzCloudService.md)
Adatok megjelenítése a felhőszolgáltatásról.

### [Get-AzCloudServiceInstanceView](Get-AzCloudServiceInstanceView.md)
Egy felhőszolgáltatás állapotát kapja meg.

### [Get-AzCloudServiceNetworkInterfaces](Get-AzCloudServiceNetworkInterfaces.md)
Szerezze be egy felhőszolgáltatás hálózati felületét.

### [Get-AzCloudServicePublicIPAddress](Get-AzCloudServicePublicIPAddress.md)
Szerezze be egy felhőszolgáltatás nyilvános IP-címét.

### [Get-AzCloudServiceRoleInstance](Get-AzCloudServiceRoleInstance.md)
Szerepkörpéldányt kap egy felhőszolgáltatásból.

### [Get-AzCloudServiceRoleInstanceRemoteDesktopFile](Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md)
Távoli asztali fájlt kap egy szerepkörpéldányhoz egy felhőszolgáltatásban.

### [Get-AzCloudServiceRoleInstanceView](Get-AzCloudServiceRoleInstanceView.md)
A felhőszolgáltatás szerepkörpéldányának futásidővel kapcsolatos állapotáról olvassa be az adatokat.

### [Invoke-AzCloudServiceRebuild](Invoke-AzCloudServiceRebuild.md)
A Szerepkörpéldányok újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei esetén, és inicializálja az általuk használt tárterület-erőforrásokat.
Ha nem szeretné inicializálni a tárterület-erőforrásokat, használhatja a Szerepkörpéldányok újraimizálása használhatja.

### [Invoke-AzCloudServiceReimage](Invoke-AzCloudServiceReimage.md)
Az aszinkron művelet újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei esetén.

### [Invoke-AzCloudServiceRoleInstanceRebuild](Invoke-AzCloudServiceRoleInstanceRebuild.md)
A szerepkörpéldány újraépítése aszinkron művelet újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei példányán, és inicializálja az általuk használt tárterület-erőforrásokat.
Ha nem szeretné inicializálni a tárterület-erőforrásokat, használhatja a Szerepkör-példány-reimage szerepkörpéldányt.

### [Invoke-AzCloudServiceRoleInstanceReimage](Invoke-AzCloudServiceRoleInstanceReimage.md)
A Reimage szerepkörpéldány aszinkron művelet újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei példányán.

### [New-AzCloudService](New-AzCloudService.md)
Felhőszolgáltatás létrehozása vagy frissítése.
Felhívjuk a figyelmét arra, hogy egyes tulajdonságok csak a felhőszolgáltatás létrehozásakor beállíthatók.

### [New-AzCloudServiceDiagnosticsExtension](New-AzCloudServiceDiagnosticsExtension.md)
Memória-objektum létrehozása diagnosztikai bővítményhez

### [New-AzCloudServiceExtensionObject](New-AzCloudServiceExtensionObject.md)
Memóriában lévő objektum létrehozása bővítményhez

### [New-AzCloudServiceLoadBalancerConfigurationObject](New-AzCloudServiceLoadBalancerConfigurationObject.md)
Create a in-memory object for LoadBalancerConfiguration

### [New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject](New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md)
Create a in-memory object for LoadBalancerFrontendIPConfiguration

### [New-AzCloudServiceRemoteDesktopExtensionObject](New-AzCloudServiceRemoteDesktopExtensionObject.md)
Memóriában lévő objektum létrehozása távoli asztali bővítményhez

### [New-AzCloudServiceRoleProfilePropertiesObject](New-AzCloudServiceRoleProfilePropertiesObject.md)
Create a in-memory object for CloudServiceRoleProfileProperties

### [New-AzCloudServiceVaultSecretGroupObject](New-AzCloudServiceVaultSecretGroupObject.md)
Create a in-memory object for Secret Group

### [Remove-AzCloudService](Remove-AzCloudService.md)
Töröl egy felhőszolgáltatást.

### [Remove-AzCloudServiceRoleInstance](Remove-AzCloudServiceRoleInstance.md)
Törli a szerepkörpéldányokat egy felhőszolgáltatásban.

### [Restart-AzCloudService](Restart-AzCloudService.md)
Egy vagy több szerepkörpéldány újraindítása egy felhőszolgáltatásban.

### [Restart-AzCloudServiceRoleInstance](Restart-AzCloudServiceRoleInstance.md)
A szerepkör-példány újraindítása aszinkron művelet egy szerepkörpéldány újraindítását kéri a felhőszolgáltatásban.

### [Set-AzCloudServiceUpdateDomain](Set-AzCloudServiceUpdateDomain.md)
Frissíti a szerepkörpéldányokat a megadott frissítési tartományban.

### [Start-AzCloudService](Start-AzCloudService.md)
Elindítja a felhőszolgáltatást.

### [Stop-AzCloudService](Stop-AzCloudService.md)
Kikapcsolja a felhőszolgáltatást.
Felhívjuk a figyelmét arra, hogy az erőforrások továbbra is csatolva vannak, és az erőforrásokért díjat számítunk fel.

### [Switch-AzCloudService](Switch-AzCloudService.md)
Az IP-pontokat felcseréli két felhőszolgáltatás (kiterjesztett támogatás) terhelésegyenleg-elosztása között.

### [Update-AzCloudService](Update-AzCloudService.md)
Felhőszolgáltatás létrehozása vagy frissítése.
Felhívjuk a figyelmét arra, hogy egyes tulajdonságok csak a felhőszolgáltatás létrehozásakor beállíthatók.

