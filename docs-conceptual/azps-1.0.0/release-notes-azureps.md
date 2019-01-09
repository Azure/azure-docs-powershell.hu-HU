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

*  https://github.com/Azure/azure-powershell/issues/7679 javítása
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
*  https://github.com/Azure/azure-powershell/issues/7402 javítása
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