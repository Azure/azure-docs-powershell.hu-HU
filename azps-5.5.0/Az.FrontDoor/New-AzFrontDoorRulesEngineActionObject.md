---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167523"
---
# <span data-ttu-id="3d537-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="3d537-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="3d537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d537-102">SYNOPSIS</span></span>
<span data-ttu-id="3d537-103">PSRulesEngineAction objektum létrehozása szabálymotorszabály létrehozásához</span><span class="sxs-lookup"><span data-stu-id="3d537-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="3d537-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3d537-104">SYNTAX</span></span>

### <span data-ttu-id="3d537-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d537-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d537-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d537-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d537-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3d537-107">DESCRIPTION</span></span>
<span data-ttu-id="3d537-108">Hozzon létre egy PSRulesEngineAction objektumot szabálymotor-szabály létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="3d537-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="3d537-109">A "New-AzFrontDoorHeaderActionObject" parancsmag használatával PSHeaderObjects parancsmagokat hozhat létre, amelyek a "-RequestHeaderActions" és a "-ResponseHeaderActions" paraméterbe írják át őket.</span><span class="sxs-lookup"><span data-stu-id="3d537-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="3d537-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3d537-110">EXAMPLES</span></span>

### <span data-ttu-id="3d537-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3d537-111">Example 1</span></span>
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

<span data-ttu-id="3d537-112">Hozzon létre egy szabálymotor-műveletet, és mutassa meg, hogyan lehet megtekinteni a létrehozott szabálymotor-műveletet.</span><span class="sxs-lookup"><span data-stu-id="3d537-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="3d537-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d537-113">PARAMETERS</span></span>

### <span data-ttu-id="3d537-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="3d537-114">-BackendPoolName</span></span>
<span data-ttu-id="3d537-115">Annak a BackendPoolnak a neve, amelyre a szabály</span><span class="sxs-lookup"><span data-stu-id="3d537-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="3d537-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="3d537-116">-CustomForwardingPath</span></span>
<span data-ttu-id="3d537-117">A szabálynak megfelelő erőforrás-elérési utak újraírásának egyéni elérési útja.</span><span class="sxs-lookup"><span data-stu-id="3d537-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="3d537-118">Hagyja üresen a bejövő útvonalat.</span><span class="sxs-lookup"><span data-stu-id="3d537-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="3d537-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="3d537-119">-CustomFragment</span></span>
<span data-ttu-id="3d537-120">Az átirányítási URL-címhez hozzáadható töredezettség.</span><span class="sxs-lookup"><span data-stu-id="3d537-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="3d537-121">A feldarabolás az URL-cím #után következő része.</span><span class="sxs-lookup"><span data-stu-id="3d537-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="3d537-122">Ne tartalmazza a #.</span><span class="sxs-lookup"><span data-stu-id="3d537-122">Do not include the #.</span></span>

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

### <span data-ttu-id="3d537-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="3d537-123">-CustomHost</span></span>
<span data-ttu-id="3d537-124">Átirányítani kell az állomást.</span><span class="sxs-lookup"><span data-stu-id="3d537-124">Host to redirect.</span></span>
<span data-ttu-id="3d537-125">Hagyja üresen, hogy a bejövő állomást használja a cél gazdakiszolgálóként.</span><span class="sxs-lookup"><span data-stu-id="3d537-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="3d537-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="3d537-126">-CustomPath</span></span>
<span data-ttu-id="3d537-127">Az átirányítás teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="3d537-127">The full path to redirect.</span></span>
<span data-ttu-id="3d537-128">Az elérési út nem lehet üres, és a /értéknek kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="3d537-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="3d537-129">Hagyja üresen, hogy a bejövő útvonalat használja célként.</span><span class="sxs-lookup"><span data-stu-id="3d537-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="3d537-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="3d537-130">-CustomQueryString</span></span>
<span data-ttu-id="3d537-131">Az átirányítási URL-címbe helyező lekérdezési karakterláncok halmaza.</span><span class="sxs-lookup"><span data-stu-id="3d537-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="3d537-132">Ennek az értéknek a beállítása lecserélné a meglévő lekérdezési karakterláncokat; hagyja üresen a bejövő lekérdezési karakterlánc megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="3d537-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="3d537-133">A lekérdezési karakterláncnak formátumban kell \<key\> = \<value\> lennie.</span><span class="sxs-lookup"><span data-stu-id="3d537-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="3d537-134">Az első?</span><span class="sxs-lookup"><span data-stu-id="3d537-134">The first ?</span></span>
<span data-ttu-id="3d537-135">és & automatikusan hozzáadja a rendszer, ezért ne foglalja bele őket az elsőbe, hanem válassza el egymástól a lekérdezési karakterláncokat &.</span><span class="sxs-lookup"><span data-stu-id="3d537-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="3d537-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d537-136">-DefaultProfile</span></span>
<span data-ttu-id="3d537-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d537-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d537-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="3d537-138">-DynamicCompression</span></span>
<span data-ttu-id="3d537-139">Hogy engedélyezi-e a dinamikus tömörítést a gyorsítótárazott tartalomhoz.</span><span class="sxs-lookup"><span data-stu-id="3d537-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="3d537-140">Az alapértelmezett érték engedélyezve van</span><span class="sxs-lookup"><span data-stu-id="3d537-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="3d537-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="3d537-141">-EnableCaching</span></span>
<span data-ttu-id="3d537-142">Hogy engedélyezi-e a gyorsítótárazást ehhez az útvonalhoz.</span><span class="sxs-lookup"><span data-stu-id="3d537-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="3d537-143">Az alapértelmezett érték hamis</span><span class="sxs-lookup"><span data-stu-id="3d537-143">Default value is false</span></span>

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

### <span data-ttu-id="3d537-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="3d537-144">-ForwardingProtocol</span></span>
<span data-ttu-id="3d537-145">A szabály által használt protokoll a háttértendékekbe továbbítja a forgalmat.</span><span class="sxs-lookup"><span data-stu-id="3d537-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="3d537-146">Az alapértelmezett érték a MatchRequest</span><span class="sxs-lookup"><span data-stu-id="3d537-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="3d537-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="3d537-147">-FrontDoorName</span></span>
<span data-ttu-id="3d537-148">Annak a front door-nak a neve, amelyhez ez az útválasztási szabály tartozik.</span><span class="sxs-lookup"><span data-stu-id="3d537-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="3d537-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="3d537-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="3d537-150">Az URL-lekérdezési kifejezések kezelése a gyorsítótárkulcs létrehozása során.</span><span class="sxs-lookup"><span data-stu-id="3d537-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="3d537-151">Az alapértelmezett érték a StripAll</span><span class="sxs-lookup"><span data-stu-id="3d537-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="3d537-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="3d537-152">-RedirectProtocol</span></span>
<span data-ttu-id="3d537-153">Annak a célhelynek a protokollja, ahová a forgalmat átirányítják.</span><span class="sxs-lookup"><span data-stu-id="3d537-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="3d537-154">Az alapértelmezett érték a MatchRequest</span><span class="sxs-lookup"><span data-stu-id="3d537-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="3d537-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="3d537-155">-RedirectType</span></span>
<span data-ttu-id="3d537-156">A szabály által a forgalom átirányításakor használt átirányítási típus.</span><span class="sxs-lookup"><span data-stu-id="3d537-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="3d537-157">Az alapértelmezett érték át van jelölve</span><span class="sxs-lookup"><span data-stu-id="3d537-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="3d537-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="3d537-158">-RequestHeaderAction</span></span>
<span data-ttu-id="3d537-159">Az AFD-től a forrásra vonatkozó kérelemben alkalmazandó fejlécműveletek listája.</span><span class="sxs-lookup"><span data-stu-id="3d537-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d537-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d537-160">-ResourceGroupName</span></span>
<span data-ttu-id="3d537-161">Az erőforráscsoport neve, amelyből a RoutingRule létrejön.</span><span class="sxs-lookup"><span data-stu-id="3d537-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="3d537-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="3d537-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="3d537-163">Az AFD-től az ügyfélre adott válaszból alkalmazandó fejlécműveletek listája.</span><span class="sxs-lookup"><span data-stu-id="3d537-163">A list of header actions to apply from the response from AFD to the client.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d537-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d537-164">CommonParameters</span></span>
<span data-ttu-id="3d537-165">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d537-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d537-166">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d537-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d537-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d537-167">INPUTS</span></span>

### <span data-ttu-id="3d537-168">Nincs</span><span class="sxs-lookup"><span data-stu-id="3d537-168">None</span></span>

## <span data-ttu-id="3d537-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d537-169">OUTPUTS</span></span>

### <span data-ttu-id="3d537-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="3d537-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="3d537-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3d537-171">NOTES</span></span>

## <span data-ttu-id="3d537-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d537-172">RELATED LINKS</span></span>
