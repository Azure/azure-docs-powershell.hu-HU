---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 2280b594ee9f525b2fa3175c917f6365cea354ba
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537121"
---
## <a name="310---november-2019"></a>3.1.0 – 2019. november
### <a name="highlights-since-the-last-major-release"></a>A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok
* Az.DataBoxEdge 1.0.0 kiadva
* Az.SqlVirtualMachine 1.0.0 kiadva

#### <a name="azcompute"></a>Az.Compute
* A virtuális gépek Reapply funkciója
    - A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.
* A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:
    - Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss
* Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében
* A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez
* A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz
* A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező
* A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült
* A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban
* A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva
    - Megrendelés lekérése
* A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva
    - Új megrendelés létrehozása
* A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva
    - Megrendelés eltávolítása
* `New-AzDataBoxEdgeShare` parancsmag módosítása
    - Mostantól helyi megosztást hoz létre
* A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva
    - Mostantól az IotRole leképezhető a Share-re
* A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva
    - Frissítések keresésének, letöltésének, telepítésének indítása az eszközön
* A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva
    - Triggerek információinak lekérdezése
* A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva
    - Új triggerek létrehozása
* A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva
    - Triggerek eltávolítása

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK a 4.4.0-s verzióra frissült
* Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja

#### <a name="azeventhub"></a>Az.EventHub
* A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült
* A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült
* Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához
    - New-AzFrontDoorBackendPoolsSettingObject

#### <a name="aznetwork"></a>Az.Network
* A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.

#### <a name="azprivatedns"></a>Az.PrivateDns
* A PrivateDns .net sdk frissült az 1.0.0-s verzióra

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.
* Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.
* SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.

#### <a name="azrediscache"></a>Az.RedisCache
* A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban. Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.
* Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.

#### <a name="azresources"></a>Az.Resources
- Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.
- Frissült a létrehozási szabályzat definíciójának súgóbeli példája
- Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.
- Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.
- A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.

#### <a name="azsql"></a>Az.Sql
* Az adatbázisbeli ReadReplicaCount mostantól támogatott.
* A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén

## <a name="300---november-2019"></a>3.0.0 – 2019. november
### <a name="general"></a>Általános kérdések
* Megjelent az Az.PrivateDns 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* A Resolve-Error aliast érintő elavulási üzenet hozzáadása.

#### <a name="azadvisor"></a>Az.Advisor
* Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.

#### <a name="azbatch"></a>Az.Batch
* A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`. Emellett egy új `LowPriorityCoreQuota` elem is található.
  - Ez hatással van a következőre: **Get-AzBatchAccount**.
* A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.
* Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez. Ezek az **New-AzBatchTask** `-ResourceFile` paraméterénél adhatók meg.
  - Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:
    - Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.
    - A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.
* A `PSApplication` **Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.
  - Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával. Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.
* Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.
  - Az `ApplicationId` mostantól az `ApplicationName` aliasa.
* Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.
* A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.
* A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.
* Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.
* A **Set-AzBatchPoolOSVersion** eltávolítva. Ez a művelet már nem támogatott.
* `PSCloudServiceConfiguration` `TargetOSVersion` eleme eltávolítva.
* A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.
* `DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.
* A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve. 
  - A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.
  - Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer. Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.
* Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.
* Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján. Ez a `PSNetworkSecurityGroupRule` `SourcePortRanges` tulajdonsága alapján történik.
* Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában. Ezt a `PSTaskContainerSettings` `WorkingDirectory` tulajdonsága szabályozza.
* Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal. Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.
* Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).
* Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).

#### <a name="azcdn"></a>Az.Cdn
* A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.
* Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.

#### <a name="azcompute"></a>Az.Compute
* Lemeztitkosítási készlet funkció
    - Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet
    - A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile        
        Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk
    - A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig
* A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz
* Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra
* ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz
* Kompatibilitástörő változások
    - A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload
    - A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK a 4.3.0-s verzióra frissült

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), a következő javításokkal
* Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.
* Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban
* Az eredeti syncflag átadásának javítása a badoffset helyreállításához
* Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez
* Concat-hiba javítása

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Különféle elgépelések kijavítva a modulban

#### <a name="azhdinsight"></a>Az.HDInsight
* Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.
* Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.
* A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0
* Öt parancsmag el lett távolítva:
    - Get-AzHDInsightOMS
    - Enable-AzHDInsightOMS
    - Disable-AzHDInsightOMS
    - Grant-AzHDInsightRdpServicesAccess
    - Revoke-AzHDInsightRdpServicesAccess
* Három parancsmag hozzáadva:
    - Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.
    - Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.
    - Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.
* A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.
* Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.
* Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.
* A következő parancsmagok kimeneti típusa megváltozott:
*  - A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.
*  - A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.
*  - A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.
* Néhány forgatókönyvi teszteset hozzáadva.
* Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.

#### <a name="aziothub"></a>Az.IotHub
* Kompatibilitástörő változások:
    - Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.
    - Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.
    - A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.
    - A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.
    - A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.
    - A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.
    - A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.
    - A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.
    - A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.
    - A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.
    - A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.
    - A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.
* Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.
* Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.
* Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.
* Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.
* Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.
* Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.
* Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.
* SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek

#### <a name="azresources"></a>Az.Resources
* A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra

#### <a name="aznetwork"></a>Az.Network
* A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.
    - Frissített parancsmag:
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Set-AzPrivateEndpointConnection
* Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.
    - Új parancsmag:
        - Get-AzPrivateLinkResource
* Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.
    - Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban
    - Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban
    - New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.
* Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás
* Új parancsmagok az Azure Firewall-szabályzat támogatásához
* A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva
    - Új hozzáadott parancsmagok:
        - Add-AzVirtualHubRoute
        - Add-AzVirtualHubRouteTable
        - Get-AzVirtualHubRouteTable
        - Remove-AzVirtualHubRouteTable
        - Set-AzVirtualHub
* Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében
    - Opcionális paraméterekkel frissített parancsmagok:
        - New-AzVirtualHub: Sku paraméter hozzáadva
        - Update-AzVirtualHub: Sku paraméter hozzáadva
        - New-AzVirtualWan: VirtualWANType paraméter hozzáadva
        - Update-AzVirtualWan: VirtualWANType paraméter hozzáadva
* Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében
    - Új hozzáadott parancsmagok:
        - Update-AzureRmVirtualHubVnetConnection
    - Opcionális paraméterekkel frissített parancsmagok:
        - New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva
        - New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva
        - Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva
        - New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva
        - Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva
* TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva
    - Új hozzáadott parancsmagok:
        - New-AzApplicationGatewayFirewallPolicySetting
        - New-AzApplicationGatewayFirewallPolicyExclusion
        - New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRuleOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRule
        - New-AzApplicationGatewayFirewallPolicyManagedRuleSet
    - Opcionális paraméterekkel frissített parancsmagok:
        - New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva
* A CustomRule Geo-Match operátorának támogatása hozzáadva
    - A GeoMatch hozzáadva a FirewallCondition operátorához
* perListener és a perSite tűzfalszabályzat támogatása hozzáadva
    - Opcionális paraméterekkel frissített parancsmagok:
        - New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva
        - New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva
* Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket
* A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban
* Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva
    - Új hozzáadott parancsmagok:
        - New-AzIpGroup
        - Remove-AzIpGroup
        - Get-AzIpGroup
        - Set-AzIpGroup

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.

#### <a name="azsql"></a>Az.Sql
* Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.
* A régi naplózási parancsmagok elavulttá váltak a kódban.
* A következő elavult aliasok el lettek távolítva:
* Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)
* Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)
* A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva
* Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva
* A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak 
* Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.

#### <a name="azstorage"></a>Az.Storage
* Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát
    -  Get-AzStorageFileHandle
    -  Close-AzStorageFileHandle
    
## <a name="280---october-2019"></a>2.8.0 – 2019. október
### <a name="general"></a>Általános kérdések
* Az.HealthcareApis 1.0.0-s kiadás

#### <a name="azaccounts"></a>Az.Accounts
* A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet
    - A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068

#### <a name="azautomation"></a>Az.Automation
* Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán. 

#### <a name="azbatch"></a>Az.Batch
* A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.

#### <a name="azcompute"></a>Az.Compute
* A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz
* Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása
* A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán. 
* A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.

#### <a name="azdatafactory"></a>Az.DataFactory
* CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.
* Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.
* Az ADF .Net SDK a 4.2.0-ás verzióra frissült

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* A PowerShell az 1.0.0-s verzióra frissült
* Az SDK a 1.0.2-s verzióra frissült
* Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz
* A kimeneti struktúra beágyazottról simítottra frissült.

#### <a name="aziothub"></a>Az.IotHub
* Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents
* Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId 

#### <a name="azmonitor"></a>Az.Monitor
* Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver
* Az általános riasztási séma használata engedélyezve a fogadók számára. Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.
* A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.

#### <a name="aznetwork"></a>Az.Network
* Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.
* Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz
    - Új hozzáadott parancsmagok:
        - New-AzureRmTrafficSelectorPolicy
    - Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection
* Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban
    - Frissített parancsmagok:
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Tovább javult a Cortex-parancsmagok kivételeinek kezelése
* A VirtualNetworkGateways új generációi és termékváltozatai
  - A VirtualNetworkGateways új generációinak bevezetése.
  - A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.

#### <a name="azrediscache"></a>Az.RedisCache
* Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.

#### <a name="azsql"></a>Az.Sql
* Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása

#### <a name="azstorage"></a>Az.Storage
* Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.
* A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni
    -  Get-AzureRmStorageContainer
* A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.

#### <a name="azwebsites"></a>Az.Websites
* Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt

## <a name="270---september-2019"></a>2.7.0 – 2019. szeptember
#### <a name="azapimanagement"></a>Az.ApiManagement
* Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában
* El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból. A „Set-AzApiManagement” használható helyette.

#### <a name="azautomation"></a>Az.Automation
* Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés
* Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz
* Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.

#### <a name="azcompute"></a>Az.Compute
* Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz
* Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz
* Alacsony prioritású virtuálisgép-funkció hozzáadása:
    - Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.
    - Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.
* Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.
* Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.
* Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.
* Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.

#### <a name="azdatafactory"></a>Az.DataFactory
* Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz
* Az ADF .Net SDK a 4.1.3-as verzióra frissült

#### <a name="azhdinsight"></a>Az.HDInsight
* Kompatibilitástörő változások a meghívással kapcsolatban

#### <a name="aziothub"></a>Az.IotHub
* Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.
* Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása. Az új parancsmagok a következők:
    - Add-AzIotHubMessageEnrichment
    - Get-AzIotHubMessageEnrichment
    - Remove-AzIotHubMessageEnrichment
    - Set-AzIotHubMessageEnrichment

#### <a name="azmonitor"></a>Az.Monitor
* A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra
   - Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat. Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.
   - Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt. A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.
   - Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték. A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis). **MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.
   - A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest. Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.
   - Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest. Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.
* A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében
    - New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza
    - Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja
* Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései
 - A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)
 - Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban
 - Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez
 - Általánosan továbbfejlesztett súgófájlok
* Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba

#### <a name="aznetwork"></a>Az.Network
* Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa 
* Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában
* Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében
* Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében
* Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében
* Ki lett javítva a biztonságiszabály-modellek helytelen leképezése
* Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez
    - Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz
    - Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz
    - Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály
* Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz
* MultiLink-támogatás a Virtuális WAN-ben
    - Új parancsmagok
        - New-AzVpnSiteLink
        - New-AzVpnSiteLinkConnection
    - Frissített parancsmag:
        - New-VpnSite
        - Update-VpnSite
        - New-VpnConnection
        - Update-VpnConnection
* Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal
* Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához

#### <a name="azresources"></a>Az.Resources
* Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés
* Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:
    - New-AzServiceFabricApplication
    - New-AzServiceFabricApplicationType
    - New-AzServiceFabricApplicationTypeVersion
    - New-AzServiceFabricService
    - Update-AzServiceFabricApplication
    - Get-AzServiceFabricApplication
    - Get-AzServiceFabricApplicationType
    - Get-AzServiceFabricApplicationTypeVersion
    - Get-AzServiceFabricService
    - Remove-AzServiceFabricApplication
    - Remove-AzServiceFabricApplicationType
    - Remove-AzServiceFabricApplicationTypeVersion
    - Remove-AzServiceFabricServic
* A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.

#### <a name="azsignalr"></a>Az.SignalR
* Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok

#### <a name="azsql"></a>Az.Sql
* Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa
* Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).
* El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban
* Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.
* Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).

#### <a name="azstorage"></a>Az.Storage
* Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa
* A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.
    -  Set-AzStorageBlobContent
* Az Azure File-megosztások Management plane API-val történő kezelésének támogatása
    -  New-AzRmStorageShare
    -  Get-AzRmStorageShare
    -  Update-AzRmStorageShare
    -  Remove-AzRmStorageShare

#### <a name="azwebsites"></a>Az.Websites
* Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor
* Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében
* Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa

## <a name="260---august-2019"></a>2.6.0 – 2019. augusztus
#### <a name="general"></a>Általános kérdések
* Különféle elgépelések kijavítva több modulban

#### <a name="azaccounts"></a>Az.Accounts
* Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)

#### <a name="azaks"></a>Az.Aks
* A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva
    * További információ: https://github.com/Azure/azure-powershell/issues/9847

#### <a name="azapimanagement"></a>Az.ApiManagement
* A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351
    - Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait
* **Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752
* Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre

#### <a name="azbatch"></a>Az.Batch
* Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre

#### <a name="azcdn"></a>Az.Cdn
* Ki lett javítva egy elgépelés CDN modulátalakító segédben

#### <a name="azcompute"></a>Az.Compute
* Új VmssId a New-AzVMConfig parancsmaghoz
* Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz
* Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz
* Új Host és HostGroup jellemzők
    - Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz
* Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára
* A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában

#### <a name="azdatafactory"></a>Az.DataFactory
* A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva
* Az ADF .Net SDK a 4.1.2-es verzióra frissült
* Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását
* Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.

#### <a name="azeventhub"></a>Az.EventHub
* Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban
* Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta
* új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz
* Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt

#### <a name="azmonitor"></a>Az.Monitor
* Hibás paraméternév lett kijavítva a súgódokumentációban

#### <a name="aznetwork"></a>Az.Network
* Frissítve lett a New-AzPrivateLinkServiceIpConfig
    - A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.
    - Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.
* Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg
* Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét. 
* Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.
* Frissült az AzNetworkServiceTag Location paraméterének leírása

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja
    - Példa hozzáadva
    - A -Name paraméter leírása frissítve lett
* Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz
* Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Frissült a Get-AzRecoveryServicesBackupJob.md

#### <a name="azresources"></a>Az.Resources
* A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót
    - Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében
    - A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek
* A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez

#### <a name="azservicebus"></a>Az.ServiceBus
* Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban
* Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni
* Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e 

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:
    - NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett. Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681
    - Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt. kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407
    - Az Add-AzServiceFabricApplicationCertificate parancsmag elavult

#### <a name="azsql"></a>Az.Sql
* Frissült a régi naplózási parancsmagok dokumentációja.

#### <a name="azstorage"></a>Az.Storage
* A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott
* A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* A rehidratálás prioritása mostantól támogatott a blobmásoláskor
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez

## <a name="250---july-2019"></a>2.5.0 – 2019. július
#### <a name="azaccounts"></a>Az.Accounts
* A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása 

#### <a name="azautomation"></a>Az.Automation
* Az erőforrássztringben található elírás javítása 

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* NetworkRuleSet támogatás hozzáadva.

#### <a name="azcompute"></a>Az.Compute
* A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása
    - További információ: https://github.com/Azure/azure-powershell/issues/9633

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK a 4.1.0-s verzióra frissült
* A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása

#### <a name="azeventhub"></a>Az.EventHub
* Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken
* ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve

#### <a name="azkeyvault"></a>Az.KeyVault
* A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása

#### <a name="azlogicapp"></a>Az.LogicApp
* A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon
    - Új MapType paraméter hozzáadva a szűréshez

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva

#### <a name="aznetwork"></a>Az.Network
* A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva
    - Új parancsmagok
        - Set-AzPrivateEndpoint
        - Set-AzPrivateLinkService
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Test-AzPrivateLinkServiceVisibility
        - Get-AzAutoApprovedPrivateLinkService
* Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban
    - New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve
        - Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.
        - Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.
* Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében
* ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz
    - Frissített parancsmagok
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként
* PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz
    - Frissített parancsmag:
        - New-AzLoadBalancerFrontendIpConfig
        - Add-AzLoadBalancerFrontendIpConfig
        - Set-AzLoadBalancerFrontendIpConfig
* Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához
    - Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ. Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* A mentett keresések alapértelmezett verziója 1 értékre frissítve. 
* Null reguláris kifejezések kezelése javítva az egyéni naplókban

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* A Get-AzRecoveryServicesBackupJob.md frissítése
* A Get-AzRecoveryServicesBackupContainer.md frissítése
* A Get-AzRecoveryServicesVault.md frissítése
* A Wait-AzRecoveryServicesBackupJob.md frissítése
* A Set-AzRecoveryServicesVaultContext.md frissítése
* A Get-AzRecoveryServicesBackupItem.md frissítése
* A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése
* A Restore-AzRecoveryServicesBackupItem.md frissítése
* A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése
* A Set-AzRecoveryServicesAsrAlertSetting.md frissítése

#### <a name="azresources"></a>Az.Resources
- A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása
- A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára

#### <a name="azservicebus"></a>Az.ServiceBus
* Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken
* ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve

#### <a name="azsql"></a>Az.Sql
* A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása
* A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása
* Egy kis elírás javítása egy figyelmeztető üzenetben.

#### <a name="azstorage"></a>Az.Storage
* A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára

#### <a name="azstoragesync"></a>Az.StorageSync
* Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.
* A 9551-es hiba javítása a TierFilesOlderThanDays betartásához

#### <a name="azwebsites"></a>Az.Websites
* A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat
* Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz
* A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása

## <a name="240---july-2019"></a>2.4.0 – 2019. július
#### <a name="azaccounts"></a>Az.Accounts
* Profilparancsmagok támogatásának hozzáadása
* A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása
* Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben

#### <a name="azadvisor"></a>Az.Advisor
* Az Az.Advisor GA-kiadása
* Ez a modul most már része az összesített `Az` modulnak

#### <a name="azapimanagement"></a>Az.ApiManagement
* A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671
    - **Get-AzApiManagementSubscription**
        - Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva
        - „/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva
* A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432
    - **Import-AzApiManagementApi**
        - Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor

#### <a name="azautomation"></a>Az.Automation
* A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.

#### <a name="azcompute"></a>Az.Compute
* A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz

#### <a name="azdatafactory"></a>Az.DataFactory
* A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.

#### <a name="azeventgrid"></a>Az.EventGrid
* Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában

#### <a name="aziothub"></a>Az.IotHub
* Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.

#### <a name="aznetwork"></a>Az.Network
* A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez
* Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* „Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban
    - További információ: https://github.com/Azure/azure-powershell/issues/9446

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Az IaaSVMs get-policy parancsának javítása

#### <a name="azresources"></a>Az.Resources
    - A Get-AzPolicyState -Top paraméter súgószövegének javítása
    - Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz
    - Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz
    - A Policy-parancsmagok néhány dokumentumának és példájának frissítése

#### <a name="azservicebus"></a>Az.ServiceBus
* A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor

#### <a name="azsql"></a>Az.Sql
* A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz
* Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból

#### <a name="azstorage"></a>Az.Storage
* Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:
    -  Enable-AzStorageStaticWebsite
* A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával
* További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul
* Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Ez a modul most már része az összesített `Az` modulnak

## <a name="232---june-2019"></a>2.3.2 – 2019. június
#### <a name="azaccounts"></a>Az.Accounts
* Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz
    - További információ: https://github.com/Azure/azure-powershell/issues/8983
* Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest

#### <a name="azcompute"></a>Az.Compute
* A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.
* Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában

#### <a name="azdns"></a>Az.Dns
* Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.

#### <a name="azeventgrid"></a>Az.EventGrid
* Frissítve a 2019-06-01-es API-verzió használatára.
* Új parancsmagok:
    - New-AzureRmEventGridDomain
        - Létrehoz egy új Azure Event Grid-tartományt.
    - Get-AzureRmEventGridDomain
        - Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.
    - Remove-AzureRmEventGridDomain
        - Eltávolít egy Azure Event Grid-tartományt.
    - New-AzureRmEventGridDomainKey
        - Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.
    - Get-AzureRmEventGridDomainKey
        - Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.
    - New-AzureRmEventGridDomainTopic:
        - Új Azure Event Grid-tartományi témakört hoz létre.
    - Get-AzureRmEventGridDomainTopic
        - Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját 
    - Remove-AzureRmEventGridDomainTopic:
        - Eltávolít egy meglévő Azure Event Grid-tartományi témakört.
* Frissített parancsmagok:
    - New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:
        - Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.
        - Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.
        - Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.
        - Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:
            - Esemény-előfizetés lejárati dátuma,
            - Speciális szűrési paraméterek.
        - Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.
        - Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése: 
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:
        - Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.
    - Remove-AzureRmEventGridSubscription
        - Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.
        - Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)
* New-AzFrontDoorWafManagedRuleObject
    - Hozzá lett adva az új értékek automatikus kitöltése

#### <a name="aznetwork"></a>Az.Network
* Virtuális hálózati átjárók erőforrás-támogatása hozzáadva
    - Új parancsmagok
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* AvailablePrivateEndpointType hozzáadva
    - Új parancsmagok 
        - Get-AzAvailablePrivateEndpointType
* PrivatePrivateLinkService hozzáadva
    - Új parancsmagok 
        - Get-AzPrivateLinkService 
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* PrivateEndpoint hozzáadva
    - Új parancsmagok
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen
    - Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.
    - Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.
* Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.
* Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.
* Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben
* Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során
* Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.
* Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében
* Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához
* Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében
* Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében
* Hozzá lett adva a Get-AzNetworkServiceTag parancsmag
* Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében
    - Frissítve lett a New-AzFirewall parancsmag:
        - Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el
        - Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el
        - Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként
        - Elavult a -PublicIpName és a -VirtualNetworkName paraméter 
* Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz. 
    - Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.
    - Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.
    - Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében

#### <a name="azresources"></a>Az.Resources
* További sablonexportálási beállítások támogatása
    - Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében
    - Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében
    - Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le

#### <a name="azsql"></a>Az.Sql
* Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja
* Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot
* Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor
    - New-AzStorageAccount
* Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint
* Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz

## <a name="220---june-2019"></a>2.2.0 – 2019. június
#### <a name="azcdn"></a>Az.Cdn
* Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión

#### <a name="azcompute"></a>Az.Compute
* A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.
    - Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM

#### <a name="azeventhub"></a>Az.EventHub
* A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket
* A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett

#### <a name="aznetwork"></a>Az.Network
* ResourceID és InputObject frissítése a Nat-átjárón
    - ResourceID és InputObject aliasának hozzáadása

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* „Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult

#### <a name="azservicebus"></a>Az.ServiceBus
* A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása
* A Service Fabric parancssorok hiányzó karakterének pótlása

#### <a name="azsql"></a>Az.Sql
* A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.
* A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése
* Threat Detection parancsmagok átnevezése Advanced Threat Protection névre
* A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.

#### <a name="azwebsites"></a>Az.Websites
* javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket

## <a name="210---may-2019"></a>2.1.0 – 2019. május
#### <a name="azapimanagement"></a>Az.ApiManagement
* Új parancsmagok a globális és API-szintű diagnosztika kezeléshez
    - **Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása
    - **New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz
    - **New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban
    - **New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.
    - **New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz
    - **Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben
    - **Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben
* Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez
    - **Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása
    - **New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban
    - **Remove-AzApiManagementCache** – Gyorsítótár eltávolítása
    - **Update-AzApiManagementCache** – Gyorsítótár frissítése
* Új parancsmagok az API-séma kezeléséhez
    - **New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz
    - **Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása
    - **Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása
    - **Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése
* Új parancsmag a felhasználói jogkivonat létrehozásához 
    - **New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.
* Új parancsmag a hálózat állapotának lekérdezéséhez
    - **Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ. Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.
* A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez 
    - Mostantól az új „Consumption” SKU is támogatott
    - Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható
    - Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is. Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.
    - Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.
* A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához
* A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez 
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]
* Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához
* Az **Import-AzApiManagementApi** parancsmag frissítése
    - API importálása az OpenApi 3.0 dokumentumspecifikációból
    - A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása
    - A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása
* A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához
* A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához
* A **New-AzApiManagementApi** parancsmag frissítése 
    - API konfigurálása OpenId engedélyezési kiszolgálón
    - API létrehozása ApiVersionSet tulajdonságban
    - API klónozása SourceApiId és SourceApiRevision használatával
    - Lehetőség a SubscriptionRequired API hatókörben való konfigurálására 
* A **Set-AzApiManagementApi** parancsmag frissítése
    - API konfigurálása OpenId engedélyezési kiszolgálón
    - API frissítése ApiVersionSet tulajdonságba    
    - Lehetőség a SubscriptionRequired API hatókörben való konfigurálására 
* A **New-AzApiManagementRevision** parancsmag frissítése
    - Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával Az új változat a szülő ApiId értékét veszi át
    - ApiRevisionDescription biztosítása
    - A „ServiceUrl” felülírása API klónozáskor
* A **New-AzApiManagementIdentityProvider** parancsmag frissítése
    - AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval
    - SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása
* A **New-AzApiManagementSubscription** parancsmag frissítése
    - A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz
    - A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz
    - Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez
* A **Set-AzApiManagementSubscription** parancsmag frissítése
    - A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz
    - A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz
    - Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez
* Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához
    - New-AzApiManagementContext
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - Get-AzApiManagementApiRelease
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - Get-AzApiManagementApiVersionSet
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - Get-AzApiManagementAuthorizationServer
    - Get-AzApiManagementBackend
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - Get-AzApiManagementCertificate 
    - Remove-AzApiManagementApiVersionSet
    - Remove-AzApiManagementSubscription

#### <a name="azautomation"></a>Az.Automation
* A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez
    - A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977
    - A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600
* A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett
    * A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347
* A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta. Most már csak az egyező csomópontot adja vissza.

#### <a name="azcompute"></a>Az.Compute
* A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz
* A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben

#### <a name="azmonitor"></a>Az.Monitor
* A hibás paraméternevek kijavítása a súgópéldákban

#### <a name="aznetwork"></a>Az.Network
* DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz
    - Frissített parancsmag:
        - Get-AzEffectiveRouteTable
* A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában

#### <a name="azresources"></a>Az.Resources
* Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez

#### <a name="azsql"></a>Az.Sql
* Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése

## <a name="200---may-2019"></a>2.0.0 – 2019. május
#### <a name="azaccounts"></a>Az.Accounts
* Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.
* A sikertelen fióklétrehozás hibájának javítása.

#### <a name="azcompute"></a>Az.Compute
* Közelségi elhelyezési csoport szolgáltatás.
    - A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.
* A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.
* A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz       
* Kompatibilitástörő változások
    - A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.
    - Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása

#### <a name="azdns"></a>Az.Dns
* Automatikus DNS NameServer-delegálás
    - A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.
    - Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása
* A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* A következő két parancsmag el lett távolítva:
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett
* A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:
    - Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.
    - A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.

#### <a name="azmonitor"></a>Az.Monitor
* Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai  
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - [További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról
    - A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait

#### <a name="aznetwork"></a>Az.Network
* A NAT-átjáró erőforrás támogatása hozzáadva
    - Új parancsmagok
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Frissített parancsmagok
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.
    - Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.
    - Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* A szabályzat-kiértékelési adatok lekérdezésének támogatása.
    - Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz. Az -Expand PolicyEvaluationDetails támogatása.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.
* Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.
* Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.
* Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.
* Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.
* További kisebb javítások.

#### <a name="azrelay"></a>Az.Relay
* Az elgépelések ki lettek javítva az ügyféloldali üzenetekben

#### <a name="azservicebus"></a>Az.ServiceBus
* Új parancsmagok hozzáadása az NetworkRuleSet, Namespace

#### <a name="azstorage"></a>Az.Storage
* A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)
* Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.
* A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.
    - New-AzStorageAccount
* A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz
* A Get-AzWebApp*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként

## <a name="180---april-2019"></a>1.8.0 – 2019. április
### <a name="highlights-since-the-last-major-release"></a>A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok
* A(z) `Az` modul általános rendelkezésre állása
* Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce
* Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében
* Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében
* Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében
* Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz

#### <a name="azaccounts"></a>Az.Accounts
* Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése

#### <a name="azbatch"></a>Az.Batch
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azcdn"></a>Az.Cdn
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azcompute"></a>Az.Compute
* Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.
* Javítsa ki a helyettesítő karakterek dokumentációja

#### <a name="azdatafactory"></a>Az.DataFactory
* Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azeventgrid"></a>Az.EventGrid
* A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.

#### <a name="azeventhub"></a>Az.EventHub
* Új parancsmagok hozzáadása az NetworkRuleSet, Namespace 

#### <a name="azhdinsight"></a>Az.HDInsight
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="aziothub"></a>Az.IotHub
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azkeyvault"></a>Az.KeyVault
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.
* Javítsa ki a helyettesítő karakterek dokumentációja

#### <a name="azmachinelearning"></a>Az.MachineLearning
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azmedia"></a>Az.Media
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azmonitor"></a>Az.Monitor
  * Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok
      - Új AzMetricAlertRuleV2DimensionSelection
      - Új AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Adjon hozzá AzMetricAlertRuleV2
  * Frissített verzió 0.22.0-preview figyelő SDK

#### <a name="aznetwork"></a>Az.Network
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.
* Javítsa ki a helyettesítő karakterek dokumentációja

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.
* Frissített táblázatos formában az SQL azure-beli virtuális gépen
* A hozzáadott alternatív módszert AzureFileShare hely beolvasása
* Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint

#### <a name="azrediscache"></a>Az.RedisCache
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.

#### <a name="azresources"></a>Az.Resources
* Javítsa ki a helyettesítő karakterek dokumentációja

#### <a name="azsql"></a>Az.Sql
* Cserélje le a függőségi figyelő SDK közös kód
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.
* Továbbfejlesztett folyamat, amely több oszlop osztályozási.
* Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.
* Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.
* Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.
* Javítsa ki a helyettesítő karakterek dokumentációja

#### <a name="azwebsites"></a>Az.Websites
* a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások
* A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.
* A webhelyek SDK frissítése.
* A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.

## <a name="170---april-2019"></a>1.7.0 – 2019. április
### <a name="highlights-since-the-last-major-release"></a>A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok
* A(z) `Az` modul általános rendelkezésre állása
* Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce
* Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében
* Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében
* Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében
* Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz

#### <a name="azaccounts"></a>Az.Accounts
* Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása
* Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez

#### <a name="azautomation"></a>Az.Automation
* Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája. Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.
* Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében

#### <a name="azcompute"></a>Az.Compute
* HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz
* Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése. 

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK verziója 3.0.2-re frissült.
* A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.

#### <a name="azresources"></a>Az.Resources
* Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor
* Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében
    - A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele
    - További információ: https://github.com/Azure/azure-powershell/issues/6856
* -IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez
    - További információ: https://github.com/Azure/azure-powershell/issues/6856

#### <a name="azsql"></a>Az.Sql
* Adatbázisadat-besorolás támogatása.

#### <a name="azstorage"></a>Az.Storage
* Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül
    - New-AzStorageContext
* Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 – 2019. március
### <a name="highlights-since-the-last-major-release"></a>A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok
* A(z) `Az` modul általános rendelkezésre állása
* Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce
* Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében
* Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében
* Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében
* Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz

#### <a name="azautomation"></a>Az.Automation
* Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:
    * Dinamikus csoportosítás
    * Előzetesen és utólagosan futtatandó szkriptek
    * Újraindítási beállítás

#### <a name="azcompute"></a>Az.Compute
* Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében
* A Compute ügyfélkódtár frissült a 25.0.0 verzióra

#### <a name="azkeyvault"></a>Az.KeyVault
* Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz

#### <a name="aznetwork"></a>Az.Network
* Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz
* Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében
* Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz

#### <a name="azresources"></a>Az.Resources
* Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében
* Az ARM általános hívása esetén használt hitelesítő adatok frissítése

#### <a name="azsql"></a>Az.Sql
* A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.

#### <a name="azstorage"></a>Az.Storage
* Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása 

## <a name="150---march-2019"></a>1.5.0 – 2019. március
#### <a name="azaccounts"></a>Az.Accounts
* A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához
* A Connect-AzAccount példáinak frissítése

#### <a name="azautomation"></a>Az.Automation
* A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében
* Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza. Most már az összes csomópontot visszaadja

#### <a name="azcdn"></a>Az.Cdn
* Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak

#### <a name="azcompute"></a>Az.Compute
* Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK verziója 3.0.1-re frissült

#### <a name="azlogicapp"></a>Az.LogicApp
* Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le

#### <a name="aznetwork"></a>Az.Network
* Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása
* SDK-frissítés
* VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból
* Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz

#### <a name="azresources"></a>Az.Resources
* `-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz
    - További információ: https://github.com/Azure/azure-powershell/issues/2933
* Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`
    - További információ: https://github.com/Azure/azure-powershell/issues/8240
* Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett
    - További információ: https://github.com/Azure/azure-powershell/issues/7930

#### <a name="azsql"></a>Az.Sql
* Az AuditingEndpointsCommunicator frissítése.
    - Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.

#### <a name="azstorage"></a>Az.Storage
* A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount

## <a name="140---february-2019"></a>1.4.0 – 2019. február
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Az AddAzureASAccount parancsmag elavult

#### <a name="azautomation"></a>Az.Automation
* Az Import-AzAutomationDscNodeConfiguration súgójának frissítése
* A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz
* Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.

#### <a name="azcompute"></a>Az.Compute
* Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma
* Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva
* A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz
* A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához

#### <a name="azeventhub"></a>Az.EventHub
* Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában 

#### <a name="azkeyvault"></a>Az.KeyVault
* A Set-AzKeyVaultSecret címkézésének kijavítása

#### <a name="azlogicapp"></a>Az.LogicApp
* Hozzáadva az integrációs fiókok alapszintű termékváltozatában
* Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén
* Új parancsmagok az integrációs fiók szerelvényeihez
    - Get-AzIntegrationAccountAssembly
    - New-AzIntegrationAccountAssembly
    - Remove-AzIntegrationAccountAssembly
    - Set-AzIntegrationAccountAssembly
* Új parancsmagok az integrációs fiók kötegkonfigurációjához
    - Get-AzIntegrationAccountBatchConfiguration
    - New-AzIntegrationAccountBatchConfiguration
    - Remove-AzIntegrationAccountBatchConfiguration
    - Set-AzIntegrationAccountBatchConfiguration
* A Logic Apps SDK frissítése a 4.1.0-s verzióra

#### <a name="azmonitor"></a>Az.Monitor
* A Get-AzMetric súgójának frissítése

#### <a name="aznetwork"></a>Az.Network
* Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.
    - Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához. 
    - A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name. 

#### <a name="azresources"></a>Az.Resources
* A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166
* A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235
* A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219
* Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba

#### <a name="azsql"></a>Az.Sql
* Rugalmas SQL DB-skálázási szint támogatása hozzáadva
* Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult

#### <a name="azwebsites"></a>Az.Websites
* A Get-AzWebAppSlotMetrics példájának javítása

## <a name="130---february-2019"></a>1.3.0 – 2019. február
#### <a name="azaccounts"></a>Az.Accounts
* Frissítés a ClientRuntime legújabb verziójára

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Az Az.AnalysisServices modul általános rendelkezésre állása.

#### <a name="azcompute"></a>Az.Compute
* AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.
* A Set-AzVMBootDiagnostics súgóleírása frissült.
* Az Update-AzImage súgóleírása és példája frissült.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Az Az.RecoveryServices modul általános rendelkezésre állása.

#### <a name="azresources"></a>Az.Resources
* Az erőforráscsoportok címkézése ki lett javítva. 
    - További információ: https://github.com/Azure/azure-powershell/issues/8166
* Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert. 
    - További információ: https://github.com/Azure/azure-powershell/issues/8235

#### <a name="azsql"></a>Az.Sql
* Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva
* Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.
* A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.

## <a name="121---january-2019"></a>1.2.1 – 2019. január
#### <a name="azaccounts"></a>Az.Accounts
* A hitelesítés megfelelő verziójával rendelkező kiadás

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Frissített hitelesítési függőségű kiadás

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Frissített hitelesítési függőségű kiadás

## <a name="120---january-2019"></a>1.2.0 – 2019. január
#### <a name="azaccounts"></a>Az.Accounts
* Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében
* Frissítve lettek az online súgók helytelen URL-címei.
* Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban

#### <a name="azaks"></a>Az.Aks
* Frissítve lettek az online súgók helytelen URL-címei.

#### <a name="azautomation"></a>Az.Automation
* Mostantól támogatottak a Python 2-runbookok.
* Frissítve lettek az online súgók helytelen URL-címei.

#### <a name="azcdn"></a>Az.Cdn
* Frissítve lettek az online súgók helytelen URL-címei.

#### <a name="azcompute"></a>Az.Compute
* Az Invoke-AzVMReimage parancsmag hozzá lett adva.
* A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.
* A New-AzVM figyelmeztető üzenete ki lett javítva.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Frissítve lettek az online súgók helytelen URL-címei.

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK verziója 3.0.0-ra frissült.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.
    - További információ: https://github.com/Azure/azure-powershell/issues/7462
* Frissítve lettek az online súgók helytelen URL-címei.

#### <a name="aziothub"></a>Az.IotHub
* Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.

#### <a name="azkeyvault"></a>Az.KeyVault
* Frissítve lettek az online súgók helytelen URL-címei.

#### <a name="aznetwork"></a>Az.Network
* Frissítve lettek az online súgók helytelen URL-címei.

#### <a name="azresources"></a>Az.Resources
* A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.
* Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.
* Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.
* Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522
* Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747
* Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.
    - További információ: https://github.com/Azure/azure-powershell/issues/2123

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.
* Bizonyos hibaüzenetek ki lettek javítva.
* Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.
* Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.

#### <a name="azsignalr"></a>Az.SignalR
* Frissítve lettek az online súgók helytelen URL-címei.

#### <a name="azsql"></a>Az.Sql
* Frissítve lettek az online súgók helytelen URL-címei.
* A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.
* Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.
* Egyéni rendezések támogatása a felügyelt példányokon

#### <a name="azstorage"></a>Az.Storage
* Frissítve lettek az online súgók helytelen URL-címei.
* Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Frissítve lettek az online súgók helytelen URL-címei.

#### <a name="azwebsites"></a>Az.Websites
* Frissítve lettek az online súgók helytelen URL-címei.
* Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.
* Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.

## <a name="110---january-2019"></a>1.1.0 – 2019. január
#### <a name="azaccounts"></a>Az.Accounts
* A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz

#### <a name="azcompute"></a>Az.Compute
* A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni
* Frissült az azonosító leírása a súgófájlokban
* Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.
    - A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva

#### <a name="azeventgrid"></a>Az.EventGrid
* Frissítve a 2019-01-01-es API-verzió használatára.
* A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához
    - New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:
        - Az esemény élettartama,
        - Az események kézbesítési kísérleteinek maximális száma,
        - A kézbesíthetetlen üzenet végpontja.
    - Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:
        - Az esemény élettartama,
        - Az események kézbesítési kísérleteinek maximális száma,
        - A kézbesíthetetlen üzenet végpontja.
* Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.
* Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.

#### <a name="aziothub"></a>Az.IotHub
* Frissítve az IoT Hub SDK legújabb verziójára

#### <a name="azlogicapp"></a>Az.LogicApp
* A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel

#### <a name="azresources"></a>Az.Resources
* Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett
    - További információ: https://github.com/Azure/azure-powershell/issues/7875
* Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban
* Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában
* A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében
    - További információ: https://github.com/Azure/azure-powershell/issues/8220

#### <a name="azsignalr"></a>Az.SignalR
* Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva

#### <a name="azsql"></a>Az.Sql
* A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.

#### <a name="azstorage"></a>Az.Storage
* A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva
    - New-AzStorageContext
* A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban
* Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva

## <a name="100---december-2018"></a>1.0.0 – 2018. december
### <a name="general"></a>Általános kérdések

- Az Az modul általános rendelkezésre állása
- Online súgó az egyes modulokhoz
- További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).
- Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azaccounts"></a>Az.Accounts
- Változások az Az.Profile-hoz képest
- Rögzített táblázatformátumok profil- és a környezettípusokhoz

### <a name="azapimanagement"></a>Az.ApiManagement
- A 7002-es hiba javításai
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azbatch"></a>Az.Batch
- A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.
- A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azbilling"></a>Az.Billing
- Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.

### <a name="azcognitivservices"></a>Az.CognitivServices
- A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.
- A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- ManagedIdentity-támogatás elérhetővé tétele

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azmonitor"></a>Az.Monitor
- Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azkeyvault"></a>Az.KeyVault
- A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.

### <a name="azmachinelearning"></a>Az.MachineLearning
- Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve

### <a name="azmedia"></a>Az.Media
- Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból

### <a name="aznetwork"></a>Az.Network
Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.
    - Új hozzáadott parancsmagok:
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.
    - A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azprofile"></a>Az.Profile
- A modul új neve Az.Accounts

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azresources"></a>Az.Resources
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azservicefabric"></a>Az.ServiceFabric
- A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azsignalr"></a>Az.SIgnalR
- PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára

### <a name="azsql"></a>Az.Sql
- Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz
- Frissültek az SQL-naplózási parancsmagok dokumentációs példái
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azstorage"></a>Az.Storage
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

### <a name="azwebsites"></a>Az.Websites
- Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).

## <a name="070---december-2018"></a>0.7.0 – 2018. december

### <a name="general"></a>Általános kérdések

* Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez

### <a name="azcompute"></a>Az.Compute

* Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* A záró perjel javítása az adls-fiók tartományában

### <a name="azfrontdoor"></a>Az.FrontDoor

* Egyes hibás hivatkozások javítása
    - A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.
    - A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.
* A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.

### <a name="azresources"></a>Az.Resources

* https://github.com/Azure/azure-powershell/issues/7679 javítása
    - A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.

### <a name="azsql"></a>Az.Sql

* Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez
* Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel
* Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.

### <a name="azstorage"></a>Az.Storage

* Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz
* Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.
    - Start-AzureStorageFileCopy
* Statikus webhely-konfiguráció támogatása
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp és Set-AzureRmWebAppSlot 
    - Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját. Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.

## <a name="061---november-2018"></a>0.6.1 – 2018. november

### <a name="azapimanagement"></a>Az.ApiManagement
* Frissítve lettek a függőségek a típustársítási hiba elhárításához.

### <a name="azautomation"></a>Az.Automation
* Swagger-alapú Azure Automation-parancsmagok érhetőek el.
* Update Management-parancsmagok lettek hozzáadva.
* Verziókövetési parancsmagok lettek hozzáadva.
* Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.
* Ki lett javítva a DSC csomópontregisztrálási parancs működése.

### <a name="azcompute"></a>Az.Compute
* Ki lett javítva a SystemAssigned identitás problémája.
* Frissítve lettek a függőségek a típustársítási hiba elhárításához.

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Frissítve lettek a függőségek a típustársítási hiba elhárításához.

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* A Marketplace-parancsmagok példáinak leírásai frissültek.

### <a name="aznetwork"></a>Az.Network
* A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.
* Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.
* Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan. 
* Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Javítva lett a védett fájlmegosztások módosítási szabályzata.
* A szabályzat időzónája mostantól nagybetűs.

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.
* Frissítve lettek a függőségek a típustársítási hiba elhárításához.

### <a name="azrelay"></a>Az.Relay
* A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.

### <a name="azresources"></a>Az.Resources
* Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.
* Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.
* Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.

### <a name="azservicefabric"></a>Az.ServiceFabric
* Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.

### <a name="azsql"></a>Az.Sql
* Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.
    - Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.
    - A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Set-AzureRmSqlDatabaseAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.

## <a name="050---november-2018"></a>0.5.0 – 2018. november
#### <a name="general"></a>Általános kérdések
* Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.

#### <a name="azprofile"></a>Az.Profile
* A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.
* A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez
* Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál
* Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor
    - https://github.com/Azure/azure-powershell/issues/6936
* Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket
    - https://github.com/Azure/azure-powershell/issues/7453
* Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor
    - https://github.com/Azure/azure-powershell/issues/7462
* Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.

#### <a name="azcompute"></a>Az.Compute
* Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag
* A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét
* Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* A DataLake csomag verziója 1.1.10-re frissült.
* Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.

#### <a name="azinsights"></a>Az.Insights
* Javítva lett a 7267-es hiba (Automatikus skálázási terület)
    - Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).
* Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor
    - A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik

#### <a name="aznetwork"></a>Az.Network
* A PeeringType kötelező paraméter lett a következő parancsmagoknál:
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Szabályzatszervizelési parancsmagok lettek hozzáadva

#### <a name="azresources"></a>Az.Resources
* https://github.com/Azure/azure-powershell/issues/7402 javítása
    - Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával

#### <a name="azservicebus"></a>Az.ServiceBus
* A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.
* Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag
    - A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).
    - Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).
* Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.

## <a name="040---october-2018"></a>0.4.0 – 2018. október
#### <a name="azprofile"></a>Az.Profile
* Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.
* A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.

#### <a name="azcompute"></a>Az.Compute
* A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.
* A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Virtuális hálózati szabályok támogatása
    - Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.
    - Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.
    - Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.
    - Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.

#### <a name="aznetwork"></a>Az.Network
* Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.
* A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.

#### <a name="azresources"></a>Az.Resources
* Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott). Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.

## <a name="030---october-2018"></a>0.3.0 – 2018. október
#### <a name="azurestorage"></a>Azure.Storage
* Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.
    - Get-AzStorageUsage
    
#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.

#### <a name="azcompute"></a>Az.Compute
* Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.
* A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.
* Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.

#### <a name="aznetwork"></a>Az.Network
* Hozzá lett adva a NetworkProfile funkció. Az alábbi új parancsmagok lettek hozzáadva
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez
* Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag
* Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag

#### <a name="azrediscache"></a>Az.RedisCache
* A továbbiakban bármilyen sztring megadható méretparaméterként. A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz

#### <a name="azresources"></a>Az.Resources
* A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz
* A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája

#### <a name="azsql"></a>Az.Sql
* Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést

#### <a name="azwebsites"></a>Az.Websites
* Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét
* Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba

## <a name="020---september-2018"></a>0.2.0 – 2018. szeptember
 Kezdeti kiadás
