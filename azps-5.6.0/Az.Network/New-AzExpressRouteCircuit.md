---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: af552e1320d9a935255d3649648ac103cfc08756
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938041"
---
# <span data-ttu-id="2f680-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f680-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="2f680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f680-102">SYNOPSIS</span></span>
<span data-ttu-id="2f680-103">Létrehoz egy Azure Express útvonal-áramkört.</span><span class="sxs-lookup"><span data-stu-id="2f680-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="2f680-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2f680-104">SYNTAX</span></span>

### <span data-ttu-id="2f680-105">ServiceProvider (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f680-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f680-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2f680-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f680-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2f680-107">DESCRIPTION</span></span>
<span data-ttu-id="2f680-108">A **New-AzExpressRouteCircuit** parancsmag létrehoz egy Azure Express útvonal-áramkört.</span><span class="sxs-lookup"><span data-stu-id="2f680-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="2f680-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2f680-109">EXAMPLES</span></span>

### <span data-ttu-id="2f680-110">1. példa: Új ExpressRoute-áramkör létrehozása</span><span class="sxs-lookup"><span data-stu-id="2f680-110">Example 1: Create a new ExpressRoute circuit</span></span>
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

### <span data-ttu-id="2f680-111">2. példa: Új ExpressRoute-áramkör létrehozása az ExpressRoutePorton</span><span class="sxs-lookup"><span data-stu-id="2f680-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
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

## <span data-ttu-id="2f680-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f680-112">PARAMETERS</span></span>

### <span data-ttu-id="2f680-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="2f680-113">-AllowClassicOperations</span></span>
<span data-ttu-id="2f680-114">A paraméter használatával a klasszikus Azure PowerShell-parancsmagok használatával kezelheti az áramkört.</span><span class="sxs-lookup"><span data-stu-id="2f680-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="2f680-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f680-115">-AsJob</span></span>
<span data-ttu-id="2f680-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2f680-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f680-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="2f680-117">-Authorization</span></span>
<span data-ttu-id="2f680-118">Az áramköri engedélyek listája.</span><span class="sxs-lookup"><span data-stu-id="2f680-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="2f680-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="2f680-119">-BandwidthInGbps</span></span>
<span data-ttu-id="2f680-120">Az áramkör sávszélessége, amikor az áramkört ExpressRoutePort-erőforráson létesítik.</span><span class="sxs-lookup"><span data-stu-id="2f680-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="2f680-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="2f680-121">-BandwidthInMbps</span></span>
<span data-ttu-id="2f680-122">Az áramkör sávszélessége.</span><span class="sxs-lookup"><span data-stu-id="2f680-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="2f680-123">Ennek olyan értéknek kell lennie, amelyet a szolgáltató támogat.</span><span class="sxs-lookup"><span data-stu-id="2f680-123">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="2f680-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f680-124">-DefaultProfile</span></span>
<span data-ttu-id="2f680-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f680-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f680-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2f680-126">-ExpressRoutePort</span></span>
<span data-ttu-id="2f680-127">Az ExpressRoutePort-erőforrásra való hivatkozás, amikor az áramkört ExpressRoutePort-erőforráson létesítik.</span><span class="sxs-lookup"><span data-stu-id="2f680-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="2f680-128">-Force</span><span class="sxs-lookup"><span data-stu-id="2f680-128">-Force</span></span>
<span data-ttu-id="2f680-129">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="2f680-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2f680-130">-Location</span><span class="sxs-lookup"><span data-stu-id="2f680-130">-Location</span></span>
<span data-ttu-id="2f680-131">Az áramkör helye.</span><span class="sxs-lookup"><span data-stu-id="2f680-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="2f680-132">-Name</span><span class="sxs-lookup"><span data-stu-id="2f680-132">-Name</span></span>
<span data-ttu-id="2f680-133">A létrehozott ExpressRoute-áramkör neve.</span><span class="sxs-lookup"><span data-stu-id="2f680-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="2f680-134">-Társviszony</span><span class="sxs-lookup"><span data-stu-id="2f680-134">-Peering</span></span>
<span data-ttu-id="2f680-135">Lista társkonfigurációi.</span><span class="sxs-lookup"><span data-stu-id="2f680-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="2f680-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="2f680-136">-PeeringLocation</span></span>
<span data-ttu-id="2f680-137">A szolgáltató által támogatott társviszony-létesítő hely neve.</span><span class="sxs-lookup"><span data-stu-id="2f680-137">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="2f680-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f680-138">-ResourceGroupName</span></span>
<span data-ttu-id="2f680-139">Az áramkört tartalmazó erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="2f680-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="2f680-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="2f680-140">-ServiceProviderName</span></span>
<span data-ttu-id="2f680-141">Az áramkör-szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="2f680-141">The name of the circuit service provider.</span></span> <span data-ttu-id="2f680-142">Ennek meg kell egyeznie a Get-AzExpressRouteServiceProvider nevével.</span><span class="sxs-lookup"><span data-stu-id="2f680-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="2f680-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="2f680-143">-SkuFamily</span></span>
<span data-ttu-id="2f680-144">Az SKU-család határozza meg a számlázási típust.</span><span class="sxs-lookup"><span data-stu-id="2f680-144">SKU family determines the billing type.</span></span> <span data-ttu-id="2f680-145">A paraméter lehetséges értékei: `MeteredData` vagy `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="2f680-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="2f680-146">Ne feledje, hogy a számlázási típust forgalmi díjas adatról Korlátlan Adat típusra módosíthatja, de nem módosíthatja a típust UnlimitedData-ről Forgalmi díjas adatokra.</span><span class="sxs-lookup"><span data-stu-id="2f680-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="2f680-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2f680-147">-SkuTier</span></span>
<span data-ttu-id="2f680-148">Az áramkör szolgáltatási rétege.</span><span class="sxs-lookup"><span data-stu-id="2f680-148">The tier of service for the circuit.</span></span> <span data-ttu-id="2f680-149">A paraméter lehetséges értékei: `Standard` vagy `Premium` `Local` .</span><span class="sxs-lookup"><span data-stu-id="2f680-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

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

### <span data-ttu-id="2f680-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="2f680-150">-Tag</span></span>
<span data-ttu-id="2f680-151">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="2f680-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2f680-152">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="2f680-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2f680-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f680-153">-Confirm</span></span>
<span data-ttu-id="2f680-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2f680-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f680-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f680-155">-WhatIf</span></span>
<span data-ttu-id="2f680-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2f680-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f680-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f680-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f680-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f680-158">CommonParameters</span></span>
<span data-ttu-id="2f680-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f680-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f680-160">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f680-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f680-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f680-161">INPUTS</span></span>

### <span data-ttu-id="2f680-162">System.String</span><span class="sxs-lookup"><span data-stu-id="2f680-162">System.String</span></span>

### <span data-ttu-id="2f680-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2f680-163">System.Int32</span></span>

### <span data-ttu-id="2f680-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2f680-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="2f680-165">System.Double</span><span class="sxs-lookup"><span data-stu-id="2f680-165">System.Double</span></span>

### <span data-ttu-id="2f680-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span><span class="sxs-lookup"><span data-stu-id="2f680-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="2f680-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span><span class="sxs-lookup"><span data-stu-id="2f680-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="2f680-168">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2f680-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2f680-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2f680-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2f680-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f680-170">OUTPUTS</span></span>

### <span data-ttu-id="2f680-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f680-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2f680-172">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2f680-172">NOTES</span></span>

## <span data-ttu-id="2f680-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f680-173">RELATED LINKS</span></span>

[<span data-ttu-id="2f680-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f680-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="2f680-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f680-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="2f680-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f680-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="2f680-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f680-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
