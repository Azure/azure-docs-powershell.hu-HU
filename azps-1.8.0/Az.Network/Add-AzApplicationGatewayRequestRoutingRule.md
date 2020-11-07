---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ffd65085cba383556f4c749c8b7e2b915bb0071c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670734"
---
# <span data-ttu-id="e4e3d-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e4e3d-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e4e3d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e3d-103">A kérések útválasztási szabályait hozzáadja az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="e4e3d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4e3d-104">SYNTAX</span></span>

### <span data-ttu-id="e4e3d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4e3d-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4e3d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e4e3d-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4e3d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4e3d-107">DESCRIPTION</span></span>
<span data-ttu-id="e4e3d-108">Az **Add-AzApplicationGatewayRequestRoutingRule** parancsmag a kérések útválasztási szabályait hozzáadja egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="e4e3d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e4e3d-109">EXAMPLES</span></span>

### <span data-ttu-id="e4e3d-110">1. példa: kérés-útválasztási szabály hozzáadása az alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="e4e3d-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="e4e3d-111">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e4e3d-112">A második parancs hozzáadja a Request Routing szabályt az Application Gateway programhoz.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="e4e3d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4e3d-113">PARAMETERS</span></span>

### <span data-ttu-id="e4e3d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4e3d-114">-ApplicationGateway</span></span>
<span data-ttu-id="e4e3d-115">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a kérések útválasztási szabályát felveszi.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e4e3d-116">-BackendAddressPool</span></span>
<span data-ttu-id="e4e3d-117">Az Application Gateway back-end Address Pool objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e4e3d-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="e4e3d-119">Az Application Gateway back-end Address Pool AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e4e3d-120">-BackendHttpSettings</span></span>
<span data-ttu-id="e4e3d-121">Egy alkalmazás átjárójának back-end HTTP Settings objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e4e3d-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e4e3d-123">A backend HTTP-beállítási AZONOSÍTÓját adja meg az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e3d-124">-DefaultProfile</span></span>
<span data-ttu-id="e4e3d-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4e3d-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e4e3d-126">-HttpListener</span></span>
<span data-ttu-id="e4e3d-127">Az Application Gateway HTTP-figyelő objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="e4e3d-128">-HttpListenerId</span></span>
<span data-ttu-id="e4e3d-129">Az Application Gateway HTTP-figyelő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4e3d-130">-Name</span></span>
<span data-ttu-id="e4e3d-131">A Request Routing szabály nevét adja meg, amely a parancsmagot adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4e3d-132">-RedirectConfiguration</span></span>
<span data-ttu-id="e4e3d-133">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4e3d-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e4e3d-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="e4e3d-135">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="e4e3d-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e4e3d-136">-RewriteRuleSet</span></span>
<span data-ttu-id="e4e3d-137">Az Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e4e3d-137">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="e4e3d-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="e4e3d-139">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="e4e3d-139">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e4e3d-140">-RuleType</span></span>
<span data-ttu-id="e4e3d-141">A Request útválasztási szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-141">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e4e3d-142">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="e4e3d-143">-UrlPathMapId</span></span>
<span data-ttu-id="e4e3d-144">A művelettervi szabály URL-elérési útjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4e3d-144">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e3d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e3d-145">CommonParameters</span></span>
<span data-ttu-id="e4e3d-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4e3d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e3d-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e3d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e3d-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4e3d-148">INPUTS</span></span>

### <span data-ttu-id="e4e3d-149">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4e3d-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4e3d-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4e3d-150">OUTPUTS</span></span>

### <span data-ttu-id="e4e3d-151">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4e3d-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4e3d-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4e3d-152">NOTES</span></span>

## <span data-ttu-id="e4e3d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4e3d-153">RELATED LINKS</span></span>

[<span data-ttu-id="e4e3d-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e4e3d-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e4e3d-155">Új – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e4e3d-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e4e3d-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e4e3d-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e4e3d-157">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e4e3d-157">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


