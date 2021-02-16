---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95f3e4b11d9253a232fc119faf39a4fa51fab60a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202884"
---
# <span data-ttu-id="da515-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da515-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="da515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da515-102">SYNOPSIS</span></span>
<span data-ttu-id="da515-103">Kéréstovábbító szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="da515-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="da515-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da515-104">SYNTAX</span></span>

### <span data-ttu-id="da515-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="da515-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da515-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="da515-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da515-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da515-107">DESCRIPTION</span></span>
<span data-ttu-id="da515-108">**Az Add-AzApplicationGatewayRequestRoutingRule** parancsmag létrehoz egy kéréstovábbítási szabályt egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="da515-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="da515-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da515-109">EXAMPLES</span></span>

### <span data-ttu-id="da515-110">1. példa: Kéréstovábbító szabály létrehozása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="da515-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="da515-111">Ez a parancs létrehoz egy Szabály01 nevű egyszerű kéréstovábbítási szabályt, és az eredményt a következő nevű változóban $Rule.</span><span class="sxs-lookup"><span data-stu-id="da515-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="da515-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da515-112">PARAMETERS</span></span>

### <span data-ttu-id="da515-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="da515-113">-BackendAddressPool</span></span>
<span data-ttu-id="da515-114">Megadja a háttércímkészletet objektumként ahhoz, hogy létrejöjjön a kérés útválasztási szabálya.</span><span class="sxs-lookup"><span data-stu-id="da515-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="da515-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="da515-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="da515-116">A létrehozni kért útválasztási szabály háttércímkészlet-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="da515-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="da515-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="da515-117">-BackendHttpSettings</span></span>
<span data-ttu-id="da515-118">Megadja a háttér-HTTP-beállításokat objektumként ahhoz, hogy a kéréstovábbirányítási szabály létrejöjjön.</span><span class="sxs-lookup"><span data-stu-id="da515-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="da515-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="da515-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="da515-120">A létrehozni kért útválasztási szabály háttér-HTTP-beállításazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="da515-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="da515-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da515-121">-DefaultProfile</span></span>
<span data-ttu-id="da515-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da515-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da515-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="da515-123">-HttpListener</span></span>
<span data-ttu-id="da515-124">Megadja a létrehozni szükséges kéréstovábbító szabály háttér-HTTP- hallgatóját.</span><span class="sxs-lookup"><span data-stu-id="da515-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="da515-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="da515-125">-HttpListenerId</span></span>
<span data-ttu-id="da515-126">Megadja a létrehozható kéréstovábbító szabály háttér-HTTP- hallgatójának azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="da515-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="da515-127">-Name</span><span class="sxs-lookup"><span data-stu-id="da515-127">-Name</span></span>
<span data-ttu-id="da515-128">A parancsmag által létrehozott kérés-útválasztási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da515-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="da515-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="da515-129">-Priority</span></span>
<span data-ttu-id="da515-130">A szabály prioritása</span><span class="sxs-lookup"><span data-stu-id="da515-130">The priority of the rule</span></span>

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

### <span data-ttu-id="da515-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="da515-131">-RedirectConfiguration</span></span>
<span data-ttu-id="da515-132">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="da515-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="da515-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="da515-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="da515-134">A RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="da515-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="da515-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da515-135">-RewriteRuleSet</span></span>
<span data-ttu-id="da515-136">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da515-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="da515-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="da515-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="da515-138">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="da515-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="da515-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="da515-139">-RuleType</span></span>
<span data-ttu-id="da515-140">A kéréstovábbítja szabály típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="da515-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="da515-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="da515-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="da515-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="da515-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="da515-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da515-143">CommonParameters</span></span>
<span data-ttu-id="da515-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da515-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da515-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da515-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da515-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da515-146">INPUTS</span></span>

### <span data-ttu-id="da515-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="da515-147">None</span></span>

## <span data-ttu-id="da515-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da515-148">OUTPUTS</span></span>

### <span data-ttu-id="da515-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da515-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="da515-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da515-150">NOTES</span></span>

## <span data-ttu-id="da515-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da515-151">RELATED LINKS</span></span>

[<span data-ttu-id="da515-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da515-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="da515-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da515-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="da515-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da515-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="da515-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da515-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


