---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332634"
---
# <span data-ttu-id="1ec8a-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ec8a-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="1ec8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ec8a-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec8a-103">Url-útvonal-megfeleltetéseket tartalmazó tömböt hoz létre egy háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="1ec8a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ec8a-104">SYNTAX</span></span>

### <span data-ttu-id="1ec8a-105">BackendSetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ec8a-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ec8a-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec8a-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ec8a-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="1ec8a-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ec8a-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec8a-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ec8a-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ec8a-109">DESCRIPTION</span></span>
<span data-ttu-id="1ec8a-110">A **New-AzApplicationGatewayUrlPathMapConfig** parancsmag URL-útvonal-megfeleltetéseket tartalmazó tömböt hoz létre egy háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="1ec8a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ec8a-111">EXAMPLES</span></span>

### <span data-ttu-id="1ec8a-112">1. példa: URL-címleképezések tömbjének létrehozása háttérkiszolgáló-készlethez</span><span class="sxs-lookup"><span data-stu-id="1ec8a-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="1ec8a-113">Ezzel a paranccsal URL-címleképezéseket tartalmazó tömböt hoz létre egy háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="1ec8a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ec8a-114">PARAMETERS</span></span>

### <span data-ttu-id="1ec8a-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1ec8a-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="1ec8a-116">Megadja a háttércímkészlet alapértelmezett útválasztási értékét abban az esetben, ha a *pathRules paraméterben* megadott szabályok egyike sem felel meg.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="1ec8a-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1ec8a-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="1ec8a-118">A háttércímkészlet alapértelmezett azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="1ec8a-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1ec8a-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="1ec8a-120">Megadja az alapértelmezett HÁTTÉR HTTP-beállításokat, amelyek abban az esetben használhatók, ha a *pathRules paraméterben* megadott egyik szabály sem felel meg.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="1ec8a-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="1ec8a-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="1ec8a-122">A háttér-http-beállítások alapértelmezett azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="1ec8a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec8a-123">-DefaultProfile</span></span>
<span data-ttu-id="1ec8a-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ec8a-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ec8a-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="1ec8a-126">Application gateway default RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ec8a-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="1ec8a-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1ec8a-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="1ec8a-128">Az alapértelmezett RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="1ec8a-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="1ec8a-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ec8a-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="1ec8a-130">Application gateway default rewrite rule set</span><span class="sxs-lookup"><span data-stu-id="1ec8a-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="1ec8a-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="1ec8a-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="1ec8a-132">Az alkalmazás-átjáró alapértelmezett újraírási szabálykészletének azonosítója</span><span class="sxs-lookup"><span data-stu-id="1ec8a-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="1ec8a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="1ec8a-133">-Name</span></span>
<span data-ttu-id="1ec8a-134">A parancsmag által létrehozott URL-útvonal-leképezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1ec8a-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="1ec8a-135">-PathRules</span></span>
<span data-ttu-id="1ec8a-136">Megadja az elérési utakra vonatkozó szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="1ec8a-137">Ne feledje, hogy az elérési utak szabályai megkülönböztetik a sorrendet, és a megadott sorrendben vannak alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="1ec8a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec8a-138">CommonParameters</span></span>
<span data-ttu-id="1ec8a-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec8a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec8a-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ec8a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec8a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ec8a-141">INPUTS</span></span>

### <span data-ttu-id="1ec8a-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="1ec8a-142">None</span></span>

## <span data-ttu-id="1ec8a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ec8a-143">OUTPUTS</span></span>

### <span data-ttu-id="1ec8a-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="1ec8a-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="1ec8a-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ec8a-145">NOTES</span></span>

## <span data-ttu-id="1ec8a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ec8a-146">RELATED LINKS</span></span>

[<span data-ttu-id="1ec8a-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ec8a-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1ec8a-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ec8a-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1ec8a-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ec8a-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1ec8a-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1ec8a-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


