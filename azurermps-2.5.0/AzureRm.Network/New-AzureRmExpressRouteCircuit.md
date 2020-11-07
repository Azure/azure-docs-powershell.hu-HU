---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: 43084ab54ed20a094cc292eca2bf133598171f09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848413"
---
# <span data-ttu-id="0caad-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0caad-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="0caad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0caad-102">SYNOPSIS</span></span>
<span data-ttu-id="0caad-103">Azure Express útvonal-áramkört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0caad-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0caad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0caad-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0caad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0caad-105">DESCRIPTION</span></span>
<span data-ttu-id="0caad-106">A **New-AzureRmExpressRouteCircuit** parancsmag az Azure Express útvonal-áramkört hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0caad-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="0caad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0caad-107">EXAMPLES</span></span>

### <span data-ttu-id="0caad-108">Példa 1: új ExpressRoute-áramkör létrehozása</span><span class="sxs-lookup"><span data-stu-id="0caad-108">Example 1: Create a new ExpressRoute circuit</span></span>
```
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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="0caad-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0caad-109">PARAMETERS</span></span>

### <span data-ttu-id="0caad-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="0caad-110">-AllowClassicOperations</span></span>
<span data-ttu-id="0caad-111">A paraméter használata lehetővé teszi, hogy a klasszikus Azure PowerShell-parancsmagok használatával kezelje az áramkört.</span><span class="sxs-lookup"><span data-stu-id="0caad-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0caad-112">-AsJob</span></span>
<span data-ttu-id="0caad-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0caad-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-114">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="0caad-114">-Authorization</span></span>
<span data-ttu-id="0caad-115">Az áramkör-engedélyezési listák listája.</span><span class="sxs-lookup"><span data-stu-id="0caad-115">A list of circuit authorizations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="0caad-116">-BandwidthInMbps</span></span>
<span data-ttu-id="0caad-117">Az áramkör sávszélessége.</span><span class="sxs-lookup"><span data-stu-id="0caad-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="0caad-118">Ennek a szolgáltató által támogatott értéknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="0caad-118">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0caad-119">-DefaultProfile</span></span>
<span data-ttu-id="0caad-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0caad-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0caad-121">-Force</span></span>
<span data-ttu-id="0caad-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0caad-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="0caad-123">-Location</span></span>
<span data-ttu-id="0caad-124">Az áramkör helye.</span><span class="sxs-lookup"><span data-stu-id="0caad-124">The location of the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0caad-125">-Name</span></span>
<span data-ttu-id="0caad-126">A létrehozandó ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="0caad-126">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-127">-Társközi</span><span class="sxs-lookup"><span data-stu-id="0caad-127">-Peering</span></span>
<span data-ttu-id="0caad-128">A lista társközi konfigurációi.</span><span class="sxs-lookup"><span data-stu-id="0caad-128">A list peer configurations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="0caad-129">-PeeringLocation</span></span>
<span data-ttu-id="0caad-130">A szolgáltató által támogatott társközi hely neve.</span><span class="sxs-lookup"><span data-stu-id="0caad-130">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0caad-131">-ResourceGroupName</span></span>
<span data-ttu-id="0caad-132">Az az erőforráscsoport, amely az áramkört fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0caad-132">The resource group that will contain the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="0caad-133">-ServiceProviderName</span></span>
<span data-ttu-id="0caad-134">Az áramkör-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="0caad-134">The name of the circuit service provider.</span></span> <span data-ttu-id="0caad-135">Ennek egyeznie kell a Get-AzureRmExpressRouteServiceProvider parancsmag által megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="0caad-135">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="0caad-136">-SkuFamily</span></span>
<span data-ttu-id="0caad-137">A SKU család a számlázási típust határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0caad-137">SKU family determines the billing type.</span></span> <span data-ttu-id="0caad-138">A paraméter lehetséges értékei a következők: `MeteredData` vagy `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="0caad-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="0caad-139">Ne feledje, hogy a MeteredData-ról UnlimitedData-ra változtathatja a számlázási típust, de a UnlimitedData-től az MeteredData-be nem változtathatja azt.</span><span class="sxs-lookup"><span data-stu-id="0caad-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0caad-140">-SkuTier</span></span>
<span data-ttu-id="0caad-141">Az áramkörhöz tartozó szolgáltatás szintje.</span><span class="sxs-lookup"><span data-stu-id="0caad-141">The tier of service for the circuit.</span></span> <span data-ttu-id="0caad-142">A paraméter lehetséges értékei a következők: `Standard` vagy `Premium` .</span><span class="sxs-lookup"><span data-stu-id="0caad-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="0caad-143">-Tag</span></span>
<span data-ttu-id="0caad-144">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="0caad-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0caad-145">Példa:</span><span class="sxs-lookup"><span data-stu-id="0caad-145">For example:</span></span>

<span data-ttu-id="0caad-146">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="0caad-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0caad-147">-Confirm</span></span>
<span data-ttu-id="0caad-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0caad-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0caad-149">-WhatIf</span></span>
<span data-ttu-id="0caad-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0caad-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0caad-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0caad-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0caad-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0caad-152">CommonParameters</span></span>
<span data-ttu-id="0caad-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0caad-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0caad-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0caad-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0caad-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0caad-155">INPUTS</span></span>

## <span data-ttu-id="0caad-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0caad-156">OUTPUTS</span></span>

### <span data-ttu-id="0caad-157">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0caad-157">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0caad-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0caad-158">NOTES</span></span>

## <span data-ttu-id="0caad-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0caad-159">RELATED LINKS</span></span>

[<span data-ttu-id="0caad-160">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0caad-160">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0caad-161">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0caad-161">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0caad-162">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0caad-162">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="0caad-163">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0caad-163">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
