---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301454"
---
# <span data-ttu-id="610cb-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="610cb-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="610cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="610cb-102">SYNOPSIS</span></span>
<span data-ttu-id="610cb-103">A kapcsolat figyelője végpontját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="610cb-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="610cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="610cb-104">SYNTAX</span></span>

### <span data-ttu-id="610cb-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="610cb-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610cb-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="610cb-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610cb-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="610cb-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610cb-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="610cb-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610cb-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="610cb-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610cb-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="610cb-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="610cb-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="610cb-111">DESCRIPTION</span></span>
<span data-ttu-id="610cb-112">New-AzNetworkWatcherConnectionMonitorEndpointObject parancsmag a kapcsolat figyelése végpontot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="610cb-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="610cb-113">Példák</span><span class="sxs-lookup"><span data-stu-id="610cb-113">EXAMPLES</span></span>

### <span data-ttu-id="610cb-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="610cb-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="610cb-115">Név: workspaceEndpoint Type: MMAWorkspaceMachine ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: scope: {"include": [{"address": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="610cb-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="610cb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="610cb-116">PARAMETERS</span></span>

### <span data-ttu-id="610cb-117">-Address (cím)</span><span class="sxs-lookup"><span data-stu-id="610cb-117">-Address</span></span>
<span data-ttu-id="610cb-118">A kapcsolati figyelő végpontjának címe (IP vagy tartománynév).</span><span class="sxs-lookup"><span data-stu-id="610cb-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

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

### <span data-ttu-id="610cb-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="610cb-119">-AzureSubnet</span></span>
<span data-ttu-id="610cb-120">Azure alhálózati végpont kapcsolója</span><span class="sxs-lookup"><span data-stu-id="610cb-120">Azure Subnet endpoint switch.</span></span>

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

### <span data-ttu-id="610cb-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="610cb-121">-AzureVM</span></span>
<span data-ttu-id="610cb-122">Azure VM végpont kapcsoló</span><span class="sxs-lookup"><span data-stu-id="610cb-122">Azure VM endpoint switch.</span></span>

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

### <span data-ttu-id="610cb-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="610cb-123">-AzureVNet</span></span>
<span data-ttu-id="610cb-124">Azure vnet végpont kapcsolója</span><span class="sxs-lookup"><span data-stu-id="610cb-124">Azure Vnet endpoint switch.</span></span>

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

### <span data-ttu-id="610cb-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="610cb-125">-CoverageLevel</span></span>
<span data-ttu-id="610cb-126">A végpont tesztelési hatóköre.</span><span class="sxs-lookup"><span data-stu-id="610cb-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="610cb-127">A támogatott értékek az alapértelmezettek, az alacsony, a BelowAverage, az átlag, a AboveAvergae, a teljes.</span><span class="sxs-lookup"><span data-stu-id="610cb-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

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

### <span data-ttu-id="610cb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610cb-128">-DefaultProfile</span></span>
<span data-ttu-id="610cb-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="610cb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="610cb-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="610cb-130">-ExcludeItem</span></span>
<span data-ttu-id="610cb-131">Azoknak az elemeknek a listája, amelyeket ki kell zárni a végponti hatókörből.</span><span class="sxs-lookup"><span data-stu-id="610cb-131">List of items which need to be excluded from endpoint scope.</span></span>

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

### <span data-ttu-id="610cb-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="610cb-132">-ExternalAddress</span></span>
<span data-ttu-id="610cb-133">Külső cím végpont kapcsolója</span><span class="sxs-lookup"><span data-stu-id="610cb-133">External Address endpoint switch.</span></span>

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

### <span data-ttu-id="610cb-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="610cb-134">-IncludeItem</span></span>
<span data-ttu-id="610cb-135">Azoknak az elemeknek a listája, amelyeket fel kell venni a endpont-tartományba.</span><span class="sxs-lookup"><span data-stu-id="610cb-135">List of items which need to be included into endpont scope.</span></span>

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

### <span data-ttu-id="610cb-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="610cb-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="610cb-137">MMA munkaterület-gép végpont kapcsolója</span><span class="sxs-lookup"><span data-stu-id="610cb-137">MMA Workspace Machine endpoint switch.</span></span>

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

### <span data-ttu-id="610cb-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="610cb-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="610cb-139">MMA-munkaterület hálózati végpont kapcsoló.</span><span class="sxs-lookup"><span data-stu-id="610cb-139">MMA Workspace Network endpoint switch.</span></span>

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

### <span data-ttu-id="610cb-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="610cb-140">-Name</span></span>
<span data-ttu-id="610cb-141">A kapcsolat figyelője végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="610cb-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="610cb-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="610cb-142">-ResourceId</span></span>
<span data-ttu-id="610cb-143">A kapcsolat figyelője végpontjának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="610cb-143">Resource ID of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="610cb-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="610cb-144">-Confirm</span></span>
<span data-ttu-id="610cb-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="610cb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="610cb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="610cb-146">-WhatIf</span></span>
<span data-ttu-id="610cb-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="610cb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="610cb-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="610cb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="610cb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610cb-149">CommonParameters</span></span>
<span data-ttu-id="610cb-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="610cb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="610cb-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="610cb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610cb-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="610cb-152">INPUTS</span></span>

### <span data-ttu-id="610cb-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="610cb-153">None</span></span>

## <span data-ttu-id="610cb-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="610cb-154">OUTPUTS</span></span>

### <span data-ttu-id="610cb-155">Microsoft. Azure. commands. Network. models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="610cb-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="610cb-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="610cb-156">NOTES</span></span>

## <span data-ttu-id="610cb-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="610cb-157">RELATED LINKS</span></span>
