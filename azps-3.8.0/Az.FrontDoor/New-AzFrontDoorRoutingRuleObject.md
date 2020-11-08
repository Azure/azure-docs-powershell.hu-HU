---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 82ce25cec07855232d627f3ae912b00d4714f104
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013839"
---
# <span data-ttu-id="5c8df-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="5c8df-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="5c8df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c8df-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8df-103">PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="5c8df-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="5c8df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c8df-104">SYNTAX</span></span>

### <span data-ttu-id="5c8df-105">ByFieldsWithForwardingParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c8df-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c8df-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c8df-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c8df-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c8df-107">DESCRIPTION</span></span>
<span data-ttu-id="5c8df-108">PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="5c8df-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="5c8df-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5c8df-109">EXAMPLES</span></span>

### <span data-ttu-id="5c8df-110">Példa 1: PSRoutingRuleObject létrehozása előtérben történő létrehozáshoz továbbítási szabállyal</span><span class="sxs-lookup"><span data-stu-id="5c8df-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="5c8df-111">2. példa: PSRoutingRuleObject létrehozása az első ajtó létrehozása átirányítási szabállyal</span><span class="sxs-lookup"><span data-stu-id="5c8df-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

<span data-ttu-id="5c8df-112">PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="5c8df-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="5c8df-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c8df-113">PARAMETERS</span></span>

### <span data-ttu-id="5c8df-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="5c8df-114">-AcceptedProtocol</span></span>
<span data-ttu-id="5c8df-115">A szabályhoz egyeztetni kívánt protokol-sémák.</span><span class="sxs-lookup"><span data-stu-id="5c8df-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="5c8df-116">Az alapértelmezett érték {HTTPS, http}</span><span class="sxs-lookup"><span data-stu-id="5c8df-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="5c8df-117">-BackendPoolName</span></span>
<span data-ttu-id="5c8df-118">Annak az BackendPool az erőforrás-azonosítója, amelyre a szabály átvezet</span><span class="sxs-lookup"><span data-stu-id="5c8df-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="5c8df-119">-CustomForwardingPath</span></span>
<span data-ttu-id="5c8df-120">A szabály által kiválasztott erőforrás-elérési utak átírásához használt egyéni elérési út.</span><span class="sxs-lookup"><span data-stu-id="5c8df-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="5c8df-121">Hagyja üresen a bejövő elérési út használatát.</span><span class="sxs-lookup"><span data-stu-id="5c8df-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="5c8df-122">-CustomFragment</span></span>
<span data-ttu-id="5c8df-123">Az átirányítási URL-címhez hozzáadni kívánt részlet</span><span class="sxs-lookup"><span data-stu-id="5c8df-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="5c8df-124">A töredék a # után elkerülő URL-cím része.</span><span class="sxs-lookup"><span data-stu-id="5c8df-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="5c8df-125">Ne szerepeljen a #.</span><span class="sxs-lookup"><span data-stu-id="5c8df-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="5c8df-126">-CustomHost</span></span>
<span data-ttu-id="5c8df-127">Állomás átirányítását.</span><span class="sxs-lookup"><span data-stu-id="5c8df-127">Host to redirect.</span></span> <span data-ttu-id="5c8df-128">Hagyja üresen a bejövő állomás rendeltetési állomásként való használatát.</span><span class="sxs-lookup"><span data-stu-id="5c8df-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="5c8df-129">-CustomPath</span></span>
<span data-ttu-id="5c8df-130">Az átirányítás teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="5c8df-130">The full path to redirect.</span></span> <span data-ttu-id="5c8df-131">Az elérési út nem lehet üres, és a/értékkel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="5c8df-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="5c8df-132">Hagyja üresen a bejövő út rendeltetési útvonalként való használatát.</span><span class="sxs-lookup"><span data-stu-id="5c8df-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="5c8df-133">-CustomQueryString</span></span>
<span data-ttu-id="5c8df-134">Az átirányítási URL-címben elhelyezni kívánt lekérdezési karakterláncok halmaza.</span><span class="sxs-lookup"><span data-stu-id="5c8df-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="5c8df-135">Beállítás: az érték felülírhatja a meglévő lekérdezési karakterláncokat; hagyja üresen a bejövő lekérdezési karakterlánc megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="5c8df-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="5c8df-136">A lekérdezési karakterláncnak be kell lennie <key>=</span><span class="sxs-lookup"><span data-stu-id="5c8df-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="5c8df-137">formázása.</span><span class="sxs-lookup"><span data-stu-id="5c8df-137">format.</span></span> <span data-ttu-id="5c8df-138">Az első?</span><span class="sxs-lookup"><span data-stu-id="5c8df-138">The first ?</span></span> <span data-ttu-id="5c8df-139">a & automatikusan felveszi a program, hogy ne szerepeljenek rajtuk, de a lekérdezési karakterláncokat külön-külön kell kiválasztania a &.</span><span class="sxs-lookup"><span data-stu-id="5c8df-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c8df-140">-DefaultProfile</span></span>
<span data-ttu-id="5c8df-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c8df-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c8df-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="5c8df-142">-DynamicCompression</span></span>
<span data-ttu-id="5c8df-143">Engedélyezi-e a dinamikus tömörítést a gyorsítótárazott tartalmak esetén, ha a gyorsítótárazás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="5c8df-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="5c8df-144">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="5c8df-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="5c8df-145">-EnableCaching</span></span>
<span data-ttu-id="5c8df-146">Engedélyezi-e az útvonal gyorsítótárazását.</span><span class="sxs-lookup"><span data-stu-id="5c8df-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="5c8df-147">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="5c8df-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="5c8df-148">-EnabledState</span></span>
<span data-ttu-id="5c8df-149">Engedélyezi-e a szabály használatát.</span><span class="sxs-lookup"><span data-stu-id="5c8df-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="5c8df-150">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="5c8df-150">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="5c8df-151">-ForwardingProtocol</span></span>
<span data-ttu-id="5c8df-152">A protokoll ezt a szabályt fogja használni, amikor forgalmat továbbít a backends alapértelmezett érték MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="5c8df-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="5c8df-153">-FrontDoorName</span></span>
<span data-ttu-id="5c8df-154">Annak a bejárati ajtónak a neve, amelyhez ez a művelettervi szabály tartozik.</span><span class="sxs-lookup"><span data-stu-id="5c8df-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="5c8df-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="5c8df-155">-FrontendEndpointName</span></span>
<span data-ttu-id="5c8df-156">A szabállyal társított frontend-végpontok neve</span><span class="sxs-lookup"><span data-stu-id="5c8df-156">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-157">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5c8df-157">-Name</span></span>
<span data-ttu-id="5c8df-158">RoutingRule neve</span><span class="sxs-lookup"><span data-stu-id="5c8df-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="5c8df-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="5c8df-159">-PatternToMatch</span></span>
<span data-ttu-id="5c8df-160">A szabály útvonali mintái nem tartalmazhatnak semmilyen \* vagy csak az útvonal végét követő végeredményt.</span><span class="sxs-lookup"><span data-stu-id="5c8df-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="5c8df-161">Az alapértelmezett érték a/\*</span><span class="sxs-lookup"><span data-stu-id="5c8df-161">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="5c8df-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="5c8df-163">Az URL-lekérdezési fogalmak kezelése a gyorsítótár-kulcs alakításakor.</span><span class="sxs-lookup"><span data-stu-id="5c8df-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="5c8df-164">Az alapértelmezett érték a StripAll</span><span class="sxs-lookup"><span data-stu-id="5c8df-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="5c8df-165">-RedirectProtocol</span></span>
<span data-ttu-id="5c8df-166">Annak a helynek a protokollja, ahol a forgalmat átirányítják.</span><span class="sxs-lookup"><span data-stu-id="5c8df-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="5c8df-167">Az alapértelmezett érték a MatchRequest</span><span class="sxs-lookup"><span data-stu-id="5c8df-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="5c8df-168">-RedirectType</span></span>
<span data-ttu-id="5c8df-169">Az átirányítás típusa: a szabály a forgalom átirányításakor használatos.</span><span class="sxs-lookup"><span data-stu-id="5c8df-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="5c8df-170">Az alapértelmezett érték áthelyezve</span><span class="sxs-lookup"><span data-stu-id="5c8df-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8df-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c8df-171">-ResourceGroupName</span></span>
<span data-ttu-id="5c8df-172">Annak az erőforráscsoport-névnek a neve, amelyet a RoutingRule fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="5c8df-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="5c8df-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8df-173">CommonParameters</span></span>
<span data-ttu-id="5c8df-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c8df-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8df-175">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5c8df-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8df-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c8df-176">INPUTS</span></span>

### <span data-ttu-id="5c8df-177">Nincs</span><span class="sxs-lookup"><span data-stu-id="5c8df-177">None</span></span>

## <span data-ttu-id="5c8df-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c8df-178">OUTPUTS</span></span>

### <span data-ttu-id="5c8df-179">Microsoft. Azure. Command. FrontDoor. models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c8df-179">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="5c8df-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c8df-180">NOTES</span></span>

## <span data-ttu-id="5c8df-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c8df-181">RELATED LINKS</span></span>

<span data-ttu-id="5c8df-182">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="5c8df-182">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
