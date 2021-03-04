---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: d86810ec15d38ecbe57a7471297b4ac167a2e526
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933866"
---
# <span data-ttu-id="751ff-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="751ff-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="751ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="751ff-102">SYNOPSIS</span></span>
<span data-ttu-id="751ff-103">Kéréstovábbító szabályt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="751ff-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="751ff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="751ff-104">SYNTAX</span></span>

### <span data-ttu-id="751ff-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="751ff-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="751ff-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="751ff-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="751ff-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="751ff-107">DESCRIPTION</span></span>
<span data-ttu-id="751ff-108">Az **Add-AzApplicationGatewayRequestRoutingRule** parancsmag hozzáad egy kéréstovábbítási szabályt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="751ff-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="751ff-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="751ff-109">EXAMPLES</span></span>

### <span data-ttu-id="751ff-110">1. példa: Kéréstovábbító szabály hozzáadása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="751ff-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="751ff-111">Az első parancs az alkalmazás átjáróját a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="751ff-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="751ff-112">A második parancs hozzáadja a kéréstovábbítási szabályt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="751ff-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="751ff-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="751ff-113">PARAMETERS</span></span>

### <span data-ttu-id="751ff-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="751ff-114">-ApplicationGateway</span></span>
<span data-ttu-id="751ff-115">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag hozzáad egy kéréstovábbító szabályt.</span><span class="sxs-lookup"><span data-stu-id="751ff-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="751ff-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="751ff-116">-BackendAddressPool</span></span>
<span data-ttu-id="751ff-117">Egy alkalmazás-átjáró háttércímkészlet-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="751ff-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="751ff-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="751ff-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="751ff-119">Egy alkalmazás-átjáró háttércímkészlet-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="751ff-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="751ff-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="751ff-120">-BackendHttpSettings</span></span>
<span data-ttu-id="751ff-121">Egy alkalmazás-átjáró háttér-HTTP-beállítási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="751ff-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="751ff-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="751ff-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="751ff-123">Egy alkalmazás-átjáró háttér-HTTP-beállításazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="751ff-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="751ff-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="751ff-124">-DefaultProfile</span></span>
<span data-ttu-id="751ff-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="751ff-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="751ff-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="751ff-126">-HttpListener</span></span>
<span data-ttu-id="751ff-127">Az alkalmazás átjárója HTTP-et hallgató objektum megadása.</span><span class="sxs-lookup"><span data-stu-id="751ff-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="751ff-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="751ff-128">-HttpListenerId</span></span>
<span data-ttu-id="751ff-129">Az alkalmazás átjárójának HTTP-hallgatóazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="751ff-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="751ff-130">-Name</span><span class="sxs-lookup"><span data-stu-id="751ff-130">-Name</span></span>
<span data-ttu-id="751ff-131">Ez a parancsmag hozzáadja a kéréstovábbítja szabály nevét.</span><span class="sxs-lookup"><span data-stu-id="751ff-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="751ff-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="751ff-132">-Priority</span></span>
<span data-ttu-id="751ff-133">A szabály prioritása</span><span class="sxs-lookup"><span data-stu-id="751ff-133">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="751ff-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="751ff-134">-RedirectConfiguration</span></span>
<span data-ttu-id="751ff-135">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="751ff-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="751ff-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="751ff-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="751ff-137">A RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="751ff-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="751ff-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="751ff-138">-RewriteRuleSet</span></span>
<span data-ttu-id="751ff-139">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="751ff-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="751ff-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="751ff-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="751ff-141">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="751ff-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="751ff-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="751ff-142">-RuleType</span></span>
<span data-ttu-id="751ff-143">A kéréstovábbítja szabály típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="751ff-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="751ff-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="751ff-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="751ff-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="751ff-145">-UrlPathMapId</span></span>
<span data-ttu-id="751ff-146">Az útválasztási szabály URL-útvonal-leképezés-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="751ff-146">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="751ff-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="751ff-147">CommonParameters</span></span>
<span data-ttu-id="751ff-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="751ff-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="751ff-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="751ff-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="751ff-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="751ff-150">INPUTS</span></span>

### <span data-ttu-id="751ff-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="751ff-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="751ff-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="751ff-152">OUTPUTS</span></span>

### <span data-ttu-id="751ff-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="751ff-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="751ff-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="751ff-154">NOTES</span></span>

## <span data-ttu-id="751ff-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="751ff-155">RELATED LINKS</span></span>

[<span data-ttu-id="751ff-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="751ff-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="751ff-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="751ff-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="751ff-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="751ff-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="751ff-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="751ff-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


