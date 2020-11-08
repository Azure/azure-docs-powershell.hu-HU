---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187412"
---
# <span data-ttu-id="5708a-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="5708a-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="5708a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5708a-102">SYNOPSIS</span></span>
<span data-ttu-id="5708a-103">PSRulesEngineAction objektum létrehozása szabály-végrehajtó szabály létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="5708a-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="5708a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5708a-104">SYNTAX</span></span>

### <span data-ttu-id="5708a-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="5708a-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5708a-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5708a-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5708a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5708a-107">DESCRIPTION</span></span>
<span data-ttu-id="5708a-108">PSRulesEngineAction objektum létrehozása szabály-végrehajtó szabály létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="5708a-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="5708a-109">A parancsmag "New-AzFrontDoorHeaderActionObject" paranccsal PSHeaderObjects hozhat létre a "-RequestHeaderActions" és a "-ResponseHeaderActions" paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="5708a-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="5708a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5708a-110">EXAMPLES</span></span>

### <span data-ttu-id="5708a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5708a-111">Example 1</span></span>
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

<span data-ttu-id="5708a-112">A szabályok motorjának létrehozása és a szabályok megadására szolgáló műveletek megtekintése</span><span class="sxs-lookup"><span data-stu-id="5708a-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="5708a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5708a-113">PARAMETERS</span></span>

### <span data-ttu-id="5708a-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="5708a-114">-BackendPoolName</span></span>
<span data-ttu-id="5708a-115">Annak a BackendPool a neve, amelyre a szabály vonatkozik</span><span class="sxs-lookup"><span data-stu-id="5708a-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="5708a-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="5708a-116">-CustomForwardingPath</span></span>
<span data-ttu-id="5708a-117">A szabály által kiválasztott erőforrás-elérési utak átírásához használt egyéni elérési út.</span><span class="sxs-lookup"><span data-stu-id="5708a-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="5708a-118">Hagyja üresen a bejövő elérési út használatát.</span><span class="sxs-lookup"><span data-stu-id="5708a-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="5708a-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="5708a-119">-CustomFragment</span></span>
<span data-ttu-id="5708a-120">Az átirányítási URL-címhez hozzáadni kívánt részlet</span><span class="sxs-lookup"><span data-stu-id="5708a-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="5708a-121">A töredék a # után elkerülő URL-cím része.</span><span class="sxs-lookup"><span data-stu-id="5708a-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="5708a-122">Ne szerepeljen a #.</span><span class="sxs-lookup"><span data-stu-id="5708a-122">Do not include the #.</span></span>

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

### <span data-ttu-id="5708a-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="5708a-123">-CustomHost</span></span>
<span data-ttu-id="5708a-124">Állomás átirányítását.</span><span class="sxs-lookup"><span data-stu-id="5708a-124">Host to redirect.</span></span>
<span data-ttu-id="5708a-125">Hagyja üresen a bejövő állomás rendeltetési állomásként való használatát.</span><span class="sxs-lookup"><span data-stu-id="5708a-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="5708a-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="5708a-126">-CustomPath</span></span>
<span data-ttu-id="5708a-127">Az átirányítás teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="5708a-127">The full path to redirect.</span></span>
<span data-ttu-id="5708a-128">Az elérési út nem lehet üres, és a/értékkel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="5708a-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="5708a-129">Hagyja üresen a bejövő út rendeltetési útvonalként való használatát.</span><span class="sxs-lookup"><span data-stu-id="5708a-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="5708a-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="5708a-130">-CustomQueryString</span></span>
<span data-ttu-id="5708a-131">Az átirányítási URL-címben elhelyezni kívánt lekérdezési karakterláncok halmaza.</span><span class="sxs-lookup"><span data-stu-id="5708a-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="5708a-132">Beállítás: az érték felülírhatja a meglévő lekérdezési karakterláncokat; hagyja üresen a bejövő lekérdezési karakterlánc megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="5708a-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="5708a-133">A lekérdezési karakterláncnak formátumban kell lennie \<key\> = \<value\> .</span><span class="sxs-lookup"><span data-stu-id="5708a-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="5708a-134">Az első?</span><span class="sxs-lookup"><span data-stu-id="5708a-134">The first ?</span></span>
<span data-ttu-id="5708a-135">a & automatikusan felveszi a program, hogy ne szerepeljenek rajtuk, de a lekérdezési karakterláncokat külön-külön kell kiválasztania a &.</span><span class="sxs-lookup"><span data-stu-id="5708a-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="5708a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5708a-136">-DefaultProfile</span></span>
<span data-ttu-id="5708a-137">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5708a-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5708a-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="5708a-138">-DynamicCompression</span></span>
<span data-ttu-id="5708a-139">Engedélyezi-e a dinamikus tömörítést a gyorsítótárazott tartalomhoz.</span><span class="sxs-lookup"><span data-stu-id="5708a-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="5708a-140">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="5708a-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="5708a-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="5708a-141">-EnableCaching</span></span>
<span data-ttu-id="5708a-142">Engedélyezi-e az útvonal gyorsítótárazását.</span><span class="sxs-lookup"><span data-stu-id="5708a-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="5708a-143">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="5708a-143">Default value is false</span></span>

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

### <span data-ttu-id="5708a-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="5708a-144">-ForwardingProtocol</span></span>
<span data-ttu-id="5708a-145">A protokoll ezt a szabályt fogja használni a forgalom backend-re való továbbításakor.</span><span class="sxs-lookup"><span data-stu-id="5708a-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="5708a-146">Az alapértelmezett érték a MatchRequest</span><span class="sxs-lookup"><span data-stu-id="5708a-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="5708a-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="5708a-147">-FrontDoorName</span></span>
<span data-ttu-id="5708a-148">Annak a bejárati ajtónak a neve, amelyhez ez a művelettervi szabály tartozik.</span><span class="sxs-lookup"><span data-stu-id="5708a-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="5708a-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="5708a-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="5708a-150">Az URL-lekérdezési fogalmak kezelése a gyorsítótár-kulcs alakításakor.</span><span class="sxs-lookup"><span data-stu-id="5708a-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="5708a-151">Az alapértelmezett érték a StripAll</span><span class="sxs-lookup"><span data-stu-id="5708a-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="5708a-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="5708a-152">-RedirectProtocol</span></span>
<span data-ttu-id="5708a-153">Annak a helynek a protokollja, ahol a forgalmat átirányítják.</span><span class="sxs-lookup"><span data-stu-id="5708a-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="5708a-154">Az alapértelmezett érték a MatchRequest</span><span class="sxs-lookup"><span data-stu-id="5708a-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="5708a-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="5708a-155">-RedirectType</span></span>
<span data-ttu-id="5708a-156">Az átirányítás típusa: a szabály a forgalom átirányításakor használatos.</span><span class="sxs-lookup"><span data-stu-id="5708a-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="5708a-157">Az alapértelmezett érték áthelyezve</span><span class="sxs-lookup"><span data-stu-id="5708a-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="5708a-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="5708a-158">-RequestHeaderAction</span></span>
<span data-ttu-id="5708a-159">Annak a fejléc-műveleteknek a listája, amelyeket a AFD-ról a származási kérelemből kell alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="5708a-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

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

### <span data-ttu-id="5708a-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5708a-160">-ResourceGroupName</span></span>
<span data-ttu-id="5708a-161">Annak az erőforráscsoport-névnek a neve, amelyet a RoutingRule fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="5708a-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="5708a-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="5708a-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="5708a-163">A AFD és az ügyfél közötti válaszból az adott választól alkalmazni kívánt fejléc-műveletek listája.</span><span class="sxs-lookup"><span data-stu-id="5708a-163">A list of header actions to apply from the response from AFD to the client.</span></span>

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

### <span data-ttu-id="5708a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5708a-164">CommonParameters</span></span>
<span data-ttu-id="5708a-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5708a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5708a-166">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5708a-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5708a-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5708a-167">INPUTS</span></span>

### <span data-ttu-id="5708a-168">Nincs</span><span class="sxs-lookup"><span data-stu-id="5708a-168">None</span></span>

## <span data-ttu-id="5708a-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5708a-169">OUTPUTS</span></span>

### <span data-ttu-id="5708a-170">Microsoft. Azure. Command. FrontDoor. models. PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="5708a-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="5708a-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5708a-171">NOTES</span></span>

## <span data-ttu-id="5708a-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5708a-172">RELATED LINKS</span></span>
