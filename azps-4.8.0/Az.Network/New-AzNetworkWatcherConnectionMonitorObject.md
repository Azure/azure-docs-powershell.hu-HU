---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 06c20432821336b57764d70b5747759b7517801f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183002"
---
# <span data-ttu-id="5bd8d-101">New-AzNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="5bd8d-101">New-AzNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="5bd8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bd8d-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd8d-103">Kapcsolat monitor v2 objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="5bd8d-103">Create a connection monitor V2 object.</span></span>

## <span data-ttu-id="5bd8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bd8d-104">SYNTAX</span></span>

### <span data-ttu-id="5bd8d-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5bd8d-105">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bd8d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5bd8d-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bd8d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5bd8d-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bd8d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bd8d-108">DESCRIPTION</span></span>
<span data-ttu-id="5bd8d-109">Az New-AzNetworkWatcherConnectionMonitorObject parancsmag létrehoz egy Connection monitor v2-objektumot.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-109">The New-AzNetworkWatcherConnectionMonitorObject cmdlet creates a connection monitor V2 object.</span></span>

## <span data-ttu-id="5bd8d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5bd8d-110">EXAMPLES</span></span>

### <span data-ttu-id="5bd8d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5bd8d-111">Example 1</span></span>
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

<span data-ttu-id="5bd8d-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs : null Notes : Tags : { "name": "value" }</span><span class="sxs-lookup"><span data-stu-id="5bd8d-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName  : NetworkWatcherRG Name               : cmV2test TestGroups         : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs            : null Notes              : Tags               : { "name": "value" }</span></span>
        
   

## <span data-ttu-id="5bd8d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bd8d-113">PARAMETERS</span></span>

### <span data-ttu-id="5bd8d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd8d-114">-DefaultProfile</span></span>
<span data-ttu-id="5bd8d-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bd8d-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="5bd8d-116">-Location</span></span>
<span data-ttu-id="5bd8d-117">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-117">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd8d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5bd8d-118">-Name</span></span>
<span data-ttu-id="5bd8d-119">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-119">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd8d-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5bd8d-120">-NetworkWatcher</span></span>
<span data-ttu-id="5bd8d-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-121">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd8d-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5bd8d-122">-NetworkWatcherName</span></span>
<span data-ttu-id="5bd8d-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd8d-124">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="5bd8d-124">-Note</span></span>
<span data-ttu-id="5bd8d-125">A kapcsolati monitorral társított megjegyzések.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-125">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="5bd8d-126">-Output (kimenet)</span><span class="sxs-lookup"><span data-stu-id="5bd8d-126">-Output</span></span>
<span data-ttu-id="5bd8d-127">A képernyőn megjelenő kimeneti célhelyek ismertetése.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-127">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd8d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd8d-128">-ResourceGroupName</span></span>
<span data-ttu-id="5bd8d-129">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-129">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd8d-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="5bd8d-130">-Tag</span></span>
<span data-ttu-id="5bd8d-131">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-131">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5bd8d-132">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="5bd8d-132">-TestGroup</span></span>
<span data-ttu-id="5bd8d-133">A vizsgálati csoportok listája.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-133">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd8d-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5bd8d-134">-Confirm</span></span>
<span data-ttu-id="5bd8d-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bd8d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd8d-136">-WhatIf</span></span>
<span data-ttu-id="5bd8d-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bd8d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bd8d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd8d-139">CommonParameters</span></span>
<span data-ttu-id="5bd8d-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bd8d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd8d-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5bd8d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd8d-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bd8d-142">INPUTS</span></span>

### <span data-ttu-id="5bd8d-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="5bd8d-143">None</span></span>

## <span data-ttu-id="5bd8d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bd8d-144">OUTPUTS</span></span>

### <span data-ttu-id="5bd8d-145">Microsoft. Azure. commands. Network. models. PSNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="5bd8d-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="5bd8d-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bd8d-146">NOTES</span></span>

## <span data-ttu-id="5bd8d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bd8d-147">RELATED LINKS</span></span>
