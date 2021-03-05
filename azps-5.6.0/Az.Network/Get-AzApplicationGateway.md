---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 70d3145c50f9f0c95e61133dd98c579e6f8ecdd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003686"
---
# <span data-ttu-id="e124f-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e124f-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="e124f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e124f-102">SYNOPSIS</span></span>
<span data-ttu-id="e124f-103">Alkalmazás-átjárót kap.</span><span class="sxs-lookup"><span data-stu-id="e124f-103">Gets an application gateway.</span></span>

## <span data-ttu-id="e124f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e124f-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e124f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e124f-105">DESCRIPTION</span></span>
<span data-ttu-id="e124f-106">A **Get-AzApplicationGateway** parancsmag alkalmazás-átjárót kap.</span><span class="sxs-lookup"><span data-stu-id="e124f-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="e124f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e124f-107">EXAMPLES</span></span>

### <span data-ttu-id="e124f-108">1. példa: Adott alkalmazás-átjáró lekérte</span><span class="sxs-lookup"><span data-stu-id="e124f-108">Example 1: Get a specified application gateway</span></span>
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
ForceFirewallPolicyAssociation      :
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

<span data-ttu-id="e124f-109">Ez a parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="e124f-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="e124f-110">2. példa: Az alkalmazás-átjárók listájának lekérte egy erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="e124f-110">Example 2: Get a list of application gateways in a resource group</span></span>
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
ForceFirewallPolicyAssociation      :
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

<span data-ttu-id="e124f-111">Ez a parancs lekérte az Erőforráscsoport01 nevű erőforráscsoport összes alkalmazás-átjáróját, és a $AppGwList tárolja.</span><span class="sxs-lookup"><span data-stu-id="e124f-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="e124f-112">3. példa: Az alkalmazás-átjárók listájának lekérte az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="e124f-112">Example 3: Get a list of application gateways in a subscription</span></span>
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
ForceFirewallPolicyAssociation      :
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

<span data-ttu-id="e124f-113">Ez a parancs az előfizetésben található összes alkalmazás-átjáró listáját lekérte, és a $AppGwList tárolja.</span><span class="sxs-lookup"><span data-stu-id="e124f-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="e124f-114">4. példa: Alkalmazás-átjárók listájának lekérte az előfizetésben szűréssel</span><span class="sxs-lookup"><span data-stu-id="e124f-114">Example 4: Get a list of application gateways in a subscription using filtering</span></span>
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
ForceFirewallPolicyAssociation      :
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

<span data-ttu-id="e124f-115">Ez a parancs az előfizetés összes olyan alkalmazás-átjáróját lekérte, amely az "ApplicationGateway01" kezdetével kezdődik, és a $AppGwList tárolja.</span><span class="sxs-lookup"><span data-stu-id="e124f-115">This command gets a list of all the application gateways in the subscription that start with "ApplicationGateway01" and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="e124f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e124f-116">PARAMETERS</span></span>

### <span data-ttu-id="e124f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e124f-117">-DefaultProfile</span></span>
<span data-ttu-id="e124f-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e124f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e124f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e124f-119">-Name</span></span>
<span data-ttu-id="e124f-120">Annak az alkalmazás-átjárónak a nevét adja meg, amelybe a parancsmagot beállítja.</span><span class="sxs-lookup"><span data-stu-id="e124f-120">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e124f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e124f-121">-ResourceGroupName</span></span>
<span data-ttu-id="e124f-122">Az alkalmazás-átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e124f-122">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="e124f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e124f-123">CommonParameters</span></span>
<span data-ttu-id="e124f-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e124f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e124f-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e124f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e124f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e124f-126">INPUTS</span></span>

### <span data-ttu-id="e124f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e124f-127">System.String</span></span>

## <span data-ttu-id="e124f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e124f-128">OUTPUTS</span></span>

### <span data-ttu-id="e124f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e124f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e124f-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e124f-130">NOTES</span></span>

## <span data-ttu-id="e124f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e124f-131">RELATED LINKS</span></span>

[<span data-ttu-id="e124f-132">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e124f-132">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


