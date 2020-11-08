---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 479b89296ae52221f714992791ed73cd14bf2fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183007"
---
# <span data-ttu-id="cc53f-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc53f-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="cc53f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc53f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc53f-103">Azure Express útvonal-áramkört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cc53f-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="cc53f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc53f-104">SYNTAX</span></span>

### <span data-ttu-id="cc53f-105">Szolgáltató (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc53f-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc53f-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cc53f-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc53f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc53f-107">DESCRIPTION</span></span>
<span data-ttu-id="cc53f-108">A **New-AzExpressRouteCircuit** parancsmag az Azure Express útvonal-áramkört hozza létre.</span><span class="sxs-lookup"><span data-stu-id="cc53f-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="cc53f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cc53f-109">EXAMPLES</span></span>

### <span data-ttu-id="cc53f-110">Példa 1: új ExpressRoute-áramkör létrehozása</span><span class="sxs-lookup"><span data-stu-id="cc53f-110">Example 1: Create a new ExpressRoute circuit</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

### <span data-ttu-id="cc53f-111">2. példa: új ExpressRoute-áramkör létrehozása a ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cc53f-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="cc53f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc53f-112">PARAMETERS</span></span>

### <span data-ttu-id="cc53f-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="cc53f-113">-AllowClassicOperations</span></span>
<span data-ttu-id="cc53f-114">A paraméter használata lehetővé teszi, hogy a klasszikus Azure PowerShell-parancsmagok használatával kezelje az áramkört.</span><span class="sxs-lookup"><span data-stu-id="cc53f-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc53f-115">-AsJob</span></span>
<span data-ttu-id="cc53f-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cc53f-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-117">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="cc53f-117">-Authorization</span></span>
<span data-ttu-id="cc53f-118">Az áramkör-engedélyezési listák listája.</span><span class="sxs-lookup"><span data-stu-id="cc53f-118">A list of circuit authorizations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="cc53f-119">-BandwidthInGbps</span></span>
<span data-ttu-id="cc53f-120">Az áramkör sávszélessége, ha az áramkör egy ExpressRoutePort-erőforráson van kiépítve.</span><span class="sxs-lookup"><span data-stu-id="cc53f-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: System.Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="cc53f-121">-BandwidthInMbps</span></span>
<span data-ttu-id="cc53f-122">Az áramkör sávszélessége.</span><span class="sxs-lookup"><span data-stu-id="cc53f-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="cc53f-123">Ennek a szolgáltató által támogatott értéknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="cc53f-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc53f-124">-DefaultProfile</span></span>
<span data-ttu-id="cc53f-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc53f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc53f-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cc53f-126">-ExpressRoutePort</span></span>
<span data-ttu-id="cc53f-127">A ExpressRoutePort-erőforrás hivatkozása, ha az áramkör egy ExpressRoutePort-erőforráson van kiépítve.</span><span class="sxs-lookup"><span data-stu-id="cc53f-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-128">-Force</span><span class="sxs-lookup"><span data-stu-id="cc53f-128">-Force</span></span>
<span data-ttu-id="cc53f-129">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="cc53f-129">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="cc53f-130">-Location</span></span>
<span data-ttu-id="cc53f-131">Az áramkör helye.</span><span class="sxs-lookup"><span data-stu-id="cc53f-131">The location of the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc53f-132">-Name</span></span>
<span data-ttu-id="cc53f-133">A létrehozandó ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="cc53f-133">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-134">-Társközi</span><span class="sxs-lookup"><span data-stu-id="cc53f-134">-Peering</span></span>
<span data-ttu-id="cc53f-135">A lista társközi konfigurációi.</span><span class="sxs-lookup"><span data-stu-id="cc53f-135">A list peer configurations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="cc53f-136">-PeeringLocation</span></span>
<span data-ttu-id="cc53f-137">A szolgáltató által támogatott társközi hely neve.</span><span class="sxs-lookup"><span data-stu-id="cc53f-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc53f-138">-ResourceGroupName</span></span>
<span data-ttu-id="cc53f-139">Az az erőforráscsoport, amely az áramkört fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="cc53f-139">The resource group that will contain the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="cc53f-140">-ServiceProviderName</span></span>
<span data-ttu-id="cc53f-141">Az áramkör-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="cc53f-141">The name of the circuit service provider.</span></span> <span data-ttu-id="cc53f-142">Ennek egyeznie kell a Get-AzExpressRouteServiceProvider parancsmag által megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="cc53f-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="cc53f-143">-SkuFamily</span></span>
<span data-ttu-id="cc53f-144">A SKU család a számlázási típust határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cc53f-144">SKU family determines the billing type.</span></span> <span data-ttu-id="cc53f-145">A paraméter lehetséges értékei a következők: `MeteredData` vagy `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="cc53f-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="cc53f-146">Ne feledje, hogy a MeteredData-ról UnlimitedData-ra változtathatja a számlázási típust, de a UnlimitedData-től az MeteredData-be nem változtathatja azt.</span><span class="sxs-lookup"><span data-stu-id="cc53f-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="cc53f-147">-SkuTier</span></span>
<span data-ttu-id="cc53f-148">Az áramkörhöz tartozó szolgáltatás szintje.</span><span class="sxs-lookup"><span data-stu-id="cc53f-148">The tier of service for the circuit.</span></span> <span data-ttu-id="cc53f-149">A paraméter lehetséges értékei a `Standard` következők: `Premium` `Local`</span><span class="sxs-lookup"><span data-stu-id="cc53f-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Local

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="cc53f-150">-Tag</span></span>
<span data-ttu-id="cc53f-151">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="cc53f-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cc53f-152">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="cc53f-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc53f-153">-Confirm</span></span>
<span data-ttu-id="cc53f-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc53f-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc53f-155">-WhatIf</span></span>
<span data-ttu-id="cc53f-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc53f-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc53f-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc53f-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc53f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc53f-158">CommonParameters</span></span>
<span data-ttu-id="cc53f-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc53f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc53f-160">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc53f-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc53f-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc53f-161">INPUTS</span></span>

### <span data-ttu-id="cc53f-162">System. String</span><span class="sxs-lookup"><span data-stu-id="cc53f-162">System.String</span></span>

### <span data-ttu-id="cc53f-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cc53f-163">System.Int32</span></span>

### <span data-ttu-id="cc53f-164">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cc53f-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="cc53f-165">System. Double</span><span class="sxs-lookup"><span data-stu-id="cc53f-165">System.Double</span></span>

### <span data-ttu-id="cc53f-166">Microsoft. Azure. commands. Network. models. PSPeering []</span><span class="sxs-lookup"><span data-stu-id="cc53f-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="cc53f-167">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitAuthorization []</span><span class="sxs-lookup"><span data-stu-id="cc53f-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="cc53f-168">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cc53f-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cc53f-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cc53f-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cc53f-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc53f-170">OUTPUTS</span></span>

### <span data-ttu-id="cc53f-171">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc53f-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cc53f-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc53f-172">NOTES</span></span>

## <span data-ttu-id="cc53f-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc53f-173">RELATED LINKS</span></span>

[<span data-ttu-id="cc53f-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc53f-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="cc53f-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc53f-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="cc53f-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc53f-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="cc53f-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cc53f-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
