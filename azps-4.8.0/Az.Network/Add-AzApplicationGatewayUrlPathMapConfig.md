---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184908"
---
# <span data-ttu-id="7567b-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7567b-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7567b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7567b-102">SYNOPSIS</span></span>
<span data-ttu-id="7567b-103">URL-elérésiút-megfeleltetések tömbjét egészíti ki a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="7567b-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7567b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7567b-104">SYNTAX</span></span>

### <span data-ttu-id="7567b-105">BackendSetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7567b-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7567b-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7567b-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7567b-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="7567b-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7567b-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7567b-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7567b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7567b-109">DESCRIPTION</span></span>
<span data-ttu-id="7567b-110">Az **Add-AzApplicationGatewayUrlPathMapConfig** parancsmag egy URL-elérési út típusú megfeleltetést ad vissza egy back end Server-készlethez.</span><span class="sxs-lookup"><span data-stu-id="7567b-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="7567b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7567b-111">EXAMPLES</span></span>

### <span data-ttu-id="7567b-112">Példa 1: URL-elérési út hozzárendelése egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7567b-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="7567b-113">Az első parancs beolvassa a appGwName nevű alkalmazás-átjárót, és $appgw változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="7567b-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="7567b-114">A második parancs beolvassa a backend-címkészlet értékét, és a $pool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7567b-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="7567b-115">A harmadik parancs a backend http-beállításait kapja, és $poolSettings változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7567b-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="7567b-116">A negyedik parancs a rule01 nevű új elérésiút-szabály konfigurációját hozza létre, és $pathRule változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7567b-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="7567b-117">Az ötödik parancs hozzáadja az URL-cím elérési útját a url01 nevű konfigurációhoz az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7567b-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="7567b-118">A hatodik parancs frissíti az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="7567b-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="7567b-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7567b-119">PARAMETERS</span></span>

### <span data-ttu-id="7567b-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7567b-120">-ApplicationGateway</span></span>
<span data-ttu-id="7567b-121">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag URL-elérésiút-megfeleltetést ad.</span><span class="sxs-lookup"><span data-stu-id="7567b-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="7567b-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7567b-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="7567b-123">Az alapértelmezett backend-címkészletet adja meg az átirányításhoz, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="7567b-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="7567b-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7567b-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="7567b-125">Az alapértelmezett backend-címkészlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7567b-125">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="7567b-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7567b-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="7567b-127">Az alapértelmezett backend-HTTP-beállításokat adja meg, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="7567b-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="7567b-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="7567b-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="7567b-129">Az alapértelmezett backend-HTTP-beállítások AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7567b-129">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="7567b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7567b-130">-DefaultProfile</span></span>
<span data-ttu-id="7567b-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7567b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7567b-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7567b-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="7567b-133">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7567b-133">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="7567b-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7567b-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="7567b-135">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="7567b-135">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="7567b-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7567b-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="7567b-137">Az alkalmazás-átjáró alapértelmezett átírási szabály beállítása</span><span class="sxs-lookup"><span data-stu-id="7567b-137">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="7567b-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="7567b-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="7567b-139">Az alkalmazás-átjáró alapértelmezett átírási szabályának azonosítója</span><span class="sxs-lookup"><span data-stu-id="7567b-139">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="7567b-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7567b-140">-Name</span></span>
<span data-ttu-id="7567b-141">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend Server-készlethez ad.</span><span class="sxs-lookup"><span data-stu-id="7567b-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="7567b-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="7567b-142">-PathRules</span></span>
<span data-ttu-id="7567b-143">Az elérésiút-szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7567b-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="7567b-144">Az elérésiút-szabályok a megkülönböztetett sorrendet használják, ezek a sorrendjük szerint vannak alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="7567b-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="7567b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7567b-145">CommonParameters</span></span>
<span data-ttu-id="7567b-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7567b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7567b-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7567b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7567b-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7567b-148">INPUTS</span></span>

### <span data-ttu-id="7567b-149">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7567b-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7567b-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7567b-150">OUTPUTS</span></span>

### <span data-ttu-id="7567b-151">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7567b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7567b-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7567b-152">NOTES</span></span>

## <span data-ttu-id="7567b-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7567b-153">RELATED LINKS</span></span>

[<span data-ttu-id="7567b-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7567b-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7567b-155">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7567b-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7567b-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7567b-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7567b-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7567b-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


