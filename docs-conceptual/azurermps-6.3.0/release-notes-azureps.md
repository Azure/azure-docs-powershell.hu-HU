---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237689"
---
# <a name="release-notes"></a>Kibocsátási megjegyzések

Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.

---
## <a name="630---june-2018"></a>6.3.0 – 2018. június
#### <a name="azurermprofile"></a>AzureRM.Profile
* Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek.
* Környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut.

#### <a name="azurestorage"></a>Azure.Storage
* További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.

#### <a name="azurermcompute"></a>AzureRM.Compute
* A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik. 
* A Compute ügyfélkódtár verziója frissült, a következő parancsmagok javítása érdekében:
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* A ValidateNotNullOrEmpty érvényesítési feltételek az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatóak.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Ki lett javítva az a probléma, amelyben nem lett visszaadva címke a Get-AzureRmKeyVault -Tag futtatásakor.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* A Policy Insights-parancsmagok nyilvános kiadása
    - A 2018. 04. 04. dátumú API-verziót használják.
    - A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* A -Vault paraméter hozzá lett adva a RecoveryServices.Backup parancsmaghoz. Ha át van adva, felülírja a Set-AzureRmRecoveryServicesContext parancsmagot.

#### <a name="azurermsql"></a>AzureRM.Sql
* A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor.
* Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként.

## <a name="621---june-2018"></a>6.2.1 – 2018. június
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja.

## <a name="620---june-2018"></a>6.2.0 – 2018. június
#### <a name="azurermprofile"></a>AzureRM.Profile
* Kijavítottuk a problémát, amely miatt a Newtonsoft.Json 10.0.3-as verziója nem töltődött be a modul importálása során

#### <a name="azurermcompute"></a>AzureRM.Compute
* VMSS VM frissítési funkciója
    - Hozzá lett adva az Update-AzureRmVmssVM és a New-AzureRmVMDataDisk parancsmag
    - A VirtualMachineScaleSetVM paraméter hozzá lett adva az Add-AzureRmVMDataDisk parancsmaghoz, hogy adatlemezt lehessen hozzáadni a VMSS VM-hez

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Az ADF .Net SDK frissült a 0.8.0-s előzetes verzióra, amely az alábbi változásokat tartalmazza:
    - Hozzá lett adva a gyári adattár konfigurálási művelete
    - Frissült a QuickBooks társított szolgáltatás a consumerKey és a consumerSecret tulajdonság elérhetővé tételéhez
    - Több modelltípus is frissült, a SecretBase-től az objektumig
    - A rendszer blobesemény-indítókkal bővült

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* A dokumentáció kimeneti példával bővült

### <a name="azurermnetwork"></a>AzureRM.Network
* Engedélyezve lettek a Traffic Analytics-paraméterek a Network Watcher-parancsmagokon

#### <a name="azurermresources"></a>AzureRM.Resources
* Kijavítottuk a „PSResource” objektum(ok) Get-AzureRmResource által visszaadott „Properties” tulajdonságával kapcsolatos hibát

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Kijavítottuk a hibát, amely miatt a ServiceBusQueueJob frissítése nem állított be új hitelesítési adatokat

### <a name="azurermsql"></a>AzureRM.Sql
* A következő parancsmagok az opcionális LicenseType paraméterrel frissültek
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Frissült a New-AzureRMWebApp, hogy képes legyen a stratégia könyvtárból származó bevett algoritmusok használatára.

## <a name="610---may-2018"></a>6.1.0 – 2018. május
#### <a name="azurermprofile"></a>AzureRM.Profile
* Ki lett javítva az a hiba, amelyben a „Clear-AzureRmContext” futtatása egy üres környezetet tartott meg az előző alapértelmezett környezet nevével, így a felhasználó nem tudott létrehozni új környezetet a régi néven

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Az átjárók társítási/társításmegszüntetési műveleteinek engedélyezése.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Az ApiVersion, ApiRelease és ApiRevision paraméterek mostantól támogatottak
* A Service Fabric háttérrendszer mostantól támogatott
* Az Application Insights naplózó mostantól támogatott
* Az „Alapszintű” termékváltozat érvényes termékváltozatként való elismerése mostantól támogatott az API Management szolgáltatásban
* A privát hitelesítésszolgáltató által kiállított tanúsítványok fő- vagy hitelesítésszolgáltatói tanúsítványként való telepítése mostantól támogatott
* Az egyéni SSL-tanúsítványok KeyVault- és többproxys gazdaneveken keresztüli fogadása mostantól támogatott
* Az MSI-identitások mostantól támogatottak
* A házirendek URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Új Get-AzureBatchPoolNodeCounts parancsmag kiadása
* Új Start-AzureBatchComputeNodeServiceLogUpload parancsmag kiadása

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* A Get-AzureRmConsumptionUsageDetail parancsmag kiegészítése új Expand, ResourceGroup, InstanceName, InstanceId, Tags és Top paraméterekkel

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Az Export-AzureRmDataLakeStoreChildItemProperties példájának kijavítása
* A Set-AzureRmDataLakeStoreItemAclEntry Recurse esetében fellépő null paraméter kivétel kijavítása 
* A Set-AzureRmDataLakeStoreItemAclEntry, a Set-AzureRmDataLakeStoreItemAcl és a Remove-AzureRmDataLakeStoreItemAclEntry súgófájljainak javítása 

#### <a name="azurermnetwork"></a>AzureRM.Network
* A hálózati SDK-verzió felléptetése a 18.0.0-s előzetes verzióról a 19.0.0-s előzetes verzióra
* Új parancsmag hozzáadva a protokollkonfigurációk létrehozásához
    - New-AzureRmNetworkWatcherProtocolConfiguration
* Új parancsmag hozzáadva az új kapcsolatcsoportok hozzáadásához a meglévő ExpressRoute-kapcsolatcsoportokhoz.
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* Új parancsmag hozzáadva a kapcsolatcsoportok eltávolításához a meglévő ExpressRoute-kapcsolatcsoportokból.
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* Új parancsmag hozzáadva a kapcsolatcsoportok lekéréséhez
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* A kiszolgálói hitelesítés létrehozott tanúsítványokkal való használata (5998. sz. hiba) ki lett javítva

#### <a name="azurermsql"></a>AzureRM.Sql
* A frissített naplózási parancsmagok lehetővé teszik az AuditAction és AuditActionGroup paraméterek eltávolítását
* A Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy hibája ki lett javítva, amikor az új rugalmas adatmegőrzési szabályzatok megadásakor a parancs a következő hibát adta vissza: „A hosszútávú adatmegőrzési szabályzat megadása Azure Recovery Services-tárolókkal és szabályzatokkal már nem támogatott. Adja le a kérést az új rugalmas adatmegőrzési szabályzattal”.
* Az összes Azure SQL Database/ElasticPool létrehozással/frissítéssel kapcsolatos parancsmag frissítve lett az új Database API használatára, amely támogatja a termékváltozat tulajdonságot a méretezéssel és szintekkel kapcsolatos tulajdonságok esetében.
* A frissített parancsmagok a következők: 
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* A Get-AzureRmTrafficManagerProfile paramétereinek frissítésével a -ResourceGroupName paraméter megadása mostantól kötelező a -Name paraméter használata esetén.