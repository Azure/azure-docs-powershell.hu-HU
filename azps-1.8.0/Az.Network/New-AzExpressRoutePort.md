---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 7f6b68b02644b8244459398028680c9872fffa84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670346"
---
# <span data-ttu-id="723ad-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="723ad-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="723ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="723ad-102">SYNOPSIS</span></span>
<span data-ttu-id="723ad-103">Azure-ExpressRoutePort hoz létre.</span><span class="sxs-lookup"><span data-stu-id="723ad-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="723ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="723ad-104">SYNTAX</span></span>

### <span data-ttu-id="723ad-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="723ad-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="723ad-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="723ad-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="723ad-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="723ad-107">DESCRIPTION</span></span>
<span data-ttu-id="723ad-108">A **New-AzExpressRoutePort** parancsmag létrehoz egy Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="723ad-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="723ad-109">Példák</span><span class="sxs-lookup"><span data-stu-id="723ad-109">EXAMPLES</span></span>

### <span data-ttu-id="723ad-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="723ad-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="723ad-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="723ad-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="723ad-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="723ad-112">PARAMETERS</span></span>

### <span data-ttu-id="723ad-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="723ad-113">-AsJob</span></span>
<span data-ttu-id="723ad-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="723ad-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="723ad-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="723ad-115">-BandwidthInGbps</span></span>
<span data-ttu-id="723ad-116">A beszerzett portok sávszélessége a Gbps-ben</span><span class="sxs-lookup"><span data-stu-id="723ad-116">Bandwidth of procured ports in Gbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723ad-117">-DefaultProfile</span></span>
<span data-ttu-id="723ad-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="723ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="723ad-119">-Beágyazás</span><span class="sxs-lookup"><span data-stu-id="723ad-119">-Encapsulation</span></span>
<span data-ttu-id="723ad-120">Beágyazási módszer a fizikai portokon.</span><span class="sxs-lookup"><span data-stu-id="723ad-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="723ad-121">-Force</span><span class="sxs-lookup"><span data-stu-id="723ad-121">-Force</span></span>
<span data-ttu-id="723ad-122">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="723ad-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="723ad-123">-Hivatkozás</span><span class="sxs-lookup"><span data-stu-id="723ad-123">-Link</span></span>
<span data-ttu-id="723ad-124">A ExpressRoutePort-erőforrás fizikai hivatkozásainak halmaza</span><span class="sxs-lookup"><span data-stu-id="723ad-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723ad-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="723ad-125">-Location</span></span>
<span data-ttu-id="723ad-126">A hely.</span><span class="sxs-lookup"><span data-stu-id="723ad-126">The location.</span></span>

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

### <span data-ttu-id="723ad-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="723ad-127">-Name</span></span>
<span data-ttu-id="723ad-128">A ExpressRoutePort neve.</span><span class="sxs-lookup"><span data-stu-id="723ad-128">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723ad-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="723ad-129">-PeeringLocation</span></span>
<span data-ttu-id="723ad-130">Annak a megadási helynek a neve, amelyet a ExpressRoutePort fizikailag társítanak.</span><span class="sxs-lookup"><span data-stu-id="723ad-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="723ad-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="723ad-131">-ResourceGroupName</span></span>
<span data-ttu-id="723ad-132">A ExpressRoutePort erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="723ad-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723ad-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="723ad-133">-ResourceId</span></span>
<span data-ttu-id="723ad-134">Az Express Route port ResourceId</span><span class="sxs-lookup"><span data-stu-id="723ad-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723ad-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="723ad-135">-Tag</span></span>
<span data-ttu-id="723ad-136">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="723ad-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="723ad-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="723ad-137">-Confirm</span></span>
<span data-ttu-id="723ad-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="723ad-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="723ad-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="723ad-139">-WhatIf</span></span>
<span data-ttu-id="723ad-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="723ad-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="723ad-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="723ad-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="723ad-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723ad-142">CommonParameters</span></span>
<span data-ttu-id="723ad-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="723ad-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723ad-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="723ad-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723ad-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="723ad-145">INPUTS</span></span>

### <span data-ttu-id="723ad-146">System. String</span><span class="sxs-lookup"><span data-stu-id="723ad-146">System.String</span></span>

### <span data-ttu-id="723ad-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="723ad-147">System.Int32</span></span>

### <span data-ttu-id="723ad-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="723ad-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="723ad-149">Microsoft. Azure. commands. Network. models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="723ad-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="723ad-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="723ad-150">OUTPUTS</span></span>

### <span data-ttu-id="723ad-151">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="723ad-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="723ad-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="723ad-152">NOTES</span></span>

## <span data-ttu-id="723ad-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="723ad-153">RELATED LINKS</span></span>

[<span data-ttu-id="723ad-154">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="723ad-154">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="723ad-155">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="723ad-155">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="723ad-156">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="723ad-156">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
