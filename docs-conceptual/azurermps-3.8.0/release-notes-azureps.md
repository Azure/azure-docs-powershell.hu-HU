---
title: Az Azure PowerShell változásnaplója | Microsoft Docs
description: Az alábbiakban az Azure PowerShell legutóbbi kiadásában végrehajtott módosítások előzményei olvashatók.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 2e17b6f7f62f25d8d91c4d32a4a1ae5c45b8665d
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821802"
---
# <a name="release-notes"></a>Kibocsátási megjegyzések

Az alábbiakban az Azure PowerShell jelen kiadásában végrehajtott módosítások listája olvasható.

## <a name="version-380"></a>3.8.0-ás verzió
* Compute
  - A Get-* parancsmagok hibájának javítása több oldalnyi adat (több, mint 120 elem) lekérésének lehetővé tétele érdekében
* DataLakeAnalytics
  - Egyes parancsok súgójának javítása a megfelelő megfogalmazás és példák érdekében.
* DataLakeStore
  - A `Get-AzureRMDataLakeStoreItemContent` parancsmag elejének és végének támogatása. Ez lehetővé teszi az új, megjelenítendő felső N vagy utolsó N vonalakkal tagolt sor visszaadását.
* HDInsight
  - Az RServer-fürttípus támogatása
    + Az élcsomópontok virtuális gépeinek mérete a New-AzureRmHDInsightCluster vagy New-AzureRmHDInsightClusterConfig parancsmagokban adható meg az RServer-fürt esetében
    + Az RServer mostantól egy konfigurációs beállítás az Add-AzureRmHDInsightConfigValues parancsmagon belül. Ez lehetővé teszi az RStudio-jelző beállítását, amely jelzi, hogy az R Studio telepítését el kell végezni.
* LogicApp
  - A Set-AzureRmIntegrationAccountSchema és Set-AzureRmIntegrationAccountMap parancsmagok contentlink-hibájának javítása (a content és contentlink paraméterek egyaránt meg voltak adva, amely a frissítés meghiúsulását okozta).
* Network (Hálózat)
  - Új webalkalmazási tűzfalszolgáltatások támogatása az Application Gateway átjárók esetében
    + A New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig parancsmag hozzáadása
    + A Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets) hozzáadása
    + A New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration frissítése: A -RuleSetType, -RuleSetVersion és -DisabledRuleGroups paraméterek hozzáadása
    + A Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration frissítése: A -RuleSetType, -RuleSetVersion és -DisabledRuleGroups paraméter hozzáadása
  - IPsec-házirendek támogatása a virtuális hálózati átjárókapcsolatok esetében
  - A New-AzureRmIpsecPolicy parancsmag hozzáadása
  - A New-AzureRmVirtualNetworkGatewayConnection frissítése: Az -IpsecPolicies és -UsePolicyBasedTrafficSelectors paraméter hozzáadása
* Profil
  - *Elavult*: A Save-AzureRmProfile parancsmag új neve: Save-AzureRmContext. Létezik egy alias a régi parancsmag nevéhez, amely a következő kiadásban el lesz távolítva.
  - *Elavult*: A Select-AzureRmProfile parancsmag új neve: Import-AzureRmContext. Létezik egy alias a régi parancsmag nevéhez, amely a következő kiadásban el lesz távolítva.
  - A profilparancsmagok PSAzureContext és PSAzureProfile kimenettípusa a következő kiadásban módosítva lesz.
  - A Save-AzureRmContext parancsmag nem rendelkezik majd OutputType paraméterrel a következő kiadásban.
  - Hiba javítása a parancsmagok általános kódjában annak érdekében, hogy azok a FIPS előírásainak megfelelő algoritmusokat használjanak az adatkivonatokhoz: https://github.com/Azure/azure-powershell/issues/3651
* SQL
  - Hibajavítások az Azure feladatátvételi csoport parancsmagjaiban
  - Műveletlekérdezés javítása
  - A GracePeriodWithDataLossHour érték javítása a FailoverPolicy paraméter Manual (Manuális) értékre való állításakor
* TrafficManager
  - A földrajzi forgalom-útválasztási módszer támogatása
    + Új „Geographic” érték a New-AzureRmTrafficManagerProfile parancsmag TrafficRoutingMethod paramétere esetében
    + Új „GeoMapping” paraméter a New-AzureRmTrafficManagerEndpoint és Add-AzureRmTrafficManagerEndpointConfig parancsmag esetében
    + Az átirányítás javítása a Get-AzureRmTrafficManagerProfile parancsmag esetében profilgyűjtemény visszaadásakor
* ServiceManagement
  - Restart-AzureVM: Az InitiateMaintenance paraméter hozzáadása arra az esetre, ha a karbantartás elvégzése a virtuális gép újraindítása során történik.
  - Get-AzureVM: Maintenance Status (Karbantartás állapota) mező hozzáadása.
  - Új parancsmagok hozzáadása a Recovery Services-tároló frissítésének támogatása érdekében
    + Test-AzureRecoveryServicesVaultUpgrade
    + Invoke-AzureRecoveryServicesVaultUpgrade
