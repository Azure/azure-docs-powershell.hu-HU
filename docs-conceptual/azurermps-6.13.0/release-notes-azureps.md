---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: eecd66ddf433cc2543ceeaef1519d69179f2f099
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534451"
---
# <a name="release-notes"></a>Kibocsátási megjegyzések

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.

---
## <a name="6130---november-2018"></a>6.13.0 – 2018. november
#### <a name="azurermprofile"></a>AzureRM.Profile
* A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Frissítve lettek a függőségek a típustársítási hiba elhárításához.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Swagger-alapú Azure Automation-parancsmagok érhetőek el.
* Update Management-parancsmagok lettek hozzáadva.
* Verziókövetési parancsmagok lettek hozzáadva.
* Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.
* Ki lett javítva a DSC csomópontregisztrálási parancs működése.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Ki lett javítva a SystemAssigned identitás problémája.
* Frissítve lettek a függőségek a típustársítási hiba elhárításához.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Frissítve lettek a függőségek a típustársítási hiba elhárításához.

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* A Marketplace-parancsmagok példáinak leírásai frissültek.

#### <a name="azurermnetwork"></a>AzureRM.Network
* A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.
* Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.
* Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan. 
* Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Javítva lett a védett fájlmegosztások módosítási szabályzata.
* A szabályzat időzónája mostantól nagybetűs.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.
* Frissítve lettek a függőségek a típustársítási hiba elhárításához.

#### <a name="azurermrelay"></a>AzureRM.Relay
* A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.

#### <a name="azurermresources"></a>AzureRM.Resources
* Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.
* Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.
* Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.

#### <a name="azurermsql"></a>AzureRM.Sql
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

## <a name="6120---november-2018"></a>6.12.0 – 2018. november
#### <a name="azurermprofile"></a>AzureRM.Profile
* A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.
* A TenantId paraméter a Connect-AzureRmAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez
* Frissítve lett a TenantId leírása a Connect-AzureRmAccount parancsmaghoz
* Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor
    - https://github.com/Azure/azure-powershell/issues/6936
* Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket
    - https://github.com/Azure/azure-powershell/issues/7453
* Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor
    - https://github.com/Azure/azure-powershell/issues/7462
* Javítva lett az a probléma, amely miatt a „Disconnect-AzureRmAccount” jelenik meg, ha nincs kapcsolat
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a>AzureRM.Automation
* A parancsmag DLL-fájlja át lett nevezve a következőre: Microsoft.Azure.Commands.Automation.dll

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Hozzá lett adva a Get-AzureRmCognitiveServicesAccountSkus művelet.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Hozzá lett adva az Add-AzureRmVmssVMDataDisk és a Remove-AzureRmVmssVMDataDisk parancsmag
* A Get-AzureRmVMImage megjeleníti a következőt: AutomaticOSUpgradeProperties
* Javítva lett az a probléma, amely miatt a SetAzureRmVMChefExtension -BootstrapOptions és -JsonAttribute beállítások értékei nem json formátumban lettek beállítva.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* A DataLake csomag verziója 1.1.10-re frissült.
* Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.

#### <a name="azurerminsights"></a>AzureRM.Insights
* Javítva lett a 7267-es hiba (Automatikus skálázási terület)
    - Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).
* Javítva lett a 7513-as hiba [Insights] A Set-AzureRmDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor
    - A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik

#### <a name="azurermnetwork"></a>AzureRM.Network
* A PeeringType kötelező paraméter lett a következő parancsmagoknál:
    - Get-AzureRmExpressRouteCircuitRouteTable
    - Get-AzureRmExpressRouteCircuitARPTable
    - Get-AzureRmExpressRouteCircuitRouteTableSummary
    - Get-AzureRMExpressRouteCrossConnectionArpTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Szabályzatszervizelési parancsmagok lettek hozzáadva

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Hozzá lett adva az Azure-fájlmegosztások támogatása a Recovery Servicesben.

#### <a name="azurermresources"></a>AzureRM.Resources
* https://github.com/Azure/azure-powershell/issues/7402 javítása
    - Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzureRmResource parancsmaggal való használatával

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.
* Javítva lett az Add-AzureRmServiceFabricClusterCertificate parancsmag
    - A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).
    - Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).
* Javítva lett az Update-AzureRmServiceFabricDurability parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.

## <a name="6110---october-2018"></a>6.11.0 – 2018. október
#### <a name="azurermprofile"></a>AzureRM.Profile
* Ki lett javítva a Get-AzureRmSubscription parancsmaggal kapcsolatos hiba a CloudShellben.
* A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Elavult Azure Backup-parancsmagok.

#### <a name="azurermcompute"></a>AzureRM.Compute
* A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a New-AzureRmVm parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.
* A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Virtuális hálózati szabályok támogatása
    - Get-AzureRmDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.
    - Add-AzureRmDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.
    - Set-AzureRmDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.
* A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.

#### <a name="azurermresources"></a>AzureRM.Resources
* Egy értelmezhető kivétel forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat eseteket, amelyekben a Get-AzureRMRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott). Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.

## <a name="6100---october-2018"></a>6.10.0 – 2018. október
#### <a name="azurestorage"></a>Azure.Storage
* Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* A Get-AzureRmCognitiveServicesAccountSkus már létező fiók nélkül is használható.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Ki lett javítva a Get-AzureRmVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon
* A SimpleParameterSet egy példája hozzá lett adva a New-AzureRmVmss parancsmag súgójához.
* Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Hozzá lett adva a NetworkProfile funkció. Az alábbi új parancsmagok lettek hozzáadva
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez
* Hozzá lett adva a New-AzureRmVirtualNetworkTap, a Get-AzureRmVirtualNetworkTap, a Set-AzureRmVirtualNetworkTap és a Remove-AzureRmVirtualNetworkTap parancsmag
* Hozzá lett adva a Set-AzureRmNEtworkInterfaceTapConfig, a Get-AzureRmNEtworkInterfaceTapConfig és a Remove-AzureRmNEtworkInterfaceTapConfig parancsmag

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* A továbbiakban bármilyen sztring megadható méretparaméterként. A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz

#### <a name="azurermresources"></a>AzureRM.Resources
* A hiányzó -Mode paraméter hozzá lett adva a Set-AzureRmPolicyDefinition parancsmaghoz
* A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzureRmProviderOperation parancsmag egy hibája

#### <a name="azurermsql"></a>AzureRM.Sql
* Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést

#### <a name="azurermstorage"></a>AzureRM.Storage
* Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Új Get-AzureRMWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhook URL-címét
* Új New-AzureRMWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba

## <a name="690---september-2018"></a>6.9.0 – 2018. szeptember
#### <a name="general"></a>Általános kérdések
* Az AzureRM.SignalR hozzáadva az AzureRM összesített modulhoz

#### <a name="azurermprofile"></a>AzureRM.Profile
* Kisebb módosítások a tárolók általános kódjában
* Teljes paramétertípusokkal frissült súgófájlok
* A -ServicePrincipal módosítása nem kötelezőre a ServicePrincipalCertificateWithSubscriptionId paraméterkészletben 

#### <a name="azurestorage"></a>Azure.Storage
* Storage-környezet létrehozásának támogatása OAuth használatával. 
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Standard_Microsoft hozzáadva a CDN-díjszabási termékváltozatban. 

#### <a name="azurermcompute"></a>AzureRM.Compute
* A Key Vault és a Storage függőségeinek áthelyezése az általános függőségekhez
* További virtuálisgép-méretek támogatása hozzáadva az AEM-parancsmagokhoz
* A PublicIPPrefix paraméter hozzáadva a New-AzureRmVmssIpConfig parancsmaghoz
* A ResourceId paraméter hozzáadva az Invoke-AzureRmVMRunCommand parancsmaghoz
* Az Invoke-AzureRmVmssVMRunCommand parancsmag hozzáadva

#### <a name="azurermdns"></a>AzureRM.Dns
* Aliasrekord támogatása hozzáadva DNS-rekord létrehozása során

#### <a name="azurerminsights"></a>AzureRM.Insights
* A 6833-as és a 7102-es hiba kijavítva (Diagnosztikai beállítások területe)
    - Az alapértelmezett név, például a „service” hibái a diagnosztikai beállítások megadása és listázása/lekérése során
    - Diagnosztikai beállítások kategóriákkal történő létrehozásának hibái
* Elavulási üzenetek hozzáadva a metrikák időfelbontási szintjeinek paramétereihez
    - Az időfelbontási szintek paramétereit még elfogadja a rendszer (ez nem egy kompatibilitástörő változás), viszont figyelmen kívül hagyja a háttérrendszerben, mivel csak a PT1M érvényes

#### <a name="azurermnetwork"></a>AzureRM.Network
* A LoadBalancer parancsmagokat érintő változások
  - LoadBalancerInboundNatPoolConfig: az IdleTimeoutInMinutes, az EnableFloatingIp és az EnableTcpReset paraméterek hozzáadva
  - LoadBalancerInboundNatRuleConfig: az EnableTcpReset paraméter hozzáadva
  - LoadBalancerRuleConfig: az EnableTcpReset paraméter hozzáadva
  - LoadBalancerProbeConfig: a Protocol paraméterhez tartozó „Https” érték támogatása hozzáadva
* Új parancsok hozzáadva a LoadBalancer új, OutboundRule nevű alerőforrásához
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* Új HostedWorkloads tulajdonság hozzáadva a PSNetworkInterface-hez
* Új parancsmagok hozzáadva a következő szolgáltatáshoz: Azure Firewall ARM-en keresztül
  - Get-AzureRmFirewall hozzáadva
  - Set-AzureRmFirewall hozzáadva
  - New-AzureRmFirewall hozzáadva
  - Remove-AzureRmFirewall hozzáadva
  - New-AzureRmFirewallApplicationRuleCollection hozzáadva
  - New-AzureRmFirewallApplicationRule hozzáadva
  - New-AzureRmFirewallNatRuleCollection hozzáadva
  - New-AzureRmFirewallNatRule hozzáadva
  - New-AzureRmFirewallNetworkRuleCollection hozzáadva
  - New-AzureRmFirewallNetworkRule hozzáadva
* Támogatás hozzáadva a megbízható főtanúsítványokhoz és az automatikus skálázás konfigurálásához az Application Gatewayben
  - Új hozzáadott parancsmagok:
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - Parancsmagok frissítve a -TrustedRootCertificate nevű, nem kötelező paraméterrel
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - Parancsmagok frissítve az -AutoscaleConfiguration nevű, nem kötelező paraméterrel
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* A Get-AzureInterfaceEndpoint parancsmag hozzáadva a felhasználói felület végpontjához
* Támogatás hozzáadva több címelőtaghoz egy alhálózaton belül Frissített parancsmagok:
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* Alhálózat-delegálási parancsmagok hozzáadva.
  - New-AzureRmDelegation: Létrehoz egy új delegálást, amelyet hozzá lehet adni egy alhálózathoz
  - Remove-AzureRmDelegation: Felvesz egy alhálózatot, és eltávolítja a megadott delegálási nevet az adott alhálózatból
  - Add-AzureRmDelegation: Felvesz egy alhálózatot, és hozzáadja a megadott szolgáltatásnevet delegálásként az adott alhálózathoz
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* A felügyelt lemezek támogatása

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Insights-függőség frissítve

#### <a name="azurermresources"></a>AzureRM.Resources
* A New-AzureRmResourceGroupDeployment frissítve az új RollbackAction paraméterrel
    - Az OnErrorDeployment támogatása az új paraméterrel
* A felügyelt identitás támogatása a szabályzat-hozzárendeléseknél
* Az alapértelmezett értékekkel rendelkező paraméterek már nem szükségesek a szabályzatok a New-AzureRmPolicyAssignmenttel történő hozzárendelésekor
* Az új Get-AzureRmPolicyAlias parancsmag hozzáadva a szabályzataliasok lekéréséhez

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* A 7161-es hiba kijavítva

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* Termékváltozatnevek frissítve Free_F1-re és Standard_S1-re
* Verzió mező hozzáadva a PSSignalRResource objektumhoz, és kapcsolati sztring hozzáadva a PSSignalRKeys objektumhoz.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Módosíthatatlansági szabályzat támogatva az AzureRM.Storage-ban 
    - Remove-AzureRmStorageAccountNetworkRule
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Két új parancsmag hozzáadva: Get-AzureRmDeletedWebApp és Restore-AzureRmDeletedWebApp
* A New-AzureRmAppServicePlan -HyperV kapcsoló hozzáadva App Service-csomag létrehozásához Windows-tárolóval
* New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot – Új paraméterek (–ContainerRegistryUser sztring -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) hozzáadva Windows-tárolóalkalmazás létrehozásához és felügyeletéhez

## <a name="681---august-2018"></a>6.8.1 – 2018. augusztus
#### <a name="general"></a>Általános kérdések
* Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.
* Frissített közös futtatókörnyezeti szerelvények

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.
* Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6603
    - Az Import-AzureRmApiManagementApi és az *-AzureRmApiManagementCertificate parancsmagok már tudják kezelni a relatív elérési utakat
* Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6879
    - A CertificateInformation egy beállítható tulajdonság, amely a Set-AzureRmApiManagement parancsmag megfelelő működését biztosítja. Javítva a nuget 4.0.4-es előzetes verziójára való frissítéssel
* Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6853
    - A termékben való név szerinti kereséshez tartozó Odata-szűrő kijavítva
* Hiba kijavítva: https://github.com/Azure/azure-powershell/issues/6814
    - Az API-ban való név szerinti kereséshez tartozó Odata-szűrő kijavítva
* Az AzureMonitor támogatása hozzáadva


#### <a name="azurermcompute"></a>AzureRM.Compute
* Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.
* Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba
* Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.
* Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)

#### <a name="azurermnetwork"></a>AzureRM.Network
* A parancsmagkimenetek alapértelmezett ábrázolása táblanézetre módosítva

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során


#### <a name="azurermresources"></a>AzureRM.Resources
* Ki lett javítva a felügyelt alkalmazások Marketplace-ről való létrehozásával kapcsolatos hiba.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Hibák kijavítva:
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* A MultiValue útválasztási módszer támogatása hozzáadva
    - Új paraméter A MultiValue-útválasztáshoz: MaxReturn
* Az alhálózati útválasztási módszer támogatása hozzáadva
    - IP-címtartományok (alhálózatok) támogatása a végpontokon
* Egyéni fejlécek profilokban való támogatása hozzáadva
* Várt állapotkód-tartományok profilokban való támogatása hozzáadva
* Egyéni fejlécek végpontokon való támogatása hozzáadva

## <a name="680---august-2018"></a>6.8.0 – 2018. augusztus
#### <a name="general"></a>Általános kérdések
* Ki lett javítva az alapértelmezett erőforráscsoportok beállításának hiányával kapcsolatos hiba.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Lejárati tulajdonság hozzáadva a Connect-AzureRmAccount során visszaadott jogkivonatokhoz

#### <a name="azurermcompute"></a>AzureRM.Compute
* Ki lett javítva a hibakimenetből hiányzó céllal kapcsolatos hiba.
* Ki lett javítva a felügyelt lemezekkel rendelkező virtuális gépek tárfióktípusával kapcsolatos hiba
* Ki lettek javítva az AEM Extension-parancsmagok az egyéb környezetekben (pl. Azure China)

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Ki lettek javítva a New-AzureRmIotHubExportDevices és a New-AzureRmIotHubImportDevices példái

#### <a name="azurermnetwork"></a>AzureRM.Network
* Az alapértelmezett modellek ábrázolása módosítva táblázatos nézetre

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Ki lett javítva az a hiba, amely az Update-AzureRmPowerBIEmbeddedCapacity kapcsán jelentkezett a felfüggesztett kapacitás méretezésére tett kísérlet során

#### <a name="azurermresources"></a>AzureRM.Resources
* Ki lett javítva a felügyelt alkalmazások MarketPlace-ről való létrehozásával kapcsolatos hiba.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Problémák megoldása
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* A MultiValue útválasztási módszer támogatása
    - Új paraméter A MultiValue-útválasztáshoz: MaxReturn
* A Subnet útválasztási módszer támogatása
    - IP-címtartományok (alhálózatok) támogatása a végpontokon
* Egyéni fejlécek támogatása a profilokban
* Várt állapotkód-tartományok támogatása a profilokban
* Egyéni fejlécek támogatása a végpontokon

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Ki lett javítva az alapértelmezett erőforráscsoportok helytelen beállításával kapcsolatos hiba.

## <a name="670---august-2018"></a>6.7.0 – 2018. augusztus
#### <a name="azurermprofile"></a>AzureRM.Profile
* Frissítve az Azure ClientRuntime legújabb verziójára.
* A környezetek ütközésének elkerülése érdekében a felhasználói azonosító hozzá lett adva az alapértelmezett környezetnévhez
    - https://github.com/Azure/azure-powershell/issues/6489
* A Clear-AzureRmContext környezetek kiválasztásával kapcsolatos hibáinak javítása #6398
* A bérlői tartomány a -TenantId paraméternek történő átadásának engedélyezése a Connect-AzureRmAccount esetén
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.Storage
* Az 5 TB-os korlátozás feloldása Azure-fájlmegosztási kvóta esetén
* Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermbatch"></a>AzureRM.Batch
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermbilling"></a>AzureRM.Billing
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Frissítve az Azure ClientRuntime legújabb verziójára.
* Az EvictionPolicy paraméter hozzá lett adva a New-AzureRmVmssConfig parancsmaghoz
* Az alapértelmezett hely használata a New-AzureRmVm DiskFileParameterSet paraméterében, ha nincs megadva hely.
* A paraméter leírásának javítása a Save-AzureRmVMImage esetén
* A Get-AzureRmVMDiskEncryptionStatus parancsmag javítása bizonyos egyetlen menetes helyzetekben

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* A hibakeresés javítása olyan esetekben, amikor a DebugPreference a PowerShell-parancssorból van beállítva
* Példa frissítve a Set-AzureRmDataLakeStoreItemAcl esetén
* Frissítve az Azure ClientRuntime legújabb verziójára.
* Példa frissítve a Set-AzureRmDataLakeStoreItemAclEntry esetén

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermdns"></a>AzureRM.Dns
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurerminsights"></a>AzureRM.Insights
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermmedia"></a>AzureRM.Media
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Példa hozzáadva a Set-AzureRmLocalNetworkGateway esetén
* Példák és leírások hozzáadva az Add-AzureRmVirtualNetworkGatewayIpConfig, a Get-AzureRmVirtualNetworkGatewayConnectionSharedKey és a New-AzureRmVirtualNetworkGatewayConnection esetén
* Példák hozzáadva a Remove-AzureRmVirtualNetworkGatewayIpConfig és a Reset-AzureRmVirtualNetworkGateway esetén
* Példa hozzáadva a Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén
* Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnectionSharedKey esetén
* Példa hozzáadva a Set-AzureRmVirtualNetworkGatewayConnection esetén
* Parancsmagok a legfrissebb kódgenerálóval történő újragenerálása az ApplicationSecurityGroup, a RouteTable és a Usage esetén
* Hibaüzenet pontosítva a Get-AzureRmVirtualNetworkSubnetConfig esetén egy nem létező alhálózat lekérésére tett kísérletkor

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Szabályzatszűrő hozzáadva a Get-AzureRmRecoveryServicesBackItem parancsmaghoz. A parancs visszaadja azon biztonsági mentési elemek listáját, amelyek az adott szabályzatazonosító védelme alá tartoznak.
* A Microsoft.Azure.Management.RecoveryServices.Backup frissítve a 3.0.0-preview verzióra.
* Frissítve az Azure ClientRuntime legújabb verziójára.
* A TargetResourceGroupName paraméter hozzá lett adva a Restore-AzureRmRecoveryServicesBackupItem parancsmaghoz. A Managed Diskek visszaállítására kijelölt erőforráscsoport. Managed Diskkel rendelkező virtuális gépek biztonsági másolataira érvényes.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermresources"></a>AzureRM.Resources
* A sablonlapú üzembe helyezés támogatása előfizetési hatókörben. Hozzáadott új parancsmagok:
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* Egy hiba javítása, amely során hibaüzenet jelenik meg, ha a Set-AzureRmResource felé egy környezetet továbbítanak
    - https://github.com/Azure/azure-powershell/issues/5705
* Példa javítva a New-AzureRmResourceGroupDeployment esetén
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermsql"></a>AzureRM.Sql
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermtags"></a>AzureRM.Tags
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Frissítve az Azure ClientRuntime legújabb verziójára.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Frissítve az Azure ClientRuntime legújabb verziójára.

## <a name="660---july-2018"></a>6.6.0 – 2018. július
#### <a name="general"></a>Általános kérdések
* Frissültek a súgófájlok, hogy minden paramétertípust és a helyes kimeneti/bemeneti típusokat tartalmazzák.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Frissült a Common.Strategy kódtár, így ellenőrizni lehet, hogy az erőforrás jelenlegi konfigurációja kompatibilis-e a célerőforrással.
* A Common.Storage új ps1xml-típusokkal egészült ki

#### <a name="azurestorage"></a>Azure.Storage
* A Storage-környezet DefaultProfile használatával történő lekérésének támogatása
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
* Set-AzureStorageBlobContent
* Set-AzureStorageFileContent

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
    - New-AzureRmApplicationGateway : EnableFIPS jelző és zónatámogatás hozzáadva
    - New-AzureRmApplicationGatewaySku : Új Standard_v2 és WAF_v2 SKU-k hozzáadva
    - Set-AzureRmApplicationGatewaySku : Új Standard_v2 és WAF_v2 SKU-k hozzáadva
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
* A szabályzatok URL-kapcsolaton keresztüli fogadása mostantól támogatott MEGJEGYZÉS: A következő parancsmagok elavulttá válnak a jövőbeli kiadásokban
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
