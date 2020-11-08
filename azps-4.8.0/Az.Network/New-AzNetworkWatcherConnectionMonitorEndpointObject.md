---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 58e26de74abb46234f6985c3973b5bbe494bd0ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180518"
---
# <span data-ttu-id="ddd2b-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="ddd2b-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="ddd2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd2b-103">A kapcsolat figyelője végpontját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="ddd2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddd2b-104">SYNTAX</span></span>

### <span data-ttu-id="ddd2b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ddd2b-105">SetByResourceId</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] -ResourceId <String>
 [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd2b-106">SetByAddress</span><span class="sxs-lookup"><span data-stu-id="ddd2b-106">SetByAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] [-Address <String>] [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd2b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddd2b-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd2b-108">New-AzNetworkWatcherConnectionMonitorEndpointObject parancsmag a kapcsolat figyelése végpontot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="ddd2b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ddd2b-109">EXAMPLES</span></span>

### <span data-ttu-id="ddd2b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ddd2b-110">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name "workspaceEndpoint" -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

<span data-ttu-id="ddd2b-111">Név: workspaceEndpoint ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace cím: szűrő: {"type": "include", "Items": [{"type": "AgentAddress"; "cím": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="ddd2b-111">Name       : workspaceEndpoint ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Filter     : { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="ddd2b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddd2b-112">PARAMETERS</span></span>

### <span data-ttu-id="ddd2b-113">-Address (cím)</span><span class="sxs-lookup"><span data-stu-id="ddd2b-113">-Address</span></span>
<span data-ttu-id="ddd2b-114">A kapcsolati figyelő végpontjának címe (IP vagy tartománynév).</span><span class="sxs-lookup"><span data-stu-id="ddd2b-114">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd2b-115">-DefaultProfile</span></span>
<span data-ttu-id="ddd2b-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddd2b-117">-FilterItem</span><span class="sxs-lookup"><span data-stu-id="ddd2b-117">-FilterItem</span></span>
<span data-ttu-id="ddd2b-118">A szűrő elemeinek listája.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-118">List of items in the filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd2b-119">-FilterType</span><span class="sxs-lookup"><span data-stu-id="ddd2b-119">-FilterType</span></span>
<span data-ttu-id="ddd2b-120">A végpontok szűrő működése</span><span class="sxs-lookup"><span data-stu-id="ddd2b-120">The behavior of the endpoint filter.</span></span> <span data-ttu-id="ddd2b-121">Jelenleg csak a "include" támogatott.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-121">Currently only 'Include' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd2b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ddd2b-122">-Name</span></span>
<span data-ttu-id="ddd2b-123">A kapcsolat figyelője végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-123">The name of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd2b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddd2b-124">-ResourceId</span></span>
<span data-ttu-id="ddd2b-125">A kapcsolat figyelője végpontjának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-125">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd2b-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ddd2b-126">-Confirm</span></span>
<span data-ttu-id="ddd2b-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd2b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd2b-128">-WhatIf</span></span>
<span data-ttu-id="ddd2b-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd2b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd2b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd2b-131">CommonParameters</span></span>
<span data-ttu-id="ddd2b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddd2b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd2b-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ddd2b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd2b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddd2b-134">INPUTS</span></span>

### <span data-ttu-id="ddd2b-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="ddd2b-135">None</span></span>

## <span data-ttu-id="ddd2b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddd2b-136">OUTPUTS</span></span>

### <span data-ttu-id="ddd2b-137">Microsoft. Azure. commands. Network. models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="ddd2b-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="ddd2b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddd2b-138">NOTES</span></span>

## <span data-ttu-id="ddd2b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddd2b-139">RELATED LINKS</span></span>
