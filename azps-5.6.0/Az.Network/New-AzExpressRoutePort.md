---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 380061134c94cdbd618aaa4d18ef39b0b3a11359
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935641"
---
# <span data-ttu-id="8cac3-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8cac3-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="8cac3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cac3-102">SYNOPSIS</span></span>
<span data-ttu-id="8cac3-103">Létrehoz egy Azure ExpressRoutePortot.</span><span class="sxs-lookup"><span data-stu-id="8cac3-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="8cac3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8cac3-104">SYNTAX</span></span>

### <span data-ttu-id="8cac3-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8cac3-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cac3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cac3-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cac3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8cac3-107">DESCRIPTION</span></span>
<span data-ttu-id="8cac3-108">A **New-AzExpressRoutePort** parancsmag létrehoz egy Azure ExpressRoutePortot</span><span class="sxs-lookup"><span data-stu-id="8cac3-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="8cac3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8cac3-109">EXAMPLES</span></span>

### <span data-ttu-id="8cac3-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="8cac3-110">Example 1</span></span>
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

### <span data-ttu-id="8cac3-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="8cac3-111">Example 2</span></span>
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

## <span data-ttu-id="8cac3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cac3-112">PARAMETERS</span></span>

### <span data-ttu-id="8cac3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cac3-113">-AsJob</span></span>
<span data-ttu-id="8cac3-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8cac3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cac3-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="8cac3-115">-BandwidthInGbps</span></span>
<span data-ttu-id="8cac3-116">A portok sávszélessége Angol fontban</span><span class="sxs-lookup"><span data-stu-id="8cac3-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="8cac3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cac3-117">-DefaultProfile</span></span>
<span data-ttu-id="8cac3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cac3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cac3-119">-Encapsulation</span><span class="sxs-lookup"><span data-stu-id="8cac3-119">-Encapsulation</span></span>
<span data-ttu-id="8cac3-120">Encapsulation method on physical ports.</span><span class="sxs-lookup"><span data-stu-id="8cac3-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="8cac3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8cac3-121">-Force</span></span>
<span data-ttu-id="8cac3-122">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="8cac3-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8cac3-123">-Identity</span><span class="sxs-lookup"><span data-stu-id="8cac3-123">-Identity</span></span>
<span data-ttu-id="8cac3-124">Felhasználóhoz rendelt identitás a MacSec-konfiguráció olvasásához</span><span class="sxs-lookup"><span data-stu-id="8cac3-124">User Assigned Identity for reading MacSec configuration</span></span>

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

### <span data-ttu-id="8cac3-125">-Link</span><span class="sxs-lookup"><span data-stu-id="8cac3-125">-Link</span></span>
<span data-ttu-id="8cac3-126">Az ExpressRoutePort erőforrás fizikai kapcsolatainak halmaza</span><span class="sxs-lookup"><span data-stu-id="8cac3-126">The set of physical links of the ExpressRoutePort resource</span></span>

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

### <span data-ttu-id="8cac3-127">-Location</span><span class="sxs-lookup"><span data-stu-id="8cac3-127">-Location</span></span>
<span data-ttu-id="8cac3-128">A hely.</span><span class="sxs-lookup"><span data-stu-id="8cac3-128">The location.</span></span>

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

### <span data-ttu-id="8cac3-129">-Name</span><span class="sxs-lookup"><span data-stu-id="8cac3-129">-Name</span></span>
<span data-ttu-id="8cac3-130">Az ExpressRoutePort neve.</span><span class="sxs-lookup"><span data-stu-id="8cac3-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="8cac3-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="8cac3-131">-PeeringLocation</span></span>
<span data-ttu-id="8cac3-132">Annak a társviszony-létesítési helynek a neve, amelyhez az ExpressRoutePort fizikailag megfeleltetve van.</span><span class="sxs-lookup"><span data-stu-id="8cac3-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="8cac3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cac3-133">-ResourceGroupName</span></span>
<span data-ttu-id="8cac3-134">Az ExpressRoutePort erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="8cac3-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="8cac3-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cac3-135">-ResourceId</span></span>
<span data-ttu-id="8cac3-136">Az expressz útvonalport Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="8cac3-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="8cac3-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="8cac3-137">-Tag</span></span>
<span data-ttu-id="8cac3-138">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="8cac3-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8cac3-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cac3-139">-Confirm</span></span>
<span data-ttu-id="8cac3-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8cac3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cac3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cac3-141">-WhatIf</span></span>
<span data-ttu-id="8cac3-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8cac3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cac3-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8cac3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cac3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cac3-144">CommonParameters</span></span>
<span data-ttu-id="8cac3-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cac3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cac3-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cac3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cac3-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8cac3-147">INPUTS</span></span>

### <span data-ttu-id="8cac3-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8cac3-148">System.String</span></span>

### <span data-ttu-id="8cac3-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8cac3-149">System.Int32</span></span>

### <span data-ttu-id="8cac3-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8cac3-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8cac3-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span><span class="sxs-lookup"><span data-stu-id="8cac3-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="8cac3-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cac3-152">OUTPUTS</span></span>

### <span data-ttu-id="8cac3-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8cac3-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="8cac3-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8cac3-154">NOTES</span></span>

## <span data-ttu-id="8cac3-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cac3-155">RELATED LINKS</span></span>

[<span data-ttu-id="8cac3-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8cac3-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="8cac3-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8cac3-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="8cac3-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8cac3-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
