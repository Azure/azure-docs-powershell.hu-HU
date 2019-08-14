---
ms.openlocfilehash: faf9313d642a3ca45731f4527aafdfd7f5096a78
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861270"
---
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