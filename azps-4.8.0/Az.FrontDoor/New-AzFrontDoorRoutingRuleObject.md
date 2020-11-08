---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183570"
---
# <span data-ttu-id="2f540-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="2f540-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="2f540-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f540-102">SYNOPSIS</span></span>
<span data-ttu-id="2f540-103">PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="2f540-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="2f540-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f540-104">SYNTAX</span></span>

### <span data-ttu-id="2f540-105">ByFieldsWithForwardingParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f540-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f540-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f540-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f540-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f540-107">DESCRIPTION</span></span>
<span data-ttu-id="2f540-108">PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="2f540-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="2f540-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2f540-109">EXAMPLES</span></span>

### <span data-ttu-id="2f540-110">Példa 1: PSRoutingRuleObject létrehozása előtérben történő létrehozáshoz továbbítási szabállyal</span><span class="sxs-lookup"><span data-stu-id="2f540-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
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

### <span data-ttu-id="2f540-111">2. példa: PSRoutingRuleObject létrehozása az első ajtó létrehozása átirányítási szabállyal</span><span class="sxs-lookup"><span data-stu-id="2f540-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
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

<span data-ttu-id="2f540-112">PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="2f540-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="2f540-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f540-113">PARAMETERS</span></span>

### <span data-ttu-id="2f540-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="2f540-114">-AcceptedProtocol</span></span>
<span data-ttu-id="2f540-115">A szabályhoz egyeztetni kívánt protokol-sémák.</span><span class="sxs-lookup"><span data-stu-id="2f540-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="2f540-116">Az alapértelmezett érték {HTTPS, http}</span><span class="sxs-lookup"><span data-stu-id="2f540-116">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="2f540-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="2f540-117">-BackendPoolName</span></span>
<span data-ttu-id="2f540-118">Annak az BackendPool az erőforrás-azonosítója, amelyre a szabály átvezet</span><span class="sxs-lookup"><span data-stu-id="2f540-118">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="2f540-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="2f540-119">-CustomForwardingPath</span></span>
<span data-ttu-id="2f540-120">A szabály által kiválasztott erőforrás-elérési utak átírásához használt egyéni elérési út.</span><span class="sxs-lookup"><span data-stu-id="2f540-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="2f540-121">Hagyja üresen a bejövő elérési út használatát.</span><span class="sxs-lookup"><span data-stu-id="2f540-121">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="2f540-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="2f540-122">-CustomFragment</span></span>
<span data-ttu-id="2f540-123">Az átirányítási URL-címhez hozzáadni kívánt részlet</span><span class="sxs-lookup"><span data-stu-id="2f540-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="2f540-124">A töredék a # után elkerülő URL-cím része.</span><span class="sxs-lookup"><span data-stu-id="2f540-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="2f540-125">Ne szerepeljen a #.</span><span class="sxs-lookup"><span data-stu-id="2f540-125">Do not include the #.</span></span>

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

### <span data-ttu-id="2f540-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="2f540-126">-CustomHost</span></span>
<span data-ttu-id="2f540-127">Állomás átirányítását.</span><span class="sxs-lookup"><span data-stu-id="2f540-127">Host to redirect.</span></span> <span data-ttu-id="2f540-128">Hagyja üresen a bejövő állomás rendeltetési állomásként való használatát.</span><span class="sxs-lookup"><span data-stu-id="2f540-128">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="2f540-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="2f540-129">-CustomPath</span></span>
<span data-ttu-id="2f540-130">Az átirányítás teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="2f540-130">The full path to redirect.</span></span> <span data-ttu-id="2f540-131">Az elérési út nem lehet üres, és a/értékkel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="2f540-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="2f540-132">Hagyja üresen a bejövő út rendeltetési útvonalként való használatát.</span><span class="sxs-lookup"><span data-stu-id="2f540-132">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="2f540-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="2f540-133">-CustomQueryString</span></span>
<span data-ttu-id="2f540-134">Az átirányítási URL-címben elhelyezni kívánt lekérdezési karakterláncok halmaza.</span><span class="sxs-lookup"><span data-stu-id="2f540-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="2f540-135">Beállítás: az érték felülírhatja a meglévő lekérdezési karakterláncokat; hagyja üresen a bejövő lekérdezési karakterlánc megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="2f540-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="2f540-136">A lekérdezési karakterláncnak be kell lennie <key>=</span><span class="sxs-lookup"><span data-stu-id="2f540-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="2f540-137">formázása.</span><span class="sxs-lookup"><span data-stu-id="2f540-137">format.</span></span> <span data-ttu-id="2f540-138">Az első?</span><span class="sxs-lookup"><span data-stu-id="2f540-138">The first ?</span></span> <span data-ttu-id="2f540-139">a & automatikusan felveszi a program, hogy ne szerepeljenek rajtuk, de a lekérdezési karakterláncokat külön-külön kell kiválasztania a &.</span><span class="sxs-lookup"><span data-stu-id="2f540-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="2f540-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f540-140">-DefaultProfile</span></span>
<span data-ttu-id="2f540-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f540-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f540-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="2f540-142">-DynamicCompression</span></span>
<span data-ttu-id="2f540-143">Engedélyezi-e a dinamikus tömörítést a gyorsítótárazott tartalmak esetén, ha a gyorsítótárazás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2f540-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="2f540-144">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="2f540-144">Default value is Enabled</span></span>

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

### <span data-ttu-id="2f540-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="2f540-145">-EnableCaching</span></span>
<span data-ttu-id="2f540-146">Engedélyezi-e az útvonal gyorsítótárazását.</span><span class="sxs-lookup"><span data-stu-id="2f540-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="2f540-147">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="2f540-147">Default value is false</span></span>

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

### <span data-ttu-id="2f540-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="2f540-148">-EnabledState</span></span>
<span data-ttu-id="2f540-149">Engedélyezi-e a szabály használatát.</span><span class="sxs-lookup"><span data-stu-id="2f540-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="2f540-150">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="2f540-150">Default value is Enabled</span></span>

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

### <span data-ttu-id="2f540-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="2f540-151">-ForwardingProtocol</span></span>
<span data-ttu-id="2f540-152">A protokoll ezt a szabályt fogja használni, amikor forgalmat továbbít a backends alapértelmezett érték MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="2f540-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

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

### <span data-ttu-id="2f540-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="2f540-153">-FrontDoorName</span></span>
<span data-ttu-id="2f540-154">Annak a bejárati ajtónak a neve, amelyhez ez a művelettervi szabály tartozik.</span><span class="sxs-lookup"><span data-stu-id="2f540-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="2f540-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="2f540-155">-FrontendEndpointName</span></span>
<span data-ttu-id="2f540-156">A szabállyal társított frontend-végpontok neve</span><span class="sxs-lookup"><span data-stu-id="2f540-156">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="2f540-157">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f540-157">-Name</span></span>
<span data-ttu-id="2f540-158">RoutingRule neve</span><span class="sxs-lookup"><span data-stu-id="2f540-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="2f540-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="2f540-159">-PatternToMatch</span></span>
<span data-ttu-id="2f540-160">A szabály útvonali mintái nem tartalmazhatnak semmilyen \* vagy csak az útvonal végét követő végeredményt.</span><span class="sxs-lookup"><span data-stu-id="2f540-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="2f540-161">Az alapértelmezett érték a/\*</span><span class="sxs-lookup"><span data-stu-id="2f540-161">Default value is /\*</span></span>

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

### <span data-ttu-id="2f540-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="2f540-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="2f540-163">Az URL-lekérdezési fogalmak kezelése a gyorsítótár-kulcs alakításakor.</span><span class="sxs-lookup"><span data-stu-id="2f540-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="2f540-164">Az alapértelmezett érték a StripAll</span><span class="sxs-lookup"><span data-stu-id="2f540-164">Default value is StripAll</span></span>

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

### <span data-ttu-id="2f540-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="2f540-165">-RedirectProtocol</span></span>
<span data-ttu-id="2f540-166">Annak a helynek a protokollja, ahol a forgalmat átirányítják.</span><span class="sxs-lookup"><span data-stu-id="2f540-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="2f540-167">Az alapértelmezett érték a MatchRequest</span><span class="sxs-lookup"><span data-stu-id="2f540-167">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="2f540-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="2f540-168">-RedirectType</span></span>
<span data-ttu-id="2f540-169">Az átirányítás típusa: a szabály a forgalom átirányításakor használatos.</span><span class="sxs-lookup"><span data-stu-id="2f540-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="2f540-170">Az alapértelmezett érték áthelyezve</span><span class="sxs-lookup"><span data-stu-id="2f540-170">Default Value is Moved</span></span>

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

### <span data-ttu-id="2f540-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f540-171">-ResourceGroupName</span></span>
<span data-ttu-id="2f540-172">Annak az erőforráscsoport-névnek a neve, amelyet a RoutingRule fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="2f540-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="2f540-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="2f540-173">-RulesEngineName</span></span>
<span data-ttu-id="2f540-174">Hivatkozás egy bizonyos szabályok motor-konfigurációra, amelyre erre az útvonalra vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="2f540-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f540-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f540-175">CommonParameters</span></span>
<span data-ttu-id="2f540-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f540-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f540-177">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2f540-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f540-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f540-178">INPUTS</span></span>

### <span data-ttu-id="2f540-179">Nincs</span><span class="sxs-lookup"><span data-stu-id="2f540-179">None</span></span>

## <span data-ttu-id="2f540-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f540-180">OUTPUTS</span></span>

### <span data-ttu-id="2f540-181">Microsoft. Azure. Command. FrontDoor. models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2f540-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="2f540-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f540-182">NOTES</span></span>

## <span data-ttu-id="2f540-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f540-183">RELATED LINKS</span></span>

<span data-ttu-id="2f540-184">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="2f540-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
