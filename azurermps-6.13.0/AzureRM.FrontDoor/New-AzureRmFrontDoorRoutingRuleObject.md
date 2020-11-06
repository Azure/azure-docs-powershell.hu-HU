---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499499"
---
# <span data-ttu-id="59abd-101">New-AzureRmFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="59abd-101">New-AzureRmFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="59abd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59abd-102">SYNOPSIS</span></span>
<span data-ttu-id="59abd-103">PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="59abd-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59abd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59abd-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59abd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59abd-105">DESCRIPTION</span></span>
<span data-ttu-id="59abd-106">PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="59abd-106">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="59abd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59abd-107">EXAMPLES</span></span>

### <span data-ttu-id="59abd-108">Példa 1: PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="59abd-108">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="59abd-109">PSRoutingRuleObject létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="59abd-109">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="59abd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59abd-110">PARAMETERS</span></span>

### <span data-ttu-id="59abd-111">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="59abd-111">-AcceptedProtocol</span></span>
<span data-ttu-id="59abd-112">A szabályhoz egyeztetni kívánt protokol-sémák.</span><span class="sxs-lookup"><span data-stu-id="59abd-112">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="59abd-113">Az alapértelmezett érték {HTTPS, http}</span><span class="sxs-lookup"><span data-stu-id="59abd-113">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="59abd-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="59abd-114">-BackendPoolName</span></span>
<span data-ttu-id="59abd-115">Annak az BackendPool az erőforrás-azonosítója, amelyre a szabály átvezet</span><span class="sxs-lookup"><span data-stu-id="59abd-115">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="59abd-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="59abd-116">-CustomForwardingPath</span></span>
<span data-ttu-id="59abd-117">A szabály által kiválasztott erőforrás-elérési utak átírásához használt egyéni elérési út.</span><span class="sxs-lookup"><span data-stu-id="59abd-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="59abd-118">Hagyja üresen a bejövő elérési út használatát.</span><span class="sxs-lookup"><span data-stu-id="59abd-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="59abd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59abd-119">-DefaultProfile</span></span>
<span data-ttu-id="59abd-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59abd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59abd-121">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="59abd-121">-DynamicCompression</span></span>
<span data-ttu-id="59abd-122">Engedélyezi-e a dinamikus tömörítést a gyorsítótárazott tartalmak esetén, ha a gyorsítótárazás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="59abd-122">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="59abd-123">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="59abd-123">Default value is Enabled</span></span>

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

### <span data-ttu-id="59abd-124">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="59abd-124">-EnableCaching</span></span>
<span data-ttu-id="59abd-125">Engedélyezi-e az útvonal gyorsítótárazását.</span><span class="sxs-lookup"><span data-stu-id="59abd-125">Whether to enable caching for this route.</span></span> <span data-ttu-id="59abd-126">Az alapértelmezett érték a hamis</span><span class="sxs-lookup"><span data-stu-id="59abd-126">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59abd-127">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="59abd-127">-EnabledState</span></span>
<span data-ttu-id="59abd-128">Engedélyezi-e a szabály használatát.</span><span class="sxs-lookup"><span data-stu-id="59abd-128">Whether to enable use of this rule.</span></span>
<span data-ttu-id="59abd-129">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="59abd-129">Default value is Enabled</span></span>

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

### <span data-ttu-id="59abd-130">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="59abd-130">-ForwardingProtocol</span></span>
<span data-ttu-id="59abd-131">A protokoll ezt a szabályt fogja használni, amikor forgalmat továbbít a backends alapértelmezett érték MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="59abd-131">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59abd-132">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="59abd-132">-FrontDoorName</span></span>
<span data-ttu-id="59abd-133">Annak a bejárati ajtónak a neve, amelyhez ez a művelettervi szabály tartozik.</span><span class="sxs-lookup"><span data-stu-id="59abd-133">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="59abd-134">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="59abd-134">-FrontendEndpointName</span></span>
<span data-ttu-id="59abd-135">A szabállyal társított frontend-végpontok neve</span><span class="sxs-lookup"><span data-stu-id="59abd-135">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="59abd-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59abd-136">-Name</span></span>
<span data-ttu-id="59abd-137">RoutingRule neve</span><span class="sxs-lookup"><span data-stu-id="59abd-137">RoutingRule name.</span></span>

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

### <span data-ttu-id="59abd-138">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="59abd-138">-PatternToMatch</span></span>
<span data-ttu-id="59abd-139">A szabály útvonali mintái nem tartalmazhatnak semmilyen \* vagy csak az útvonal végét követő végeredményt.</span><span class="sxs-lookup"><span data-stu-id="59abd-139">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="59abd-140">Az alapértelmezett érték a/\*</span><span class="sxs-lookup"><span data-stu-id="59abd-140">Default value is /\*</span></span>

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

### <span data-ttu-id="59abd-141">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="59abd-141">-QueryParameterStripDirective</span></span>
<span data-ttu-id="59abd-142">Az URL-lekérdezési fogalmak kezelése a gyorsítótár-kulcs alakításakor.</span><span class="sxs-lookup"><span data-stu-id="59abd-142">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="59abd-143">Az alapértelmezett érték a StripAll</span><span class="sxs-lookup"><span data-stu-id="59abd-143">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59abd-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59abd-144">-ResourceGroupName</span></span>
<span data-ttu-id="59abd-145">Annak az erőforráscsoport-névnek a neve, amelyet a RoutingRule fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="59abd-145">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="59abd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59abd-146">CommonParameters</span></span>
<span data-ttu-id="59abd-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59abd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59abd-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59abd-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59abd-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59abd-149">INPUTS</span></span>

### <span data-ttu-id="59abd-150">Nincs</span><span class="sxs-lookup"><span data-stu-id="59abd-150">None</span></span>

## <span data-ttu-id="59abd-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59abd-151">OUTPUTS</span></span>

### <span data-ttu-id="59abd-152">Microsoft. Azure. Command. FrontDoor. models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="59abd-152">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="59abd-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59abd-153">NOTES</span></span>

## <span data-ttu-id="59abd-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59abd-154">RELATED LINKS</span></span>

<span data-ttu-id="59abd-155">[Új – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="59abd-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
