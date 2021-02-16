---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206695"
---
# <span data-ttu-id="477d1-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="477d1-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="477d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="477d1-102">SYNOPSIS</span></span>
<span data-ttu-id="477d1-103">Kapcsolatfigyelő végpont létrehozása.</span><span class="sxs-lookup"><span data-stu-id="477d1-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="477d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="477d1-104">SYNTAX</span></span>

### <span data-ttu-id="477d1-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="477d1-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="477d1-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="477d1-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="477d1-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="477d1-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="477d1-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="477d1-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="477d1-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="477d1-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="477d1-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="477d1-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="477d1-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="477d1-111">DESCRIPTION</span></span>
<span data-ttu-id="477d1-112">New-AzNetworkWatcherConnectionMonitorEndpointObject parancsmag kapcsolatfigyelő végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="477d1-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="477d1-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="477d1-113">EXAMPLES</span></span>

### <span data-ttu-id="477d1-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="477d1-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="477d1-115">Név: workspaceEndpoint Type : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address : Scope : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span><span class="sxs-lookup"><span data-stu-id="477d1-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="477d1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="477d1-116">PARAMETERS</span></span>

### <span data-ttu-id="477d1-117">-Address</span><span class="sxs-lookup"><span data-stu-id="477d1-117">-Address</span></span>
<span data-ttu-id="477d1-118">A kapcsolatfigyelő végpont címe (IP vagy tartománynév).</span><span class="sxs-lookup"><span data-stu-id="477d1-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="477d1-119">-AzureSubnet</span></span>
<span data-ttu-id="477d1-120">Azure Alnet-végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="477d1-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="477d1-121">-AzureVM</span></span>
<span data-ttu-id="477d1-122">Azure VM végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="477d1-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="477d1-123">-AzureVNet</span></span>
<span data-ttu-id="477d1-124">Azure Vnet-végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="477d1-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="477d1-125">-CoverageLevel</span></span>
<span data-ttu-id="477d1-126">Tesztelje a végpont lefedettségét.</span><span class="sxs-lookup"><span data-stu-id="477d1-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="477d1-127">A támogatott értékek: Default, Low, BelowAverage, Average, AboveAvergae, Full.</span><span class="sxs-lookup"><span data-stu-id="477d1-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477d1-128">-DefaultProfile</span></span>
<span data-ttu-id="477d1-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="477d1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="477d1-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="477d1-130">-ExcludeItem</span></span>
<span data-ttu-id="477d1-131">Azon elemek listája, amelyeket ki kell zárni a végpontok hatóköre alól.</span><span class="sxs-lookup"><span data-stu-id="477d1-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="477d1-132">-ExternalAddress</span></span>
<span data-ttu-id="477d1-133">Külső cím végpont kapcsolója.</span><span class="sxs-lookup"><span data-stu-id="477d1-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="477d1-134">-IncludeItem</span></span>
<span data-ttu-id="477d1-135">Azon elemek listája, amelyeket a végpontok hatókörében meg kell jelenni.</span><span class="sxs-lookup"><span data-stu-id="477d1-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="477d1-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="477d1-137">MMA Workspace Machine végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="477d1-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="477d1-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="477d1-139">MMA Workspace Network végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="477d1-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-140">-Name</span><span class="sxs-lookup"><span data-stu-id="477d1-140">-Name</span></span>
<span data-ttu-id="477d1-141">A kapcsolatfigyelő végpont neve.</span><span class="sxs-lookup"><span data-stu-id="477d1-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="477d1-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="477d1-142">-ResourceId</span></span>
<span data-ttu-id="477d1-143">A kapcsolatfigyelő végpont erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="477d1-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d1-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="477d1-144">-Confirm</span></span>
<span data-ttu-id="477d1-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="477d1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="477d1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="477d1-146">-WhatIf</span></span>
<span data-ttu-id="477d1-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="477d1-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="477d1-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="477d1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="477d1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477d1-149">CommonParameters</span></span>
<span data-ttu-id="477d1-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="477d1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477d1-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="477d1-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477d1-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="477d1-152">INPUTS</span></span>

### <span data-ttu-id="477d1-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="477d1-153">None</span></span>

## <span data-ttu-id="477d1-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="477d1-154">OUTPUTS</span></span>

### <span data-ttu-id="477d1-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="477d1-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="477d1-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="477d1-156">NOTES</span></span>

## <span data-ttu-id="477d1-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="477d1-157">RELATED LINKS</span></span>
