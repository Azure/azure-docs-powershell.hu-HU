---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 07/26/2017
ms.openlocfilehash: 563f84c3af98de066611dd80102e552b31f12883
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274925"
---
# <a name="release-notes"></a>Kibocsátási megjegyzések

Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.

## <a name="20170925---version-440"></a>2017.09.25. – 4.4.0-s verzió
* AnalysisServices
  * Új adatsíkparancsmag, amely lehetővé teszi az adatbázisok szinkronizálását az olvasható és írható példányokról az írásvédett példányokra
    - Mellékelt súgófájl a parancsmaghoz
    - Hozzáadott memóriabeli tesztek és forgatókönyvteszt (csak élő)
  * Az Add-AzureAsAccount parancsmag hibáinak javítása
* Automation
  * A korábbi kiadásokban javított parancsmagok súgódokumentumainak javítása.
  * 4 új parancsmag lett hozzáadva a DSC csomópont-konfigurációk előkészített kibocsátásának támogatásához.
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* CognitiveServices
  * Integráció a Cognitive Services Management SDK 2.0.0-s verziójával.
  * A Get-AzureRmCognitiveServicesAccount most már megfelelően támogatja a lapozást.
* Compute
  * A futtatási parancs funkciója:
    - Az új Invoke-AzureRmVMRunCommand parancsmag futtatás parancsot indít egy virtuális gépen
    - Az új Get-AzureRmVMRunCommandDocument parancsmag megjeleníti a futtatás paranccsal kapcsolatos elérhető dokumentumokat
  * A StorageAccountType paraméter hozzá lett adva a Set-AzureRmDataDisk parancsmaghoz
  * A rendelkezésre állási zóna támogatása a virtuális gépekhez, virtuálisgép-méretezési csoportokhoz és lemezekhez
    - Új Zone paraméter a New-AzureRmVM, New-AzureRmVMConfig, New-AzureRmVmssConfig, New-AzureRmDiskConfig parancsmaghoz
  * Virtuálisgép-méretezési csoportok működés közbeni frissítési szolgáltatása:
    - Az új Start-AzureRmVmssRollingOSUpgrade parancsmag a virtuálisgép-méretezési csoport operációs rendszerének frissítését indítja el
    - Az új Set-AzureRmVmssRollingUpgradePolicy parancsmag beállítja a virtuálisgép-méretezési csoport működés közbeni frissítésének frissítési szabályzatát.
    - Az új Stop-AzureRmVmssRollingUpgrade parancsmag a virtuálisgép-méretezési csoport működés közbeni frissítését vonja vissza
    - Az új Get-AzureRmVmssRollingUpgrade parancsmag a virtuálisgép-méretezési csoport működés közbeni frissítésének állapotát jeleníti meg.
  * Az új AssignIdentity kapcsolóparaméter a rendszerhez rendelt identitáshoz használható.
    - Új AssignIdentity paraméter a New-AzureRmVMConfig, New-AzureRmVmssConfig és Update-AzureRmVM parancsmaghoz
  * Vmss lemeztitkosítási szolgáltatás:
    - Az új Set-AzureRmVmssDiskEncryptionExtension parancsmag engedélyezi a lemeztitkosítást a virtuálisgép-méretezési csoporton
    - Az új Disable-AzureRmVmssDiskEncryption parancsmag letiltja a lemeztitkosítást a virtuálisgép-méretezési csoporton
    - Az új Get-AzureRmVmssDiskEncryptionStatus parancsmag megjeleníti a virtuálisgép-méretezési csoportok lemeztitkosítási állapotát
    - Az új Get-AzureRmVmssVMDiskEncryptionStatus parancsmag megjeleníti a virtuálisgép-méretezési csoportban lévő virtuális gépek lemeztitkosítási állapotát
* ContainerInstance
  * Új PowerShell-parancsmagok az Azure Container Instance-hez
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* Insights
  * Új Disable-AzureRmActivityLogAlert parancsmag
    - Új parancsmag a meglévő tevékenységnapló-riasztások letiltásához.
    - Ezzel a parancsmaggal opcionálisan a címkék is beállíthatók.
  * Új Enable-AzureRmActivityLogAlert parancsmag
    - Új parancsmag meglévő tevékenységnapló-riasztások engedélyezéséhez.
    - Ezzel a parancsmaggal opcionálisan a címkék is beállíthatók.
  * Új Get-AzureRmActivityLogAlert parancsmag
    - Új parancsmag egy vagy több tevékenységnapló-riasztás lekéréséhez.
    - A riasztások név, erőforráscsoport vagy előfizetés alapján kérhetők le.
  * Új New-AzureRmActionGroup parancsmag
    - Új parancsmag egy ActionGroup objektum memóriában való létrehozásához (nem tartalmaz kérelmet.)
  * Új New-AzureRmActivityLogAlertCondition parancsmag
    - Új parancsmag egy tevékenységnapló-riasztás levélfeltétel objektumának a memóriában való létrehozásához (nem tartalmaz kérelmet.)
  * Új Set-AzureRmActivityLogAlert parancsmag
    - Új parancsmag tevékenységnapló-riasztás létrehozásához vagy frissítéséhez.
  * Új Remove-AzureRmActivityLogAlert parancsmag
    - Új parancsmag egy tevékenységnapló-riasztás eltávolításához.
  * Új Set-AzureRmActionGroup parancsmag
    - Új parancsmag új műveletcsoport létrehozásához vagy meglévő műveletcsoport frissítéséhez.
  * Új Get-AzureRmActionGroup parancsmag
    - Új parancsmag egy vagy több műveletcsoport lekéréséhez.
    - A műveletcsoportok név, erőforráscsoport vagy előfizetés alapján kérhetők le.
  * Új Remove-AzureRmActionGroup parancsmag
    - Új parancsmag egy műveletcsoport eltávolításához.
  * Új New-AzureRmActionGroupReceiver parancsmag
    - Új parancsmag új műveletcsoport-fogadó memóriában való létrehozásához.
* KeyVault
  * Új/frissített parancsmagok a KeyVault-tanúsítványok helyreállítható törlésének támogatásához
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* Network (Hálózat)
  * Végpontszolgáltatások támogatása virtuális hálózati alhálózatokhoz
    - Frissített Add-AzureRmVirtualSubnetConfig: Új választható -ServiceEndpoint paraméter
    - Frissített New-AzureRmVirtualSubnetConfig: Új választható -ServiceEndpoint paraméter
    - Frissített Set-AzureRmVirtualSubnetConfig: Új választható -ServiceEndpoint paraméter
  * Új parancsmag a helyen elérhető végpontszolgáltatások listázásához
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * Lehetségessé vált a külső sugáron alapuló P2S hitelesítés konfigurálása a következő parancsmagok esetén
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * Új parancsmag a VPN-profilok létrehozásának engedélyezéséhez a külső sugáron alapuló P2S esetén
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * Az SKU paraméter most már támogatott a nyilvános IP-címek és terheléselosztók esetén
    - Frissített New-AzureRMLoadBalancer: Új választható -Sku paraméter
    - Frissített New-AzureRMPublicIpAddress: Új választható -Sku paraméter
  * A DisableOutboundSNAT támogatása a terheléselosztó-szabályokhoz
    - Frissített New-AzureRMLoadBalancerRuleConfig: Új választható DisableOutboundSNAT paraméter
    - Frissített Add-AzureRMLoadBalancerRuleConfig: Új választható DisableOutboundSNAT paraméter
    - Frissített Set-AzureRMLoadBalancerRuleConfig: Új választható DisableOutboundSNAT paraméter
  * Az IkeV2 P2S támogatása
    - Frissített New-AzureRmVirtualNetworkGateway: Új választható -VpnClientProtocol paraméter; az alapértelmezett értéke [SSTP, IkeV2]
    - Frissített Set-AzureRmVirtualNetworkGateway: Új választható -VpnClientProtocol paraméter
  * A MultiValued szabályok támogatása a hálózati biztonsági szabályokban és a hatályos hálózati biztonsági szabályokban
    - Frissített Add-AzureRmNetworkSecurityRuleConfig: A SourcePortRange, DestinationPortRange, SourceAddressPrefix paraméterek frissültek a sztringek listájának elfogadása érdekében
    - Frissített New-AzureRmNetworkSecurityRuleConfig: A SourcePortRange, DestinationPortRange, SourceAddressPrefix paraméterek frissültek a sztringek listájának elfogadása érdekében
    - Frissített Set-AzureRmNetworkSecurityRuleConfig: A SourcePortRange, DestinationPortRange, SourceAddressPrefix paraméterek frissültek a sztringek listájának elfogadása érdekében
    - Frissített Add-AzureRmNetworkSecurityRuleConfig: A SourcePortRange, DestinationPortRange, SourceAddressPrefix paraméterek frissültek a sztringek listájának elfogadása érdekében
    - Frissített New-AzureRmNetworkSecurityGroup : A SecurityRules paraméter frissült a SourcePortRange, DestinationPortRange, SourceAddressPrefix paraméterek elfogadásához, amelyek sztringek listái egy PSSecurityRule objektumban
    - Frissített Get-AzureRmEffectiveNetworkSecurityGroup: Hozzáadott TagMap paraméter
    - Frissített Get-AzureRmEffectiveNetworkSecurityGroup: A visszaadott PSEffectiveSecurityRule objektum a SourcePortRange, DestinationPortRange, SourceAddressPrefix paraméterekkel frissült, amelyek sztringek listái.
  * A DDoS-védelem támogatása virtuális hálózatokhoz
    - Frissített New-AzureRmVirtualNetwork: Új EnableDDoSProtection és EnableVmProtection kapcsolóparaméterek
    - Új EnableDDoSProtection és EnableVmProtection tulajdonságok PSVirtualNetwork objektumban
  * A magas rendelkezésre állású belső terheléselosztó támogatása
    - Frissített Add-AzureRmLoadBalancerRuleConfig: Az All paraméter a protokoll-paraméterek elfogadható értéke lett
    - Frissített AzureRmLoadBalancerRuleConfig: Az All paraméter a protokoll-paraméterek elfogadható értéke lett
    - Frissített Set-AzureRmLoadBalancerRuleConfig: Az All paraméter a protokoll-paraméterek elfogadható értéke lett
  * Alkalmazásbiztonsági csoportok támogatása
    - Új New-AzureRmApplicationSecurityGroup
    - Új Get-AzureRmApplicationSecurityGroup
    - Új Remove-AzureRmApplicationSecurityGroup
    - Frissített New-AzureRmNetworkInterface: Új választható ApplicationSecurityGroup és ApplicationSecurityGroupId paraméterek
    - Frissített New-AzureRmNetworkInterfaceIpConfig: Új választható ApplicationSecurityGroup és ApplicationSecurityGroupId paraméterek
    - Frissített Add-AzureRmNetworkInterfaceIpConfig: Új választható ApplicationSecurityGroup és ApplicationSecurityGroupId paraméterek
    - Frissített Set-AzureRmNetworkInterfaceIpConfig: Új választható ApplicationSecurityGroup és ApplicationSecurityGroupId paraméterek
    - Frissített New-AzureRmNetworkSecurityRuleConfig: Új választható SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup és DestinationApplicationSecurityGroupId paraméterek
    - Frissített Add-AzureRmNetworkSecurityRuleConfig: Új választható SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup és DestinationApplicationSecurityGroupId paraméterek
    - Frissített Set-AzureRmNetworkSecurityRuleConfig: Új választható SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup és DestinationApplicationSecurityGroupId paraméterek
  * Új parancsok a VpnDeviceConfiguration szkriptekhez
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* Profil
  * A Start-Job támogatása az AzureRm parancsmagokhoz.
    * Minden AzureRm parancsmag hozzáadja az -AzureRmContext paramétert, amely tudja fogadni a környezeteket (környezet parancsmagok kimenetét).
      - Környezetmegőrzéssel rendelkező feladatok általános mintája LETILTVA: `Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)`
      - Környezetmegőrzéssel rendelkező feladatok általános mintája ENGEDÉLYEZVE: `Start-Job {New-AzureRmVM [... other parameters]}`
  * Bejelentkezési információk megőrzése a munkamenetek között, új parancsmagok:
    - Enable-AzureRmContextAutosave – Hitelesítő adatok munkamenetek közötti megőrzésének engedélyezése.
    - Disable-AzureRmContextAutosave – Hitelesítő adatok munkamenetek közötti megőrzésének letiltása.
  * Környezeti információk kezelése, új parancsmagok
    - Select-AzureRmContext – Az aktív elnevezett környezet kiválasztása.
    - Rename-AzureRmContext – A meglévő környezet átnevezése a könnyű hivatkozás érdekében.
    - Remove-AzureRmContext – Meglévő környezet eltávolítása.
    - Remove-AzureRmAccount – Egy fiókkal társított összes hitelesítő adat, előfizetés és bérlő eltávolítása.
  * Környezeti információk kezelése, parancsmag módosításai:
    - Hozzáadott hatókör = (Folyamat | AktuálisFelhasználó) a hitelesítő adatokat módosító összes parancsmaghoz
    - Get-AzureRmContext – Új ListAvailable paraméter az összes mentett környezet listájához
* További források
  * PolicySetDefinition parancsmagok hozzáadása
    - New-AzureRmPolicySetDefinition parancsmag szabályzatkészlet-definíciók létrehozásához
    - Get-AzureRmPolicySetDefinition parancsmag az összes szabályzatkészlet-definíció listázásához vagy adott szabályzatkészlet-definíció lekéréséhez
    - Remove-AzureRmPolicySetDefinition parancsmag szabályzatkészlet-definíciók törléséhez
    - Set-AzureRmPolicySetDefinition parancsmag meglévő szabályzatkészlet-definíciók frissítéséhez
  * A -PolicySetDefinition, -Sku és -NotScope paraméterek hozzáadva a New-AzureRmPolicyAssignment és a Set-AzureRmPolicyAssignment parancsmagokhoz
  * A szabályzatokban lévő url-ek továbbítása New-AzureRmPolicyDefinition és Set-AzureRmPolicyDefinition parancsmagokba
  * A -Mode paraméter hozzáadása a New-AzureRmPolicyDefinition parancsmaghoz
  * Szerepkör-hozzárendelés eltávolításának támogatása PSRoleAssignment objektummal
    - A felhasználók már használhatják a PSRoleassignmnet bemeneti objektumot a Remove-AzureRMRoleAssignment parancsmaggal a szerepkör-hozzárendelés eltávolításához.
  * ManagedApplication parancsmagok hozzáadása
    - New-AzureRmManagedApplication parancsmag felügyelt alkalmazás létrehozásához
    - Get-AzureRmManagedApplication parancsmag előfizetés alatti összes felügyelt alkalmazás listázásához vagy adott felügyelt alkalmazás lekéréséhez
    - Remove-AzureRmManagedApplication parancsmag felügyelt alkalmazások törléséhez
    - Set-AzureRmManagedApplication parancsmag meglévő felügyelt alkalmazások frissítéséhez
  * ManagedApplicationDefinition parancsmagok hozzáadása
    - New-AzureRmManagedApplicationDefinition parancsmag felügyelt alkalmazás definíciójának létrehozásához zip fájl uri-jával vagy mainTemplate és createUiDefinition json-fájlokkal
    - Get-AzureRmManagedApplicationDefinition parancsmag egy erőforráscsoport alatti összes felügyelt alkalmazásdefiníció listázásához vagy adott felügyelt alkalmazásdefiníció lekéréséhez
    - Remove-AzureRmManagedApplicationDefinition parancsmag felügyelt alkalmazások definíciójának törléséhez
    - Set-AzureRmManagedApplicationDefinition parancsmag meglévő felügyelt alkalmazásdefiníciók frissítéséhez
* SQL
  * Virtuális hálózati szabályok támogatása
    - Új Get-AzureRmSqlServerVirtualNetworkRule parancsmag, amely egy adott szabálynév vagy Azure SQL Server-kiszolgálón lévő virtuális hálózati szabályok alapján kéri le a virtuális hálózati szabályokat.
    - Új Set-AzureRmSqlServerVirtualNetworkRule parancsmag, amely módosítja a virtuális hálózatot, amelyre a szabály mutat.
    - Új Remove-AzureRmSqlServerVirtualNetworkRule parancsmag, amely eltávolít egy virtuális hálózati szabályt egy Azure SQL Server-kiszolgálón.
    - Új New-AzureRmSqlServerVirtualNetworkRule parancsmag, amely új virtuális hálózati szabályt hoz létre egy Azure SQL Server-kiszolgálóhoz.
* Webhelyek
  * App Service-csomagok PremiumV2 szintjének hozzáadása
* Azure.Storage
  * Frissítés az Azure Storage ügyféloldali kódtárának 8.4.0-s és az Azure Storage adatátviteli kódtárának 0.6.1-es verziójára
  * PremiumPageBlobTier támogatás a blobok feltöltési és másolási API-ján
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * Az AzureStorageContainer, AzureStorageBlob, AzureStorageQueue, AzureStorageTable konzolkimeneti formátumának finomítása
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>2017.08.10. – 4.3.1-es verzió
  * A szerelvények aláírásával kapcsolatos probléma megoldására szolgáló frissítés

## <a name="20170807---version-430"></a>2017.08.07. – 4.3.0-s verzió
* AnalysisServices
  * A Set-AzureRmAnalysisServciesServer parancsmag hibájának javítása
    - Ha nincs megadva a rendszergazda, a rendszer eltávolítja a rendszergazdát.
  * Megjelent a BackupBlobContainerUri paraméter a New-AzureRmAnalysisServicesServer és a Set-AzureRmAnalysisServicesServer parancsmagban
    - Biztonsági blobtároló beállításának vagy letiltásának lehetősége tartalék vagy visszaállítási Azure Analysis Services-kiszolgálóhoz
  * A termékváltozat-keresés frissítése a New-AzureRmAnalysisServicesServer és a Set-AzureRmAnalysisServicesServer parancsmagban
    - Módosítva lett a dinamikus keresés nem változtatható termékváltozata.
  * Az Add-AzureAnalysisServicesAccount parancsmag most már támogatja a szolgáltatásnévvel való bejelentkezést
* Automation
  * Módosítva lettek az Automation DSC* parancsmagok, hogy 100-nál több rekordot kérjenek le
  * Meg lett oldva a probléma, amely miatt a részletes streamek néhány Automation-parancsmag (például a Get-AzureRmAutomationVariable és a Get-AzureRmAutomationJob) meghívása után nem működnek tovább.
  * Most már támogatott a csomópont-konfiguráció buildjeinek verziószámozása a StartAzureAutomationDscCompilationJob és az ImportAzureAutomationDscNodeConfiguration parancsmagban
  * Meglévő problémák hibajavításai – az aliasokkal kapcsolatos, 3775-ös számú probléma, valamint a runOn aliasok és a hibrid feldolgozók támogatásának javítása.
* Compute
  * Set-AzureRmVMAEMExtension: Mostantól támogatottak az új prémium szintű lemezméretek
  * Set-AzureRmVMAEMExtension: Mostantól támogatott az M-sorozat
  * Megjelent a ForceUpdateTag paraméter az Add-AzureRmVmssExtension parancsmagban
  * Megjelent a Primary paraméter a New-AzureRmVmssIpConfig parancsmagban
  * Megjelent az EnableAcceleratedNetworking paraméter az Add-AzureRmVmssNetworkInterfaceConfig parancsmagban
  * Megjelent az InstanceId paraméter a Set-AzureRmVmss parancsmagban
  * A MaintenanceRedeployStatus paraméter megjelenítése a Get-AzureRmVM parancsmag kimenetében
  * A korlátozások és a képességek megjelenítése a Get-AzureRmComputeResourceSku parancsmag táblázatformátumában
* DataLakeStore
  * A probléma megoldása: https://github.com/Azure/azure-powershell/issues/4323
* EventHub
  * Megjelent a ResourceGroup tulajdonság a névtérattribútumok között
    - A ResourceGroup tulajdonság azon erőforráscsoport nevét olvassa be, melyben a névtér található
  * A parancsmagok frissítése névtérre és EventHubra vonatkozó paraméterkészletekkel, engedélyezési szabályok használatához
    - New-AzureRmEventHubAuthorizationRule – Új engedélyezési szabályt ad hozzá egy meglévő névtérhez vagy EventHubhoz.
    - Get-AzureRmEventHubAuthorizationRule – Beolvas egy engedélyezési szabályt vagy az engedélyezési szabályok listáját egy meglévő névtérből vagy EventHubból.
    - Set-AzureRmEventHubAuthorizationRule – Frissíti egy meglévő névtér vagy EventHub tulajdonságait.
    - Remove-AzureRmEventHubAuthorizationRule – Töröl egy meglévő engedélyezési szabályt egy meglévő névtérből vagy EventHubból.
    - New-AzureRmEventHubKey – Új elsődleges és másodlagos kulcsot generál egy meglévő névtér vagy EventHub egy engedélyezési szabályához.
    - Get-AzureRmEventHubKey – Beolvassa egy meglévő névtér vagy EventHub egy engedélyezési szabályának elsődleges és másodlagos kulcsát.
* Network (Hálózat)
    * Most már támogatott az IPv6 használata, és új nem kötelező paraméterként megjelent a -PeerAddressType
      * New-AzureRmExpressRouteCircuitPeeringConfig:
      * Set-AzureRmExpressRouteCircuitPeeringConfig: Most már támogatott az IPv6 használata. Új nem kötelező paraméter jelent meg
      * Remove-AzureRmExpressRouteCircuitPeeringConfig: Most már támogatott az IPv6 használata. Új nem kötelező paraméter jelent meg
    * A -ProbeEnabled paraméter meg lett jelölve elavultként
      - Add-AzureRmApplicationGatewayBackendHttpSettings
      - New-AzureRmApplicationGatewayBackendHttpSettings
      - Set-AzureRmApplicationGatewayBackendHttpSettings
* Profil
    * Az adatgyűjtés most már alapértelmezés szerint engedélyezve van. A Microsoft a felhasználói élmény javítása érdekében gyűjti a használati adatokat. Az adatok névtelenek, és nem tartalmazzák a parancssori argumentumok értékeit.
      - A funkció a Disable-AzureRmDataCollection parancsmaggal kapcsolható ki
      - A funkció az Enable-AzureRmDataCollection parancsmaggal kapcsolható be
* További források
    * Mostantól támogatott a hatókörök érvényesítése az ARM-nek küldött kérelem küldése előtt az alábbi szerepkör-definíciós és szerepkör-hozzárendelési parancsmagok esetében
      - Get-AzureRMRoleAssignment
      - New-AzureRMRoleAssignment
      - Remove-AzureRMRoleAssignment
      - Get-AzureRMRoleDefinition
      - New-AzureRMRoleDefinition
      - Remove-AzureRMRoleDefinition
      - Set-AzureRMRoleDefinition
* ServiceBus
  * Az alábbi új engedélyezési szabályokkal, névterekkel, üzenetsorokkal és témakörökkel kapcsolatos parancsmagok jelentek meg. a rendszer a paraméterkészlet alapján elvégzi az engedélyezési szabályokra vonatkozó műveleteket.
    - New-AzureRmServiceBusAuthorizationRule – Új engedélyezési szabályt ad hozzá egy meglévő ServiceBus-névtérhez, -üzenetsorhoz vagy -témakörhöz.
    - Get-AzureRmServiceBusAuthorizationRule – Beolvas egy engedélyezési szabályt vagy az engedélyezési szabályok listáját egy meglévő ServiceBus-névtérből, -üzenetsorból vagy -témakörből.
    - Set-AzureRmServiceBusAuthorizationRule – Frissíti egy meglévő ServiceBus-névtér, -üzenetsor vagy -témakör tulajdonságait.
    - New-AzureRmServiceBusKey – Új elsődleges és másodlagos kulcsot generál egy meglévő ServiceBus-névtér, -üzenetsor vagy -témakör egy engedélyezési szabályához.
    - Get-AzureRmServiceBusKey – Beolvassa egy meglévő ServiceBus-névtér, -üzenetsor vagy -témakör egy engedélyezési szabályának elsődleges és másodlagos kulcsát.
    - Remove-AzureRmServiceBusNamespaceAuthorizationRule – Törli egy meglévő ServiceBus-névtér, -üzenetsor vagy -témakör egy meglévő engedélyezési szabályát.
  * Megjelent a ResourceGroup tulajdonság a névtérattribútumok között

* SQL
    * A Set-AzureRmSqlServerTransparentDataEncryptionProtector parancsmag frissítése, hogy figyelmeztetést jelenítsen meg és megerősítést kérjen, ha a titkosítási védelem típusa az AzureKeyVault értékre van állítva
    * Új, frissített naplózási beállításokra vonatkozó parancsmagok jelentek meg
      - A Get-AzureRmSqlDatabaseAuditing parancsmag, mely egy Azure SQL Database-adatbázis naplózási beállításait olvassa be.
      - A Get-AzureRmSqlServerAuditing parancsmag, mely egy Azure SQL Server-kiszolgáló naplózási beállításait olvassa be.
      - A Set-AzureRmSqlDatabaseAuditing parancsmag, mely egy Azure SQL Database-adatbázis naplózási beállításait módosítja.
      - A Set-AzureRmSqlServerAuditing parancsmag, mely egy Azure SQL Server-kiszolgáló naplózási beállításait módosítja.
    * A meglévő naplózási szabályzatra vonatkozó parancsmagok elavulttá válnak
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * A sémafájlok elemzése az Update-AzureRmSqlSyncGroup parancsmag esetében mostantól nem különbözteti meg a kis- és nagybetűket.
* Storage
    * A NetworkRule tulajdonság támogatása az erőforrásmód-tárfiókok parancsmagjaihoz
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

## <a name="20170717---version-421"></a>2017.07.17. – 4.2.1-es verzió
* Compute
  - Kijavítottuk a virtuálisgép-lemez és a virtuálisgép-lemez pillanatfelvételének létrehozásához és frissítéséhez használt parancsmagok hibáit (hivatkozás)[<https://github.com/azure/azure-powershell/issues/4309>]
    - New-AzureRmDisk
    - New-AzureRmSnapshot
    - Update-AzureRmDisk
    - Update-AzureRmSnapshot
* Profil
  - Kijavítottuk a nem interaktív felhasználói hitelesítéssel kapcsolatos hibát az RDFE-ben (hivatkozás)[<https://github.com/Azure/azure-powershell/issues/4299>]

* ServiceManagement
  - Kijavítottuk a nem interaktív felhasználói hitelesítéssel kapcsolatos hibát (hivatkozás)[<https://github.com/Azure/azure-powershell/issues/4299>]

## <a name="2017711---version-420"></a>2017.07.11. – 4.2.0-ás verzió
* AnalysisServices
    * Új adatsík API hozzáadása
        - API az AS-kiszolgálónapló lekéréséhez, Export-AzureAnalysisServicesInstanceLog
* Automatizálás
    * Időzóna értékének helyes beállítása a New-AzureRmAutomationSchedule heti és havi ütemezéseihez
        - További információt itt találhat: https://github.com/Azure/azure-powershell/issues/3043
* AzureBatch
    - Új Get-AzureBatchJobPreparationAndReleaseTaskStatus parancsmag hozzáadása.
    - Bájttartomány kezdő és záró értékének hozzáadása a Get-AzureBatchNodeFileContent paraméterekhez.
* CognitiveServices
    * Integráció a Cognitive Services Management SDK 1.0.0-ás verziójával.
    * Kijavítottunk egy fióknév hosszának ellenőrzését érintő hibát.
* Számítás
    * Tárfiók típusának támogatása lemezképhez:
        - A StorageAccountType paraméter a Set-AzureRmImageOsDisk és az Add-AzureRmImageDataDisk parancsmaghoz
    * PrivateIP és PublicIP szolgáltatás a VMSS IP-konfigurációban:
        - Új PrivateIPAddressVersion, PublicIPAddressConfigurationName, PublicIPAddressConfigurationIdleTimeoutInMinutes, DnsSetting nevek a New-AzureRmVmssIpConfig parancsmaghoz
        - PrivateIPAddressVersion paraméter az IPv4 vagy IPv6 meghatározásához a New-AzureRmVmssIpConfig parancsmagban
    * Teljesítmény-karbantartási szolgáltatás:
        - Új PerformMaintenance kapcsolóparaméter az Restart-AzureRmVM parancsmaghoz.
        - A Get-AzureRmVM -Status az adott virtuális gép teljesítmény-karbantartási információit jeleníti meg
    * Virtuálisgép-identitási szolgáltatás:
        - Új IdentityType paraméter a New-AzureRmVMConfig és az UpdateAzureRmVM parancsmaghoz
        - A Get-AzureRmVM az adott virtuális gép identitásának információit jeleníti meg
    * VMSS-identitási szolgáltatás:
        - Új IdentityType paraméter a New-AzureRmVmssConfig parancsmaghoz
        - A Get-AzureRmVmss az adott VMSS identitásának információit jeleníti meg
    * VMSS rendszerindítási diagnosztikai szolgáltatás:
        - Új parancsmag a VMSS-objektumok rendszerindítási diagnosztikájának beállításához: Set-AzureRmVmssBootDiagnostics
        - Új BootDiagnostic paraméter a New-AzureRmVmssConfig parancsmaghoz
    * VMSS LicenseType szolgáltatás:
        - Új LicenseType paraméter a New-AzureRmVmssConfig parancsmaghoz
    * RecoveryPolicyMode támogatása:
        - Új RecoveryPolicyMode paraméter a New-AzureRmVmssConfig parancsmaghoz
    * Számítási erőforrás termékváltozata szolgáltatás:
        - Az új Get-AzureRmComputeResourceSku parancsmag a számítási erőforrások termékváltozatainak listáját jeleníti meg
* DataFactories
    * A New-AzureRmDataFactoryGatewayKey parancsmag elavult
    * Új átjáró-hitelesítési kulcs szolgáltatás az új New-AzureRmDataFactoryGatewayAuthKey és Get-AzureRmDataFactoryGatewayAuthKey parancsmaggal
* DataLakeAnalytics
    * Számítási szabályzat CRUD-jának hozzáadása a következő parancsokkal:
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * Feladat kapcsolati metaadatainak támogatása az ismétlődő feladatok és feladatfolyamatok segítéséhez Az alábbi parancsok lettek frissítve vagy hozzáadva:
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * A token célrendszere frissült a feladat és katalógus API-k esetében, hogy a megfelelő Data Lake célrendszert használják az Azure Resource célrendszer helyett.
* DataLakeStore
    * Felhasználók által felügyelt KeyVault-kulcsrotálás támogatása a Set-AzureRMDataLakeStoreAccount parancsmagban
    * Új kényelmi frissítés, amely automatikusan elindít egy `enableKeyVault`-hívást a felhasználó által felügyelt KeyVault hozzáadásakor vagy egy kulcs rotálásakor.
    * A token célrendszere frissült a feladat és katalógus API-k esetében, hogy a megfelelő Data Lake célrendszert használják az Azure Resource célrendszer helyett.
    * Kijavítottunk egy, az alábbi parancsmagokkal létrehozott vagy hozzáfűzött fájlok méretét korlátozó hibát:
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* DNS
    * Kijavítottuk az Get-AzureRmDnsZone átirányítási forgatókönyvében lévő hibát
        - További információt itt találhat: https://github.com/Azure/azure-powershell/issues/4203
* HDInsight
    * Operations Management Suite (OMS) engedélyezésének és letiltásának támogatása
    * Új parancsmagok
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * Új paraméterek a Spark egyéni konfigurációjának megadásához a Add-AzureRmHDInsightConfigValues parancsmaghoz
        - SparkDefaults és SparkThriftConf paraméter a Spark 1.6-os verziójához
        - Spark2Defaults és Spark2ThriftConf paraméter a Spark 2.0-ás verziójához
* Insights
    * 4215. hiba (módosítási kérés): eltávolítottuk a 15 napos korlátot a Get-AzureRmLog parancsmag időtartományából. Kisebb módosítások az egység tesztneveiben.
    * Kijavítottuk a 3957. hibát a Get-AzureRmLog parancsmag esetében
        - 1. probléma: A háttérrendszer a rekordokat 200 rekordot tartalmazó oldalakon adja vissza, és az oldalakat a folytatási token kapcsolja össze. A felhasználók azt tapasztalták, hogy a parancsmag csak 200 rekordot adott vissza, pedig több volt ennél. Ez a MaxEvents esetében megadott értéktől függetlenül bekövetkezett, kivéve, ha az érték kisebb volt, mint 200.
        - 2. probléma: A dokumentáció helytelen adatokat tartalmazott erről a parancsmagról. Például a timewindow alapértelmezett értéke 1 óra volt.
        - 1. javítás: A parancsmag mostantól a háttérrendszer által visszaadott folytatási tokent követi, amíg el nem éri a MaxEvents tulajdonságot vagy a készlet végét.<br>A MaxEvents alapértelmezett értéke 1000, az maximális értéke pedig 100000. A MaxEvents 1-nél kisebb értékei figyelmen kívül lesznek hagyva, és az alapértelmezett érték lesz használva. Ezek az értékek és viselkedések nem módosultak, és már helyesen vannak dokumentálva.<br>Egy alias (MaxRecords) hozzá lett adva a MaxEvents-hez, mivel a parancsmag neve már nem jelzi az eseményeket, csak a naplókat.
        - 2. javítás: A dokumentáció helyes és részletesebb információkat tartalmaz: új alias, helyes időtartomány, helyes alapértelmezett, minimális és maximális értékek.
* KeyVault
    * E-mail-cím eltávolítása a címtárlekérdezésből, amikor a -UserPrincipalName meg van adva a Set-AzureRMKeyVaultAccessPolicy és a Remove-AzureRMKeyVaultAccessPolicy parancsmaghoz.
      - Mostantól mindkét parancsmag rendelkezik -EmailAddress paraméterrel, amely a -UserPrincipalName paraméter helyett használható, ha az e-mail-cím lekérdezése megfelelő.  Ha egynél több egyező e-mail-cím található a címtárban, a parancsmag futtatása sikertelen lesz.
* Network (Hálózat)
    * New-AzureRmIpsecPolicy: A SALifeTimeSeconds és a SADataSizeKilobytes már nem kötelező paraméterek
        - Az SALifeTimeSeconds alapértelmezett értéke 27000 másodperc
        - Az SADataSizeKilobytes alapértelmezett értéke 102400000 KB
    * Egyéni titkosítócsomagok konfigurálásának támogatása az SSL-szabályzat használatával és minden SSL-beállítási API megjelenítése az Application Gateway-ben
        - Új választható paraméterek: -PolicyType, -PolicyName, -MinProtocolVersion, -Ciphersuite
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - Új Get-AzureRmApplicationGatewayAvailableSslOptions parancsmag (Alias: List-AzureRmApplicationGatewayAvailableSslOptions)
        - Új Get-AzureRmApplicationGatewaySslPredefinedPolicy parancsmag (Alias: List-AzureRmApplicationGatewaySslPredefinedPolicy)
    * Átirányítás támogatása az Application Gateway-ben
        - Új Add-AzureRmApplicationGatewayRedirectConfiguration parancsmag
        - Új Get-AzureRmApplicationGatewayRedirectConfiguration parancsmag
        - Új New-AzureRmApplicationGatewayRedirectConfiguration parancsmag
        - Új Remove-AzureRmApplicationGatewayRedirectConfiguration parancsmag
        - Új Set-AzureRmApplicationGatewayRedirectConfiguration parancsmag
        - Új választható paraméter: -RedirectConfiguration
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - Új választható paraméter: -DefaultRedirectConfiguration
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - Új választható paraméter: -RedirectConfiguration
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - Új választható paraméter: -RedirectConfigurations
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * Azure-webhelyek támogatása az Application Gateway-ben
        - Új New-AzureRmApplicationGatewayProbeHealthResponseMatch parancsmag
        - Új választható paraméterek: -PickHostNameFromBackendHttpSettings, -MinServers, -Match
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - Új választható paraméterek: -PickHostNameFromBackendAddress, -AffinityCookieName, -ProbeEnabled, -Path
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * Frissített Get-AzureRmPublicIPaddress parancsmag, amely a Virtuális gép méretezési csoportjával létrehozott publicipaddress erőforrásokat kéri le
    * Új parancsmag a virtuális hálózat aktuális kihasználásának lekéréséhez
        - Get-AzureRmVirtualNetworkUsageList
* Profil
    * Kijavítottuk az Import-AzureRmContext és a Save-AzureRmContext parancsmag használatakor fellépő hibát
        - További információt itt találhat: https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * Új modul bevezetése az Azure Site Recovery műveletekhez.
        - Minden parancsmag a következővel kezdődik: AzureRmRecoveryServicesAsr*
* SQL
    * Adatszinkronizálási PowerShell-parancsmagok hozzáadása az AzureRM.Sql-hez
    * Az AzureRmSqlServer parancsmagok frissítése az új REST API-verziók használatára, amelyek elkerülik az időtúllépéseket kiszolgáló létrehozásakor.
    * A kiszolgálófrissítési parancsmagok elavultak, mert a régi kiszolgálóverzió (2.0) többé nem létezik.
    * A New-AzureRmSqlServer és Set-AzureRmSqlServer parancsmaghoz hozzáadott új AssignIdentity választható paraméter támogatja az erőforrás-identitás kiépítését SQL kiszolgáló-erőforráshoz
    * A ResourceGroupName paraméter mostantól nem kötelező a Get-AzureRmSqlServer parancsmaghoz
        - További információt itt találhat: https://github.com/Azure/azure-powershell/issues/635
* ServiceManagement ExpressRoute-hoz:
    * A frissített New-AzureBgpPeering parancsmag az alábbi új beállításokat tartalmazza:
        - PeerAddressType: Az IPv4 vagy az IPv6 értékei megadhatók a megfelelő címcsalád-típus BGP társviszonyának létrehozásához
    * A frissített Set-AzureBgpPeering parancsmag az alábbi új beállításokat tartalmazza:
        - PeerAddressType: Az IPv4 vagy az IPv6 értékei megadhatók a megfelelő címcsalád-típus BGP társviszonyának frissítéséhez
    * A frissített Remove-AzureBgpPeering parancsmag az alábbi új beállításokat tartalmazza:
        - PeerAddressType: Az IPv4, IPv6 vagy mindegyik értékei megadhatók a megfelelő címcsalád-típus vagy mindegyik BGP társviszonyának eltávolításához

## <a name="20170607---version-410"></a>2017.06.07. – 4.1.0-ás verzió
* AnalysisServices
    * Új termékváltozatok: B1, B2, S0
    * Vertikális felskálázás/leskálázás támogatásának hozzáadása
* CognitiveServices
    * Frissült a licencszerződések részletes megjelenítése a Cognitive Services-erőforrások létrehozásakor
* Számítás
    * Kijavítottuk a Test-AzureRmVMAEMExtension parancsmagot a több felügyelt lemezzel rendelkező virtuális gépekhez
    * Frissült Set-AzureRmVMAEMExtension parancsmag: Gyorsítótárazási információ hozzáadása a prémium szintű felügyelt lemezekhez
    * Add-AzureRmVhd: A virtuális merevlemezek méretkorlátja 4 TB-ra emelkedett.
    * Stop-AzureRmVM: Dokumentáció tisztázása a STayProvisioned paraméter esetében
    * New-AzureRmDiskUpdateConfig
      * Elavult paraméterek: CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId
    * Set-AzureRmDiskUpdateImageReference: Elavult parancsmag
    * New-AzureRmSnapshotUpdateConfig
      * Elavult paraméterek: CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId
    * Set-AzureRmSnapshotUpdateImageReference Elavult parancsmag
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)
      * KeyVault által felügyelt titkosítás engedélyezése a DataLake Store-hoz
* DevTestLabs
    * A frissített parancsmagok használhatók az aktuális és frissített DevTest Labs API-verzióval.
* IoTHub
    * Útválasztás támogatása az IoTHub-parancsmagokhoz
* KeyVault
  * Az új parancsmagok támogatják a hozzáférési kulcsokat a KeyVault által felügyelt tárfiókokhoz
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* Network (Hálózat)
    * Get-AzureRmNetworkUsage: Új parancsmag a hálózathasználat és a kapacitás részleteinek megjelenítésére
    * Új GatewaySku beállítások a VirtualNetworkGateways-hez
        * A VpnGw1, a VpnGw2 és a VpnGw3 a VPN-átjárókhoz hozzáadott új termékváltozatok
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * Kijavítottuk a súgó példáit
* NotificationHubs
    * NotificationHubs parancsmagok átlátható frissítése új API esetében
* Profil
    * Resolve-AzureRmError
      * Új parancsmag a parancsmagok által okozott hibák és kivételek részleteit jeleníti meg, beleértve a kiszolgálókérés és kiszolgálóválasz adatait
    * Send-Feedback
      * Bejelentkezés nélkül küldhető visszajelzés engedélyezése
    * Get-AzureRmSubscription
      * Kijavítottuk a CSP-előfizetések lekérésekor fellépő hibát
* Erőforrások
    * Kijavítottuk a hibát, amely miatt a Get-AzureRMRoleAssignment Hibás kérést eredményezett, ha a szerepkörkiosztások száma nagyobb volt, mint 1000
        * A felhasználók mostantól akkor is használhatják a Get-AzureRMRoleAssignment parancsmagot, ha a visszaadandó szerepkörkiosztások száma nagyobb, mint 1000
* SQL
    * Restore-AzureRmSqlDatabase: Frissítettük a dokumentáció példáit
* Tárolás
    * AssignIdentity beállítás támogatása az erőforrásmód-tárfiók parancsmagokhoz
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * Ügyfélkulcs támogatása az erőforrásmód-tárfiók parancsmagokhoz
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* TrafficManager

    * Új monitorozási beállítások: MonitorIntervalInSeconds, MonitorTimeoutInSeconds, MonitorToleratedNumberOfFailures
    * Új monitorozási protokoll: TCP
* ServiceManagement
    * Add-AzureVhd: A virtuális merevlemezek méretkorlátja 4 TB-ra emelkedett.
    * New-AzureBGPPeering: LegacyMode támogatása
* Azure.Storage
    * Frissítettük a helyettesítő karaktereket elfogadó paraméterek súgóját és a StorageContext típust

## <a name="20170523---version-402"></a>2017.05.23. – 4.0.2-es verzió
* Profil
    * Add-AzureRmAccount
      * Új `-EnvironmentName` paraméteralias az AzureRM.profile 2.x verzióival való visszamenőleges kompatibilitáshoz

## <a name="20170512---version-401"></a>2017.05.12. – 4.0.1-es verzió
 * Kijavítottuk a New-AzureStorageContext parancsmaggal kapcsolatos, offline forgatókönyvekben fellépő hibát: https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>2017.05.10. – 4.0.0-ás verzió


* Ez a kiadás jelentős változásokat tartalmaz. A változás részleteit és a meglévő szkriptekre gyakorolt hatást [a migrálási útmutatóban](https://aka.ms/azps-migration-guide) találja.
* ApiManagement
  - Külső csoportok konfigurálásának támogatása a New-AzureRmApiManagementGroup parancsmagban.
* Számlázás
  - Új Get-AzureRmBillingPeriod parancsmag
    + az Azure-előfizetés elszámolási időszakainak beolvasásához.
  - Módosult a Get-AzureRmBillingInvoice parancsmag
  - Új BillingPeriodNames tulajdonság
  - Kimenet listanézetben
* Számítás
  - A módosult Set-AzureRmVMAEMExtension és Test-AzureRmVMAEMExtension parancsmagok támogatják a prémium szintű Managed Disks szolgáltatást
  - Az IaaS VM-ek titkosítási beállításainak biztonsági mentése; hiba esetén visszaállítása
  - A ChefServiceInterval beállítás új neve mostantól ChefDaemonInterval, de a régi név is használható.
  - A duplikált DataDiskNames és NetworkInterfaceIDs tulajdonságok el lettek távolítva a PS VM-objektumából.
  - A DataDiskNames és a NetworkInterfaceIDs paraméterek mostantól nem kötelezőek a Remove-AzureRmVMDataDisk és a Remove-AzureRmVMNetworkInterface parancsmagban.
  - Kijavítottuk a Get parancsmagok átirányítását listaobjektum visszaadásakor.
  - Az RDFE-parancsmagokkal ütköző parancsmagok új nevet kaptak. További részletek az alábbi problémánál találhatók: https://github.com/Azure/azure-powershell/issues/2917
    + A `New-AzureVMSqlServerAutoBackupConfig` új nevet kapott: `New-AzureRmVMSqlServerAutoBackupConfig`
    + A `New-AzureVMSqlServerAutoPatchingConfig` új nevet kapott: `New-AzureRmVMSqlServerAutoPatchingConfig`
    + A `New-AzureVMSqlServerKeyVaultCredentialConfig` új nevet kapott: `New-AzureRmVMSqlServerKeyVaultCredentialConfig`
* Használat
  - Új Get-AzureRmConsumptionUsageDetail parancsmag
    + az előfizetés használati adatainak beolvasásához.
* ContainerRegistry
  - Új PowerShell-parancsmagok az Azure Container Registry szolgáltatásban
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - A katalóguscsomag beolvasásának és listázásának támogatása
  - Az alábbi katalóguselemek mélyebb szintű elődökből való listázásának támogatása:
    + Tábla
    + TVF
    + Nézet
    + Statisztika
* DataLakeStore
  - Az `Import-AzureRMDataLakeStoreItem` és az `Export-AzureRMDataLakeStoreItem` nyomkövetési naplózása alapértelmezés szerint le lett tiltva a teljesítmény javítása céljából. Ha nyomkövetési naplózásra van szükség, használja a `-DiagnosticLogLevel` és a `-DiagnosticLogPath` paramétereket
  - Kijavítottunk egy, nagy mennyiségű kis fájl ADLS-be való feltöltésekor a PowerShell összeomlását okozó hibát.
* EventHub
  - Hibajavítás:
    + Kijavítottunk egy hibát a Set-AzureRmEventHubNamespace parancsmagban (a Tier értéke SkuName helyett nem lehet null)
    + Set-AzureRmEventHub – kijavítottuk az EventHub frissítésekor jelentkező „Az objektumhivatkozás nincs beállítva az objektum egyik példányára” hibát
* Insights
  - Add-AzureRm*AlertRule
    + Egyetlen objektumot ad vissza: newResource, statusCode, requestId
  - Get-AzureRmAlertRule
    + A kimenet mostantól enumerált, és nem egyetlen objektumnak számít. A típus nem változott, továbbra is listának minősül.
  - Remove-AzureRmAlertRule
    + A statusCode a kérelem által visszaadott állapotkódot követi – korábban mindig OK értékű volt.
  - Add-AzureRmAutoscaleSetting
    + Egyetlen objektumot ad vissza (nem pedig egy listát, mint korábban), amelyben szerepel az állapotkód, a kérés azonosítója és az újonnan létrehozott vagy módosított erőforrás.
    + A statusCode a kérelem által visszaadott állapotot követi – korábban mindig OK értékű volt.
  - New-AzureRmAutoscaleRule
    + A ScaleActionType paraméter ki lett bővítve, mostantól megkapja a következő értékeket: ChangeCount, PercentChangeCount, ExactCount.
  - Remove-AzureRmAutoscaleSetting
    + A kimenetben szereplő statusCode a kérelem által visszaadott statusCode értéket követi. Korábban mindig OK értékű volt.
  - Get-AzureRMLogProfile
    + A kimenet mostantól enumerált, míg korábban egyetlen objektumnak számított. A kimenet típusa nem változott, továbbra is listának minősül.
  - Remove-AzureRmLogProfile
    + Implementáltuk a PassThru paramétert.
  - Metrikák API
    + Az SDK mostantól az MDM-től kéri le a metrikákat.
  - Get-AzureRmMetricDefinition
    + A kimenet továbbra is listának minősül, de a lista szerkezete megváltozott.
  - Get-AzureRmMetric
    + A hívás megváltozott. Az új szintaxis: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]
    + A kimenet listának minősül, és az elemek szerkezete megváltozott.
* KeyVault
  - A KeyVault titkos kódjai támogatják a biztonsági mentést/visszaállítást
    + Biztonsági másolat készíthető a titkos kódokról, és vissza lehet állítani azokat – ugyanúgy, ahogy eddig a kulcsokat

  - A kulcsok és a titkos kódok biztonsági mentési parancsmagjai mostantól bemeneti paraméterként fogadják a megfelelő objektumokat
    + A hívó elvégezheti a lekérési és a biztonsági mentési műveletek láncolását: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - A biztonsági mentési parancsmagok mostantól támogatják a -Force kapcsolót, amellyel elvégezhető egy korábbi fájl felülírása
    + Ne feledje, hogy a korábbi fájlok felülírási kísérletére a rendszer mostantól nem dob hibát, ehelyett arra fogja kérni a felhasználót, hogy válasszon egy folytatási lehetőséget.
* LogicApp
  - Az adatcsere ellenőrzőszámához tartozó vészhelyreállítási parancsmagok új paraméterei:
    + A nem kötelező -AgreementType paraméterrel (X12 vagy Edifact) lehet megadni a megfelelő ellenőrzőszámokat
* Machine Learning
  - A szolgáltatás az Azure Machine Learning .Net SDK új verzióját használja, és egy új parancsmag is elérhető benne
    + Add-AzureRmMlWebServiceRegionalProperty
  - Kisebb fogalmazási hibákat javítottunk a súgószövegben.
* Network (Hálózat)
  - Új parancsmag: Test-AzureRmNetworkWatcherConnectivity
    + A forrásként és célként megadott virtuális gép összekapcsolhatósági adatait adja vissza
    + Ha a forrás és a cél közötti kapcsolatot nem lehet létrehozni, a parancsmag a probléma részleteit adja vissza
* Profil
  - Az új Send-Feedback parancsmaggal a felhasználók az Azure PowerShell csapatának visszajelzést küldő rendszerüzeneteket kezdeményezhetnek.
  - Az alábbi aliasokat eltávolítottuk, mert az Azure modulban meglévő parancsmagok neveivel ütköztek:
    + `Enable-AzureDataCollection` (az `Enable-AzureRmDataCollection` támogatta)
    + `Disable-AzureDataCollection` (a `Disable-AzureRmDataCollection` támogatta)
* Továbbító
  - Az új Azure Relay-parancsmagokkal a felhasználók az összes Azure Relay-erőforrás létrehozását és kezelését elvégezhetik.
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* Erőforrások
  - Több erőforráscsoportra kiterjedő üzembe helyezés támogatása a New-AzureRmResourceGroupDeployment parancsmaghoz
    + A felhasználók mostantól beágyazott üzembe helyezések révén különböző erőforráscsoportokba helyezhetnek üzembe erőforrásokat.
* ServiceBus

  - Hibajavítás: A ServiceBus Queue objektumának tulajdonságai null értékre lettek állítva, és az objektum bemeneti paraméterként szolgál a Set-AzureRmServiceBusQueue parancsmagban az üzenetsor frissítésekor.
    - Az érintett tulajdonságok a következők: LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount és MessageCount
* ServiceFabric

  - Új Service Fabric-parancsmagok
    + Add-AzureRmServiceFabricApplicationCertificate       Alkalmazás-tanúsítványként szolgáló tanúsítvány felvétele
    + Add-AzureRmServiceFabricClientCertificate       Köznapi név vagy ujjlenyomat hozzáadása a fürtbeállításokhoz az ügyfél hitelesítése céljából
    + Add-AzureRmServiceFabricClusterCertificate       Másodlagos fürttanúsítvány hozzáadása a fürthöz a meglévő tanúsítvány kiegészítése céljából
    + Add-AzureRmServiceFabricNodes       Adott csomóponttípusú csomópontok vagy virtuális gépek hozzáadása a fürthöz
    + Add-AzureRmServiceFabricNodeType       Csomóponttípus vagy virtuális gépek hozzáadása meglévő fürthöz
    + Get-AzureRmServiceFabricCluster       A fürterőforrás részleteinek beolvasása
    + New-AzureRmServiceFabricCluster Új ServiceFabric-fürt létrehozása. A parancsnak többféle változata létezik az eltérő helyzetek kezelésére
    + Remove-AzureRmServiceFabricClientCertificate       Fürtök elérésére használható ügyféltanúsítvány eltávolítása
    + Remove-AzureRmServiceFabricClusterCertificate       Fürtbiztonsági célra használható fürttanúsítvány eltávolítása
    + Remove-AzureRmServiceFabricNodes       Csomópontok eltávolítása a fürt adott csomóponttípusából
    + Remove-AzureRmServiceFabricNodeType       Csomóponttípus eltávolítása a fürtből
    + Remove-AzureRmServiceFabricSettings       Legalább egy ServiceFabric-beállítás eltávolítása a fürtből
    + Set-AzureRmServiceFabricSettings       A fürt legalább egy ServiceFabric-beállításának megadása vagy módosítása
    + Set-AzureRmServiceFabricUpgradeType       A fürt ServiceFabric-frissítéstípusának módosítása
    + Update-AzureRmServiceFabricDurability       A fürt tartóssági szintjének módosítása
    + Update-AzureRmServiceFabricReliability       A fürt megbízhatósági szintjének módosítása
* SQL
  - Új paraméter (-SampleName) a New-AzureRmSqlDatabase parancsmaghoz
  - Megváltoztak a feladatátvételi csoport parancsmagjai
  - A Tag paraméterek el lettek távolítva
  - A Remove-AzureRmSqlDatabaseFailoverGroup parancsmagnál megszűnt a PartnerResourceGroupName és a PartnerServerName paraméter
  - A GracePeriodWithDataLossHour paramétert majdan leváltó GracePeriodWithDataLossHours paraméter jelent meg a New- és a Set- parancsmagokhoz
  - Bővült és frissült a dokumentáció
  - Módosítottuk a visszaadott objektumok formázását, és kijavítottunk néhány hibát, amelyek miatt bizonyos mezők feltöltése nem mindig történt meg
  - Új tulajdonságok a feladatátvételi csoport objektumához: DatabaseNames és PartnerLocation
  - Kijavítottunk egy hibát, amely miatt a Switch- parancsmag azonnal visszatért ahelyett, hogy megvárta volna a művelet befejezését
  - Kijavítottunk a türelmi időszakhoz tartozó magas értékek használatakor jelentkező egészszám-túlcsordulási hibát
  - A türelmi időszak értéke legalább 1 óra lesz, ha ennél alacsonyabb értéket adnak meg
  - A Usage_Anomaly el lett távolítva a Set-AzureRmSqlDatabaseThreatDetectionPolicy és a Set-AzureRmSqlServerThreatDetectionPolicy parancsmag ExcludedDetectionType paraméterének elfogadható értékei közül.
* Tárolás
  - Az SRP SDK a 6.3.0-s verzióra frissült
  - New/Set-AzureRmStorageAccount: az EnableHttpsTrafficOnly attribútumot támogató új paraméter
  - New/Set/Get-AzureRmStorageAccount: A visszaadott tárfióknak új attribútuma van (EnableHttpsTrafficOnly)
* Azure.Storage
  - Frissítés az Azure Storage ügyféloldali kódtárának 8.1.1-es és az Azure Storage adatátviteli kódtárának 0.5.1-es verziójára
  - Új, a blob növekményes másolati szolgáltatását támogató parancsmag
