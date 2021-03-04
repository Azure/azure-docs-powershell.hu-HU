---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 385301bf9cab32474aea59937de09003356a5798
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921881"
---
# <span data-ttu-id="f7f3a-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="f7f3a-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="f7f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f3a-103">Kapcsolatfigyelő végpont létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="f7f3a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7f3a-104">SYNTAX</span></span>

### <span data-ttu-id="f7f3a-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f7f3a-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f3a-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="f7f3a-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f3a-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="f7f3a-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f3a-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="f7f3a-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f3a-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="f7f3a-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f3a-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="f7f3a-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f3a-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7f3a-111">DESCRIPTION</span></span>
<span data-ttu-id="f7f3a-112">New-AzNetworkWatcherConnectionMonitorEndpointObject parancsmag kapcsolatfigyelő végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="f7f3a-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7f3a-113">EXAMPLES</span></span>

### <span data-ttu-id="f7f3a-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="f7f3a-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="f7f3a-115">Név: workspaceEndpoint Type : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address : Scope : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span><span class="sxs-lookup"><span data-stu-id="f7f3a-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="f7f3a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7f3a-116">PARAMETERS</span></span>

### <span data-ttu-id="f7f3a-117">-Address</span><span class="sxs-lookup"><span data-stu-id="f7f3a-117">-Address</span></span>
<span data-ttu-id="f7f3a-118">A kapcsolatfigyelő végpont címe (IP vagy tartománynév).</span><span class="sxs-lookup"><span data-stu-id="f7f3a-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

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

### <span data-ttu-id="f7f3a-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="f7f3a-119">-AzureSubnet</span></span>
<span data-ttu-id="f7f3a-120">Azure Alnet-végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-120">Azure Subnet endpoint switch.</span></span>

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

### <span data-ttu-id="f7f3a-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f7f3a-121">-AzureVM</span></span>
<span data-ttu-id="f7f3a-122">Azure VM végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-122">Azure VM endpoint switch.</span></span>

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

### <span data-ttu-id="f7f3a-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="f7f3a-123">-AzureVNet</span></span>
<span data-ttu-id="f7f3a-124">Azure Vnet-végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-124">Azure Vnet endpoint switch.</span></span>

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

### <span data-ttu-id="f7f3a-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="f7f3a-125">-CoverageLevel</span></span>
<span data-ttu-id="f7f3a-126">Tesztelje a végpont lefedettségét.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="f7f3a-127">A támogatott értékek: Default, Low, BelowAverage, Average, AboveAvergae, Full.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

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

### <span data-ttu-id="f7f3a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f3a-128">-DefaultProfile</span></span>
<span data-ttu-id="f7f3a-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7f3a-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="f7f3a-130">-ExcludeItem</span></span>
<span data-ttu-id="f7f3a-131">Azon elemek listája, amelyeket ki kell zárni a végpontok hatóköre alól.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-131">List of items which need to be excluded from endpoint scope.</span></span>

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

### <span data-ttu-id="f7f3a-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="f7f3a-132">-ExternalAddress</span></span>
<span data-ttu-id="f7f3a-133">Külső cím végpont kapcsolója.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-133">External Address endpoint switch.</span></span>

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

### <span data-ttu-id="f7f3a-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="f7f3a-134">-IncludeItem</span></span>
<span data-ttu-id="f7f3a-135">Azon elemek listája, amelyeket a végpontok hatókörében meg kell jelenni.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-135">List of items which need to be included into endpont scope.</span></span>

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

### <span data-ttu-id="f7f3a-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="f7f3a-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="f7f3a-137">MMA Workspace Machine végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-137">MMA Workspace Machine endpoint switch.</span></span>

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

### <span data-ttu-id="f7f3a-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="f7f3a-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="f7f3a-139">MMA Workspace Network végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-139">MMA Workspace Network endpoint switch.</span></span>

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

### <span data-ttu-id="f7f3a-140">-Name</span><span class="sxs-lookup"><span data-stu-id="f7f3a-140">-Name</span></span>
<span data-ttu-id="f7f3a-141">A kapcsolatfigyelő végpont neve.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="f7f3a-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7f3a-142">-ResourceId</span></span>
<span data-ttu-id="f7f3a-143">A kapcsolatfigyelő végpont erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-143">Resource ID of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="f7f3a-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7f3a-144">-Confirm</span></span>
<span data-ttu-id="f7f3a-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f3a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f3a-146">-WhatIf</span></span>
<span data-ttu-id="f7f3a-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7f3a-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f3a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f3a-149">CommonParameters</span></span>
<span data-ttu-id="f7f3a-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f3a-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7f3a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f3a-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7f3a-152">INPUTS</span></span>

### <span data-ttu-id="f7f3a-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="f7f3a-153">None</span></span>

## <span data-ttu-id="f7f3a-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7f3a-154">OUTPUTS</span></span>

### <span data-ttu-id="f7f3a-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="f7f3a-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="f7f3a-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7f3a-156">NOTES</span></span>

## <span data-ttu-id="f7f3a-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7f3a-157">RELATED LINKS</span></span>
