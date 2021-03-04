---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cc2a30e5a5633dcda345184bef121befe710ad8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918682"
---
# <span data-ttu-id="a8c57-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8c57-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="a8c57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8c57-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c57-103">A háttérkiszolgáló-készlet URL-útvonal-megfeleltetési tömbjének konfigurációját állítja be.</span><span class="sxs-lookup"><span data-stu-id="a8c57-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a8c57-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8c57-104">SYNTAX</span></span>

### <span data-ttu-id="a8c57-105">BackendSetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8c57-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8c57-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8c57-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8c57-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="a8c57-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8c57-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8c57-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8c57-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8c57-109">DESCRIPTION</span></span>
<span data-ttu-id="a8c57-110">A **Set-AzApplicationGatewayUrlPathMapConfig** parancsmag beállítja egy háttérkiszolgáló-készlet URL-útvonal-megfeleltetések tömbjének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="a8c57-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a8c57-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8c57-111">EXAMPLES</span></span>

### <span data-ttu-id="a8c57-112">1. példa: URL-cím megfeleltetésének frissítése</span><span class="sxs-lookup"><span data-stu-id="a8c57-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="a8c57-113">Az első parancs az appGwName nevű alkalmazás-átjárót kapja meg, és az eredményt a $appgw tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8c57-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="a8c57-114">A második parancs frissíti a map01 nevű URL-útvonal-megfeleltetést az alkalmazás átjáróban.</span><span class="sxs-lookup"><span data-stu-id="a8c57-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="a8c57-115">A harmadik parancs frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="a8c57-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="a8c57-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8c57-116">PARAMETERS</span></span>

### <span data-ttu-id="a8c57-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8c57-117">-ApplicationGateway</span></span>
<span data-ttu-id="a8c57-118">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag URL-útvonal-leképezés-konfigurációt állít be.</span><span class="sxs-lookup"><span data-stu-id="a8c57-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="a8c57-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8c57-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="a8c57-120">Megadja a háttércímkészlet alapértelmezett útválasztási értékét abban az esetben, ha a *pathRules paraméterben* megadott szabályok egyike sem felel meg.</span><span class="sxs-lookup"><span data-stu-id="a8c57-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="a8c57-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a8c57-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="a8c57-122">A háttércímkészlet alapértelmezett azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8c57-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="a8c57-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a8c57-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="a8c57-124">Megadja az alapértelmezett HÁTTÉR HTTP-beállításokat, amelyek abban az esetben használhatók, ha a *pathRules paraméterben* megadott egyik szabály sem felel meg.</span><span class="sxs-lookup"><span data-stu-id="a8c57-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="a8c57-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="a8c57-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="a8c57-126">A háttér-http-beállítások alapértelmezett azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8c57-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="a8c57-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c57-127">-DefaultProfile</span></span>
<span data-ttu-id="a8c57-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8c57-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8c57-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8c57-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="a8c57-130">Application gateway default RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8c57-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="a8c57-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a8c57-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="a8c57-132">Az alapértelmezett RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="a8c57-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="a8c57-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a8c57-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="a8c57-134">Application gateway default rewrite rule set</span><span class="sxs-lookup"><span data-stu-id="a8c57-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="a8c57-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="a8c57-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="a8c57-136">Az alkalmazás-átjáró alapértelmezett újraírási szabálykészletének azonosítója</span><span class="sxs-lookup"><span data-stu-id="a8c57-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="a8c57-137">-Name</span><span class="sxs-lookup"><span data-stu-id="a8c57-137">-Name</span></span>
<span data-ttu-id="a8c57-138">Megadja annak az URL-útvonal-leképezésnek a nevét, amelyhez a parancsmag beállítja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a8c57-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="a8c57-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="a8c57-139">-PathRules</span></span>
<span data-ttu-id="a8c57-140">Megadja az elérési utakra vonatkozó szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="a8c57-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="a8c57-141">Ne feledje, hogy az elérési utak szabályai megkülönböztetik a sorrendet, és a megadott sorrendben vannak alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="a8c57-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="a8c57-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c57-142">CommonParameters</span></span>
<span data-ttu-id="a8c57-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c57-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c57-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c57-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c57-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8c57-145">INPUTS</span></span>

### <span data-ttu-id="a8c57-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8c57-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a8c57-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8c57-147">OUTPUTS</span></span>

### <span data-ttu-id="a8c57-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8c57-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a8c57-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8c57-149">NOTES</span></span>

## <span data-ttu-id="a8c57-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8c57-150">RELATED LINKS</span></span>

[<span data-ttu-id="a8c57-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8c57-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a8c57-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8c57-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a8c57-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8c57-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a8c57-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8c57-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


