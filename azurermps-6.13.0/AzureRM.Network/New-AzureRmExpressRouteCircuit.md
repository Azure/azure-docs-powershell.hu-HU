---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: cee0318367ad764a9cc9e37995f092462cd157a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495920"
---
# <span data-ttu-id="a2301-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a2301-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="a2301-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2301-102">SYNOPSIS</span></span>
<span data-ttu-id="a2301-103">Azure Express útvonal-áramkört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a2301-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2301-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2301-104">SYNTAX</span></span>

### <span data-ttu-id="a2301-105">Szolgáltató</span><span class="sxs-lookup"><span data-stu-id="a2301-105">ServiceProvider</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ServiceProviderName <String>] [-PeeringLocation <String>]
 [-BandwidthInMbps <Int32>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2301-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a2301-106">ExpressRoutePort</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ExpressRoutePort <PSExpressRoutePort>] [-BandwidthInGbps <Double>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2301-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2301-107">DESCRIPTION</span></span>
<span data-ttu-id="a2301-108">A **New-AzureRmExpressRouteCircuit** parancsmag az Azure Express útvonal-áramkört hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a2301-108">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="a2301-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a2301-109">EXAMPLES</span></span>

### <span data-ttu-id="a2301-110">Példa 1: új ExpressRoute-áramkör létrehozása</span><span class="sxs-lookup"><span data-stu-id="a2301-110">Example 1: Create a new ExpressRoute circuit</span></span>
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

### <span data-ttu-id="a2301-111">2. példa: új ExpressRoute-áramkör létrehozása a ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a2301-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="a2301-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2301-112">PARAMETERS</span></span>

### <span data-ttu-id="a2301-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="a2301-113">-AllowClassicOperations</span></span>
<span data-ttu-id="a2301-114">A paraméter használata lehetővé teszi, hogy a klasszikus Azure PowerShell-parancsmagok használatával kezelje az áramkört.</span><span class="sxs-lookup"><span data-stu-id="a2301-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="a2301-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2301-115">-AsJob</span></span>
<span data-ttu-id="a2301-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a2301-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2301-117">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="a2301-117">-Authorization</span></span>
<span data-ttu-id="a2301-118">Az áramkör-engedélyezési listák listája.</span><span class="sxs-lookup"><span data-stu-id="a2301-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="a2301-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="a2301-119">-BandwidthInGbps</span></span>
<span data-ttu-id="a2301-120">Az áramkör sávszélessége, ha az áramkör egy ExpressRoutePort-erőforráson van kiépítve.</span><span class="sxs-lookup"><span data-stu-id="a2301-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2301-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="a2301-121">-BandwidthInMbps</span></span>
<span data-ttu-id="a2301-122">Az áramkör sávszélessége.</span><span class="sxs-lookup"><span data-stu-id="a2301-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="a2301-123">Ennek a szolgáltató által támogatott értéknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a2301-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2301-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2301-124">-DefaultProfile</span></span>
<span data-ttu-id="a2301-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2301-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2301-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a2301-126">-ExpressRoutePort</span></span>
<span data-ttu-id="a2301-127">A ExpressRoutePort-erőforrás hivatkozása, ha az áramkör egy ExpressRoutePort-erőforráson van kiépítve.</span><span class="sxs-lookup"><span data-stu-id="a2301-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2301-128">-Force</span><span class="sxs-lookup"><span data-stu-id="a2301-128">-Force</span></span>
<span data-ttu-id="a2301-129">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a2301-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a2301-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="a2301-130">-Location</span></span>
<span data-ttu-id="a2301-131">Az áramkör helye.</span><span class="sxs-lookup"><span data-stu-id="a2301-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="a2301-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2301-132">-Name</span></span>
<span data-ttu-id="a2301-133">A létrehozandó ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="a2301-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="a2301-134">-Társközi</span><span class="sxs-lookup"><span data-stu-id="a2301-134">-Peering</span></span>
<span data-ttu-id="a2301-135">A lista társközi konfigurációi.</span><span class="sxs-lookup"><span data-stu-id="a2301-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="a2301-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="a2301-136">-PeeringLocation</span></span>
<span data-ttu-id="a2301-137">A szolgáltató által támogatott társközi hely neve.</span><span class="sxs-lookup"><span data-stu-id="a2301-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2301-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2301-138">-ResourceGroupName</span></span>
<span data-ttu-id="a2301-139">Az az erőforráscsoport, amely az áramkört fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="a2301-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="a2301-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="a2301-140">-ServiceProviderName</span></span>
<span data-ttu-id="a2301-141">Az áramkör-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="a2301-141">The name of the circuit service provider.</span></span> <span data-ttu-id="a2301-142">Ennek egyeznie kell a Get-AzureRmExpressRouteServiceProvider parancsmag által megadott névvel.</span><span class="sxs-lookup"><span data-stu-id="a2301-142">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2301-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="a2301-143">-SkuFamily</span></span>
<span data-ttu-id="a2301-144">A SKU család a számlázási típust határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a2301-144">SKU family determines the billing type.</span></span> <span data-ttu-id="a2301-145">A paraméter lehetséges értékei a következők: `MeteredData` vagy `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="a2301-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="a2301-146">Ne feledje, hogy a MeteredData-ról UnlimitedData-ra változtathatja a számlázási típust, de a UnlimitedData-től az MeteredData-be nem változtathatja azt.</span><span class="sxs-lookup"><span data-stu-id="a2301-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="a2301-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a2301-147">-SkuTier</span></span>
<span data-ttu-id="a2301-148">Az áramkörhöz tartozó szolgáltatás szintje.</span><span class="sxs-lookup"><span data-stu-id="a2301-148">The tier of service for the circuit.</span></span> <span data-ttu-id="a2301-149">A paraméter lehetséges értékei a következők: `Standard` vagy `Premium` .</span><span class="sxs-lookup"><span data-stu-id="a2301-149">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2301-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="a2301-150">-Tag</span></span>
<span data-ttu-id="a2301-151">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="a2301-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a2301-152">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="a2301-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a2301-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2301-153">-Confirm</span></span>
<span data-ttu-id="a2301-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2301-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2301-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2301-155">-WhatIf</span></span>
<span data-ttu-id="a2301-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2301-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2301-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2301-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2301-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2301-158">CommonParameters</span></span>
<span data-ttu-id="a2301-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2301-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2301-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2301-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2301-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2301-161">INPUTS</span></span>

### <span data-ttu-id="a2301-162">System. String</span><span class="sxs-lookup"><span data-stu-id="a2301-162">System.String</span></span>

### <span data-ttu-id="a2301-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a2301-163">System.Int32</span></span>

### <span data-ttu-id="a2301-164">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSPeering, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a2301-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPeering, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a2301-165">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSExpressRouteCircuitAuthorization, Microsoft. Azure. commands. Network, Version = 6.4.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a2301-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a2301-166">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a2301-166">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a2301-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2301-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a2301-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2301-168">OUTPUTS</span></span>

### <span data-ttu-id="a2301-169">Microsoft. Azure. commands. Network. models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a2301-169">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a2301-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2301-170">NOTES</span></span>

## <span data-ttu-id="a2301-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2301-171">RELATED LINKS</span></span>

[<span data-ttu-id="a2301-172">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a2301-172">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a2301-173">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a2301-173">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a2301-174">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a2301-174">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a2301-175">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a2301-175">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
