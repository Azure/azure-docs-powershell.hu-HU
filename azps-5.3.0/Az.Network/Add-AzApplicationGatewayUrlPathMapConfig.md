---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480017"
---
# <span data-ttu-id="9f902-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9f902-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="9f902-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f902-102">SYNOPSIS</span></span>
<span data-ttu-id="9f902-103">URL-címleképezéseket tartalmazó tömböt ad egy háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="9f902-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9f902-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f902-104">SYNTAX</span></span>

### <span data-ttu-id="9f902-105">BackendSetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f902-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f902-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f902-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f902-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="9f902-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f902-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f902-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f902-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f902-109">DESCRIPTION</span></span>
<span data-ttu-id="9f902-110">Az **Add-AzApplicationGatewayUrlPathMapConfig** parancsmag url-útvonal-megfeleltetések tömbjét adja a háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="9f902-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="9f902-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f902-111">EXAMPLES</span></span>

### <span data-ttu-id="9f902-112">1. példa: URL-útvonal-megfeleltetés hozzáadása egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="9f902-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="9f902-113">Az első parancs egy appGwName nevű alkalmazás-átjárót kap, és egy $appgw tárolja.</span><span class="sxs-lookup"><span data-stu-id="9f902-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="9f902-114">A második parancs a háttércímkészletet kapja meg, és egy $pool tárolja.</span><span class="sxs-lookup"><span data-stu-id="9f902-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="9f902-115">A harmadik parancs háttér-http-beállításokat kap, és egy $poolSettings tárolja.</span><span class="sxs-lookup"><span data-stu-id="9f902-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="9f902-116">A negyedik parancs létrehozza a rule01 nevű új útvonalszabály-konfigurációt, és azt egy $pathRule tárolja.</span><span class="sxs-lookup"><span data-stu-id="9f902-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="9f902-117">Az ötödik parancs hozzáadja az URL-útvonal-megfeleltetés url01 nevű konfigurációját az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="9f902-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="9f902-118">A hatodik parancs frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="9f902-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="9f902-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f902-119">PARAMETERS</span></span>

### <span data-ttu-id="9f902-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f902-120">-ApplicationGateway</span></span>
<span data-ttu-id="9f902-121">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag URL-útvonal-leképezés-konfigurációt ad.</span><span class="sxs-lookup"><span data-stu-id="9f902-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="9f902-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9f902-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="9f902-123">Megadja a háttércímkészlet alapértelmezett útválasztási értékét abban az esetben, ha a *pathRules paraméterben* megadott szabályok egyike sem felel meg.</span><span class="sxs-lookup"><span data-stu-id="9f902-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="9f902-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9f902-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="9f902-125">A háttércímkészlet alapértelmezett azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f902-125">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="9f902-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9f902-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="9f902-127">Megadja az alapértelmezett HÁTTÉR HTTP-beállításokat, amelyek abban az esetben használhatók, ha a *pathRules paraméterben* megadott egyik szabály sem felel meg.</span><span class="sxs-lookup"><span data-stu-id="9f902-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="9f902-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="9f902-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="9f902-129">A háttér-http-beállítások alapértelmezett azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f902-129">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="9f902-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f902-130">-DefaultProfile</span></span>
<span data-ttu-id="9f902-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f902-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f902-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f902-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="9f902-133">Application gateway default RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f902-133">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="9f902-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9f902-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="9f902-135">Az alapértelmezett RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="9f902-135">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="9f902-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9f902-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="9f902-137">Application gateway default rewrite rule set</span><span class="sxs-lookup"><span data-stu-id="9f902-137">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="9f902-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="9f902-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="9f902-139">Az alkalmazás-átjáró alapértelmezett újraírási szabálykészletének azonosítója</span><span class="sxs-lookup"><span data-stu-id="9f902-139">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="9f902-140">-Name</span><span class="sxs-lookup"><span data-stu-id="9f902-140">-Name</span></span>
<span data-ttu-id="9f902-141">Megadja azt az URL-útvonal-leképezésnevet, amely a parancsmag hozzáadható a háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="9f902-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="9f902-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="9f902-142">-PathRules</span></span>
<span data-ttu-id="9f902-143">Megadja az elérési utakra vonatkozó szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="9f902-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="9f902-144">Az elérési utak szabályai megkülönböztetik a sorrendet, és a megadott sorrendben alkalmazzák őket.</span><span class="sxs-lookup"><span data-stu-id="9f902-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="9f902-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f902-145">CommonParameters</span></span>
<span data-ttu-id="9f902-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f902-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f902-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f902-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f902-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f902-148">INPUTS</span></span>

### <span data-ttu-id="9f902-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f902-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f902-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f902-150">OUTPUTS</span></span>

### <span data-ttu-id="9f902-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f902-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f902-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f902-152">NOTES</span></span>

## <span data-ttu-id="9f902-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f902-153">RELATED LINKS</span></span>

[<span data-ttu-id="9f902-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9f902-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9f902-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9f902-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9f902-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9f902-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9f902-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9f902-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


