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
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368177"
---
# <a name="release-notes"></a>Kibocsátási megjegyzések

Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.

---
## <a name="660---july-2018"></a>6.6.0 – 2018. július
#### <a name="general"></a>Általános kérdések
* Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással. Az alapértelmezett beállítás mindig az igaz érték, az egyéni erőforrások és az alapértelmezett érték felülírásának lehetősége.
* A Common.Storage új ps1xml-típusokkal egészült ki

#### <a name="azurestorage"></a>Azure.Storage
* Támogatott a Storage-környezet beolvasása a DefaulfProfile-ból
* A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6370
    - Javítottuk az Automapper hibáját, amely a PsApiManagementApi ApiContractra történő fordítása során jelentkezett
* Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6515
    - Javítottuk a File.Save hibáját, hogy a kódolási típus ne terhelje túl
* Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6560
    - Frissült a 4.0.3-as Nuget-verzióra, amely felszámolta az apiId mintában jelentkező kivételeit

#### <a name="azurermcompute"></a>AzureRM.Compute
* Javítottuk a hibát, amely miatt meghiúsult a virtuális gépek létrehozása a DiskFileParameterSet elemmel a New-AzureRmVm parancsmagban, mert átneveződött a PremiumLRS tárfiók típusa.
* Javítottuk az Invoke-AzureRmVMRunCommand parancsmagot
* Frissült a Get-AzureRmAvailabilitySet, hogy lehetővé váljon egy előfizetés összes rendelkezésre állási csoportjának listázása.  (A ResouceGroupName paraméter mostantól opcionális.)
* Frissült a SimpleParameterSet a New-AzureRmVm parancsmagban, hogy engedélyezni lehessen a gyorsított hálózatot az arra alkalmas virtuális gépeken.
* Frissült a New-AzureRmVmss egyszerű paraméterkészlet, hogy ne jöjjön létre vmss, ha egy felhasználó által megadott LB már létezik.
* Frissült a New-AzureRmDisk példája
* Hozzá lett adva egy, a New-AzureRmVM-re vonatkozó példa
* Frissült a Set-AzureRmVMOSDisk leírása
* Megfelelő helyesírással és előtaggal frissült a Set-AzureRmVMBginfoExtension 1. példája. 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Az ADF.Net SDK verziója 1.1.0-ra frissült.
* Támogatást kaptak az adat-előállítók között megosztott helyi integrációs modulok.
     - Hozzá lett adva a -SharedIntegrationRuntimeResourceId paraméter a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.
     - Hozzá lett adva a -LinkedDataFactoryName paraméter a Remove-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* A DataPlane SDK (Microsoft.Azure.DataLake.Store) verziója 1.1.9-re frissült

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban

#### <a name="azurerminsights"></a>AzureRM.Insights
* Javítottuk az OutputType formázását a súgófájlokban
* A Microsoft.Azure.Management.Monitor SDK 0.19.1-es előzetes verziója elérhetővé vált

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Javítottuk a Set-AzureRmKeyVaultAccessPolicy átirányítási hibáját

#### <a name="azurermnetwork"></a>AzureRM.Network
* Új példák lettek hozzáadva a LoadBalancerInboundNatPoolConfig parancsmagokhoz.

#### <a name="azurermresources"></a>AzureRM.Resources
* Javítottuk a hibát, amely akkor jelentkezett, amikor a címke neve és értéke is meg lett adva a Get-AzureRmResource-hoz
    - https://github.com/Azure/azure-powershell/issues/6765
* Javítottuk a Set-AzureRmResource átirányítási forgatókönyvét

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Frissült az InputObject és a ResourceId átirányítása az eltávolítási parancsmagokban
* Kijavítottunk néhány hibát
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* A következő parancsmagokkal támogatást biztosítottunk a kiszolgáló komplex veszélyforrások elleni védelméhez:
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* A következő parancsmagokkal támogatást biztosítottunk a sebezhetőségi felméréshez:
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* Javítottuk a Remove-AzureRmSqlServerFirewallRule példáját
* Javítottuk a dátum és idő helytelen kezelését a Get-AzureSqlSyncGroupLog USA-n kívüli kulturális környezeteiben

#### <a name="azurermstorage"></a>AzureRM.Storage
* A Ps1XmlAttribute hozzá lett adva a parancsmagok kimeneti típusainak tulajdonságaihoz
* A StorageAccount parancsmag kimenete táblanézetben is megjeleníthetővé vált
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* El lett távolítva egy helytelen állítás a Tag parancsmag súgójából
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 – 2018. július
#### <a name="azurermprofile"></a>AzureRM.Profile
* A Get-AzureRmContextAutosaveSetting súgójának frissítése

#### <a name="azurestorage"></a>Azure.Storage
* Blob vagy fájl feltöltésének támogatása csak írási SAS-jogkivonattal
- Set-AzureStorageBlobContent
- Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* A kötelező ResourceGroupName tulajdonság hozzáadása az AS-hez.

#### <a name="azurermautomation"></a>AzureRM.Automation
* A súgó frissítése és a New-AzureRMAutomationSchedule példájának hozzáadása

#### <a name="azurermcompute"></a>AzureRM.Compute
* A -Tag paraméter hozzáadása a következőhöz: Update/New-AzureRmAvailabilitySet
* Az Add-AzureRmVmssExtension példájának hozzáadása
* A Remove-AzureRmVmssExtension példáinak hozzáadása
* A Set-AzureRmVMAccessExtension súgójának frissítése
* A New-AzureRmVmss SimpleParameterSet készletének frissítése, hogy a SinglePlacementGroup alapértelmezés szerint false (hamis) legyen, és a SinglePlacementGroup kapcsolóparaméter hozzáadása, amellyel a felhasználó egyetlen elhelyezési csoportban hozhatja létre a VMSS-t.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSEventHubDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* A Set-AzureRmKeyVaultAccessPolicy hibaüzenetének frissítése

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* „A paraméterkészlet nem oldható fel” hiba kijavítása a következőben: New-AzureRmLogicApp

#### <a name="azurermnetwork"></a>AzureRM.Network
* Társviszony-létesítés engedélyezése több bérlőben lévő virtuális hálózatok között a következőhöz: Set/Add-AzureRmVirtualNetworkPeering
* Az alábbi parancsmagok frissítése az Application Gatewayhez
    - New-AzureRmApplicationGateway: Hozzáadott EnableFIPS jelző és zónatámogatás
    - New-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k
    - Set-AzureRmApplicationGatewaySku: Hozzáadott új Standard_v2 és WAF_v2 SKU-k
* A legújabb generátorverzióval újból létrehozott RouteTable parancsmagok

#### <a name="azurermrelay"></a>AzureRM.Relay
* Frissített Markdown-fájlok, a példában lévő paraméternév-hiba javítása

#### <a name="azurermresources"></a>AzureRM.Resources
* A Roleassignment és a roledefinition parancsmagok frissítése:
    - A felesleges roledefinition hívások eltávolítása a lapozás részeként.
* A Get-AzureRmRoleAssignment parancsmag javítása
    - Az -ExpandPrincipalGroups parancsparaméter működésének javítása
* A Get-AzureRmResource hibájának kijavítása, ahol a -ResourceType paraméter különbséget tett a kis- és nagybetűk között

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* A top és skip paraméter hozzáadása a listázási parancsmagokhoz
* Standard – Prémium NameSpace migrálási parancsmagok hozzáadása:
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* A csak olvasási PendingReplicationOperationsCount tulajdonság hozzáadása a PSServiceBusDRConfigurationAttributes osztályhoz, amely megadja a függőben lévő replikációs műveletek számát a replikáció során

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* A New-AzureRmServiceFabricCluster példájának frissítése

#### <a name="azurermsql"></a>AzureRM.Sql
* Új parancsmagok hozzáadása a Management.Sql elemhez, amelyekkel az ügyfelek TDE-tanúsítványt adhatnak az SQL Server-példányhoz vagy egy felügyelt példányhoz
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* A `Set-AzureRmWebApp -AssignIdentity` és `Set-AzureRmWebAppSlot -AssignIdentity` a false (hamis) érték esetén mostantól eltávolítja az Identitás tulajdonságot a hely object.Removing „előzetes verzió” címkéjéből is.
* A `Get-AzureRmWebAppMetrics` és a `Get-AzureRmAppServicePlanMetrics` példa frissítése
* A `Set-AzureRmWebApp -PhpVersion` támogatja az off értéket érvényes PHP-verzióként

## <a name="640---july-2018"></a>6.4.0 – 2018. július
#### <a name="general"></a>Általános kérdések
* Az OutputType attribútum formázása javítva a legtöbb modul súgófájljaiban

#### <a name="azurermprofile"></a>AzureRM.Profile
* A Ps1Xml attribútum hozzáadva az alapszintű kimenettípusokhoz

#### <a name="azurermcompute"></a>AzureRM.Compute
* A VMSS IP-címke funkciója
    - A „New-AzureRmVmssIpTagConfig” parancsmag hozzáadva
    - Az IpTag paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz
* A VMSS automatikus operációsrendszer-visszaállítási funkciója
    - A DisableAutoRollback-paraméterek hozzáadva a New-AzureRmVmssConfig és az Update-AzureRmVmss parancsmaghoz
* A VMSS operációsrendszer-frissítési előzmények funkciója
    - Az OSUpgradeHistory kapcsolóparaméter hozzáadva a Get-AzureRmVmss parancsmaghoz

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Katalógushozzáférés-vezérlési listák támogatása hozzáadva az alábbi parancsokhoz:
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Megszakítás támogatása és az előrehaladás nyomon követése hozzáadva a Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry és Set-AzureRmDataLakeStoreItemAcl parancshoz
* Megszakítás támogatása hozzáadva az Export-AzureRmDataLakeStoreChildItemProperties parancshoz
* A rekurzív műveleteket végző parancsmagok hibakeresési üzeneteinek kiürítése javítva
* A DataLake-parancsmagok tesztelési helye javítva

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Opcionális MaxCount paraméter hozzáadva a Get-AzureRmEventHub és a Get-AzureRmEventHubConsumerGroup listaműveleti parancsmaghoz
* Ki lett javítva egy probléma a New-AzureRmEventHub parancsmagban, ahol legalább egy paramétert meg kellett adni az új EventHub létrehozásakor. Az alapértelmezett paraméterkészlet rendelkezésre áll.
* -KeyValue opcionális paraméter hozzáadva a New-AzureRmEventHubKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Ki lett javítva az a probléma, hogy a Get-AzureRmKeyVault -Tag paramétere az összes erőforrást visszaadta

#### <a name="azurermnetwork"></a>AzureRM.Network
* Új termékváltozatok közzététele a zónaredundáns VirtualNetworkGatewayshez
* Új parancsok hozzáadva a következő funkcióhoz: ExpressRoute-partner API-k az ARM-en keresztül
    - Get-AzureRmExpressRouteCrossConnection hozzáadva
    - Set-AzureRmExpressRouteCrossConnection hozzáadva
    - Add-AzureRmExpressRouteCrossConnectionPeering hozzáadva
    - Get-AzureRmExpressRouteCrossConnectionPeering hozzáadva
    - Remove-AzureRmExpressRouteCrossConnectionPeering hozzáadva
    - Get-AzureRMExpressRouteCrossConnectionArpTable hozzáadva
    - Get-AzureRMExpressRouteCrossConnectionRouteTable hozzáadva
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary hozzáadva

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Get-AzureRmRecoveryServicesBackupStatus parancsmag hozzáadva. Ez a parancsmag egy virtuális gép azonosítójának használatával ellenőrzi, hogy a virtuális gépet védi-e tároló az előfizetésben. Ha van ilyen tároló, a parancsmag megjeleníti annak részleteit.

#### <a name="azurermresources"></a>AzureRM.Resources
* Frissültek a Get-AzureRmPolicyAssignment-parancsmagok:
    - -Scope-értékek listázásának támogatása hozzáadva a felügyeleti csoport szintjén
    - -Scope-értékekkel történő egyedi hozzárendelések lekérésének támogatása hozzáadva a felügyeleti csoport szintjén
    - -Effective és -All kapcsoló hozzáadva a vezérlő paraméterhez
* Frissültek a Get/New/Remove/Set-AzureRmPolicyDefinition-parancsmagok
    - -ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához
    - -SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához
* Frissültek a Get/New/Remove/Set-AzureRmPolicySetDefinition-parancsmagok
    - -ManagementGroupName paraméter hozzáadva a műveletek adott felügyeleti csoporton történő alkalmazásához
    - -SubscriptionId paraméter hozzáadva a műveletek adott előfizetésen történő alkalmazásához
* KeyVault titkoskulcs-referencia paraméterekben történő használatának támogatása hozzáadva a TemplateParameterObject használatakor a New-AzureRmResourceGroupDeployment parancsmagban
* Ki lett javítva egy probléma, amelynek során a rendszer nem vette figyelembe a New-AzureRmADAppCredential parancsmag -EndDate paraméterét
    - https://github.com/Azure/azure-powershell/issues/6505
* Ki lett javítva egy probléma, amelynek során az Add-AzureRmADGroupMember parancsmag nem megfelelő URL-címet használt a kérések elvégzéséhez
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* A -KeyValue opcionális paraméter hozzáadva a New-AzureRmServiceBusKey parancsmaghoz, amellyel a felhasználó megadhatja a KeyValue paraméter értékét.

#### <a name="azurermsql"></a>AzureRM.Sql
* Tisztázva lettek az SQLDW felhasználó által meghatározott visszaállítási pontjai a New-AzureRmSqlDatabaseRestorePoint súgójában
* Frissült a -ComputeGeneration paraméter dokumentációja több parancsmagban

## <a name="630---june-2018"></a>6.3.0 – 2018. június
#### <a name="azurermprofile"></a>AzureRM.Profile
* Az Enable-AzureRmContextAutoSave hibaüzenetei frissültek
* Egy környezet jön létre minden előfizetéshez, amelyben a Connect-AzureRmAccount korábbi környezet nélkül fut

#### <a name="azurestorage"></a>Azure.Storage
* További információk lettek hozzáadva a súgófájlokhoz a -Permissions paraméterrel kapcsolatban.

#### <a name="azurermcompute"></a>AzureRM.Compute
* A Get-AzureRmVmDiskEncryptionStatus kijavít egy hibát, amely az adatlemezekkel nem rendelkező virtuális gépeken jelentkezik 
* A Compute ügyfélkódtár-verziója frissült, a következő parancsmagok javítása érdekében
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* A következő parancsmagok ki lettek javítva, így helyesen jelenítik meg a műveletazonosítót és a művelet állapotát:
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzureRmVM
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
* A ValidateNotNullOrEmpty érvényesítési feltételei az Update-AzureRmEventGridSubscription parancsmagban található SubjectBeginsWith/SubjectEndsWith esetében el lettek távolítva, így ha szükséges, ezek a paraméterek üres sztringre módosíthatók.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Ki lett javítva egy probléma, amelynek során a parancs nem adott vissza címkét a Get-AzureRmKeyVault -Tag futtatásakor

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* A Policy Insights-parancsmagok nyilvános kiadása
    - A 2018.04.04. dátumú API-verziót használják
    - A PolicyDefinitionReferenceId hozzá lett adva a Get-AzureRmPolicyStateSummary eredményeihez

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* A -Vault paraméter hozzá lett adva a RecoveryServices.Backup-parancsmagokhoz. Ha át van adva, felülbírálja a Set-AzureRmRecoveryServicesContext parancsmagot.

#### <a name="azurermsql"></a>AzureRM.Sql
* A Get-AzureRmSqlDatabaseExpanded súgófájljában lévő példa frissült

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Az Add-AzureRmTrafficManagerEndpointConfig súgófájlja frissült

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Frissült a Set-AzureRmWebApp, így az AppSettings nem lesz felülírva az -AssignIdentity használatakor
* Frissült a New-AzureRmWebAppSlot, így figyelembe veszi az AppServicePlan paramétert választható paraméterként

## <a name="621---june-2018"></a>6.2.1 – 2018. június
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Frissült a PSWorkspace modell, így lehetővé teszi, hogy a hálózat a típust paraméterként használja

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