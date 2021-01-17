---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371306"
---
# <span data-ttu-id="986c2-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="986c2-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="986c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="986c2-102">SYNOPSIS</span></span>
<span data-ttu-id="986c2-103">A háttérkiszolgáló-készlet URL-útvonal-megfeleltetési tömbjének konfigurációját állítja be.</span><span class="sxs-lookup"><span data-stu-id="986c2-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="986c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="986c2-104">SYNTAX</span></span>

### <span data-ttu-id="986c2-105">BackendSetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="986c2-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="986c2-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="986c2-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="986c2-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="986c2-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="986c2-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="986c2-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="986c2-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="986c2-109">DESCRIPTION</span></span>
<span data-ttu-id="986c2-110">A **Set-AzApplicationGatewayUrlPathMapConfig** parancsmagkészlet beállítja a háttérkiszolgáló-készlethez való URL-útvonalleképezések tömbjének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="986c2-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="986c2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="986c2-111">EXAMPLES</span></span>

### <span data-ttu-id="986c2-112">1. példa: URL-cím megfeleltetésének frissítése</span><span class="sxs-lookup"><span data-stu-id="986c2-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="986c2-113">Az első parancs az appGwName nevű alkalmazás-átjárót kapja meg, és az eredményt a $appgw tárolja.</span><span class="sxs-lookup"><span data-stu-id="986c2-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="986c2-114">A második parancs frissíti a map01 nevű URL-útvonal-megfeleltetést az alkalmazás átjáróban.</span><span class="sxs-lookup"><span data-stu-id="986c2-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="986c2-115">A harmadik parancs frissíti az alkalmazás átjáróját.</span><span class="sxs-lookup"><span data-stu-id="986c2-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="986c2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="986c2-116">PARAMETERS</span></span>

### <span data-ttu-id="986c2-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="986c2-117">-ApplicationGateway</span></span>
<span data-ttu-id="986c2-118">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag URL-útvonal-leképezés-konfigurációt állít be.</span><span class="sxs-lookup"><span data-stu-id="986c2-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="986c2-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="986c2-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="986c2-120">Megadja a háttércímkészlet alapértelmezett útválasztási értékét abban az esetben, ha a *pathRules paraméterben* megadott szabályok egyike sem felel meg.</span><span class="sxs-lookup"><span data-stu-id="986c2-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="986c2-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="986c2-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="986c2-122">A háttércímkészlet alapértelmezett azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="986c2-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="986c2-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="986c2-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="986c2-124">Megadja az alapértelmezett HÁTTÉR HTTP-beállításokat, amelyek abban az esetben használhatók, ha a *pathRules paraméterben* megadott egyik szabály sem felel meg.</span><span class="sxs-lookup"><span data-stu-id="986c2-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="986c2-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="986c2-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="986c2-126">A háttér-http-beállítások alapértelmezett azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="986c2-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="986c2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="986c2-127">-DefaultProfile</span></span>
<span data-ttu-id="986c2-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="986c2-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="986c2-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="986c2-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="986c2-130">Application gateway default RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="986c2-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="986c2-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="986c2-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="986c2-132">Az alapértelmezett RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="986c2-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="986c2-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="986c2-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="986c2-134">Application gateway default rewrite rule set</span><span class="sxs-lookup"><span data-stu-id="986c2-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="986c2-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="986c2-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="986c2-136">Az alkalmazás-átjáró alapértelmezett újraírási szabálykészletének azonosítója</span><span class="sxs-lookup"><span data-stu-id="986c2-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="986c2-137">-Name</span><span class="sxs-lookup"><span data-stu-id="986c2-137">-Name</span></span>
<span data-ttu-id="986c2-138">Megadja annak az URL-útvonal-leképezésnek a nevét, amelyhez ez a parancsmag beállítja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="986c2-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="986c2-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="986c2-139">-PathRules</span></span>
<span data-ttu-id="986c2-140">Megadja az elérési utakra vonatkozó szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="986c2-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="986c2-141">Ne feledje, hogy az elérési utak szabályai megkülönböztetik a sorrendet, és a megadott sorrendben vannak alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="986c2-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="986c2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986c2-142">CommonParameters</span></span>
<span data-ttu-id="986c2-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="986c2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986c2-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="986c2-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986c2-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="986c2-145">INPUTS</span></span>

### <span data-ttu-id="986c2-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="986c2-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="986c2-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="986c2-147">OUTPUTS</span></span>

### <span data-ttu-id="986c2-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="986c2-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="986c2-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="986c2-149">NOTES</span></span>

## <span data-ttu-id="986c2-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="986c2-150">RELATED LINKS</span></span>

[<span data-ttu-id="986c2-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="986c2-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="986c2-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="986c2-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="986c2-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="986c2-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="986c2-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="986c2-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


