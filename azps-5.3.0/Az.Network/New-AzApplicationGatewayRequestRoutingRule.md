---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95f3e4b11d9253a232fc119faf39a4fa51fab60a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379383"
---
# <span data-ttu-id="b6201-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6201-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b6201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6201-102">SYNOPSIS</span></span>
<span data-ttu-id="b6201-103">Kéréstovábbító szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b6201-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="b6201-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b6201-104">SYNTAX</span></span>

### <span data-ttu-id="b6201-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6201-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6201-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b6201-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6201-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b6201-107">DESCRIPTION</span></span>
<span data-ttu-id="b6201-108">**Az Add-AzApplicationGatewayRequestRoutingRule** parancsmag létrehoz egy kéréstovábbítási szabályt egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b6201-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="b6201-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b6201-109">EXAMPLES</span></span>

### <span data-ttu-id="b6201-110">1. példa: Kéréstovábbító szabály létrehozása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="b6201-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="b6201-111">Ez a parancs létrehoz egy Szabály01 nevű egyszerű kéréstovábbítási szabályt, és az eredményt a következő nevű változóban $Rule.</span><span class="sxs-lookup"><span data-stu-id="b6201-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="b6201-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6201-112">PARAMETERS</span></span>

### <span data-ttu-id="b6201-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b6201-113">-BackendAddressPool</span></span>
<span data-ttu-id="b6201-114">Megadja a háttércímkészletet objektumként ahhoz, hogy létrejöjjön a kérés útválasztási szabálya.</span><span class="sxs-lookup"><span data-stu-id="b6201-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="b6201-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b6201-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="b6201-116">A létrehozni kért útválasztási szabály háttércímkészlet-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6201-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="b6201-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b6201-117">-BackendHttpSettings</span></span>
<span data-ttu-id="b6201-118">Megadja a háttér-HTTP-beállításokat objektumként ahhoz, hogy a kéréstovábbirányítási szabály létrejöjjön.</span><span class="sxs-lookup"><span data-stu-id="b6201-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="b6201-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="b6201-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="b6201-120">A létrehozni kért útválasztási szabály háttér-HTTP-beállításazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6201-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="b6201-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6201-121">-DefaultProfile</span></span>
<span data-ttu-id="b6201-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6201-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6201-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="b6201-123">-HttpListener</span></span>
<span data-ttu-id="b6201-124">Megadja a létrehozni szükséges kéréstovábbító szabály háttér-HTTP- hallgatóját.</span><span class="sxs-lookup"><span data-stu-id="b6201-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="b6201-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="b6201-125">-HttpListenerId</span></span>
<span data-ttu-id="b6201-126">Megadja a létrehozható kéréstovábbító szabály háttér-HTTP-jának listener-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="b6201-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="b6201-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b6201-127">-Name</span></span>
<span data-ttu-id="b6201-128">A parancsmag által létrehozott kéréstovábbítja szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6201-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b6201-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="b6201-129">-Priority</span></span>
<span data-ttu-id="b6201-130">A szabály prioritása</span><span class="sxs-lookup"><span data-stu-id="b6201-130">The priority of the rule</span></span>

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

### <span data-ttu-id="b6201-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6201-131">-RedirectConfiguration</span></span>
<span data-ttu-id="b6201-132">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6201-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="b6201-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b6201-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="b6201-134">A RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="b6201-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="b6201-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6201-135">-RewriteRuleSet</span></span>
<span data-ttu-id="b6201-136">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6201-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b6201-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="b6201-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="b6201-138">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="b6201-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b6201-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="b6201-139">-RuleType</span></span>
<span data-ttu-id="b6201-140">A kéréstovábbítja szabály típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b6201-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="b6201-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="b6201-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="b6201-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="b6201-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="b6201-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6201-143">CommonParameters</span></span>
<span data-ttu-id="b6201-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6201-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6201-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6201-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6201-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6201-146">INPUTS</span></span>

### <span data-ttu-id="b6201-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="b6201-147">None</span></span>

## <span data-ttu-id="b6201-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6201-148">OUTPUTS</span></span>

### <span data-ttu-id="b6201-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6201-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b6201-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b6201-150">NOTES</span></span>

## <span data-ttu-id="b6201-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6201-151">RELATED LINKS</span></span>

[<span data-ttu-id="b6201-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6201-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b6201-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6201-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b6201-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6201-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b6201-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b6201-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


