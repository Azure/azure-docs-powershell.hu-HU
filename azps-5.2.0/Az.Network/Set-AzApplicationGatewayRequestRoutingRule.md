---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: f815994a6f60490bd930a17748cd00167c2b52ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327218"
---
# <span data-ttu-id="635db-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="635db-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="635db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="635db-102">SYNOPSIS</span></span>
<span data-ttu-id="635db-103">Módosít egy kéréstovábbító szabályt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="635db-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="635db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="635db-104">SYNTAX</span></span>

### <span data-ttu-id="635db-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="635db-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="635db-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="635db-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="635db-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="635db-107">DESCRIPTION</span></span>
<span data-ttu-id="635db-108">A **Set-AzApplicationGatewayRequestRoutingRule** parancsmag módosítja a kéréstovábbítási szabályt.</span><span class="sxs-lookup"><span data-stu-id="635db-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="635db-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="635db-109">EXAMPLES</span></span>

### <span data-ttu-id="635db-110">1. példa: Kéréstovábbirányítási szabály frissítése</span><span class="sxs-lookup"><span data-stu-id="635db-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="635db-111">Az első parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="635db-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="635db-112">A második parancs módosítja az alkalmazás-átjáró kéréstovábbítási szabályát úgy, hogy a $Setting változóban megadott háttér-HTTP-beállításokat, a $Listener változóban megadott HTTP- hallgatót és a $Pool változóban megadott háttércímkészletet használja.</span><span class="sxs-lookup"><span data-stu-id="635db-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="635db-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="635db-113">PARAMETERS</span></span>

### <span data-ttu-id="635db-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="635db-114">-ApplicationGateway</span></span>
<span data-ttu-id="635db-115">Azt az alkalmazás-átjáróobjektumot adja meg, amellyel a parancsmag kéréstovábbító szabályt társít.</span><span class="sxs-lookup"><span data-stu-id="635db-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="635db-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="635db-116">-BackendAddressPool</span></span>
<span data-ttu-id="635db-117">Az alkalmazás átjárója háttércímkészletét adja meg.</span><span class="sxs-lookup"><span data-stu-id="635db-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="635db-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="635db-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="635db-119">Az alkalmazás-átjáró háttércímkészlet-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="635db-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="635db-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="635db-120">-BackendHttpSettings</span></span>
<span data-ttu-id="635db-121">Az alkalmazás átjárója háttér-HTTP-beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="635db-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="635db-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="635db-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="635db-123">Az alkalmazás átjárójának háttér-HTTP-beállításazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="635db-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="635db-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="635db-124">-DefaultProfile</span></span>
<span data-ttu-id="635db-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="635db-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="635db-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="635db-126">-HttpListener</span></span>
<span data-ttu-id="635db-127">Az alkalmazás-átjáró HTTP- hallgatóját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="635db-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="635db-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="635db-128">-HttpListenerId</span></span>
<span data-ttu-id="635db-129">Az alkalmazás átjárójának HTTP-hallgatóazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="635db-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="635db-130">-Name</span><span class="sxs-lookup"><span data-stu-id="635db-130">-Name</span></span>
<span data-ttu-id="635db-131">Annak a kéréstovábbító szabálynak a nevét adja meg, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="635db-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="635db-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="635db-132">-Priority</span></span>
<span data-ttu-id="635db-133">A szabály prioritása</span><span class="sxs-lookup"><span data-stu-id="635db-133">The priority of the rule</span></span>

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

### <span data-ttu-id="635db-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="635db-134">-RedirectConfiguration</span></span>
<span data-ttu-id="635db-135">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="635db-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="635db-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="635db-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="635db-137">A RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="635db-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="635db-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="635db-138">-RewriteRuleSet</span></span>
<span data-ttu-id="635db-139">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="635db-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="635db-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="635db-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="635db-141">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="635db-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="635db-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="635db-142">-RuleType</span></span>
<span data-ttu-id="635db-143">A kéréstovábbítja szabály típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="635db-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="635db-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="635db-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="635db-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="635db-145">-UrlPathMapId</span></span>
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

### <span data-ttu-id="635db-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="635db-146">CommonParameters</span></span>
<span data-ttu-id="635db-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="635db-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="635db-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="635db-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="635db-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="635db-149">INPUTS</span></span>

### <span data-ttu-id="635db-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="635db-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="635db-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="635db-151">OUTPUTS</span></span>

### <span data-ttu-id="635db-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="635db-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="635db-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="635db-153">NOTES</span></span>

## <span data-ttu-id="635db-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="635db-154">RELATED LINKS</span></span>

[<span data-ttu-id="635db-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="635db-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="635db-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="635db-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="635db-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="635db-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="635db-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="635db-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


