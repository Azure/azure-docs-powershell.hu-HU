---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167531"
---
# <span data-ttu-id="b0739-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="b0739-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="b0739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0739-102">SYNOPSIS</span></span>
<span data-ttu-id="b0739-103">PSRoutingRuleObject létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="b0739-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="b0739-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b0739-104">SYNTAX</span></span>

### <span data-ttu-id="b0739-105">ByFieldsWithForwardingParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0739-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0739-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0739-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0739-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b0739-107">DESCRIPTION</span></span>
<span data-ttu-id="b0739-108">PSRoutingRuleObject létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="b0739-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="b0739-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b0739-109">EXAMPLES</span></span>

### <span data-ttu-id="b0739-110">1. példa: PSRoutingRuleObject létrehozása továbbítási s szabály alkalmazásával</span><span class="sxs-lookup"><span data-stu-id="b0739-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
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

### <span data-ttu-id="b0739-111">2. példa: PsRoutingRuleObject létrehozása a front door létrehozásához átirányítási s szabály segítségével</span><span class="sxs-lookup"><span data-stu-id="b0739-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
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

<span data-ttu-id="b0739-112">PSRoutingRuleObject létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="b0739-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="b0739-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0739-113">PARAMETERS</span></span>

### <span data-ttu-id="b0739-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="b0739-114">-AcceptedProtocol</span></span>
<span data-ttu-id="b0739-115">A szabálynak megfelelő protokollsémák.</span><span class="sxs-lookup"><span data-stu-id="b0739-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="b0739-116">Az alapértelmezett érték a következő: {Https, Http}</span><span class="sxs-lookup"><span data-stu-id="b0739-116">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="b0739-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="b0739-117">-BackendPoolName</span></span>
<span data-ttu-id="b0739-118">Annak a BackendPoolnak az erőforrás-azonosítója, amelyre ez a szabály</span><span class="sxs-lookup"><span data-stu-id="b0739-118">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="b0739-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="b0739-119">-CustomForwardingPath</span></span>
<span data-ttu-id="b0739-120">A szabálynak megfelelő erőforrás-elérési utak újraírásának egyéni elérési útja.</span><span class="sxs-lookup"><span data-stu-id="b0739-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="b0739-121">Hagyja üresen a bejövő útvonalat.</span><span class="sxs-lookup"><span data-stu-id="b0739-121">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="b0739-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="b0739-122">-CustomFragment</span></span>
<span data-ttu-id="b0739-123">Az átirányítási URL-címhez hozzáadható töredezettség.</span><span class="sxs-lookup"><span data-stu-id="b0739-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="b0739-124">A feldarabolás az URL-cím #után következő része.</span><span class="sxs-lookup"><span data-stu-id="b0739-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="b0739-125">Ne tartalmazza a #.</span><span class="sxs-lookup"><span data-stu-id="b0739-125">Do not include the #.</span></span>

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

### <span data-ttu-id="b0739-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="b0739-126">-CustomHost</span></span>
<span data-ttu-id="b0739-127">Átirányítani kell az állomást.</span><span class="sxs-lookup"><span data-stu-id="b0739-127">Host to redirect.</span></span> <span data-ttu-id="b0739-128">Hagyja üresen, hogy a bejövő állomást használja a cél gazdakiszolgálóként.</span><span class="sxs-lookup"><span data-stu-id="b0739-128">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="b0739-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="b0739-129">-CustomPath</span></span>
<span data-ttu-id="b0739-130">Az átirányítás teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="b0739-130">The full path to redirect.</span></span> <span data-ttu-id="b0739-131">Az elérési út nem lehet üres, és a /értéknek kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="b0739-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="b0739-132">Hagyja üresen, hogy a bejövő útvonalat használja célként.</span><span class="sxs-lookup"><span data-stu-id="b0739-132">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="b0739-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="b0739-133">-CustomQueryString</span></span>
<span data-ttu-id="b0739-134">Az átirányítási URL-címbe helyező lekérdezési karakterláncok halmaza.</span><span class="sxs-lookup"><span data-stu-id="b0739-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="b0739-135">Ennek az értéknek a beállítása lecserélné a meglévő lekérdezési karakterláncokat; hagyja üresen a bejövő lekérdezési karakterlánc megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="b0739-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="b0739-136">A lekérdezési karakterláncnak a következőben kell lennie: <key>=</span><span class="sxs-lookup"><span data-stu-id="b0739-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="b0739-137">formátumot.</span><span class="sxs-lookup"><span data-stu-id="b0739-137">format.</span></span> <span data-ttu-id="b0739-138">Az első?</span><span class="sxs-lookup"><span data-stu-id="b0739-138">The first ?</span></span> <span data-ttu-id="b0739-139">és & automatikusan hozzáadja a rendszer, ezért ne foglalja bele őket az elsőbe, hanem válassza el egymástól a lekérdezési karakterláncokat &.</span><span class="sxs-lookup"><span data-stu-id="b0739-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="b0739-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0739-140">-DefaultProfile</span></span>
<span data-ttu-id="b0739-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0739-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0739-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="b0739-142">-DynamicCompression</span></span>
<span data-ttu-id="b0739-143">Engedélyezi-e a dinamikus tömörítést a gyorsítótárazott tartalomhoz, ha engedélyezve van a gyorsítótárazás.</span><span class="sxs-lookup"><span data-stu-id="b0739-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="b0739-144">Az alapértelmezett érték engedélyezve van</span><span class="sxs-lookup"><span data-stu-id="b0739-144">Default value is Enabled</span></span>

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

### <span data-ttu-id="b0739-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="b0739-145">-EnableCaching</span></span>
<span data-ttu-id="b0739-146">Hogy engedélyezi-e a gyorsítótárazást ehhez az útvonalhoz.</span><span class="sxs-lookup"><span data-stu-id="b0739-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="b0739-147">Az alapértelmezett érték hamis</span><span class="sxs-lookup"><span data-stu-id="b0739-147">Default value is false</span></span>

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

### <span data-ttu-id="b0739-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b0739-148">-EnabledState</span></span>
<span data-ttu-id="b0739-149">Hogy engedélyezi-e a szabály használatát.</span><span class="sxs-lookup"><span data-stu-id="b0739-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="b0739-150">Az alapértelmezett érték engedélyezve van</span><span class="sxs-lookup"><span data-stu-id="b0739-150">Default value is Enabled</span></span>

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

### <span data-ttu-id="b0739-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="b0739-151">-ForwardingProtocol</span></span>
<span data-ttu-id="b0739-152">A szabály által használt protokoll a Forgalom backends szolgáltatásba való továbbításakor a MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="b0739-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

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

### <span data-ttu-id="b0739-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="b0739-153">-FrontDoorName</span></span>
<span data-ttu-id="b0739-154">Annak a front door-nak a neve, amelyhez ez az útválasztási szabály tartozik.</span><span class="sxs-lookup"><span data-stu-id="b0739-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="b0739-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="b0739-155">-FrontendEndpointName</span></span>
<span data-ttu-id="b0739-156">A s szabályhoz társított frontend végpontok neve</span><span class="sxs-lookup"><span data-stu-id="b0739-156">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="b0739-157">-Name</span><span class="sxs-lookup"><span data-stu-id="b0739-157">-Name</span></span>
<span data-ttu-id="b0739-158">RoutingRule név.</span><span class="sxs-lookup"><span data-stu-id="b0739-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="b0739-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="b0739-159">-PatternToMatch</span></span>
<span data-ttu-id="b0739-160">A szabály útvonal mintái, nem lehet \*, kivéve, ha az útvonal végén az utolsó /után van.</span><span class="sxs-lookup"><span data-stu-id="b0739-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="b0739-161">Az alapértelmezett érték a /\*</span><span class="sxs-lookup"><span data-stu-id="b0739-161">Default value is /\*</span></span>

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

### <span data-ttu-id="b0739-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="b0739-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="b0739-163">Az URL-lekérdezési kifejezések kezelése a gyorsítótárkulcs létrehozása során.</span><span class="sxs-lookup"><span data-stu-id="b0739-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="b0739-164">Az alapértelmezett érték a StripAll</span><span class="sxs-lookup"><span data-stu-id="b0739-164">Default value is StripAll</span></span>

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

### <span data-ttu-id="b0739-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="b0739-165">-RedirectProtocol</span></span>
<span data-ttu-id="b0739-166">Annak a célhelynek a protokollja, ahová a forgalmat átirányítják.</span><span class="sxs-lookup"><span data-stu-id="b0739-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="b0739-167">Az alapértelmezett érték a MatchRequest</span><span class="sxs-lookup"><span data-stu-id="b0739-167">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="b0739-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="b0739-168">-RedirectType</span></span>
<span data-ttu-id="b0739-169">A szabály által a forgalom átirányításakor használt átirányítási típus.</span><span class="sxs-lookup"><span data-stu-id="b0739-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="b0739-170">Az alapértelmezett érték át van jelölve</span><span class="sxs-lookup"><span data-stu-id="b0739-170">Default Value is Moved</span></span>

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

### <span data-ttu-id="b0739-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0739-171">-ResourceGroupName</span></span>
<span data-ttu-id="b0739-172">Az erőforráscsoport neve, amelyből a RoutingRule létrejön.</span><span class="sxs-lookup"><span data-stu-id="b0739-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="b0739-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="b0739-173">-RulesEngineName</span></span>
<span data-ttu-id="b0739-174">Hivatkozás egy adott szabálymotor konfigurációra, amely erre az útvonalra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b0739-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

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

### <span data-ttu-id="b0739-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0739-175">CommonParameters</span></span>
<span data-ttu-id="b0739-176">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0739-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0739-177">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0739-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0739-178">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0739-178">INPUTS</span></span>

### <span data-ttu-id="b0739-179">Nincs</span><span class="sxs-lookup"><span data-stu-id="b0739-179">None</span></span>

## <span data-ttu-id="b0739-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0739-180">OUTPUTS</span></span>

### <span data-ttu-id="b0739-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b0739-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="b0739-182">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b0739-182">NOTES</span></span>

## <span data-ttu-id="b0739-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0739-183">RELATED LINKS</span></span>

<span data-ttu-id="b0739-184">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="b0739-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
