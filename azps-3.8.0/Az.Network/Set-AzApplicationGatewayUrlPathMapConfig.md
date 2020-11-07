---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847013"
---
# <span data-ttu-id="7512b-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7512b-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7512b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7512b-102">SYNOPSIS</span></span>
<span data-ttu-id="7512b-103">URL-elérésiút-megfeleltetések konfigurációját állítja be a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="7512b-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7512b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7512b-104">SYNTAX</span></span>

### <span data-ttu-id="7512b-105">BackendSetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7512b-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7512b-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7512b-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7512b-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="7512b-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7512b-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7512b-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7512b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7512b-109">DESCRIPTION</span></span>
<span data-ttu-id="7512b-110">A **set-AzApplicationGatewayUrlPathMapConfig** parancsmag a backend-kiszolgálók készletéből URL-elérési utakhoz való megfeleltetések konfigurációját állítja be.</span><span class="sxs-lookup"><span data-stu-id="7512b-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7512b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7512b-111">EXAMPLES</span></span>

### <span data-ttu-id="7512b-112">Példa 1: URL-elérési út megfeleltetésének frissítése</span><span class="sxs-lookup"><span data-stu-id="7512b-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="7512b-113">Az első parancs beolvassa a appGwName nevű alkalmazás-átjárót, és az eredményt az $appgw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7512b-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="7512b-114">A második parancs frissíti az map01 nevű URL-címet az alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="7512b-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="7512b-115">A harmadik parancs frissíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="7512b-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="7512b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7512b-116">PARAMETERS</span></span>

### <span data-ttu-id="7512b-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7512b-117">-ApplicationGateway</span></span>
<span data-ttu-id="7512b-118">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag az URL-elérési út megfeleltetését állítja be.</span><span class="sxs-lookup"><span data-stu-id="7512b-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="7512b-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7512b-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="7512b-120">Az alapértelmezett backend-címkészletet adja meg az átirányításhoz, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="7512b-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7512b-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7512b-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="7512b-122">Az alapértelmezett backend-címkészlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7512b-122">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7512b-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7512b-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="7512b-124">Az alapértelmezett backend-HTTP-beállításokat adja meg, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="7512b-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7512b-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="7512b-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="7512b-126">Az alapértelmezett backend-HTTP-beállítások AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7512b-126">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7512b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7512b-127">-DefaultProfile</span></span>
<span data-ttu-id="7512b-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7512b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7512b-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7512b-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="7512b-130">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7512b-130">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7512b-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7512b-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="7512b-132">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="7512b-132">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7512b-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7512b-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="7512b-134">Az alkalmazás-átjáró alapértelmezett átírási szabály beállítása</span><span class="sxs-lookup"><span data-stu-id="7512b-134">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7512b-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="7512b-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="7512b-136">Az alkalmazás-átjáró alapértelmezett átírási szabályának azonosítója</span><span class="sxs-lookup"><span data-stu-id="7512b-136">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7512b-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7512b-137">-Name</span></span>
<span data-ttu-id="7512b-138">Annak az URL-elérési útvonalnak a nevét adja meg, amelyben a parancsmag beállítja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="7512b-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="7512b-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="7512b-139">-PathRules</span></span>
<span data-ttu-id="7512b-140">Az elérésiút-szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7512b-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="7512b-141">Ügyeljen arra, hogy az elérésiút-szabályok a megrendelésük során bizalmasak legyenek, ezeket a program a megadott sorrendben alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="7512b-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7512b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7512b-142">CommonParameters</span></span>
<span data-ttu-id="7512b-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7512b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7512b-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7512b-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7512b-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7512b-145">INPUTS</span></span>

### <span data-ttu-id="7512b-146">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7512b-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7512b-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7512b-147">OUTPUTS</span></span>

### <span data-ttu-id="7512b-148">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7512b-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7512b-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7512b-149">NOTES</span></span>

## <span data-ttu-id="7512b-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7512b-150">RELATED LINKS</span></span>

[<span data-ttu-id="7512b-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7512b-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7512b-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7512b-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7512b-153">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7512b-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7512b-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7512b-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


