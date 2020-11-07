---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: d03b52c477686f3aa724057771285eaf9d522a56
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841362"
---
# <span data-ttu-id="4696e-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4696e-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="4696e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4696e-102">SYNOPSIS</span></span>
<span data-ttu-id="4696e-103">Azure Express útvonal-áramkört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4696e-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="4696e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4696e-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4696e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4696e-105">DESCRIPTION</span></span>
<span data-ttu-id="4696e-106">A **New-AzExpressRouteCircuit** parancsmag az Azure Express útvonal-áramkört hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4696e-106">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="4696e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4696e-107">EXAMPLES</span></span>

### <span data-ttu-id="4696e-108">Példa 1: új ExpressRoute-áramkör létrehozása</span><span class="sxs-lookup"><span data-stu-id="4696e-108">Example 1: Create a new ExpressRoute circuit</span></span>
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
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="4696e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4696e-109">PARAMETERS</span></span>

### <span data-ttu-id="4696e-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="4696e-110">-AllowClassicOperations</span></span>
<span data-ttu-id="4696e-111">A paraméter használata lehetővé teszi, hogy a klasszikus Azure PowerShell-parancsmagok használatával kezelje az áramkört.</span><span class="sxs-lookup"><span data-stu-id="4696e-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="4696e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4696e-112">-AsJob</span></span>
<span data-ttu-id="4696e-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4696e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4696e-114">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="4696e-114">-Authorization</span></span>
<span data-ttu-id="4696e-115">Az áramkör-engedélyezési listák listája.</span><span class="sxs-lookup"><span data-stu-id="4696e-115">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="4696e-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="4696e-116">-BandwidthInMbps</span></span>
<span data-ttu-id="4696e-117">Az áramkör sávszélessége.</span><span class="sxs-lookup"><span data-stu-id="4696e-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="4696e-118">Ennek a szolgáltató által támogatott értéknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4696e-118">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="4696e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4696e-119">-DefaultProfile</span></span>
<span data-ttu-id="4696e-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4696e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4696e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4696e-121">-Force</span></span>
<span data-ttu-id="4696e-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4696e-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4696e-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="4696e-123">-Location</span></span>
<span data-ttu-id="4696e-124">Az áramkör helye.</span><span class="sxs-lookup"><span data-stu-id="4696e-124">The location of the circuit.</span></span>

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

### <span data-ttu-id="4696e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4696e-125">-Name</span></span>
<span data-ttu-id="4696e-126">A létrehozandó ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="4696e-126">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="4696e-127">-Társközi</span><span class="sxs-lookup"><span data-stu-id="4696e-127">-Peering</span></span>
<span data-ttu-id="4696e-128">A lista társközi konfigurációi.</span><span class="sxs-lookup"><span data-stu-id="4696e-128">A list peer configurations.</span></span>

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

### <span data-ttu-id="4696e-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="4696e-129">-PeeringLocation</span></span>
<span data-ttu-id="4696e-130">A szolgáltató által támogatott társközi hely neve.</span><span class="sxs-lookup"><span data-stu-id="4696e-130">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="4696e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4696e-131">-ResourceGroupName</span></span>
<span data-ttu-id="4696e-132">Az az erőforráscsoport, amely az áramkört fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="4696e-132">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="4696e-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="4696e-133">-ServiceProviderName</span></span>
<span data-ttu-id="4696e-134">Az áramkör-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="4696e-134">The name of the circuit service provider.</span></span> <span data-ttu-id="4696e-135">Ennek egyeznie kell a Get-AzExpressRouteServiceProvider parancsmag által megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="4696e-135">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="4696e-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="4696e-136">-SkuFamily</span></span>
<span data-ttu-id="4696e-137">A SKU család a számlázási típust határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4696e-137">SKU family determines the billing type.</span></span> <span data-ttu-id="4696e-138">A paraméter lehetséges értékei a következők: `MeteredData` vagy `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="4696e-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="4696e-139">Ne feledje, hogy a MeteredData-ról UnlimitedData-ra változtathatja a számlázási típust, de a UnlimitedData-től az MeteredData-be nem változtathatja azt.</span><span class="sxs-lookup"><span data-stu-id="4696e-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="4696e-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4696e-140">-SkuTier</span></span>
<span data-ttu-id="4696e-141">Az áramkörhöz tartozó szolgáltatás szintje.</span><span class="sxs-lookup"><span data-stu-id="4696e-141">The tier of service for the circuit.</span></span> <span data-ttu-id="4696e-142">A paraméter lehetséges értékei a következők: `Standard` vagy `Premium` .</span><span class="sxs-lookup"><span data-stu-id="4696e-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

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

### <span data-ttu-id="4696e-143">-Címke</span><span class="sxs-lookup"><span data-stu-id="4696e-143">-Tag</span></span>
<span data-ttu-id="4696e-144">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="4696e-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4696e-145">Példa:</span><span class="sxs-lookup"><span data-stu-id="4696e-145">For example:</span></span>

<span data-ttu-id="4696e-146">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="4696e-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4696e-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4696e-147">-Confirm</span></span>
<span data-ttu-id="4696e-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4696e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4696e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4696e-149">-WhatIf</span></span>
<span data-ttu-id="4696e-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4696e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4696e-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4696e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4696e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4696e-152">CommonParameters</span></span>
<span data-ttu-id="4696e-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4696e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4696e-154">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4696e-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4696e-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4696e-155">INPUTS</span></span>

## <span data-ttu-id="4696e-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4696e-156">OUTPUTS</span></span>

### <span data-ttu-id="4696e-157">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4696e-157">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4696e-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4696e-158">NOTES</span></span>

## <span data-ttu-id="4696e-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4696e-159">RELATED LINKS</span></span>

[<span data-ttu-id="4696e-160">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4696e-160">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4696e-161">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4696e-161">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="4696e-162">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4696e-162">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="4696e-163">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4696e-163">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
