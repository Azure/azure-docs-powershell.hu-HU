---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
ms.openlocfilehash: 8d3b204815fc273f97a549582a193002f5f4a48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495041"
---
# <span data-ttu-id="152c0-101">New-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="152c0-101">New-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="152c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="152c0-102">SYNOPSIS</span></span>
<span data-ttu-id="152c0-103">Azure-ExpressRoutePort hoz létre.</span><span class="sxs-lookup"><span data-stu-id="152c0-103">Creates an Azure ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="152c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="152c0-104">SYNTAX</span></span>

### <span data-ttu-id="152c0-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="152c0-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="152c0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="152c0-106">ResourceIdParameterSet</span></span>
```
New-AzureRmExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="152c0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="152c0-107">DESCRIPTION</span></span>
<span data-ttu-id="152c0-108">A **New-AzureRmExpressRoutePort** parancsmag létrehoz egy Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="152c0-108">The **New-AzureRmExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="152c0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="152c0-109">EXAMPLES</span></span>

### <span data-ttu-id="152c0-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="152c0-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

### <span data-ttu-id="152c0-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="152c0-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

## <span data-ttu-id="152c0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="152c0-112">PARAMETERS</span></span>

### <span data-ttu-id="152c0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="152c0-113">-AsJob</span></span>
<span data-ttu-id="152c0-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="152c0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="152c0-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="152c0-115">-BandwidthInGbps</span></span>
<span data-ttu-id="152c0-116">A beszerzett portok sávszélessége a Gbps-ben</span><span class="sxs-lookup"><span data-stu-id="152c0-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="152c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152c0-117">-DefaultProfile</span></span>
<span data-ttu-id="152c0-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="152c0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="152c0-119">-Beágyazás</span><span class="sxs-lookup"><span data-stu-id="152c0-119">-Encapsulation</span></span>
<span data-ttu-id="152c0-120">Beágyazási módszer a fizikai portokon.</span><span class="sxs-lookup"><span data-stu-id="152c0-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="152c0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="152c0-121">-Force</span></span>
<span data-ttu-id="152c0-122">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="152c0-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="152c0-123">-Hivatkozás</span><span class="sxs-lookup"><span data-stu-id="152c0-123">-Link</span></span>
<span data-ttu-id="152c0-124">A ExpressRoutePort-erőforrás fizikai hivatkozásainak halmaza</span><span class="sxs-lookup"><span data-stu-id="152c0-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="152c0-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="152c0-125">-Location</span></span>
<span data-ttu-id="152c0-126">A hely.</span><span class="sxs-lookup"><span data-stu-id="152c0-126">The location.</span></span>

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

### <span data-ttu-id="152c0-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="152c0-127">-Name</span></span>
<span data-ttu-id="152c0-128">A ExpressRoutePort neve.</span><span class="sxs-lookup"><span data-stu-id="152c0-128">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="152c0-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="152c0-129">-PeeringLocation</span></span>
<span data-ttu-id="152c0-130">Annak a megadási helynek a neve, amelyet a ExpressRoutePort fizikailag társítanak.</span><span class="sxs-lookup"><span data-stu-id="152c0-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="152c0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="152c0-131">-ResourceGroupName</span></span>
<span data-ttu-id="152c0-132">A ExpressRoutePort erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="152c0-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="152c0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="152c0-133">-ResourceId</span></span>
<span data-ttu-id="152c0-134">Az Express Route port ResourceId</span><span class="sxs-lookup"><span data-stu-id="152c0-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="152c0-135">-Címke</span><span class="sxs-lookup"><span data-stu-id="152c0-135">-Tag</span></span>
<span data-ttu-id="152c0-136">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="152c0-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="152c0-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="152c0-137">-Confirm</span></span>
<span data-ttu-id="152c0-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="152c0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="152c0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="152c0-139">-WhatIf</span></span>
<span data-ttu-id="152c0-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="152c0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="152c0-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="152c0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="152c0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152c0-142">CommonParameters</span></span>
<span data-ttu-id="152c0-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="152c0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152c0-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="152c0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152c0-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="152c0-145">INPUTS</span></span>

### <span data-ttu-id="152c0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="152c0-146">System.String</span></span>

### <span data-ttu-id="152c0-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="152c0-147">System.Int32</span></span>

### <span data-ttu-id="152c0-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="152c0-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="152c0-149">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSExpressRouteLink, Microsoft. Azure. commands. Network, Version = 6.3.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="152c0-149">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink, Microsoft.Azure.Commands.Network, Version=6.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="152c0-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="152c0-150">OUTPUTS</span></span>

### <span data-ttu-id="152c0-151">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="152c0-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="152c0-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="152c0-152">NOTES</span></span>

## <span data-ttu-id="152c0-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="152c0-153">RELATED LINKS</span></span>
