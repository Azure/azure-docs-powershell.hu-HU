---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 63fda9c2f5b0231a2072483d4df05f6940b8fef8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837217"
---
# <span data-ttu-id="f20a6-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f20a6-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="f20a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f20a6-102">SYNOPSIS</span></span>
<span data-ttu-id="f20a6-103">Azure-ExpressRoutePort hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f20a6-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="f20a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f20a6-104">SYNTAX</span></span>

### <span data-ttu-id="f20a6-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f20a6-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20a6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f20a6-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f20a6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f20a6-107">DESCRIPTION</span></span>
<span data-ttu-id="f20a6-108">A **New-AzExpressRoutePort** parancsmag létrehoz egy Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f20a6-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="f20a6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f20a6-109">EXAMPLES</span></span>

### <span data-ttu-id="f20a6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f20a6-110">Example 1</span></span>
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

### <span data-ttu-id="f20a6-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="f20a6-111">Example 2</span></span>
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

## <span data-ttu-id="f20a6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f20a6-112">PARAMETERS</span></span>

### <span data-ttu-id="f20a6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f20a6-113">-AsJob</span></span>
<span data-ttu-id="f20a6-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f20a6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f20a6-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="f20a6-115">-BandwidthInGbps</span></span>
<span data-ttu-id="f20a6-116">A beszerzett portok sávszélessége a Gbps-ben</span><span class="sxs-lookup"><span data-stu-id="f20a6-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="f20a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20a6-117">-DefaultProfile</span></span>
<span data-ttu-id="f20a6-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f20a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f20a6-119">-Beágyazás</span><span class="sxs-lookup"><span data-stu-id="f20a6-119">-Encapsulation</span></span>
<span data-ttu-id="f20a6-120">Beágyazási módszer a fizikai portokon.</span><span class="sxs-lookup"><span data-stu-id="f20a6-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="f20a6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f20a6-121">-Force</span></span>
<span data-ttu-id="f20a6-122">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f20a6-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f20a6-123">– Identitás</span><span class="sxs-lookup"><span data-stu-id="f20a6-123">-Identity</span></span>
<span data-ttu-id="f20a6-124">Felhasználó által kiosztott identitás a MacSec-konfiguráció olvasásához</span><span class="sxs-lookup"><span data-stu-id="f20a6-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20a6-125">-Hivatkozás</span><span class="sxs-lookup"><span data-stu-id="f20a6-125">-Link</span></span>
<span data-ttu-id="f20a6-126">A ExpressRoutePort-erőforrás fizikai hivatkozásainak halmaza</span><span class="sxs-lookup"><span data-stu-id="f20a6-126">The set of physical links of the ExpressRoutePort resource</span></span>

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

### <span data-ttu-id="f20a6-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="f20a6-127">-Location</span></span>
<span data-ttu-id="f20a6-128">A hely.</span><span class="sxs-lookup"><span data-stu-id="f20a6-128">The location.</span></span>

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

### <span data-ttu-id="f20a6-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f20a6-129">-Name</span></span>
<span data-ttu-id="f20a6-130">A ExpressRoutePort neve.</span><span class="sxs-lookup"><span data-stu-id="f20a6-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="f20a6-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="f20a6-131">-PeeringLocation</span></span>
<span data-ttu-id="f20a6-132">Annak a megadási helynek a neve, amelyet a ExpressRoutePort fizikailag társítanak.</span><span class="sxs-lookup"><span data-stu-id="f20a6-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="f20a6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f20a6-133">-ResourceGroupName</span></span>
<span data-ttu-id="f20a6-134">A ExpressRoutePort erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f20a6-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="f20a6-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f20a6-135">-ResourceId</span></span>
<span data-ttu-id="f20a6-136">Az Express Route port ResourceId</span><span class="sxs-lookup"><span data-stu-id="f20a6-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="f20a6-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="f20a6-137">-Tag</span></span>
<span data-ttu-id="f20a6-138">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f20a6-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f20a6-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f20a6-139">-Confirm</span></span>
<span data-ttu-id="f20a6-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f20a6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f20a6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f20a6-141">-WhatIf</span></span>
<span data-ttu-id="f20a6-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f20a6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f20a6-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f20a6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f20a6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20a6-144">CommonParameters</span></span>
<span data-ttu-id="f20a6-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f20a6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20a6-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f20a6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20a6-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f20a6-147">INPUTS</span></span>

### <span data-ttu-id="f20a6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f20a6-148">System.String</span></span>

### <span data-ttu-id="f20a6-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f20a6-149">System.Int32</span></span>

### <span data-ttu-id="f20a6-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f20a6-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f20a6-151">Microsoft. Azure. commands. Network. models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="f20a6-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="f20a6-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f20a6-152">OUTPUTS</span></span>

### <span data-ttu-id="f20a6-153">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f20a6-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="f20a6-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f20a6-154">NOTES</span></span>

## <span data-ttu-id="f20a6-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f20a6-155">RELATED LINKS</span></span>

[<span data-ttu-id="f20a6-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f20a6-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="f20a6-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f20a6-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="f20a6-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f20a6-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
