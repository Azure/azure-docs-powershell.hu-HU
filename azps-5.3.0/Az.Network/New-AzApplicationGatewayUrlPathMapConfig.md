---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466789"
---
# <span data-ttu-id="f6f1f-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f6f1f-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="f6f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f1f-103">Url-útvonal-megfeleltetéseket tartalmazó tömböt hoz létre egy háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f6f1f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6f1f-104">SYNTAX</span></span>

### <span data-ttu-id="f6f1f-105">BackendSetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6f1f-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6f1f-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6f1f-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6f1f-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="f6f1f-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6f1f-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6f1f-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6f1f-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6f1f-109">DESCRIPTION</span></span>
<span data-ttu-id="f6f1f-110">A **New-AzApplicationGatewayUrlPathMapConfig** parancsmag URL-útvonal-megfeleltetéseket tartalmazó tömböt hoz létre egy háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f6f1f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6f1f-111">EXAMPLES</span></span>

### <span data-ttu-id="f6f1f-112">1. példa: URL-címleképezések tömbjének létrehozása háttérkiszolgáló-készlethez</span><span class="sxs-lookup"><span data-stu-id="f6f1f-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="f6f1f-113">Ezzel a paranccsal URL-címleképezéseket tartalmazó tömböt hoz létre egy háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f6f1f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6f1f-114">PARAMETERS</span></span>

### <span data-ttu-id="f6f1f-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f6f1f-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="f6f1f-116">Megadja a háttércímkészlet alapértelmezett útválasztási értékét abban az esetben, ha a *pathRules paraméterben* megadott szabályok egyike sem felel meg.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="f6f1f-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f6f1f-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="f6f1f-118">A háttércímkészlet alapértelmezett azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="f6f1f-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f6f1f-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="f6f1f-120">Megadja az alapértelmezett HÁTTÉR HTTP-beállításokat, amelyek abban az esetben használhatók, ha a *pathRules paraméterben* megadott egyik szabály sem felel meg.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="f6f1f-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f6f1f-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="f6f1f-122">A háttér-http-beállítások alapértelmezett azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="f6f1f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f1f-123">-DefaultProfile</span></span>
<span data-ttu-id="f6f1f-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6f1f-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6f1f-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="f6f1f-126">Application gateway default RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6f1f-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="f6f1f-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f6f1f-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="f6f1f-128">Az alapértelmezett RedirectConfiguration alkalmazás-átjáró azonosítója</span><span class="sxs-lookup"><span data-stu-id="f6f1f-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="f6f1f-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f6f1f-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="f6f1f-130">Application gateway default rewrite rule set</span><span class="sxs-lookup"><span data-stu-id="f6f1f-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="f6f1f-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="f6f1f-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="f6f1f-132">Az alkalmazás-átjáró alapértelmezett újraírási szabálykészletének azonosítója</span><span class="sxs-lookup"><span data-stu-id="f6f1f-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="f6f1f-133">-Name</span><span class="sxs-lookup"><span data-stu-id="f6f1f-133">-Name</span></span>
<span data-ttu-id="f6f1f-134">A parancsmag által létrehozott URL-útvonal-leképezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f6f1f-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="f6f1f-135">-PathRules</span></span>
<span data-ttu-id="f6f1f-136">Megadja az elérési utakra vonatkozó szabályok listáját.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="f6f1f-137">Ne feledje, hogy az elérési utak szabályai megkülönböztetik a sorrendet, és a megadott sorrendben vannak alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="f6f1f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f1f-138">CommonParameters</span></span>
<span data-ttu-id="f6f1f-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f1f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f1f-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6f1f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f1f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6f1f-141">INPUTS</span></span>

### <span data-ttu-id="f6f1f-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="f6f1f-142">None</span></span>

## <span data-ttu-id="f6f1f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6f1f-143">OUTPUTS</span></span>

### <span data-ttu-id="f6f1f-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="f6f1f-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="f6f1f-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6f1f-145">NOTES</span></span>

## <span data-ttu-id="f6f1f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6f1f-146">RELATED LINKS</span></span>

[<span data-ttu-id="f6f1f-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f6f1f-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f6f1f-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f6f1f-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f6f1f-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f6f1f-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f6f1f-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f6f1f-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


