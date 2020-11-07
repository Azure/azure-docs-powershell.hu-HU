---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: bd6888402a2e3a88b9d3d19da752b0ac18d20f32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837793"
---
# <span data-ttu-id="f6bf0-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f6bf0-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f6bf0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="f6bf0-103">Módosítja a kérések útválasztási szabályát egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="f6bf0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6bf0-104">SYNTAX</span></span>

### <span data-ttu-id="f6bf0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6bf0-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6bf0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f6bf0-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6bf0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6bf0-107">DESCRIPTION</span></span>
<span data-ttu-id="f6bf0-108">A **set-AzApplicationGatewayRequestRoutingRule** parancsmag módosítja a kérések útválasztási szabályát.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="f6bf0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f6bf0-109">EXAMPLES</span></span>

### <span data-ttu-id="f6bf0-110">Példa 1: a Request útválasztási szabály frissítése</span><span class="sxs-lookup"><span data-stu-id="f6bf0-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="f6bf0-111">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f6bf0-112">A második parancs módosítja az alkalmazás átjárójának Request (útválasztási) szabályát a $Setting változóban megadott, a $Listener változóban megadott HTTP-figyelők, valamint a $Pool változóban megadott, a végpontokat tartalmazó címkészlet használatára.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="f6bf0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6bf0-113">PARAMETERS</span></span>

### <span data-ttu-id="f6bf0-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6bf0-114">-ApplicationGateway</span></span>
<span data-ttu-id="f6bf0-115">Azt az alkalmazásobjektum-objektumot adja meg, amelyhez ez a parancsmag a kérések útválasztási szabályát társítja.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="f6bf0-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f6bf0-116">-BackendAddressPool</span></span>
<span data-ttu-id="f6bf0-117">Az Application Gateway back-end címkészletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="f6bf0-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f6bf0-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="f6bf0-119">Az Application Gateway back-end Address Pool AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="f6bf0-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f6bf0-120">-BackendHttpSettings</span></span>
<span data-ttu-id="f6bf0-121">Az Application Gateway backend HTTP-beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="f6bf0-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f6bf0-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="f6bf0-123">Az Application Gateway back-end HTTP-beállításai AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="f6bf0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6bf0-124">-DefaultProfile</span></span>
<span data-ttu-id="f6bf0-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6bf0-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f6bf0-126">-HttpListener</span></span>
<span data-ttu-id="f6bf0-127">Az Application Gateway HTTP-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="f6bf0-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="f6bf0-128">-HttpListenerId</span></span>
<span data-ttu-id="f6bf0-129">Az alkalmazás-átjáró HTTP-figyelő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="f6bf0-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6bf0-130">-Name</span></span>
<span data-ttu-id="f6bf0-131">Annak a kérési művelettervi szabálynak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f6bf0-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6bf0-132">-RedirectConfiguration</span></span>
<span data-ttu-id="f6bf0-133">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6bf0-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f6bf0-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f6bf0-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="f6bf0-135">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="f6bf0-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f6bf0-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f6bf0-136">-RewriteRuleSet</span></span>
<span data-ttu-id="f6bf0-137">Az Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f6bf0-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f6bf0-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="f6bf0-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="f6bf0-139">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="f6bf0-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f6bf0-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="f6bf0-140">-RuleType</span></span>
<span data-ttu-id="f6bf0-141">A Request útválasztási szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6bf0-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="f6bf0-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="f6bf0-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="f6bf0-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="f6bf0-143">-UrlPathMapId</span></span>
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

### <span data-ttu-id="f6bf0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6bf0-144">CommonParameters</span></span>
<span data-ttu-id="f6bf0-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6bf0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6bf0-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6bf0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6bf0-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6bf0-147">INPUTS</span></span>

### <span data-ttu-id="f6bf0-148">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6bf0-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6bf0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6bf0-149">OUTPUTS</span></span>

### <span data-ttu-id="f6bf0-150">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6bf0-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6bf0-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6bf0-151">NOTES</span></span>

## <span data-ttu-id="f6bf0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6bf0-152">RELATED LINKS</span></span>

[<span data-ttu-id="f6bf0-153">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f6bf0-153">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f6bf0-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f6bf0-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f6bf0-155">Új – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f6bf0-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f6bf0-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f6bf0-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


