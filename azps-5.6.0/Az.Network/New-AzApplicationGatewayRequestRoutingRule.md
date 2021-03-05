---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 53963e7672881255cf23df99e53a1471c3c42250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010326"
---
# <span data-ttu-id="f8d8d-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f8d8d-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f8d8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d8d-103">Kéréstovábbító szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="f8d8d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f8d8d-104">SYNTAX</span></span>

### <span data-ttu-id="f8d8d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f8d8d-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8d8d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f8d8d-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8d8d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f8d8d-107">DESCRIPTION</span></span>
<span data-ttu-id="f8d8d-108">**Az Add-AzApplicationGatewayRequestRoutingRule** parancsmag létrehoz egy kéréstovábbítási szabályt egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="f8d8d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f8d8d-109">EXAMPLES</span></span>

### <span data-ttu-id="f8d8d-110">1. példa: Kéréstovábbító szabály létrehozása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="f8d8d-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="f8d8d-111">Ez a parancs létrehoz egy Szabály01 nevű egyszerű kéréstovábbítási szabályt, és az eredményt a Következő nevű változóban $Rule.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="f8d8d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8d8d-112">PARAMETERS</span></span>

### <span data-ttu-id="f8d8d-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f8d8d-113">-BackendAddressPool</span></span>
<span data-ttu-id="f8d8d-114">Megadja a háttércímkészletet objektumként ahhoz, hogy létrejöjjön a kérés útválasztási szabálya.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="f8d8d-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f8d8d-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="f8d8d-116">A létrehozni kért útválasztási szabály háttércímkészlet-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="f8d8d-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f8d8d-117">-BackendHttpSettings</span></span>
<span data-ttu-id="f8d8d-118">Megadja a háttér-HTTP-beállításokat objektumként ahhoz, hogy a kéréstovábbirányítási szabály létrejöjjön.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="f8d8d-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f8d8d-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="f8d8d-120">A létrehozni kért útválasztási szabály háttér-HTTP-beállításazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="f8d8d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d8d-121">-DefaultProfile</span></span>
<span data-ttu-id="f8d8d-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8d8d-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f8d8d-123">-HttpListener</span></span>
<span data-ttu-id="f8d8d-124">Megadja a létrehozni szükséges kéréstovábbító szabály háttér-HTTP- hallgatóját.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="f8d8d-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="f8d8d-125">-HttpListenerId</span></span>
<span data-ttu-id="f8d8d-126">Megadja a létrehozható kéréstovábbító szabály háttér-HTTP-jának listener-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="f8d8d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f8d8d-127">-Name</span></span>
<span data-ttu-id="f8d8d-128">A parancsmag által létrehozott kérés-útválasztási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f8d8d-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="f8d8d-129">-Priority</span></span>
<span data-ttu-id="f8d8d-130">A szabály prioritása</span><span class="sxs-lookup"><span data-stu-id="f8d8d-130">The priority of the rule</span></span>

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

### <span data-ttu-id="f8d8d-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8d8d-131">-RedirectConfiguration</span></span>
<span data-ttu-id="f8d8d-132">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8d8d-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f8d8d-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f8d8d-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="f8d8d-134">A RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="f8d8d-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f8d8d-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8d8d-135">-RewriteRuleSet</span></span>
<span data-ttu-id="f8d8d-136">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8d8d-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f8d8d-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="f8d8d-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="f8d8d-138">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="f8d8d-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f8d8d-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="f8d8d-139">-RuleType</span></span>
<span data-ttu-id="f8d8d-140">A kéréstovábbítja szabály típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="f8d8d-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="f8d8d-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="f8d8d-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="f8d8d-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="f8d8d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d8d-143">CommonParameters</span></span>
<span data-ttu-id="f8d8d-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8d8d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d8d-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8d8d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d8d-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8d8d-146">INPUTS</span></span>

### <span data-ttu-id="f8d8d-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="f8d8d-147">None</span></span>

## <span data-ttu-id="f8d8d-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8d8d-148">OUTPUTS</span></span>

### <span data-ttu-id="f8d8d-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f8d8d-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f8d8d-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f8d8d-150">NOTES</span></span>

## <span data-ttu-id="f8d8d-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8d8d-151">RELATED LINKS</span></span>

[<span data-ttu-id="f8d8d-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f8d8d-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f8d8d-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f8d8d-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f8d8d-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f8d8d-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f8d8d-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f8d8d-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


