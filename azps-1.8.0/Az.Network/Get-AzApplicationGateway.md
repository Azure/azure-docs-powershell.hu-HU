---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: d2ce826ffe958f138402066a698153dd699082b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670681"
---
# <span data-ttu-id="bf1af-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf1af-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="bf1af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf1af-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1af-103">Bekerül egy alkalmazás-átjáróba.</span><span class="sxs-lookup"><span data-stu-id="bf1af-103">Gets an application gateway.</span></span>

## <span data-ttu-id="bf1af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf1af-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf1af-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf1af-105">DESCRIPTION</span></span>
<span data-ttu-id="bf1af-106">A **Get-AzApplicationGateway** parancsmag alkalmazás-átjárót kap.</span><span class="sxs-lookup"><span data-stu-id="bf1af-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="bf1af-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf1af-107">EXAMPLES</span></span>

### <span data-ttu-id="bf1af-108">1. példa: megadott alkalmazásspecifikus átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="bf1af-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="bf1af-109">Ez a parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bf1af-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="bf1af-110">2. példa: az alkalmazás-átjárók listájának beszerzése egy erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="bf1af-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="bf1af-111">Ez a parancs felsorolja a ResourceGroup01 nevű erőforráscsoport összes alkalmazás-átjáróját, és a $AppGwList változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bf1af-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="bf1af-112">3. példa: az alkalmazás-átjárók listájának beszerzése az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="bf1af-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="bf1af-113">Ez a parancs felsorolja az előfizetésben szereplő összes alkalmazás-átjárót, és a $AppGwList változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bf1af-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="bf1af-114">Példa 4: az alkalmazás-átjárók listájának beszerzése az előfizetésben szűréssel</span><span class="sxs-lookup"><span data-stu-id="bf1af-114">Example 4: Get a list of application gateways in a subscription using filtering</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -Name ApplicationGateway*

Sku                                 : Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
SslPolicy                           :
GatewayIPConfigurations             : {appGatewayFrontendIP}
AuthenticationCertificates          : {}
SslCertificates                     : {}
TrustedRootCertificates             : {}
FrontendIPConfigurations            : {appGatewayFrontendIP}
FrontendPorts                       : {appGatewayFrontendPort}
Probes                              : {}
BackendAddressPools                 : {appGatewayBackendPool}
BackendHttpSettingsCollection       : {appGatewayBackendHttpSettings}
HttpListeners                       : {appGatewayHttpListener}
UrlPathMaps                         : {}
RequestRoutingRules                 : {rule1}
RewriteRuleSets                     : {}
RedirectConfigurations              : {}
WebApplicationFirewallConfiguration :
AutoscaleConfiguration              :
CustomErrorConfigurations           : {}
EnableHttp2                         :
EnableFips                          :
Zones                               : {}
OperationalState                    : Running
ProvisioningState                   : Succeeded
Identity                            :
GatewayIpConfigurationsText         : []
AuthenticationCertificatesText      : []
SslCertificatesText                 : []
FrontendIpConfigurationsText        : []
FrontendPortsText                   : []
BackendAddressPoolsText             : []
BackendHttpSettingsCollectionText   : []
HttpListenersText                   : []
RewriteRuleSetsText                 : []
RequestRoutingRulesText             : []
ProbesText                          : []
UrlPathMapsText                     : []
IdentityText                        : null
SslPolicyText                       : null
ResourceGroupName                   : tjp-rg
Location                            : westus
ResourceGuid                        : 00000000-0000-0000-0000-000000000000
Type                                : Microsoft.Network/applicationGateways
Tag                                 : {}
TagsTable                           :
Name                                : ApplicationGateway01
Etag                                : W/"00000000-0000-0000-0000-000000000000"
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/provide
                                      rs/Microsoft.Network/applicationGateways/ApplicationGateway01
```

<span data-ttu-id="bf1af-115">Ez a parancs a "ApplicationGateway01" kezdetű előfizetés összes alkalmazás-átjárójának listáját beolvassa, és a $AppGwList változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bf1af-115">This command gets a list of all the application gateways in the subscription that start with "ApplicationGateway01" and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="bf1af-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf1af-116">PARAMETERS</span></span>

### <span data-ttu-id="bf1af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1af-117">-DefaultProfile</span></span>
<span data-ttu-id="bf1af-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf1af-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1af-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf1af-119">-Name</span></span>
<span data-ttu-id="bf1af-120">Annak az alkalmazás-átjárónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="bf1af-120">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="bf1af-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf1af-121">-ResourceGroupName</span></span>
<span data-ttu-id="bf1af-122">Az alkalmazás-átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf1af-122">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="bf1af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1af-123">CommonParameters</span></span>
<span data-ttu-id="bf1af-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf1af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1af-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf1af-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1af-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf1af-126">INPUTS</span></span>

### <span data-ttu-id="bf1af-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bf1af-127">System.String</span></span>

## <span data-ttu-id="bf1af-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf1af-128">OUTPUTS</span></span>

### <span data-ttu-id="bf1af-129">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf1af-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bf1af-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf1af-130">NOTES</span></span>

## <span data-ttu-id="bf1af-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf1af-131">RELATED LINKS</span></span>

[<span data-ttu-id="bf1af-132">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf1af-132">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


