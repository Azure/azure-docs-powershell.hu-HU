---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5eac1bee53bfadf57d053ad60d6267657b145d67
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427139"
---
# <a name="azure-powershell-release-notes"></a>Az Azure PowerShell kibocsátási megjegyzései

## <a name="500---october-2020"></a>5.0.0 – 2020. október
#### <a name="azaccounts"></a>Az.Accounts
* [Kompatibilitástörő változás] A Get-AzProfile és a Select-AzProfile paraméter el lett távolítva.
* Az Azure Directory Authentication Libraryt a Microsoft Authentication Library (MSAL) váltotta fel.

#### <a name="azaks"></a>Az.Aks
* [Kompatibilitástörő változás] A New-AzAksCluster és Set-AzAksCluster parancsmagban lévő ClientIdAndSecret paraméteralias el lett távolítva.
* [Kompatibilitástörő változás] A NodeVmSetType alapértelmezett értéke AvailabilitySet értékről VirtualMachineScaleSets értékre változott a New-AzAksCluster parancsmagban.
* [Kompatibilitástörő változás] A NetworkPlugin alapértelmezett értéke None értékről azure értékre változott a New-AzAksCluster parancsmagban.
* [Kompatibilitástörő változás] A NodeOsType paraméter el lett távolítva a New-AzAksCluster parancsmagban, mivel a Linux csak egy értéket támogat.

#### <a name="azbilling"></a>Az.Billing
* A Get-AzBillingAccount parancsmag hozzáadva
* Új parancsmag: Get-AzBillingProfile
* Új parancsmag: Get-AzInvoiceSection
* Új paraméterek hozzáadva a Get-AzBillingInvoice parancsmagba
* A Get-AzBillingInvoice parancsmag válaszából a DownloadUrlExpiry, Type, BillingPeriodNames tulajdonság el lett távolítva.

#### <a name="azcdn"></a>Az.Cdn
* Parancsmagok hozzáadva a több forrású és privát kapcsolatok támogatásához. 

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Az SDK a 7.4.0-preview verzióra frissült.

#### <a name="azcompute"></a>Az.Compute
* A -VmssId paraméter hozzá lett adva a New-AzVm parancsmaghoz.
* A PlatformFaultDomainCount paraméter hozzá lett adva a New-AzVmss parancsmaghoz.
* Új Get-AzDiskEncryptionSetAssociatedResource parancsmag
* A Tier és LogicalSectorSize opcionális paraméterek hozzáadva a New-AzDiskConfig parancsmaghoz. 
* A Tier, MaxSharesCount, DiskIOPSReadOnly és DiskMBpsReadOnly opcionális paraméterek hozzáadva a New-AzDiskUpdateConfig parancsmaghoz. 

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* [Kompatibilitástörő változás] Az API-verzió a 2019. 05. 01-es verzióra frissült.
* [Kompatibilitástörő változás] A Classic termékváltozat és a StorageAccountName paraméter el lett távolítva a New-AzContainerRegistry parancsmagból
* Hozzáadott új parancsmagok: Connect-AzContainerRegistry, Import-AzContainerRegistry, Get-AzContainerRegistryUsage, New-AzContainerRegistryNetworkRule, Set-AzContainerRegistryNetworkRule
* Új NetworkRuleSet paraméter hozzáadva az Update-AzContainerRegistry parancsmaghoz

#### <a name="azdatabricks"></a>Az.Databricks
* Ki lett javítva egy hiba, amely a databricks-munkaterület `-EncryptionKeyVersion` nélküli frissítésének meghiúsulását okozhatja.

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK a 4.12.0-s verzióra frissült
* Az ADF titkosítási kliens SDK a 4.14.7587.7-es verzióra frissült
* A Stop-AzDataFactoryV2TriggerRun és Invoke-AzDataFactoryV2TriggerRun parancsok hozzáadva

#### <a name="azdesktopvirtualization"></a>Az.DesktopVirtualization
* A felső szintű ARM-objektumok létrehozásához szükség van a hely tulajdonságra.
        * A `ApplicationGroupType` használata mostantól kötelező a `New-AzWvdApplicationGroup` parancsmaghoz.
        * A `HostPoolArmPath` használata mostantól kötelező a `New-AzWvdApplicationGroup` parancsmaghoz.
        * `PreferredAppGroupType` hozzáadva a `New-AzWvdHostPool` parancsmaghoz.

#### <a name="azfunctions"></a>Az.Functions
* [Kompatibilitástörő változás] Az IncludeSlot kapcsolóparaméter egy kivételével a Get-AzFunctionApp készlet összes paraméteréből el lett távolítva. A parancsmag mostantól támogatja az üzembehelyezési pontok lekérését az eredményekben, ha az "-IncludeSlot" meg van adva. 
* Frissítve: New-AzFunctionApp:
  - A -DisableApplicationInsights funkció ki lett javítva, hogy a beállítás megadásakor ne jöjjön létre Application Insights-projekt. [#12728]
  - [Kompatibilitástörő változás] A PowerShell 6.2-függvényalkalmazások létrehozásának támogatása megszűnt.
  - [Kompatibilitástörő változás] A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Windows-rendszerű PowerShell-függvényalkalmazások esetén 6.2-ről 7.0-ra változott azokban az esetekben, amikor a RuntimeVersion paraméter nincs megadva.
  - [Kompatibilitástörő változás] A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Windows- és Linux-rendszerű Node-függvényalkalmazások esetén 10-ről 12-re változott azokban az esetekben, amikor a RuntimeVersion paraméter nincs megadva.
  - [Kompatibilitástörő változás] A Functions 3 verziójában az alapértelmezett futtatókörnyezet verziója a Linux-rendszerű Python-függvényalkalmazások esetén 3.7-ről 3.8-ra változott azokban az esetekben, amikor a RuntimeVersion paraméter nincs megadva.

#### <a name="azhdinsight"></a>Az.HDInsight
 * A New-AzHDInsightCluster parancsmag esetében:
     - A DefaultStorageAccountName paraméter lecserélve a StorageAccountResourceId paraméterre
     - A DefaultStorageAccountKey paraméter lecserélve a StorageAccountKey paraméterre
     - A DefaultStorageAccountType paraméter lecserélve a StorageAccountType paraméterre
     - A PublicNetworkAccessType paraméter el lett távolítva
     - Az OutboundPublicNetworkAccessType paraméter el lett távolítva
     - Új paraméterek hozzáadva: StorageFileSystem és StorageAccountManagedIdentity az ADLSGen2 támogatásához
     - Új EnableIDBroker paraméter hozzáadva a HDInsight ID Broker támogatásához
     - Új paraméterek hozzáadva: KafkaClientGroupId, KafkaClientGroupName és KafkaManagementNodeSize a Kafka Rest Proxy támogatásához
 * A New-AzHDInsightClusterConfig parancsmag esetében:
     - A DefaultStorageAccountName paraméter lecserélve a StorageAccountResourceId paraméterre
     - A DefaultStorageAccountKey paraméter lecserélve a StorageAccountKey paraméterre
     - A DefaultStorageAccountType paraméter lecserélve a StorageAccountType paraméterre
     - A PublicNetworkAccessType paraméter el lett távolítva
     - Az OutboundPublicNetworkAccessType paraméter el lett távolítva
* A Set-AzHDInsightDefaultStorage parancsmag esetében:
    - A StorageAccountName paraméter lecserélve a StorageAccountResourceId paraméterre
* Az Add-AzHDInsightSecurityProfile parancsmag esetében:
    - A Domain paraméter lecserélve a DomainResourceId paraméterre
    - Az OrganizationalUnitDN paraméter kötelező követelményének eltávolítása

#### <a name="azkeyvault"></a>Az.KeyVault
* [Kompatibilitástörő változás] Elavult a DisableSoftDelete paraméter a New-AzKeyVault, és EnableSoftDelete paraméter az Update-AzKeyVault parancsmagban
* [Kompatibilitástörő változás] A SecretValueText attribútum el lett távolítva a SecretValue közvetlen megjelenítésének elkerülése érdekében [#12266]
* Új erőforrástípus támogatása: felügyelt HSM
    - Felügyelt HSM és parancsmagok CRUD-műveletei a kulcsok felügyelt HSM-en való üzemeltetéséhez.
    - HSM teljes biztonsági mentése/visszaállítása, AES-kulcsok létrehozása, biztonsági tartomány biztonsági mentése/visszaállítása, RBAC

#### <a name="azmanagedservices"></a>Az.ManagedServices
* [Kompatibilitástörő változás] Paraméterek elnevezési konvenciói és a kapcsolódó példák frissítve

#### <a name="aznetwork"></a>Az.Network
* [Kompatibilitástörő változás] A HostedSubnet paraméter el lett távolítva, helyette a Subnet hozzáadva
* Új parancsmagok hozzáadva a virtuális útválasztó társútvonalaihoz.
    - Get-AzVirtualRouterPeerLearnedRoute
    - Get-AzVirtualRouterPeerAdvertisedRoute
* Frissítve lett a New-AzFirewall parancsmag:
    - Hozzáadott paraméter: -SkuTier
    - Az -SkuName paraméter hozzáadva, amelyhez Sku lett megadva aliasként
    - Eltávolított paraméter: -Sku
* [Kompatibilitástörő változás] A Connectionlink argumentum mostantól kötelező a Start-AzVpnConnectionPacketCapture és a Stop-AzVpnConnectionPacketCapture parancsmagban
* [Kompatibilitástörő változás] A New-AzNetworkWatcherConnectionMonitorEndPointObject frissítve lett a -Filter paraméter eltávolítása érdekében
* [Kompatibilitástörő változás] A New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject parancsmag lecserélve a New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject parancsmagra.
* Frissített parancsmag: New-AzNetworkWatcherConnectionMonitorEndPointObject:
    - Hozzáadott paraméter: -Type
    - Hozzáadott paraméter: -CoverageLevel
    - Hozzáadott paraméter: -Scope
* A New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject parancsmag az új -DestinationPortBehavior paraméterrel frissült

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* A számítási feladatok visszaállításának kijavítása közreműködői engedélyekhez.
* Új paraméterek és érvényesítések hozzáadva a Restore-AzRecoveryServicesBackupItem parancsmaghoz.

#### <a name="azresources"></a>Az.Resources
* Értelmezési hiba kijavítva
* Az ARM-sablon What-If parancsmagjainak frissítése az előzetes verzió üzenetének eltávolításához az eredményekből
* Ki lett javítva az a hiba, amely miatt a sablon üzembe helyezési parancsmagjai összeomlanak, ha a -WhatIf érték magasabb hatókörre van beállítva [#13038]
* Ki lett javítva az a hiba, amely miatt a sablon üzembe helyezési parancsmagjai nem őrzik meg a sablon paramétereinek írásmódját
* Alapértelmezett API-verzió hozzáadva az Export-AzResourceGroup parancsmagban való használathoz
* Parancsmagok hozzáadva a sablonspecifikációkhoz (Get-AzTemplateSpec, Set-AzTemplateSpec, New-AzTemplateSpec, Remove-AzTemplateSpec, Export-AzTemplateSpec)
* A sablonspecifikációk meglévő telepítési parancsmagokkal való üzembe helyezése mostantól támogatott (az új -TemplateSpecId paraméterrel) 
* A Get-AzResourceGroupDeploymentOperation frissítve az SDK használatára.
* Az -ApiVersion paraméter el lett távolítva az *-AzDeployment parancsmagokból.

#### <a name="azsql"></a>Az.Sql
* Ki lett javítva az a hiba, amely miatt a New-AzSqlDatabaseExport meghiúsul, ha a networkIsolation nincs megadva [#13097]
* Ki lett javítva az a hiba, amely miatt a New-AzSqlDatabaseExport és a New-AzSqlDatabaseImport nem adott vissza OperationStatusLink értéket az eredményobjektumban [#13097]
* Az Azure párosított régiók URL-jének frissítése a biztonsági mentési tár redundanciafigyelmeztetésében 

#### <a name="azstorage"></a>Az.Storage
* Elavult RestorePolicy.LastEnabledTime tulajdonság eltávolítva
    - 'Enable-AzStorageBlobRestorePolicy'
    - 'Disable-AzStorageBlobRestorePolicy'
    - Get-AzStorageBlobServiceProperty
    - Update-AzStorageBlobServiceProperty
* A DaysAfterModificationGreaterThan típusának módosítása int típusról int? típusra
    - 'Set-AzStorageAccountManagementPolicy'
    - 'Get-AzStorageAccountManagementPolicy'
    - 'Add-AzStorageAccountManagementPolicyAction'
    - 'New-AzStorageAccountManagementPolicyRule'
* A fájlmegosztások hozzáférési szinttel való létrehozásának/frissítésének támogatása
    - New-AzRmStorageShare
    - Update-AzRmStorageShare
* ACL rekurzív beállításának/frissítésének/eltávolításának támogatása a Data Lake Gen2 elemen 
    -  Set-AzDataLakeGen2AclRecursive 
    -  Update-AzDataLakeGen2AclRecursive 
    -  Remove-AzDataLakeGen2AclRecursive
* Támogatott tároló-hozzáférési szabályzat új x,t engedéllyel
    -  New-AzStorageContainerStoredAccessPolicy
    -  'Set-AzStorageContainerStoredAccessPolicy'
* A lekérés/beállítás tárolóhozzáférési szabályzat parancsmagi kimenetének módosítása a gyermektulajdonság engedélytípusának enum típusról String típusra való változtatásával
    -  'Get-AzStorageContainerStoredAccessPolicy'
    -  'Set-AzStorageContainerStoredAccessPolicy'
* A felügyeleti házirend JSON-t használó mintaszkriptjének hibája ki lett javítva
    -  'Set-AzStorageAccountManagementPolicy'

#### <a name="azwebsites"></a>Az.Websites
* A prémium V3 tarifacsomag támogatása
* A WebSites SDK frissítése 3.1.0-s verzióra.

### <a name="thanks-to-our-community-contributors"></a>Köszönjük a közösség alábbi tagjainak
* @atul-ram, A Get-AzDelegation.md frissítése (#13176)
* @dineshreddy007, Alkalmazás-szerepkörök megfelelő hozzárendelése a Stack HCI-regisztráció esetén WAC-jogkivonat használatával. (#13249)
* @kongou-ae, a New-AzOffice365PolicyProperty.md frissítése (#13217)
* Lohith Chowdary Chilukuri (@Lochiluk), A Set-AzApplicationGateway.md frissítése (#13150)
* Matthew Burleigh (@mburleigh)
  * Hivatkozások hozzáadása a dokumentumban hivatkozott PowerShell-parancsmagokhoz (#13203)
  * Hivatkozások hozzáadása a dokumentumban hivatkozott PowerShell-parancsmagokhoz (#13190)
  * Hivatkozások hozzáadása a dokumentumban hivatkozott PowerShell-parancsmagokhoz (#13189)
  * hivatkozások hozzáadása a hivatkozott parancsmagokhoz (#13137)
  * Hivatkozások hozzáadása a dokumentumban hivatkozott PowerShell-parancsmagokhoz (#13204)
  * Hivatkozások hozzáadása a dokumentumban hivatkozott PowerShell-parancsmagokhoz (#13205)

## <a name="480---october-2020"></a>4.8.0 – 2020. október
#### <a name="azaccounts"></a>Az.Accounts
* Javítva lett a közös kódtárakban előforduló DateTime-elemzési probléma [#13045]

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Hozzá lett adva a „New-AzCognitiveServicesAccountApiProperty” parancsmag.
* A „New-AzCognitiveServicesAccount” és „Set-AzCognitiveServicesAccount” parancsmag támogatja az „ApiProperty” paramétert

#### <a name="azcompute"></a>Az.Compute
* A FailoverTypes feltöltése által javítva lett az „Update-ASRRecoveryPlan” parancsmagban előforduló hiba
* A „Get-AzVmImage” parancsmaghoz hozzá lett adva a „-Top” és „-OrderBy” opcionális paraméter. 

#### <a name="azdatabricks"></a>Az.Databricks
* Az „Az.Databricks” modul általános rendelkezésre állása
* Hozzá lett adva a virtuális hálózatok közötti társviszonyok támogatása

#### <a name="azdatafactory"></a>Az.DataFactory
* Javítva lett a kimeneti üzenetekben egy elgépelés

#### <a name="azeventhub"></a>Az.EventHub
* A „Set-AzEventHubNetworkRuleSet” parancsmaghoz hozzá lett adva a „TrustedServiceAccessEnabled” opcionális kapcsolóparaméter

#### <a name="azhdinsight"></a>Az.HDInsight
* Hozzá lett adva a „PublicNetworkAccessType” és „OutboundPublicNetworkAccessType” paraméter tervezett elavulttá válására figyelmeztető üzenet
* Hozzá lett adva a „DefaultStorageAccountName” paraméter a „StorageAccountResourceId” paraméterre történő tervezett lecserélésre figyelmeztető üzenet
* Hozzá lett adva a „DefaultStorageAccountKey” paraméter a „StorageAccountKey” paraméterre történő tervezett lecserélésre figyelmeztető üzenet
* Hozzá lett adva a „DefaultStorageAccountType” paraméter a „StorageAccountType” paraméterre történő tervezett lecserélésre figyelmeztető üzenet
* Hozzá lett adva a „DefaultStorageContainer” paraméter a „StorageContainer” paraméterre történő tervezett lecserélésre figyelmeztető üzenet
* Hozzá lett adva a „DefaultStorageRootPath” paraméter a „StorageRootPath” paraméterre történő tervezett lecserélésre figyelmeztető üzenet

#### <a name="aziothub"></a>Az.IotHub
* Frissítve lett az eszközök SDK-ja.

#### <a name="azkeyvault"></a>Az.KeyVault
* Meg lett adva a SecretValueText tulajdonság eltávolításának pontos dátuma

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Frissítve lettek a kompatibilitástörő változásra figyelmeztető üzenetek a felügyelt szolgáltatások hozzárendeléséhez és definíciójához tartozó parancsmagoknál

#### <a name="azmonitor"></a>Az.Monitor
* Javítva lett az a hiba, amelynek következtében a figyelmeztető üzenetet nem lehetett bezárni. [#12889]
* Támogatott lett a „SkipMetricValidation” paraméter a riasztási szabályok feltételeiben. Ez lehetővé teszi egy riasztási szabály létrehozását egy még ki nem bocsátott egyéni metrikához, mivel kihagyja a metrika ellenőrzését.

#### <a name="aznetwork"></a>Az.Network
* Hozzá lett adva egy Office365-szabályzat a VPNSite-erőforráshoz
    - „New-AzO365PolicyProperty”

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Hozzá lett adva a tárolónév ellenőrzése a számítási feladatok biztonsági mentéséhez.

#### <a name="azrediscache"></a>Az.RedisCache
* A „New-AzRedisCache” és „Set-AzRedisCache” parancsmag mostantól nem végződik sikertelenül a Microsoft.Cache RP regisztrálásával kapcsolatos engedélyezési hiba miatt.

#### <a name="azsql"></a>Az.Sql
* Hozzá lett adva a „BackupStorageRedundancy” a következőkhöz: 
    - „Restore-AzureRmSqlDatabase”
    - „New-AzSqlDatabaseCopy”
    - „New-AzSqlDatabaseSecondary”
* Mostantól egyik SQL DB-hivatkozás esetében sincsenek megkülönböztetve a kis- és nagybetűk a „BackupStorageRedundancy” paraméternél 
* Frissítve lett a BackupStorageRedundancy figyelmeztető üzenet neve

#### <a name="azstorage"></a>Az.Storage
* Támogatottá vált a tulajdonságok engedélyezése/letiltása/lekérése/megosztása/visszavonható törlése a Storage-fiókok fájlszolgáltatásán
    - „Update-AzStorageFileServiceProperty”
    - „Get-AzStorageFileServiceProperty”
* Támogatottá vált a fájlmegosztások listázásakor a tárfiók törölt fájlmegosztásainak belefoglalása és a különálló fájlmegosztások használati adatainak lekérése
    - „Get-AzRmStorageShare”
* Támogatottá vált a törölt fájlmegosztások visszaállítása
    - „Restore-AzRmStorageShare”
* Változtak a blobszolgáltatás tulajdonságait módosító parancsmagok, amelyek nem kérik le az eredeti tulajdonságokat a kiszolgálóról, csak beállítják a módosított tulajdonságokat.
    - „Enable-AzStorageBlobDeleteRetentionPolicy”
    - „Disable-AzStorageBlobDeleteRetentionPolicy”  
    - 'Enable-AzStorageBlobRestorePolicy'
    - 'Disable-AzStorageBlobRestorePolicy'
    - Update-AzStorageBlobServiceProperty
* Javítva lett a New-AzStorageAccount -Kind paraméter alapértelmezett értékének súgóproblémája [#12189]
* Egy példa hozzáadásával javítva lett a megfelelő ContentType beállításának bemutatása a blobok feltöltésekor [#12989]

## <a name="470---september-2020"></a>4.7.0 – 2020. szeptember
#### <a name="azaccounts"></a>Az.Accounts
* A jövőbeni kompatibilitástörő változáshoz kapcsolódó üzenetek formázva lettek
* Az Azure.Core frissítve lett az 1.4.1-es verzióra

#### <a name="azaks"></a>Az.Aks
* Az ügyféloldali paraméter ellenőrzési logikája hozzá lett adva a 'New-AzAksCluster', a 'set-AzAksCluster' és a 'New-AzAksNodePool' esetében. [#12372]
* A 'New-AzAksCluster' bővítményei mostantól támogatottak. [#11239]
* Az 'Enable-AzAksAddOn' és a 'Disable-AzAksAddOn' parancsmagok hozzá lettek adva a bővítmények esetében. [#11239]
* A 'GenerateSshKey' paraméter hozzá lett adva a 'New-AzAksCluster' esetében. [#12371]
* Az API-verzió frissítve lett a 2020-06-01-es verzióra.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* További jogi feltételek lettek megjelenítve bizonyos API-k esetében.

#### <a name="azcompute"></a>Az.Compute
* Az '-EncryptionType' opcionális paraméter hozzá lett adva a következőhöz: 'New-AzVmDiskEncryptionSetConfig'
* Új parancsmagok az új erőforrás-típusok esetében: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'
* A '-DiskAccessId' és a '-NetworkAccessPolicy' opcionális paraméterek hozzá lettek adva a következőhöz: 'New-AzSnapshotConfig'
* A '-DiskAccessId' és a '-NetworkAccessPolicy' opcionális paraméterek hozzá lettek adva a következőhöz: 'New-AzDiskConfig'
* A 'PatchStatus' tulajdonság hozzá lett adva a virtuális gép példánynézetéhez
* A 'VMHealth' tulajdonság hozzá lett adva a virtuális gép példánynézetéhez, és ez lesz a visszaadott objektum, ha a 'Get-AzVm' meghívása a '-Status' paraméterrel történik
* Az 'AssignedHost' mező hozzá lett adva a 'Get-AzVm' és a 'Get-AzVmssVM' példánynézetekhez. A mezőben a virtuálisgép-példány erőforrás-azonosítója látható
* A '-SupportAutomaticPlacement' opcionális paraméter hozzá lett adva a következőhöz: 'New-AzHostGroup' 
* A '-HostGroupId' paraméter hozzá lett adva a következőkhöz: 'New-AzVm' és 'New-AzVmss'

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK a 4.11.0-s verzióra frissült

#### <a name="azeventhub"></a>Az.EventHub
* Új fürtparancsmagok lettek hozzáadva – 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.
* Ki lett javítva a 10722-es számú hiba: Ki lett javítva, hogy csak a 'Listen' paraméter legyen hozzárendelve az AuthorizationRule jogosultságokhoz.

#### <a name="azfunctions"></a>Az.Functions
* El lett távolítva az a képesség, amely lehetővé tette, hogy az azokat nem támogató régiókban is lehessen v2 függvényeket létrehozni.
* A PowerShell 6.2 elavult. Figyelmeztetés lett hozzáadva arra az esetre, ha a felhasználó olyan PowerShell 6.2 függvényalkalmazást hoz létre, amely PowerShell 7.0-függvényalkalmazás létrehozását javasolja.

#### <a name="azhdinsight"></a>Az.HDInsight
* Támogatott a fürtlétrehozás az automatikus skálázási konfiguráció használatával
    - Új 'AutoscaleConfiguration' paraméter lett hozzáadva a 'New-AzHDInsightCluster' parancsmaghoz
* Támogatott az üzemeltető fürt automatikus skálázási konfigurációja
    - Hozzáadott új parancsmag: 'Get-AzHDInsihgtClusterAutoscaleConfiguration'
    - Hozzáadott új parancsmag: 'New-AzHDInsihgtClusterAutoscaleConfiguration'
    - Hozzáadott új parancsmag: 'Set-AzHDInsihgtClusterAutoscaleConfiguration'
    - Hozzáadott új parancsmag: 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'
    - Hozzáadott új parancsmag: 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'

#### <a name="azkeyvault"></a>Az.KeyVault
* Az RBAC-engedélyezés mostantól támogatott [#10557]
* Továbbfejlesztett hibakezelés a következőben: 'Set-AzKeyVaultAccessPolicy' [#4007]

#### <a name="azkusto"></a>Az.Kusto
* Az 'Az.Kusto' modul általános rendelkezésre állása

#### <a name="aznetwork"></a>Az.Network
* [Kompatibilitástörő változás] Az alábbi parancsmagok frissítve lettek az erőforrás virtuális útválasztója és a virtuális központ megfeleltetéséhez
    - 'New-AzVirtualRouter': 
        - A -HostedSubnet paraméter hozzá lett adva az IP-konfigurációs gyermekerőforrás támogatásához
        - A -HostedGateway és a -HostedGatewayId paraméter törölve lett
    - 'Get-AzVirtualRouter':
        - Előfizetés-szintű paraméterkészlet lett hozzáadva
    - 'Remove-AzVirtualRouter'
    - 'Add-AzVirtualRouterPeer'
    - 'Get-AzVirtualRouterPeer'
    - 'Remove-AzVirtualRouterPeer'
* Új parancsmag lett hozzáadva az Azure ExpressRoute-port esetében
    - 'New-AzExpressRoutePortLOA'
* A RemoteBgpCommunities tulajdonság hozzá lett adva a virtuális hálózat társhálózat-létesítési erőforrásához
* A „New-AzLoadBalancerFrontendIpConfig”, „New-AzPublicIpAddress” és „New-AzPublicIpPrefix” figyelmeztető üzenete módosult.
* A VpnGatewayIpConfigurations hozzá lett adva a 'Get-AzVpnGateway' kimenetéhez
* Ki lett javítva a hiba a 'Set-AzApplicationGatewaySslCertificate' esetében [#9488]
* Az 'AllowActiveFTP' paraméter hozzá lett adva a következőhöz: 'AzureFirewall'
* Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Engedélyezze az internetbiztonság-beállítási/eltávolítási funkciót a VirtualWan P2SVpnGateway átjárón.
- Frissült a 'New-AzP2sVpnGateway': Az 'EnableInternetSecurityFlag' opcionális kapcsolóparaméter hozzá lett adva a felhasználók számára, amelynek true (igaz) értékre való beállításával engedélyezhetik az internetbiztonságot a P2SVpnGateway átjárón – ez pont–hely ügyfelekre fog vonatkozni.
- Frissült az 'Update-AzP2sVpnGateway': Az 'EnableInternetSecurityFlag' vagy a 'DisableInternetSecurityFlag' opcionális kapcsolóparaméter hozzá lett adva a felhasználók számára, amelynek true (igaz)/false (hamis) értékre való beállításával engedélyezhetik/letilthatják az internetbiztonságot a P2SVpnGateway átjárón – ez pont–hely ügyfelekre fog vonatkozni.
* Új 'Reset-AzP2sVpnGateway' parancsmag lett hozzáadva a felhasználók számára, hogy alaphelyzetbe állíthassák/újraindíthassák a VirtualWan P2SVpnGateway átjárót a hibaelhárításhoz.
* Új 'Reset-AzVpnGateway' parancsmag lett hozzáadva a felhasználók számára, hogy alaphelyzetbe állíthassák/újraindíthassák a VirtualWan VpnGateway átjárót a hibaelhárításhoz.
* Frissült a 'Set-AzVirtualNetworkSubnetConfig'
    - Állítsa null értékre az alhálózat NSG- és útválasztásitáblázat-tulajdonságait, ha azok explicit módon meg vannak adva a paraméterekben [#1548] [#9718]

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Ki lett javítva a Biztonsági másolati elemek számítási feladat törlési állapota.

#### <a name="azresources"></a>Az.Resources
* Hozzá lett adva a hiányzó ellenőrzés a Set-AzRoleAssignment parancsmag esetében
* Kompatibilitástörő változást okozó attribútum lett hozzáadva a 'Get-AzResourceGroupDeploymentOperation' parancsmag 'SubscriptionId' paraméteréhez
* Az ARM-sablon What-If parancsmagjai úgy lettek frissítve, hogy az 'Ignore' erőforrás módosításait jelenítsék meg utoljára
* Az üzembehelyezési parancsmagok biztonsági és tömbparaméter-szerializálási hibái ki lettek javítva [#12773]

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Új parancsmagok lettek hozzáadva a következő felügyelt fürtökhöz és csomóponttípusokhoz:
    - 'New-AzServiceFabricManagedCluster'
    - 'Get-AzServiceFabricManagedCluster'
    - 'Set-AzServiceFabricManagedCluster'
    - 'Remove-AzServiceFabricManagedCluster'
    - 'Add-AzServiceFabricManagedClusterClientCertificate'
    - 'Remove-AzServiceFabricManagedClusterClientCertificate'
    - 'New-AzServiceFabricManagedNodeType'
    - 'Get-AzServiceFabricManagedNodeType'
    - 'Set-AzServiceFabricManagedNodeType'
    - 'Remove-AzServiceFabricManagedNodeType'
    - 'Add-AzServiceFabricManagedNodeTypeVMExtension'
    - 'Add-AzServiceFabricManagedNodeTypeVMSecret'
    - 'Remove-AzServiceFabricManagedNodeTypeVMExtension'
    - 'Restart-AzServiceFabricManagedNodeTyp'
* A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2020-03-01-es API-verzióját használja a jelenlegi modell, illetve a 2020-01-01-es előzetes verziót a felügyelt fürtök esetében.

#### <a name="azsql"></a>Az.Sql
* A BackupStorageRedundancy hozzá lett adva a következőkhöz: 'New-AzSqlInstance és 'Get-AzSqlInstance'
* A 'Get-AzSqlServerActiveDirectoryOnlyAuthentication' parancsmag hozzá lett adva
* Az 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' parancsmag hozzá lett adva
* Force paraméter lett hozzáadva a következőhöz: 'New-AzSqlInstance'
* Parancsmagok lettek hozzáadva a felügyelt adatbázis naplóvisszajátszási szolgáltatása esetében
    - 'Start-AzSqlInstanceDatabaseLogReplay'
    - 'Get-AzSqlInstanceDatabaseLogReplay'
    - 'Complete-AzSqlInstanceDatabaseLogReplay'
    - 'Stop-AzSqlInstanceDatabaseLogReplay'
* A 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' parancsmag hozzá lett adva
* Az 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' parancsmag hozzá lett adva
* A 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' parancsmag hozzá lett adva
* A 'New-AzSqlDatabaseImport' és 'New-AzSqlDatabaseExport' parancsmagok frissítve lettek a hálózatelkülönítési funkció támogatásához
* A 'New-AzSqlDatabaseImportExisting' parancsmag hozzá lett adva
* Az adatbázis-parancsmagok frissítve lettek a biztonsági mentési tártípus-specifikáció támogatásához
* Force paraméter lett hozzáadva a következőhöz: 'New-AzSqlDatabase'
* A BackupStorageRedundancy konfigurációra vonatkozó figyelmeztetés lett hozzáadva a 'New-AzSqlDatabase' egyes régióiban
* Frissítve lettek a kiszolgáló és a példány ActiveDirectoryOnlyAuthentication parancsmagjai, hogy a ResourceID és az InputObject paramétereket is tartalmazzák

#### <a name="azstorage"></a>Az.Storage
* Ki lett javítva a blobfeltöltési hiba a Microsoft.Azure.Storage.DataMovement 2.0.0-s verziójára való frissítéssel [#12220]
* Támogatott az időponthoz kötött visszaállítás
    - 'Enable-AzStorageBlobRestorePolicy'
    - 'Disable-AzStorageBlobRestorePolicy'
    - 'New-AzStorageBlobRangeToRestore'
    - 'Restore-AzStorageBlobRange'
* Támogatott a tárfiók blobhelyreállítási állapotának lekérése a get-AzureRMStorageAccount parancsmag -IncludeBlobRestoreStatus paraméterrel való futtatásával 
    - 'Get-AzureRMStorageAccount'
* Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a jövőbeli parancsmagkimenet- módosítás esetében
    - 'Get-AzStorageContainerStoredAccessPolicy'
    - 'Set-AzStorageContainerStoredAccessPolicy'
    - 'Set-AzStorageAccountManagementPolicy'
    - 'Get-AzStorageAccountManagementPolicy'
    - 'Add-AzStorageAccountManagementPolicyAction'
    - 'New-AzStorageAccountManagementPolicyRule'
* A Microsoft.Azure.Cosmos.Table SDK az 1.0.8-as verzióra frissült

### <a name="thanks-to-our-community-contributors"></a>Köszönjük a közösség alábbi tagjainak
* Thomas Van Laere (@ThomVanL), A Dockerfile-alpine-3.10 hozzáadása (#12911) 
* Lohith Chowdary Chilukuri (@Lochiluk), A Remove-AzNetworkInterfaceIpConfig.md frissítése (#12807) 
* Roberth Strand (@roberthstrand), Get-AzResourceGroup – Új példa és a felesleges tartalmak törlése (#12828) 
* Ravi Mishra (@inmishrar), Az Azure-webalkalmazásokhoz tartozó futtatókörnyezeti verem frissítése a következőre: DOTNETCORE (#12833) 
* @jack-education, A Set-AzVirtualNetworkSubnetConfig frissítése az NSG és az útválasztási táblázat alhálózatból való eltávolításának engedélyezéséhez (#12351) 
* @hagop-globanet, Az Add-AzApplicationGatewayCustomError.md frissítése (#12784) 
* Joshua Van Daalen (@greenSacrifice)
  * A Property helyesírásának frissítése (#12821) 
  * A New-AzResourceLock.md példáinak frissítése (#12806)
* Eragon Riddle (@eragonriddle), A paramétermező-név javítása a példában (#12825) 
* @rossifumax, Az elírás kijavítása a következőben: New-AzConfigurationAssignment.md (#12701)

## <a name="461---august-2020"></a>4.6.1 – 2020. augusztus
#### <a name="azcompute"></a>Az.Compute
* A New-AzVm -EncryptionAtHost paraméterének javítása az alapértelmezett False érték eltávolításához [#12776]

## <a name="460---august-2020"></a>4.6.0 – 2020. augusztus
#### <a name="azaccounts"></a>Az.Accounts
* Az összes nyilvános felhőkörnyezet betöltődik, ha a felderítési végpont nem ad vissza alapértelmezett AzureCloud- vagy más nyilvános környezetet [#12633]
* A SubscriptionPolicies elérhetővé lett téve a 'Get-AzSubscription' parancsmagban [#12551]

#### <a name="azautomation"></a>Az.Automation
* A '-RunOn' paraméterek hozzá lettek adva a 'Set-AzAutomationWebhook' parancsmaghoz hibridfeldolgozó-csoport megadásához

#### <a name="azcompute"></a>Az.Compute
* Az '-EncryptionAtHost' paraméter hozzá lett adva a 'New-AzVm', a 'New-AzVmss', a 'New-AzVMConfig', a 'New-AzVmssConfig', az 'Update-AzVM' és az 'Update-AzVmss' parancsmaghoz
* A 'SecurityProfile' hozzá lett adva a 'Get-AzVm' és a 'Get-AzVmssVM' visszaadott objektumhoz
* Az '-InstanceView' kapcsoló hozzá lett adva választható paraméterként a 'Get-AzHostGroup' parancsmaghoz
* Hozzá lett adva az új 'Invoke-AzVmPatchAssessment' parancsmag

#### <a name="azdatafactory"></a>Az.DataFactory
* A hiányzó tulajdonságok hozzá lettek adva a PSPipelineRun osztályhoz.

#### <a name="azhdinsight"></a>Az.HDInsight
* Támogatottá vált a fürtlétrehozás a gazdagépen végzett titkosítási funkcióval.

#### <a name="azkeyvault"></a>Az.KeyVault
* Figyelmeztető üzenetek lettek hozzáadva a helyreállítható törlés letiltásának tervezésekor
* Figyelmeztető üzenetek lettek hozzáadva a SecretValueText attribútum eltávolításának tervezésekor

#### <a name="azmaintenance"></a>Az.Maintenance
* Opcionális ütemezéssel kapcsolatos mezők lettek hozzáadva a 'New-AzMaintenanceConfiguration' parancsmaghoz
* Új parancsmag lett hozzáadva a 'Get-AzMaintenancePublicConfiguration' használatához

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Kompatibilitástörő változásra figyelmeztető üzenetek lettek hozzáadva a felügyelt szolgáltatások hozzárendeléséhez és definíciójához tartozó parancsmagokhoz

#### <a name="azmonitor"></a>Az.Monitor
* A 'set-AzDiagnosticSetting' paraméterkészlete ki lett bővítve a naplók és metrikák engedélyezésének szétválasztása érdekében [#12482]
* Ki lett javítva az 'Add-AzMetricAlertRuleV2' folyamatból érkező metrikariasztáskor jelentkező hibája

#### <a name="azresources"></a>Az.Resources
* Frissült a 'Get-AzPolicyAlias'-válasz, amely mostantól információt tartalmaz arról, hogy az alias módosítható-e az Azure Policyval.
* Létre lett hozva az új 'Set-AzRoleAssignment' parancsmag
* Hozzá lett adva a 'Get-AzDeploymentManagementGroupWhatIfResult' az ARM-sablon What-If típusú eredményeinek a felügyeleti csoport hatókörében történő lekéréséhez
* Hozzá lett adva az új 'Get-AzTenantWhatIfResult' parancsmag az ARM-sablonok What-If típusú eredményeinek bérlői hatókörben történő lekéréséhez
* A '-WhatIf' és a '-Confirm' felül lett bírálva a 'New-AzManagementGroupDeployment' és a 'New-AzTenantDeployment' esetében az ARM-sablon What-If típusú eredményeinek használata érdekében
* Ki lett javítva a '-WhatIf' és a '-Confirm' viselkedése az új üzembehelyezési parancsmagok esetében, hogy megfeleljenek a hamis és 
* Ki lett javítva a szerializálási hiba a '-TemplateObject' és a 'TemplateParameterObject' esetében [#1528] [#6292]
* Kompatibilitástörő változást okozó attribútum lett hozzáadva a 'Get-AzResourceGroupDeploymentOperation' parancsmaghoz a kimenet típusának közelgő változása miatt

#### <a name="azsignalr"></a>Az.SignalR
* Ki lettek javítva a 'Restart-AzSignalR' és az 'Update-AzSignalR' súgófájljainak hibái
* Hozzá lett adva az 'Update-AzSignalRNetworkAcl' és a 'Set-AzSignalRUpstream' parancsmag

#### <a name="azstorage"></a>Az.Storage
* A blobok lekérdezésgyorsítása támogatottá vált
    -  'Get-AzStorageBlobQueryResult'
    -  'New-AzStorageBlobQueryConfig'
* Frissült a súgófájl, több leírás lett hozzáadva, és javítva lett egy elírás
    -  Start-AzStorageBlobCopy
    -  Get-AzDataLakeGen2Item
* Ki lett javítva a hiba, amely során meghiúsult a blobletöltés, ha a megfelelő alkönyvtár nem létezett [#12592]
    -  Get-AzStorageBlobContent
* Támogatottá vált a Storage-fiókok objektumreplikációs szabályzatának lekérése/beállítása/eltávolítása
    - 'New-AzStorageObjectReplicationPolicyRule'
    - 'Set-AzStorageObjectReplicationPolicy'
    - 'Get-AzStorageObjectReplicationPolicy'
    - 'Remove-AzStorageObjectReplicationPolicy'
* Támogatottá vált a Blob szolgáltatásbeli változáscsatorna engedélyezése/letiltása a Storage-fiókoknál
    - Update-AzStorageBlobServiceProperty

## <a name="450---august-2020"></a>4.5.0 – 2020. augusztus
#### <a name="azaccounts"></a>Az.Accounts
* „Connect-AzAccount” parancsmag frissítve a „MaxContextPopulation” paraméter elfogadására [#9865]
* A SubscriptionClient-verzió frissítve a 2019. 06. 01. verzióra és a bérlői tartományok megjelenítése [#9838]
* Az előfizetés támogatott otthoni bérlői és managedBy bérlői információi
* A modul neve és a verzió adatai javítva a telemetriai adatokban
* Korrigált SqlDatabaseDnsSuffix és ServiceManagementUrl, ha a környezeti metaadatok végpontja inkompatibilis értéket ad vissza

#### <a name="azaks"></a>Az.Aks
* A „ClientIdAndSecret” eltávolítva és lecserélve a ServicePrincipalIdAndSecret parancsmagra, és „ClientIdAndSecret” beállítva aliasként [#12381].
* A „Get-AzAks”/„New-AzAks”/„Remove-AzAks”/„Set-AzAks” eltávolítva és lecserélve a „Get-AzAksCluster”/„New-AzAksCluster”/„Remove-AzAksCluster”/„Set-AzAksCluster” parancsmagra, és az eredetiek beállítva aliasként [#12373].

#### <a name="azapimanagement"></a>Az.ApiManagement
* Új 'Add-AzApiManagementApiToGateway' parancsmag hozzáadva.
* Új „Get-AzApiManagementGateway” parancsmag hozzáadva.
* Új „Get-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.
* Új „Get-AzApiManagementGatewayKey” parancsmag hozzáadva.
* Új „New-AzApiManagementGateway” parancsmag hozzáadva.
* Új „New-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.
* Új „New-AzApiManagementResourceLocationObject” parancsmag hozzáadva.
* Új „Remove-AzApiManagementApiFromGateway” parancsmag hozzáadva.
* Új „Remove-AzApiManagementGateway” parancsmag hozzáadva.
* Új „Remove-AzApiManagementGatewayHostnameConfiguration” parancsmag hozzáadva.
* Új „Update-AzApiManagementGateway” parancsmag hozzáadva.
* Új választható [-GatewayId] paramétert hozzáadva a „Get-AzApiManagementApi” parancsmaghoz.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* A „Deny” utasítás kifejezetten a NetworkRules alapértelmezett műveleteként lett használva.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Kijavítottunk egy hibát, ahol kivétel történt, amikor az Enum.Parse null értéket próbált kényszeríteni egy engedélyezett vagy letiltott enumerálási értékre [#12344]

#### <a name="azhdinsight"></a>Az.HDInsight
* Támogatott a fürtlétrehozás az átvitel közbeni titkosítási funkcióval.
    - Új „EncryptionInTransit” paraméter hozzáadva a „New-AzHDInsightCluster” parancsmaghoz
    - Új „EncryptionInTransit” paraméter hozzáadva a „New-AzHDInsightClusterConfig” parancsmaghoz
* Támogatotta a fürtlétrehozás a privát kapcsolat funkcióval:
    - Új „PublicNetworkAccessType” és az „OutboundPublicNetworkAccessType” paraméterek hozzáadva a „New-AzHDInsightCluster” parancsmaghoz
    - Új „PublicNetworkAccessType” és az „OutboundPublicNetworkAccessType” paraméterek hozzáadva a „New-AzHDInsightClusterConfig” parancsmaghoz
* Virtuális hálózati adatok visszaadása a „New-AzHDInsightCluster” vagy a „Get-AzHDInsightCluster” meghívásakor

#### <a name="aznetwork"></a>Az.Network
* Az AddressPrefixType paraméter mostantól támogatott a Remove-AzExpressRouteCircuitConnectionConfig esetében
* Hozzáadott nem kompatibilitástörő változások: PeerAddressType funkció a privát társviszony-létesítéshez a „Remove-AzExpressRouteCircutPeeringConfig” parancsmagban.
* A kód úgy lett módosítva, hogy figyelmen kívül hagyja az AddressPrefixType és a PeerAddressType paramétert.
* A „New-AzLoadBalancerFrontendIpConfig”, „New-AzPublicIpAddress” és „New-AzPublicIpPrefix” figyelmeztető üzenete módosult.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* A „-ForceDelete” kapcsoló hozzáadva a „Remove-AzOperationalInsightsworkspace” parancsmaghoz
* Új „Get-AzOperationalInsightsDeletedWorkspace” parancsmag hozzáadva
* Új „Restore-AzOperationalInsightsWorkspace” parancsmag hozzáadva

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Az Azure Backup tároló-/elemfelderítési funkciója továbbfejlesztve.

#### <a name="azresources"></a>Az.Resources
* A „Condition”, a „ConditionVersion” és a „Description” tulajdonság hozzáadva a „New-AzRoleAssignment” parancsmaghoz
    - Ebbe beletartozik az adatmodellek összes kapcsolódó változása

#### <a name="azsql"></a>Az.Sql
* Ki lett javítva a „New-AzSqlServer” és a „set-AzSqlServer” esetében a kiszolgálónevekben a kis- és nagybetűk meg nem különböztetését eredményező hiba
* A „New-AzSqlDatabaseSecondary” parancsmagban egy meglévő adatbázishiba miatt helytelen adatbázisnevet visszaadó hiba javítva lett

#### <a name="azstorage"></a>Az.Storage
* A tároló/blob SAS-jogkivonat létrehozása támogatott az új x,t engedéllyel
    -  New-AzStorageBlobSASToken
    -  „New-AzStorageContainerSASToken”
* A fiók SAS-jogkivonat létrehozása támogatott az új x,t,f engedéllyel
    -  „New-AzStorageAccountSASToken”
* Az egyetlen fájlmegosztás használatának lekérése támogatott
    - „Get-AzRmStorageShare”

## <a name="440---july-2020"></a>4.4.0 – 2020. július
#### <a name="azaccounts"></a>Az.Accounts
* Invoke-AzRestMethod új parancsmag hozzáadása
* Kijavítottunk egy olyan problémát, amely hitelesítési hibákat okozhat az olyan többfolyamatos forgatókönyvekben, mint például több Azure PowerShell parancsmag futtatása a Start-Job paranccsal [#9448]

#### <a name="azaks"></a>Az.Aks
* Ki lett javítva az a hiba, amely miatt a Get-AzAks nem kér le minden fürtöt [#12296]

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* A hitelesítés projekthivatkozása eltávolítva

#### <a name="azautomation"></a>Az.Automation
* Ki lett javítva az a hiba, amely miatt a feloldójeleket tartalmazó sztringek nem alakíthatók át JSON-objektummá.

#### <a name="azcompute"></a>Az.Compute
* Figyelmeztetés jelenik meg a New-AzVmss a „latest” rendszerképverzió nélküli használatakor

#### <a name="azdatafactory"></a>Az.DataFactory
* Globális paraméterek hozzáadva a Data Factoryhez.

#### <a name="azeventgrid"></a>Az.EventGrid
* Frissítve a 2020-06-01-es API-verzió használatára.
* Új funkciók hozzáadva:
    - Bemenetleképezés
    - Eseménykézbesítési séma
    - Privát kapcsolat
    - V10 felhő-eseményséma
    - Service Bus-témakör célértékként
    - Azure-függvény célértékként
    - Webhookkötegelés
    - Biztonságos webhook (AAD-támogatás)
    - IP-szűrés
* Frissített parancsmagok:
    - New-AzEventGridSubscription/Update-AzEventGridSubscription:
        - Új választható paraméterek lettek hozzáadva a webhookkötegelés támogatásáért.
        - Új választható paraméterek lettek hozzáadva a biztonságos webhook AAD-vel való használatának támogatásáért.
        - Új felsorolási érték lett hozzáadva az EndpointType paraméterhez az Azure-függvény és a Service Bus-témakör új célértékként való támogatásáért.
        - Új választható paraméter lett hozzáadva a kézbesítési sémához.
    - New-AzEventGridTopic/Update-AzEventGridTopic és New-AzEventGridDomain/Update-AzEventGridDomain:
        - Új választható paraméterek lettek hozzáadva az IP-szűrés támogatásáért.
    - New-AzEventGridTopic/New-AzEventGridDomain:
        - Új választható paraméterek lettek hozzáadva a bemenetleképezés támogatásáért.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Modul frissítve a 2020-05-01-es API-verzió használatára
* Privátkapcsolat-támogatás hozzáadva a Storage-, KeyVault- és Web App Service-erőforrásokhoz

#### <a name="azhdinsight"></a>Az.HDInsight
* ADLSGen1/2-tárolóval rendelkező fürt országos felhőkben való létrehozásának támogatása.

#### <a name="azmonitor"></a>Az.Monitor
* Ki lett javítva a Get-AzDiagnosticSetting hibája, amely miatt a metrikák vagy naplók null értékűek [#12272]

#### <a name="aznetwork"></a>Az.Network
* A paraméterek felcserélése ki lett javítva a VWan–HubVnet kapcsolatban
* Új parancsmagok lettek hozzáadva az Azure hálózati virtuális berendezések helyéhez
    - Get-AzVirtualApplianceSite
    - New-AzVirtualApplianceSite
    - Remove-AzVirtualApplianceSite
    - Update-AzVirtualApplianceSite
    - New-AzOffice365PolicyProperty
* Új parancsmagok lettek hozzáadva az Azure hálózati virtuális berendezésekhez
    - Get-AzNetworkVirtualAppliance
    - New-AzNetworkVirtualAppliance
    - Remove-AzNetworkVirtualAppliance
    - Update-AzNetworkVirtualAppliance
    - Get-AzNetworkVirtualApplianceSku
    - New-AzVirtualApplianceSkuProperty
* Application Gateway előkészítve a Private Link gyakori parancsmagjaihoz
* StorageSync előkészítve a Private Link gyakori parancsmagjaihoz
* SignalR előkészítve a Private Link gyakori parancsmagjaihoz

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* A hitelesítés projekthivatkozása eltávolítva
* Azure Backup-parancsmagok finomhangolása a pontosabb szövegért.
* Az Azure Backup mostantól támogatott az MAB-ügynökfeladatok beolvasásához a Get-AzRecoveryServicesBackupJob parancsmag használatával.

#### <a name="azresources"></a>Az.Resources
* A Save-AzResourceGroupDeploymentTemplate frissítése az SDK használatához.
* Unregister-AzResourceProvider parancsmag hozzáadva.

#### <a name="azsql"></a>Az.Sql
* Szolgáltatásnév és vendégfelhasználók támogatása hozzáadva a Set-AzSqlInstanceActiveDirectoryAdministrator parancsmagban
* Ki lett javítva egy hiba az adatbesorolási parancsmagokban.
* A felügyelt Azure SQL-példány feladatátvétele mostantól támogatott: Invoke-AzSqlInstanceFailover

#### <a name="azstorage"></a>Az.Storage
* Ki lett javítva az a probléma, amely miatt a UserAgent nem adható hozzá egyes adatsíkparancsmagokhoz.
* Storage-fiók létrehozásának/frissítésének támogatása a MinimumTlsVersion és az AllowBlobPublicAccess használatával
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* A Storage-fiókok Blob service-beli verziószámozása engedélyezésének/letiltásának támogatása
    - Update-AzStorageBlobServiceProperty
* Blobok blobverziókkal való listázásának támogatása
    - Get-AzStorageBlob
* Egyetlen blobpillanatkép vagy blobverzió lekérésének/eltávolításának támogatása
    - Get-AzStorageBlob
    - Remove-AzStorageBlob
* Az Azure.Storage.Blobs 12-es verziójában létrehozott blobobjektum folyamatának támogatása
    - Get-AzStorageBlobContent
    - New-AzStorageBlobSASToken
    - Remove-AzStorageBlob
    - Set-AzStorageBlobContent
    - Start-AzStorageBlobCopy

#### <a name="azstoragesync"></a>Az.StorageSync
* A 2020-03-01-es API-verziót célzó StorageSync SDK új verziója hozzáadva
* Tárolószinkronizálási szolgáltatás frissítési parancsmagja hozzáadva
    - Set-AzStorageSyncService
* IncomingTrafficPolicy és PrivateEndpointConnections hozzáadva a StorageSyncService parancsmagokhoz.

#### <a name="azwebsites"></a>Az.Websites
* Támogatás hozzáadva az olyan Pontok műveleteinek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag

## <a name="430---june-2020"></a>4.3.0 – 2020. június
#### <a name="azaccounts"></a>Az.Accounts
* A környezetfelderítés beállítása és a környezet hozzáadása az Add-AzEnvironment használatával alapértelmezés szerint támogatott
* Előre betöltött szerelvények frissítése [#12024], [#11976]
* Az Azure.Core szerelvény frissült
* Ki lett javítva egy probléma, amely a Connect-AzAccount meghiúsulását okozhatta többszálas végrehajtás esetében [#11201]

#### <a name="azaks"></a>Az.Aks
* A régi [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) használata helyébe a [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) és a [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) API-k meghívása lépett

#### <a name="azbatch"></a>Az.Batch
* Frissítve lett az Az.Batch a Microsoft.Azure.Management.Batch SDK 11.0.0-s verziójának használatára
* Hozzá lett adva a BatchAccount identitás beállításának lehetősége a New-AzBatchAccount parancsmagban

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* A fiók képességeinek megjelenítése támogatott.
* Támogatott a PublicNetworkAccess paraméter módosítása.

#### <a name="azcompute"></a>Az.Compute
* A SimulateEviction paraméter hozzá lett adva a Set-AzVm és a Set-AzVmssVM parancsmagokhoz.
* A Premium_LRS hozzá lett adva a StorageAccountType paraméter argumentumbefejezőjéhez a New-AzGalleryImageVersion parancsmagban.
* Alállapotok lettek hozzáadva a VMCustomScriptExtension bővítményhez [#11297]
* A Törlés lehetőség hozzá lett adva az EvictionPolicy paraméter argumentumbefejezőjéhez a New-AzVM és a New-AzVMConfig parancsmagokban.
* Az új virtuálisgép-bővítmény neve ki lett javítva az SAP esetében

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK a 4.9.0-s verzióra frissült

#### <a name="azeventhub"></a>Az.EventHub
* Managed Identity-paraméterek lettek hozzáadva a New-AzEventHubNamespace és a Set-AzEventHubNamespace parancsmaghoz

#### <a name="azfunctions"></a>Az.Functions
* A PowerShell 7.0- és a Java 11-függvényalkalmazások létrehozása mostantól támogatott

#### <a name="azhdinsight"></a>Az.HDInsight
* Támogatott a gazdagépek listázása és a HDInsight-fürt adott gazdagépeinek újraindítása.

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Az SDK a 1.1.0-s verzióra frissült
* Az exportálási beállítások és a Managed Identity mostantól támogatottak

#### <a name="azmonitor"></a>Az.Monitor
* Ki lett javítva a bemeneti objektumparaméter a Set-AzActivityLogAlert parancsmag esetében
* Ki lett javítva az InputObject paraméter a Set-AzActionGroup parancsmag esetében [#10868]

#### <a name="aznetwork"></a>Az.Network
* Az AddressPrefixType paraméter mostantól támogatott a Remove-AzExpressRouteCircuitConnectionConfig esetében
* Új parancsmagok lettek hozzáadva az Azure FirewallPolicy szabályzathoz
    - New-AzFirewallPolicyDnsSetting
    - A tűzfalszabályzathoz tartozó hálózati szabályok céltartományneveinek támogatása
* A háttércímkészlet műveletei mostantól támogatottak
    - New-AzLoadBalancerBackendAddressConfig
    - New-AzLoadBalancerBackendAddressPool
    - Set-AzLoadBalancerBackendAddressPool
    - Remove-AzLoadBalancerBackendAddressPool
    - Get-AzLoadBalancerBackendAddressPool
* A New-AzIpGroup névérvényesítése hozzáadva
* Új parancsmagok lettek hozzáadva az Azure FirewallPolicy szabályzathoz
    - New-AzFirewallPolicyThreatIntelWhitelist
* Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni DNS-kiszolgálók beállítása/eltávolítása a VirtualWan-P2SVpnGateway átjárón.
    - Frissült a New-AzP2sVpnGateway: A -CustomDnsServer opcionális paraméter hozzá lett adva az ügyfelek számára, hogy megadhassák a P2SVpnGateway átjárón beállítani kívánt DNS-kiszolgálókat (ezeket pont–hely ügyfelek is használhatják).
    - Frissült az AzP2sVpnGateway: A -CustomDnsServer opcionális paraméter hozzá lett adva az ügyfelek számára, hogy megadhassák a P2SVpnGateway átjárón beállítani kívánt DNS-kiszolgálókat (ezeket pont–hely ügyfelek is használhatják).
* Frissült az Update-AzVpnGateway
    - A -BgpPeeringAddress opcionális paraméter hozzá lett adva az ügyfelek számára a VPN Gateway átjárón beállítani kívánt egyéni bgps megadásához.
* Új parancsmag lett hozzáadva a VirtualHub-erőforrás útválasztási állapota visszaállításának támogatásához:
    - Reset-AzHubRouter
* A tűzfalszabályzat legutóbbi Swagger-módosításának megfelelően frissültek az alábbi tételek
    - A RuleGroup, a RuleCollectionGroup és a RuleType neve megváltozott
    - Mostantól támogatott a tűzfalszabályzat NAT-szabálygyűjteménye esetében több NAT-szabálygyűjtemény használata
* [Kompatibilitástörő változás] Kötelező SourceIpGroup paraméter lett hozzáadva a New-AzFirewallPolicyApplicationRule és a New-AzFirewallPolicyNetworkRule esetében.
* [Kompatibilitástörő változás] A New-AzFirewallPolicyApplicationRule ki lett javítva, a SourceAddress paramétert kötelező megadni.
* [Kompatibilitástörő változás] A New-AzFirewallPolicyApplicationRule ki lett javítva, a SourceAddress paramétert kötelező megadni.
* [Kompatibilitástörő változás] Eltávolított kötelező paraméterek: TranslatedAddress, TranslatedPort a New-AzFirewallPolicyNatRuleCollection esetében.
* Új parancsmagok lettek hozzáadva a PrivateLink támogatásához az Application Gatewayen
    - New-AzApplicationGatewayPrivateLinkConfiguration
    - Get-AzApplicationGatewayPrivateLinkConfiguration
    - New-AzApplicationGatewayPrivateLinkConfiguration
    - Set-AzApplicationGatewayPrivateLinkConfiguration
    - Remove-AzApplicationGatewayPrivateLinkConfiguration
    - New-AzApplicationGatewayPrivateLinkIpConfiguration
* Új parancsmagok lettek hozzáadva a VirtualHub HubRouteTables gyermekerőforrásai esetében.
    - New-AzVHubRoute
    - New-AzVHubRouteTable
    - Get-AzVHubRouteTable
    - Update-AzVHubRouteTable
    - Remove-AzVHubRouteTable
* Frissültek a meglévő parancsmagok az opcionális RoutingConfiguration bemeneti paraméter támogatásához az egyéni útválasztás esetében a VirtualWanban.
    - New-AzExpressRouteConnection
    - Set-AzExpressRouteConnection
    - New-AzVirtualHubVnetConnection
    - Update-AzVirtualHubVnetConnection
    - New-AzVpnConnection
    - Update-AzVpnConnection
    - New-AzP2sVpnGateway
    - Update-AzP2sVpnGateway

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Ki lett javítva az a PSWorkspace-hiba, amely miatt meghiúsult az IOperationalInsightsWorkspace implementálása [#12135]
* A pergb2018 hozzá lett adva az SKU paraméter érvényes értékéhez a Set-AzOperationalInsightsWorkspace esetében 
* A FunctionParameters alias hozzá lett adva a FunctionParameter paraméterhez a következők esetében:
    - New-AzOperationalInsightsSavedSearch
    - Set-AzOperationalInsightsSavedSearch

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Az Azure Backup mostantól támogatott az MAB-elemek beolvasásához.
* Az Azure Site Recovery támogatja a StandardSSD_LRS lemeztípust

#### <a name="azresources"></a>Az.Resources
* A UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail paraméterek hozzá lettek adva a PSADUser esetében [#10526] [#10497]
* Ki lett javítva az a hiba, hogy a -Mail nem működött a Get-AzADUser esetében [#11981]
* Az -ExcludeChangeType paraméter hozzá lett adva a következőkhöz: Get-AzDeploymentWhatIfResult és Get-AzResourceGroupDeploymentWhatIfResult
* A -WhatIfExcludeChangeType paraméter hozzá lett adva a következőkhöz: New-AzDeployment és New-AzResourceGroupDeployment
* A Test-Az*Deployment parancsmagok frissültek a megfelelőbb hibaüzenetek megjelenítéséhez
* Ki lett javítva az üzemelő példány -Name paraméterének súgóüzenete a create és a What-If parancsmagok esetében

#### <a name="azsql"></a>Az.Sql
* Szolgáltatásnév támogatása hozzáadva a Set SQL Server Azure Active Directory Admin parancsmag esetében
* Ki lett javítva a szinkronizálási probléma az adatbesorolási parancsmagok esetében.
* Támogatott az e-mail-cím alapján történő felhasználókeresés a következő esetében: Set-AzSqlServerActiveDirectoryAdministrator [#12192]

#### <a name="azstorage"></a>Az.Storage
* Támogatott a tárfiók RequireInfrastructureEncryption használatával való létrehozása
    -  New-AzStorageAccount
* Át lett helyezve az Azure.Core betöltési logikája Az.Accounts modulba

#### <a name="azwebsites"></a>Az.Websites
* Hozzáadott védelem a létrehozott webalkalmazás törléséhez, ha a visszaállítás nem sikerült a Restore-AzDeletedWebApp esetében
* A SourceWebApp.Location paraméter hozzá lett adva a New-AzWebApp és a New-AzWebAppSlot esetében
* Ki lett javítva az a hiba, amely megakadályozta a tárolóbeállítások módosítását a Set-AzWebApp és a Set-AzWebAppSlot esetében
* Ki lett javítva a SiteConfig lekérésének hibája, ha a -Name nem lett megadva a Get-AzWebApp esetében
* Támogatás hozzáadva ASP létráhozásához Linux-alkalmazások esetében
* Kivételek hozzáadva az erőforráscsoportok közötti klónozás esetében

## <a name="420---june-2020"></a>4.2.0 – 2020. június
#### <a name="azaccounts"></a>Az.Accounts
* Kijavítottunk egy problémát, amely miatt az Az Azure Automation-naplókat vagy PowerShell-feladatokat hagyott ki [#11492]

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Frissítettük az adatsík parancsmagjainak szerelvényverzióját

#### <a name="azapimanagement"></a>Az.ApiManagement
* Frissítettük a szolgáltatásfelügyeleti parancsmagok szerelvényverzióját

#### <a name="azbilling"></a>Az.Billing
* Frissítettük a felhasználási parancsmagok szerelvényverzióját

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* A PrivateEndpoint és a PublicNetworkAccess vezérlők támogatása. 

#### <a name="azdatafactory"></a>Az.DataFactory
* Frissítettük a Data Factory V2 parancsmagjainak szerelvényverzióját

#### <a name="azdatashare"></a>Az.DataShare
* Az Az.DataShare modul általános rendelkezésre állása

#### <a name="azdesktopvirtualization"></a>Az.DesktopVirtualization
* Az „Az.DesktopVirtualization” modul általános rendelkezésre állása

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* SDK frissítve a 0.21.0-s verzióra
* Választható paraméterek hozzáadva a következőkhöz: 
    - New-AzOperationalInsightsSavedSearch
    - Set-AzOperationalInsightsSavedSearch

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Javítottuk a Start-AzPolicyComplianceScan 3. példáját

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Frissítettük a PowerBI-parancsmagok szerelvényverzióját

#### <a name="azprivatedns"></a>Az.PrivateDns
* Javítottuk a Remove-AzPrivateDnsRecordSet kimeneti sztringjének formázását

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery-támogatás helyreállítási terv létrehozásához az xml-bemenetből kezdeményezett, zónák közötti replikáció esetében.
* Frissítettük a SiteRecovery és a Backup parancsmagok szerelvényverzióját

#### <a name="azresources"></a>Az.Resources
* Szélsőérték paraméter hozzáadva a Get-AzDeploymentScriptLog és a Save-AzDeploymentScriptLog parancsmagokhoz
* Kimeneti tulajdonság formázása és megjelenítése a Get-AzDeploymentScript parancsmag kimenetén
* A -DeploymentScriptInputObject paraméter új neve -DeploymentScriptObject
* Javítottuk a parancsmagüzenetek hiányzó fájl-/célnevét.
* Frissítettük a Resource Manager és a címkék parancsmagjainak szerelvényverzióját

#### <a name="azsql"></a>Az.Sql
* UsePrivateLinkConnection hozzáadva a következőkhöz: New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember és Update-AzSqlSyncMember
* SyncMemberAzureDatabaseResourceId hozzáadva a következőkhöz: New-AzSqlSyncMember és Update-AzSqlSyncMember
* Vendégfelhasználó-keresés támogatása hozzáadva a Set SQL Server Azure Active Directory Admin parancsmaghoz

#### <a name="azstorage"></a>Az.Storage
* Frissítettük az adatsík parancsmagjainak szerelvényverzióját

## <a name="410---may-2020"></a>4.1.0 – 2020. május
### <a name="highlights-since-the-last-release"></a>A legutóbbi kiadás óta bevezetett újdonságok
* Támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7
* Az Az.Functions általános rendelkezésre állása 
* A következők rendelkeznek nagyobb kiadással: Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources és Az.Storage

#### <a name="azaccounts"></a>Az.Accounts
* Frissítve lett az Add-AzEnvironment és a Set-AzEnvironment parancsmag, amelyek mostantól elfogadják az AzureSynapseAnalyticsEndpointResourceId és az AzureSynapseAnalyticsEndpointSuffix paramétereket
* Hozzá lettek adva az Azure.Core-hoz kapcsolódó szerelvények az Az.Accounts-hoz, a támogatott platformok a Windows PowerShell 5.1, a PowerShell Core 6.2.4 és a PowerShell 7+

#### <a name="azaks"></a>Az.Aks
* Az API-verzió frissítve lett a 2019-10-01-es verzióra
* Az AKS Windows-tárolókkal történő létrehozásának támogatása
* Elérhető új parancsmagok: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool,        Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion

#### <a name="azapimanagement"></a>Az.ApiManagement
* New-AzApiManagement és Set-AzApiManagement: az [-AssignIdentity] paraméter új neve [-SystemAssignedIdentity]
* New-AzApiManagement és Set-AzApiManagement: Új paraméter lett hozzáadva: [-UserAssignedIdentity <String[]>]
* A Get-AzApiManagementProperty át lett nevezve a következőre: Get-AzApiManagementNamedValue. A PropertyId paraméter át lett nevezve a következőre: NamedValueId.
* A New-AzApiManagementProperty át lett nevezve a következőre: New-AzApiManagementNamedValue. A PropertyId paraméter át lett nevezve a következőre: NamedValueId. 
* A Set-AzApiManagementProperty át lett nevezve a következőre: Set-AzApiManagementNamedValue. A PropertyId paraméter át lett nevezve a következőre: NamedValueId.
* A Remove-AzApiManagementProperty át lett nevezve a következőre: Remove-AzApiManagementNamedValue. A PropertyId paraméter át lett nevezve a következőre: NamedValueId.
* Hozzá lett adva az új Get-AzApiManagementAuthorizationServerClientSecret parancsmag, valamint a Get-AzApiManagementAuthorizationServer már nem ad vissza titkos ügyfélkulcsot.
* Hozzá lett adva az új Get-AzApiManagementNamedValueSecretValue parancsmag, és a Get-AzApiManagementNamedValue nem ad vissza titkos kulcsot.
* Hozzá lett adva az új Get-AzApiManagementOpenIdConnectProviderClientSecret parancsmag, valamint a Get-AzApiManagementOpenIdConnectProvider már nem ad vissza titkos ügyfélkulcsot.
* Hozzá lett adva az új Get-AzApiManagementSubscriptionKey parancsmag, és a Get-AzApiManagementSubscription már nem ad vissza előfizetési azonosítót.
* Hozzá lett adva az új Get-AzApiManagementTenantAccessSecret parancsmag, és a Get-AzApiManagementTenantAccess már nem ad vissza kulcsot.
* Hozzá lett adva az új Get-AzApiManagementTenantGitAccessSecret parancsmag, és a Get-AzApiManagementTenantGitAccess már nem ad vissza kulcsot.

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Hozzáadott paraméterek: A New-AzApplicationInsights esetében: RetentionInDays, PublicNetworkAccessForIngestion, PublicNetworkAccessForQuery
* Létre lett hozva az Update-AzApplicationInsights parancsmag
* Parancsmagok lettek létrehozva a társított tárfiókhoz

#### <a name="azbatch"></a>Az.Batch
* Frissítve lett az Az.Batch a Microsoft.Azure.Batch SDK 13.0.0.-s verziójának és a Microsoft.Azure.Management.Batch SDK 9.0.0-s verziójának használatára.
* Kiválaszthatóvá vált a hozzáadni kívánt tanúsítvány típusa a New-AzBatchCertificate új -CertificateKind paraméterének használatával.
* El lett távolítva az ApplicationPackages tulajdonság a PSApplicationből, amelynek típusa eddig mindig '' volt.
  - Most már lekérhetők az alkalmazásokon belüli adott csomagok a Get-AzBatchApplicationPackage használatával. Például: Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication.
* Egy készlet New-AzBatchPool használatával történő létrehozásakor a PSImageReference VirtualMachineImageId tulajdonsága már csak a Shared Image Gallery-ben található rendszerképre hivatkozhat.
* Egy készlet New-AzBatchPool használatával történő létrehozásakor a készlet nyilvános IP-cím nélkül is létrehozható a PSNetworkConfiguration új PublicIPAddressConfiguration tulajdonságával.
  - A PSNetworkConfiguration PublicIPs tulajdonsága a PSPublicIPAddressConfiguration esetében is elérhető. Ez a tulajdonság csak akkor adható meg, ha az IPAddressProvisioningType UserManaged típusú.

#### <a name="azcompute"></a>Az.Compute
* A HostId paraméter hozzá lett adva az Update-AzVM parancsmaghoz
* Frissültek a New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem és Set-AzVmssOsProfile parancsmagok súgódokumentumai.
* Kompatibilitástörő változások
    - A FilterExpression paraméter el lett távolítva a Get-AzVMImage parancsmagból.
    - Az AssignIdentity paraméter el lett távolítva a New-AzVmssConfig, New-AzVMConfig és Update-AzVM parancsmagokból.
    - Az AutomaticRepairMaxInstanceRepairsPercent paraméter el lett távolítva a New-AzVmssConfig és az Update-AzVmss parancsmagokból.
    - Az AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus és VirtualMachineScaleSetsColocationStatus tulajdonságok el lettek távolítva a ProximityPlacementGroup paraméterből.
    - A MaxInstanceRepairsPercent tulajdonság el lett távolítva a következőből: AutomaticRepairsPolicy.
    - Az AvailabilitySets, VirtualMachines és VirtualMachineScaleSets típusa IList<SubResource> helyett mostantól IList<SubResourceWithColocationStatus>.
* Frissült a Get-AzVM parancsmag leírása, hogy pontosabban ismertesse a parancsmagot. 

#### <a name="azdatafactory"></a>Az.DataFactory
* Adatfolyam futtatókörnyezeti tulajdonságaihoz tartozó CRUD támogatása a felügyelt IR-ben.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Új parancsmagok lettek hozzáadva a Front Door szabálymotor-objektumának létrehozására, frissítésére, lekérésére és törlésére.
* Hozzá lettek adva segítő parancsmagok a Front Door szabálymotor-objektumának létrehozásához
* Hozzá lett adva a szabálymotor-referencia a Front Door útválasztásiszabály-objektumához.
* Hozzá lettek adva privát kapcsolati paraméterek a Front Door háttérobjektumához

#### <a name="azfunctions"></a>Az.Functions
* Az Az.Functions modul általános rendelkezésre állása

#### <a name="azhdinsight"></a>Az.HDInsight
* Az ügyfél által felügyelt kulcson alapuló lemeztitkosítás mostantól támogatott.

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* A hozzáférési szabályzatok már nem tartoznak alapértelmezés szerint az aktuális rendszerbiztonsági taghoz

#### <a name="aziothub"></a>Az.IotHub
* Hozzá lett adva egy parancsmag, amellyel egy SQL-szerű nyelv használatával végzett, információkat lekérő lekérdezés indítható el az IoT Hubban.
* Javítva a hiba, amely miatt az Add-AzIotHubDevice gyermekeszköz nélkül nem tudott Edge-kompatibilis eszközt létrehozni [#11597]
* Hozzá lett adva egy parancsmag egy SAS-token létrehozásához az IoT Hub, eszköz vagy modul számára.
* Hozzá lett adva egy parancsmag a konfiguráció-metrikák lekérdezésének meghívásához.
* Az IoT Edge nagy léptékű automatikus üzembe helyezésének kezelése. Az új parancsmagok a következők:
    - Add-AzIotHubDeployment
    - Get-AzIotHubDeployment
    - Remove-AzIotHubDeployment
    - Set-AzIotHubDeployment
* Hozzá lett adva egy parancsmag, amellyel az IoT Edge üzembehelyezési metrikáit lekérő lekérdezést hívható meg.
* Hozzá lett adva egy parancsmag a konfiguráció tartalmának egy adott Edge-eszközre történő alkalmazásához.

#### <a name="azkeyvault"></a>Az.KeyVault
* A következő két alias el lett távolítva: New-AzKeyVaultCertificateAdministratorDetails és New-AzKeyVaultCertificateOrganizationDetails
* Alapértelmezés szerint engedélyezve lett a helyreállítható törlés egy kulcstartó létrehozásakor
* Kulcstartó létrehozásakor a hálózati szabályok beállíthatók a megadott hálózati helyekről való hozzáférés szabályozására
* A saját kulcs használata (BYOK) már támogatott
    - Az Add-AzKeyVaultKey támogatja a kulcscserekulcsok létrehozását
    - A Get-AzKeyVaultKey támogatja a nyilvános kulcsok PEM formátumban való letöltését
* Frissült az Add-AzKeyVaultKey súgódokumentációjának KeyOps része

#### <a name="azmonitor"></a>Az.Monitor
* Javítva a Set-AzDiagnosticSettings hibája, amely miatt a megtartási szabályzat nem vonatkozott minden kategóriára [#11589]
* A WebTest rendelkezésre állási feltételeinek támogatása a 2-es verziójú metrikariasztás esetében
    - New-AzMetricAlertRuleV2Criteria: mostantól megadhatók a webteszt rendelkezésre állási feltételei
    - Add-AzMetricAlertRuleV2: támogatja a webteszt új rendelkezésre állási feltételeit
* El lett távolítva a RetentionPolicy redundáns definíciója a PSLogProfile-ból [#7608]
* El lettek távolítva a PSEventData objektumban meghatározott redundáns tulajdonságok [#11353]
* A Get-Azlog át lett nevezve a következőre: Get-AzActivityLog

#### <a name="aznetwork"></a>Az.Network
* Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely figyelmeztet a Zone alapértelmezett viselkedésének változásáról
    - New-AzPublicIpAddress
    - New-AzPublicIpPrefix
    - New-AzLoadBalancerFrontendIpConfig
* Hozzá lett adva az új, SecurityPartnerProvider legfelsőbb szintű erőforrás támogatása
    - Új hozzáadott parancsmagok:
        - New-AzSecurityPartnerProvider
        - Remove-AzSecurityPartnerProvider
        - Get-AzSecurityPartnerProvider
        - Set-AzSecurityPartnerProvider
* Hozzá lett adva a RequiredZoneNames tulajdonság a PSPrivateLinkResource esetében, és a GroupId a PSPrivateEndpointConnection esetében
* Kijavítva a SuccessThresholdRoundTripTimeMs paraméter típusa a New-AzNetworkWatcherConnectionMonitorTestConfigurationObject esetében
* Frissítve lettek a VirtualWan parancsmagok az AllowVnetToVnetTraffic argumentum True értékre való állításához.
    - New-AzVirtualWan
    - Update-AzVirtualWan
* Új parancsmagok lettek hozzáadva a privát végpontok DNS-zónacsoportjainak támogatásához
    - New-AzPrivateDnsZoneConfig
    - Get-AzPrivateDnsZoneGroup
    - New-AzPrivateDnsZoneGroup
    - Set-AzPrivateDnsZoneGroup
    - Remove-AzPrivateDnsZoneGroup
* Hozzá lett adva a DNSEnableProxy, a DNSRequireProxyForNetworkRules és a DNSServers paraméter az AzureFirewall-hoz
* Hozzá lett adva az EnableDnsProxy, a DnsProxyNotRequiredForNetworkRule és a DnsServer paraméter az AzureFirewall-hoz
    - Frissített parancsmag:
        - New-AzFirewall

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Frissítve lett a régi kód az újonnan létrehozott SDK alkalmazásához
* Az elavult API-k miatt törölt parancsmagok
    - Get-AzOperationalInsightsSavedSearchResult (alias: Get-AzOperationalInsightsSavedSearchResults)
    - Get-AzOperationalInsightsSearchResult (alias: Get-AzOperationalInsightsSearchResults)
    - Get-AzOperationalInsightsLinkTarget (alias: Get-AzOperationalInsightsLinkTargets)
* Paraméterek lettek hozzáadva a Set-AzOperationalInsightsWorkspace és New-AzOperationalInsightsWorkspace parancsmaghoz
* Parancsmagok lettek létrehozva a társított tárfiókhoz
* Parancsmagok lettek létrehozva a fürtökhöz és a társított szolgáltatáshoz

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Hozzá lett adva az Azure Site Recovery-támogatás a közelségi elhelyezési csoportokban lévő virtuális gépek védelme érdekében, az Azure–Azure szolgáltatók esetében.
* Hozzá lett adva az Azure Site Recovery-támogatás a zónák közötti replikáció esetében.
* Az Azure Backup már támogatja a hosszú távú megőrzést az Azure FileShare helyreállítási pontok esetében.
* Hozzá lettek adva az Azure Backup lemezkizárási tulajdonságok a Get-AzRecoveryServicesBackupItem parancsmag kimenetéhez.
* Hozzá lett adva a privát végpont a Vault hitelesítési fájljaihoz a Site Recovery szolgáltatás esetében.

#### <a name="azresources"></a>Az.Resources
* Hozzá lett adva a megtekintés késéséről figyelmeztető üzenet az új szerepkör-definíció létrehozása során
* Módosítva lettek a szabályzat-parancsmagok a szigorú típusmegadású objektumok megjelenítéséhez
* El lett távolítva a Get-AzResourceLock parancsmaghoz használt -TenantLevel paraméter [#11335]
* Javítva a Remove-AzResourceGroup -Id ResourceId parancsmag [#9882]
* Hozzá lett adva egy új parancsmag az ARM-sablon What-If típusú eredményeinek lekéréséhez az erőforráscsoport hatókörében: Get-AzDeploymentResourceGroupWhatIfResult
* Hozzá lett adva egy új parancsmag az ARM-sablonok What-If típusú eredményeinek lekéréséhez az előfizetés hatókörében: Get-AzDeploymentWhatIfResult
   - Alias: Get-AzSubscriptionDeploymentWhatIf
* A -WhatIf és a -Confirm paraméter felül lett írva a New-AzDeployment és a New-AzResourceGroupDeployment parancsmagok esetében az ARM-sablon What-If típusú eredményeinek használata érdekében
* Hozzá lett adva az elavulási üzenet az ApiVersion paraméterhez az üzembehelyezési parancsmagokban
* Hozzá lett adva egy képesség, amely lehetővé teszi, hogy fejlettebb hibaüzenetek jelenjenek meg az üzembehelyezési hibák esetén
* Hozzá lett adva a correlationId-naplózása az üzembehelyezési hibák esetében
* Hozzá lett adva az error tulajdonság az üzembehelyezési szkript kimenetéhez
* A Microsoft.Azure.Management.ResourceManager NuGet frissítve lett a 3.7.1-preview verzióra
* El lettek távolítva adott tesztesetek, mivel a DeploymentValidateResult Error tulajdonsága csak olvasható állapotúra változott a NuGet 3.7.1-preview verziójától kezdődően
* A GenericResourceExpanded át lett hozva a ResourceManager SDK 3.7.1-preview verziójából
* Hozzá lett adva a címketámogatás az összes, üzembe helyezéshez használt Get parancsmaghoz, valamint a következőkhöz:
    - New-AzDeployment
    - New-AzManagementGroupDeployment
    - New-AzResourceGroupDeployment
    - New-AzTenantDeployment

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Javítva a hiba, amely hibás tanúsítvány-ujjlenyomatot kért le a tanúsítvány --SecretIdentifier használatával történő hozzáadásakor

#### <a name="azsql"></a>Az.Sql
* Javult a következők teljesítménye:
    - Set-AzSqlDatabaseSensitivityClassification
    - Set-AzSqlInstanceDatabaseSensitivityClassification
    - Remove-AzSqlDatabaseSensitivityClassification
    - Remove-AzSqlInstanceDatabaseSensitivityClassification
    - Enable-AzSqlDatabaseSensitivityRecommendation
    - Enable-AzSqlInstanceDatabaseSensitivityRecommendation
    - Disable-AzSqlDatabaseSensitivityRecommendation
    - Disable-AzSqlInstanceDatabaseSensitivityRecommendation
* El lett távolítva a RetentionDays paraméter ügyféloldali érvényesítése a Set-AzSqlDatabaseBackupShortTermRetentionPolicy parancsmagból
* A Vnet-ben található tárfiók naplózása, javítva a Storage Blob-adatok közreműködői szerepkörének létrehozásakor fellépő hiba.

#### <a name="azstorage"></a>Az.Storage
* Hozzá lett adva az -AsJob a fiók Get-AzStorageAccount parancsmagjának lekéréséhez vagy listázásához
* A KeyVersion választható lett a Storage-fiók KeyvaultEncryption használatával történő frissítésekor a kulcs automatikus rotálásának támogatásához
    - Set-AzStorageAccount
* Javítva a hiba, amely során az Azure File Directory eltávolítása egy folyamattal meghiúsult
    - Remove-AzStorageDirectory
* [#9880] javítva: Módosítva lett a NetWorkRule DefaultAction értékdefiníciója, hogy megfeleljen a Swaggernek.
    - Update-AzStorageAccountNetworkRuleSet
    - Get-AzStorageAccountNetworkRuleSet
* [#11624] javítva: Duplikált szabályok kihagyása NetworkRules hozzáadásakor a kiszolgáló meghibásodásának elkerülése érdekében
    - Add-AzStorageAccountNetworkRule
* A Microsoft.Azure.Cosmos.Table SDK verziója 1.0.7-re frissült
* Hozzá lett adva egy figyelmeztető üzenet, amely emlékezteti a felhasználót, hogy listázzon újra a ContinuationToken használatával, ha csak részleges elemeket ad vissza a rendszer a Data Lake Gen2 elemek listáján
    - Get-AzDataLakeGen2ChildItem
* Storage-fiók létrehozásának és frissítésének támogatása Azure Files Active Directory Domain Service-hitelesítéssel
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Storage-fiók Kerberos-kulcsai listázásának vagy új Kerberos-kulcsok létrehozásának támogatása
    -  New-AzStorageAccountKey
    -  Get-AzStorageAccountKey
* Feladatátvételi Storage-fiók támogatása
    - Invoke-AzStorageAccountFailover
* Frissítve a Get-AzStorageBlobCopyState súgója
* Frissítve a Get-AzStorageFileCopyState és a Start-AzStorageBlobCopy súgója
* A Storage-ügyfélkódtár 12-es verziója integrálva lett a Queue és a File parancsmagokba
* A kimenet típusa CloudFile helyett mostantól AzureStorageFile, az eredeti kimenet az új kimenet gyermektulajdonsága lesz
    - Get-AzStorageFile
    - Remove-AzStorageFile
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent
    - Start-AzStorageFileCopy
* A kimenet típusa CloudFileDirectory helyett mostantól AzureStorageFileDirectory, az eredeti kimenet az új kimenet gyermektulajdonsága lesz
    - New-AzStorageDirectory
    - Remove-AzStorageDirectory
* A kimenet típusa CloudFileShare helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet gyermektulajdonsága lesz
    - Get-AzStorageShare
    - New-AzStorageShare
    - Remove-AzStorageShare
* A kimenet típusa FileShareProperties helyett mostantól AzureStorageFileShare, az eredeti kimenet az új kimenet gyermek-altulajdonsága lesz
    - Set-AzStorageShareQuota

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Javítva a hibás profilnév a DisableAzureTrafficManagerEndpoint részletes kimenetében

#### <a name="azwebsites"></a>Az.Websites
* Javítva az elgépelés az Update-AzWebAppAccessRestrictionConfig súgójában.

## <a name="380---april-2020"></a>3.8.0 – 2020. április
### <a name="highlights-since-the-last-release"></a>A legutóbbi kiadás óta bevezetett újdonságok
* Az Az.Storage által támogatott PowerShell-verziók: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7

#### <a name="azaccounts"></a>Az.Accounts
* Frissítve lett az Azure PowerShell-felmérés URL-címe a következő helyen: Resolve-AzError [#11507]

#### <a name="azapimanagement"></a>Az.ApiManagement
* Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban
* Set-AzApiManagementGroup – Frissítve lett a dokumentáció a GroupId paraméter meghatározása érdekében

#### <a name="azcdn"></a>Az.Cdn
* Ki lett javítva a díjszabási termékváltozat megjelenítése a ChinaCDN kapcsán

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Támogatott identitás, Titkosítás, UserOwnedStorage

#### <a name="azcompute"></a>Az.Compute
* Hozzá lett adva a Set-AzVmssOrchestrationServiceState parancsmag.
* A Get-AzVmss az InstanceView használatával az OrchestrationService állapotait mutatja.

#### <a name="aziothub"></a>Az.IotHub
* Az IoT-ikereszköz konfigurációjának kezelése, Az új parancsmagok a következők:
    - Get-AzIotHubDeviceTwin
    - Update-AzIotHubDeviceTwin
* Hozzá lett adva egy parancsmag a közvetlen metódusok az IoT Hubban lévő eszközökön való meghívásához.
* Az IoT-ikereszköz modulja konfigurációjának kezelése, Az új parancsmagok a következők:
    - Get-AzIotHubModuleTwin
    - Update-AzIotHubModuleTwin
* Nagy méretekben történő automatikus IoT-eszközfelügyelet konfigurációjának kezelése. Az új parancsmagok a következők:
    - Add-AzIotHubConfiguration
    - Get-AzIotHubConfiguration
    - Remove-AzIotHubConfiguration
    - Set-AzIotHubConfiguration
* Hozzá lett adva egy parancsmag az Edge-modul metódusok az IoT Hubban való meghívásához.

#### <a name="azkeyvault"></a>Az.KeyVault
* Hozzá lett adva egy új Update-AzKeyVault parancsmag a helyreállító törlés és végleges törlés elleni védelem tárolón való engedélyezéséhez
* Támogatás a következőhöz: Microsoft.PowerShell.SecretManagement [#11178]
* Ki lettek javítva a Remove-AzKeyVaultManagedStorageSasDefinition [#11479] példáinak hibái
* Támogatás a privát végponthoz

#### <a name="azmaintenance"></a>Az.Maintenance
* Karbantartási parancsmagok végleges verziójának közzététele az általánosan elérhető kiadás számára

#### <a name="azmonitor"></a>Az.Monitor
* Parancsmagok hozzáadva a privát kapcsolat hatóköréhez
    - Get-AzInsightsPrivateLinkScope
    - Remove-AzInsightsPrivateLinkScope
    - New-AzInsightsPrivateLinkScope
    - Update-AzInsightsPrivateLinkScope
    - Get-AzInsightsPrivateLinkScopedResource
    - New-AzInsightsPrivateLinkScopedResource
    - Remove-AzInsightsPrivateLinkScopedResource

#### <a name="aznetwork"></a>Az.Network
* Frissítve lettek a parancsmagok a virtuális hálózati átjáróhoz való csatlakozás engedélyezéséhez magánhálózati IP-cím esetében.
    - New-AzVirtualNetworkGateway
    - Set-AzVirtualNetworkGateway
    - New-AzVirtualNetworkGatewayConnection
    - Set-AzVirtualNetworkGatewayConnection
* Frissítve lettek a parancsmagok az FQDN-alapú LocalNetworkGateways és VpnSites engedélyezéséhez
    - New-AzLocalNetworkGateway
    - New-AzVpnSiteLink
* Az IPv6-címcsalád támogatása a következőben: ExpressRouteCircuitConnectionConfig (Global Reach)
    - Hozzá lett adva a Set-AzExpressRouteCircuitConnectionConfig
        - lehetővé teszi az összes meglévő tulajdonság beállítását, beleértve a következőt is: IPv6CircuitConnectionProperties
    - Frissítve lett az Add-AzExpressRouteCircuitConnectionConfig
        - Hozzá lett adva egy másik opcionális AddressPrefixType paraméter a címelőtag címcsaládjának meghatározásához
* Frissítve lettek a parancsmagok a DPD-időtúllépés beállításának engedélyezéséhez a virtuális hálózati átjáró kapcsolatain.
    - New-AzVirtualNetworkGatewayConnection
    - Set-AzVirtualNetworkGatewayConnection

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Hozzá lett adva a Start-AzPolicyComplianceScan parancsmag a szabályzatok megfelelőségi vizsgálatának elindításához
* Szabályzatdefiníció, készletdefiníció és hozzárendelési verziók hozzáadva a Get-AzPolicyState kimenetéhez

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Tovább lett fejlesztve a kódok formázása és a használhatóság a New-AzServiceFabricCluster példái esetében

#### <a name="azsql"></a>Az.Sql
* Hozzá lettek adva a Get-AzSqlInstanceOperation és a Stop-AzSqlInstanceOperation parancsmagok
* Naplózás támogatása egy VNet-ben található tárfiókhoz.

#### <a name="azstorage"></a>Az.Storage
* Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó értesítés az Azure File parancsmagok kimenetére vonatkozóan egy későbbi kiadásban
* Támogatott új SkuName StandardGZRS, StandardRAGZRS a Storage-fiók létrehozása/frissítése során
    - New-AzStorageAccount
    - Set-AzStorageAccount
* Támogatott Data Lake Gen2
    - New-AzDataLakeGen2Item
    - Get-AzDataLakeGen2Item
    - Get-AzDataLakeGen2ChildItem
    - Move-AzDataLakeGen2Item
    - Set-AzDataLakeGen2ItemAclObject
    - Update-AzDataLakeGen2Item
    - Get-AzDataLakeGen2ItemContent
    - Remove-AzDataLakeGen2Item

## <a name="0100-preview---april-2020"></a>0.10.0-s előzetes verzió – 2020. április
### <a name="general"></a>Általános kérdések
* Az Az modulok előzetes verziója mostantól elérhető az Azure Stack Hubon. Ez lehetővé teszi a platformok közötti kompatibilitást a Linux és a macOs rendszerekkel. A Azure Stack Hub mostantól támogatja a PowerShell Core-t az Az modulokkal, további információt [itt](/azure-stack/operator/powershell-install-az-module) talál
* Az Az modulok támogatják a 2019-03-01-hybrid profilt:
  - Az.Billing
  - Az.Compute
  - Az.DataBoxEdge
  - Az.EventHub
  - Az.IotHub
  - Az.KeyVault
  - Az.Monitor
  - Az.Network
  - Az.Resources
  - Az.Storage
  - Az.Websites
* A következő három új PowerShell-modul lett bevezetve, amelyek használhatók az Azure Stack Hubbal: Az.Databox, Az.IotHub és Az.EventHub
* A parancsok viszonylag változatlanok maradnak, kisebb módosításokkal. Például az Az helyébe az AzureRM lép.
* Az Azure Stack Hubhoz kapcsolódó PowerShell-dokumentáció frissített hivatkozását [itt](/azure-stack/operator/powershell-install-az-module) találja

## <a name="370---march-2020"></a>3.7.0 – 2020. március
#### <a name="azaccounts"></a>Az.Accounts
* Ki lett javítva az a hiba, hogy a Get-AzTenant/Get-AzDefault/Set-AzDefault parancs NullReferenceException hibát ad vissza kijelentkezett állapotban [#10292]

#### <a name="azcompute"></a>Az.Compute
* A következő paraméterek lettek hozzáadva a New-AzDiskConfig parancsmaghoz:
    - DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference
* Engedélyezve lett a New-AzGalleryImageVersion parancsmag célparaméterének titkosítási tulajdonsága.
* Ki lett javítva a tempDisk hibája a Set-AzVmss -Reimage és az Invoke-AzVMReimage parancsmag esetében. [#11354]
* Az alábbi parancsmagok mostantól támogatottak az új SAP-bővítmény esetében
    - Set-AzVMAEMExtension
    - Get-AzVMAEMExtension
    - Remove-AzVMAEMExtension
    - Update-AzVMAEMExtension
* Ki lettek javítva a súgódokumentáció példáinak hibái
* Táblázatos formátumban jelenítette meg a sztring pontos értékét a PowerState virtuális gép esetében.
* New-AzVmssConfig: ki lett javítva az AutomaticRepairs tulajdonság szerializálása a SinglePlacementGroup letiltott állapota esetén. [#11257]

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK a 4.8.0-s verzióra frissült
* Opcionális paraméterek lettek hozzáadva az Invoke-AzDataFactoryV2Pipeline parancshoz az újrafuttatás támogatásához

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Hozzá lett adva a kompatibilitástörő változás leírása az Export-AzDataLakeStoreItem és az Import-AzDataLakeStoreItem parancsok esetében
* A bájtkódolási lehetőség hozzá lett adva a New-AzDataLakeStoreItem, az Add-AzDAtaLakeStoreItemContent és a Get-AzDAtaLakeStoreItemContent parancsok esetében

#### <a name="azhdinsight"></a>Az.HDInsight
* Fürt létrehozásakor a minimálisan támogatott TLS-verzió megadása támogatott.

#### <a name="aziothub"></a>Az.IotHub
* Hozzá lett adva az elosztott beállítások eszközönkénti felügyeletének támogatása. Az új parancsmagok a következők:
    - Get-AzIotHubDistributedTracing
    - Set-AzIotHubDistributedTracing

#### <a name="azkeyvault"></a>Az.KeyVault
* Kompatibilitástörő változást okozó attribútumok lettek hozzáadva a New-AzKeyVault parancshoz

#### <a name="azmonitor"></a>Az.Monitor
* Frissült a New-AzScheduledQueryRuleLogMetricTrigger dokumentációja

#### <a name="aznetwork"></a>Az.Network
* Frissültek a parancsmagok a több-bérlős VirtualHubVnetConnections engedélyezéséhez
    - New-AzVirtualHubVnetConnection
    - Update-AzVirtualHubVnetConnection
    - New-AzVirtualHub
    - Update-AzVirtualHub
* Az SQL Management SDK-függőség el lett távolítva

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Továbbfejlesztett hibaüzenetek

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Hozzá lett adva az Azure Site Recovery-támogatás az Azure Diskkel titkosított virtuális gépek védelmének újbóli beállítása és frissített virtuálisgép-tulajdonságai esetében.
* Hozzá lett adva az Azure Site Recovery VmwareToAzure tulajdonságainak vészhelyreállítási monitorozása
* Hozzá lett adva az Azure Backup-támogatás a sikertelen elemekre vonatkozó szabályzatfrissítés újbóli végrehajtása esetében.
* Hozzá lett adva az Azure Backup-támogatás a lemezkizárási beállításokhoz a biztonsági mentés és a visszaállítás során.
* Hozzá lett adva az Azure Backup-támogatás több fájl/mappa visszaállításához az AzureFileShare-ben
* Hozzá lett adva az Azure Backup-támogatás a felhasználó által megadott erőforráscsoport támogatásához az IaasVM-szabályzat frissítésekor

#### <a name="azresources"></a>Az.Resources
* Ki lett javítva a Get-AzResource-ResourceGroupName-Name-ExpandProperties-ResourceType parancs, hogy ezentúl az erőforrások aktuális API-verzióját használja az alapértelmezett verzió helyett [#11267]
* Hozzá lett adva a CorrelationId-naplózás a hibaforgatókönyvek esetében
* A Get-AzResourceLock dokumentációjában kisebb módosítás történt. Példa hozzáadva.
* A szimpla idézőjel fel lett oldva a Get-AzADUser paraméterértékében [#11317]
* Új parancsmagok lettek hozzáadva az üzembehelyezési szkriptekhez (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript)

#### <a name="azsql"></a>Az.Sql
* Olvasható másodlagos paraméter lett hozzáadva az Invoke-AzSqlDatabaseFailover parancshoz
* A Disable-AzSqlServerActiveDirectoryOnlyAuthentication parancsmag hozzá lett adva
* Az érzékenységi besorolás mentése megtörténik az adatbázis oszlopainak osztályozásakor.

#### <a name="azsupport"></a>Az.Support
* Az Az.Support modul általános rendelkezésre állása

#### <a name="azwebsites"></a>Az.Websites
* Mostantól támogatott a webalkalmazások forgalom-útválasztási szabályainak az alábbi új parancsmagokkal történő használata
    - Get-AzWebAppTrafficRouting
    - Update-AzWebAppTrafficRouting
    - Add-AzWebAppTrafficRouting
    - Remove-AzWebAppTrafficRouting

## <a name="361---march-2020"></a>3.6.1 – 2020. március
#### <a name="azaccounts"></a>Az.Accounts
* Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]
* Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]
* Az-verzió hozzáadva az UserAgenthez

#### <a name="azapimanagement"></a>Az.ApiManagement
* Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]
* Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]
* Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.
* New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1

#### <a name="aziothub"></a>Az.IotHub
* Az eszközök az IoT Hubban való kezelése mostantól támogatott. Az új parancsmagok a következők:
    - Add-AzIotHubDevice
    - Get-AzIotHubDevice
    - Remove-AzIotHubDevice
    - Set-AzIotHubDevice
* A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott. Az új parancsmagok a következők:
    - Add-AzIotHubModule
    - Get-AzIotHubModule
    - Remove-AzIotHubModule
    - Set-AzIotHubModule
* Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.
* Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.
* Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott. Az új parancsmagok a következők:
    - Get-AzIotHubDeviceParent
    - Get-AzIotHubDevice
* Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.

#### <a name="azmonitor"></a>Az.Monitor
* A Get-AzMetricDefinition kimeneti értéke javítva [#9714]

#### <a name="aznetwork"></a>Az.Network
* SQL Management SDK frissítve.
* Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.
    - Az ActionsRequired mező leképezése a követezőre: ActionRequired
* PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer

#### <a name="azresources"></a>Az.Resources
* A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva
* A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]
* Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]
* A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]
* A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva
* Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz
* Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez
* A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében
    - Get-AzTag -ResourceId
    - New-AzTag -ResourceId
    - Remove-AzTag -ResourceId
* Új címkeparancsmag hozzáadva
    - Update-AzTag -ResourceId
* A ScopedDeployment áthozva az SDK 3.3.0-ból

#### <a name="azsql"></a>Az.Sql
* PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer
* Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében
    - LTR-szabályzat lekérése/beállítása felügyelt adatbázison
    - LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint
    - LTR biztonsági másolat eltávolítása
    - LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához
* MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer
* MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance
* Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network

#### <a name="azstorage"></a>Az.Storage
* Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy
    - Set-AzRmStorageContainerImmutabilityPolicy
* Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban
    - New-AzStorageTable
    - Get-AzStorageTable

#### <a name="azwebsites"></a>Az.Websites
* Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan
* A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza
* Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag
* Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre
* Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva

## <a name="350---february-2020"></a>3.5.0 – 2020. február
### <a name="highlights-since-the-last-major-release"></a>A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok
* Frissült az ügyféloldali telemetria.
* Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.
* Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.

#### <a name="azaccounts"></a>Az.Accounts
* A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.

#### <a name="azautomation"></a>Az.Automation
* Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Az SDK a 7.0-ás verzióra frissült
* Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként

#### <a name="azcompute"></a>Az.Compute
* A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez

#### <a name="aziothub"></a>Az.IotHub
* Az eszközök az IoT Hubban való kezelése mostantól támogatott. Az új parancsmagok a következők:
    - Add-AzIotHubDevice
    - Get-AzIotHubDevice
    - Remove-AzIotHubDevice
    - Set-AzIotHubDevice

#### <a name="azkeyvault"></a>Az.KeyVault
* Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege

#### <a name="azmonitor"></a>Az.Monitor
* Ki lett javítva a Get-AzLog parancsmag leírása.
* Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.
    - A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).

#### <a name="aznetwork"></a>Az.Network
* Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.
* A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.
* Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.
* Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon
    - Nem lettek hozzáadva új parancsmagok. Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.

#### <a name="azresources"></a>Az.Resources
* Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok
    - Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: *-AzManagementGroupDeployment
    - Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: *-AzTenantDeployment
    - Az *-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve
    - Az *-AzSubscriptionDeployment aliasok lettek létrehozva az *-AzDeployment parancsmagokhoz
* Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében
* Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.
* A súgófájlok újra létre lettek hozva

#### <a name="azsql"></a>Az.Sql
* Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.
* A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott
* Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez

#### <a name="azstoragesync"></a>Az.StorageSync
* Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.

## <a name="340---february-2020"></a>3.4.0 – 2020. február
### <a name="highlights-since-the-last-major-release"></a>A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok
* Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója
* Az.Network ConnectionMonitor V2 támogatásának hozzáadása

#### <a name="azaccounts"></a>Az.Accounts
* A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el
* Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626
* **New-AzApiManagementProduct** _ és _ *Set-AzApiManagementProduct**
  - https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva
* **Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva

#### <a name="azcompute"></a>Az.Compute
* A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.
* Update-AzDiskEncryptionSet parancsmagok hozzáadása
* Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:
    - New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig
* A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* LIST műveletek hozzáadása az erőforrásokhoz
* Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein

#### <a name="azhdinsight"></a>Az.HDInsight
* A New-AzHDInsightCluster dokumentációs hibájának javítása.

#### <a name="azkeyvault"></a>Az.KeyVault
* Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.

#### <a name="aznetwork"></a>Az.Network
* Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.
* Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog
    - Frissítve lett a New-AzFirewall parancsmag:
        - Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el
        - Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie
* A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.
* Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.
* Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.
    - Új hozzáadott parancsmagok:
        - New-AzApplicationGatewayRewriteRuleUrlConfiguration
    - A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel
        - New-AzApplicationGatewayRewriteRuleActionSet
* A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása
    - -ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz
* A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása
* A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery-támogatás a replikált lemezek eltávolításához.
* Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.

#### <a name="azresources"></a>Az.Resources
* A -Scope választható a *-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés
* Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva

#### <a name="azsql"></a>Az.Sql
A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.

#### <a name="azstorage"></a>Az.Storage
* A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor
    - New-AzStorageAccount
* RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel
* A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása

#### <a name="azwebsites"></a>Az.Websites
* A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat
* Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.

## <a name="330---january-2020"></a>3.3.0 – 2020. január
#### <a name="azaccounts"></a>Az.Accounts
* Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket

#### <a name="azcdn"></a>Az.Cdn
* A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban

#### <a name="azcompute"></a>Az.Compute
* Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag
  - Az Edge Storage-tároló lekérése
* Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag
  - Új Edge Storage-tároló létrehozása
* Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag
  - Az Edge Storage-tároló eltávolítása
* Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag
  - Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez
* Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag
  - Az Edge Storage-fiók lekérése
* Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag
  - Új Edge Storage-fiók létrehozása
* Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag
  - Az Edge Storage-fiók eltávolítása
* Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag
  - Meghívási művelet a megosztott adatok frissítéséhez
* Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag
  - Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása

#### <a name="azdatafactory"></a>Az.DataFactory
* Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz
* Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra
* A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.

#### <a name="azdevtestlabs"></a>Az.DevTestLabs
* A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból

#### <a name="azeventhub"></a>Az.EventHub
* A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében

#### <a name="azhdinsight"></a>Az.HDInsight
* Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el
  - Get-AzMlOpCluster
  - Get-AzMlOpClusterKey
  - New-AzMlOpCluster
  - Remove-AzMlOpCluster
  - Set-AzMlOpCluster
  - Test-AzMlOpClusterSystemServicesUpdateAvailability
  - Update-AzMlOpClusterSystemService

#### <a name="aznetwork"></a>Az.Network
* Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.
* Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.
* Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.
* Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.

#### <a name="azresources"></a>Az.Resources
* Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.

#### <a name="azsql"></a>Az.Sql
* Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.
* Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Hozzá lett adva a DR, mint új érvényes licenctípus

#### <a name="azstorage"></a>Az.Storage
* Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban
    - Update-AzStorageAccountNetworkRuleSet
* Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával
    - Get-AzureRMStorageAccount

## <a name="320---december-2019"></a>3.2.0 – 2019. december

### <a name="general"></a>Általános kérdések
* A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják

#### <a name="azaccounts"></a>Az.Accounts
* A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában
* Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű

#### <a name="azbatch"></a>Az.Batch
* Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.

#### <a name="azdatafactory"></a>Az.DataFactory
* Az ADF .Net SDK a 4.5.0-s verzióra frissült

#### <a name="azfrontdoor"></a>Az.FrontDoor
* A WAF felügyeleti szabályok kizárása mostantól támogatott
* Hozzá lett adva a SocketAddr automatikus kitöltése

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Kivételkezelés

#### <a name="azkeyvault"></a>Az.KeyVault
* Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba
* Az elliptikus görbéjű titkosítási tanúsítványok kezelése
    - A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása

#### <a name="azmonitor"></a>Az.Monitor
* Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz. Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven dedikált adattípus) szerint kell végrehajtani

#### <a name="aznetwork"></a>Az.Network
* Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.

#### <a name="azresources"></a>Az.Resources
* Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.
* Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.

#### <a name="azsql"></a>Az.Sql
* Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben

#### <a name="azstorage"></a>Az.Storage
* A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása
    - New-AzStorageContainerSASToken
    - New-AzStorageBlobSASToken
* Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható
    - Revoke-AzStorageAccountUserDelegationKeys
* Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.
* A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.
    - New-AzRmStorageShare
    - Update-AzRmStorageShare
* A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez
    - Set-AzStorageShareQuota
* Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot
    - Set-AzStorageContainerAcl

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
* Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez. Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.
  - Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:
    - Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.
    - A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.
* A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.
  - Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával. Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.
* Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.
  - Az `ApplicationId` mostantól az `ApplicationName` aliasa.
* Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.
* A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.
* A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.
* Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.
* A **Set-AzBatchPoolOSVersion** eltávolítva. Ez a művelet már nem támogatott.
* `PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.
* A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.
* `DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.
* A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.
  - A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.
  - Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer. Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.
* Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.
* Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján. Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.
* Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában. Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.
* Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal. Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.
* Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).
* Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).

#### <a name="azcdn"></a>Az.Cdn
* A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.
* Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.

#### <a name="azcompute"></a>Az.Compute
* Lemeztitkosítási készlet funkció
    - Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet
    - A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk
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
* Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal
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
    - [További](/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról
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

* [https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása
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
* [https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása
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