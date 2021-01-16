---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 06c20432821336b57764d70b5747759b7517801f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372201"
---
# <span data-ttu-id="9907d-101">New-AzNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="9907d-101">New-AzNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="9907d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9907d-102">SYNOPSIS</span></span>
<span data-ttu-id="9907d-103">Kapcsolatfigyelő V2-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="9907d-103">Create a connection monitor V2 object.</span></span>

## <span data-ttu-id="9907d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9907d-104">SYNTAX</span></span>

### <span data-ttu-id="9907d-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9907d-105">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9907d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9907d-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9907d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9907d-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9907d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9907d-108">DESCRIPTION</span></span>
<span data-ttu-id="9907d-109">A New-AzNetworkWatcherConnectionMonitorObject parancsmag létrehoz egy kapcsolatfigyelő V2 objektumot.</span><span class="sxs-lookup"><span data-stu-id="9907d-109">The New-AzNetworkWatcherConnectionMonitorObject cmdlet creates a connection monitor V2 object.</span></span>

## <span data-ttu-id="9907d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9907d-110">EXAMPLES</span></span>

### <span data-ttu-id="9907d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9907d-111">Example 1</span></span>
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

<span data-ttu-id="9907d-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs : null Notes : Tags : { "name": "value" }</span><span class="sxs-lookup"><span data-stu-id="9907d-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName  : NetworkWatcherRG Name               : cmV2test TestGroups         : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs            : null Notes              : Tags               : { "name": "value" }</span></span>
        
   

## <span data-ttu-id="9907d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9907d-113">PARAMETERS</span></span>

### <span data-ttu-id="9907d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9907d-114">-DefaultProfile</span></span>
<span data-ttu-id="9907d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9907d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9907d-116">-Location</span><span class="sxs-lookup"><span data-stu-id="9907d-116">-Location</span></span>
<span data-ttu-id="9907d-117">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="9907d-117">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9907d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9907d-118">-Name</span></span>
<span data-ttu-id="9907d-119">A kapcsolatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="9907d-119">The connection monitor name.</span></span>

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

### <span data-ttu-id="9907d-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9907d-120">-NetworkWatcher</span></span>
<span data-ttu-id="9907d-121">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="9907d-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="9907d-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9907d-122">-NetworkWatcherName</span></span>
<span data-ttu-id="9907d-123">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="9907d-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="9907d-124">-Note</span><span class="sxs-lookup"><span data-stu-id="9907d-124">-Note</span></span>
<span data-ttu-id="9907d-125">A kapcsolatfigyelővel társított jegyzetek.</span><span class="sxs-lookup"><span data-stu-id="9907d-125">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="9907d-126">-Kimenet</span><span class="sxs-lookup"><span data-stu-id="9907d-126">-Output</span></span>
<span data-ttu-id="9907d-127">A kapcsolatfigyelő kimeneti célhelyét ismerteti.</span><span class="sxs-lookup"><span data-stu-id="9907d-127">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="9907d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9907d-128">-ResourceGroupName</span></span>
<span data-ttu-id="9907d-129">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9907d-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9907d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9907d-130">-Tag</span></span>
<span data-ttu-id="9907d-131">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="9907d-131">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9907d-132">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="9907d-132">-TestGroup</span></span>
<span data-ttu-id="9907d-133">A tesztcsoportok listája.</span><span class="sxs-lookup"><span data-stu-id="9907d-133">The list of test groups.</span></span>

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

### <span data-ttu-id="9907d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9907d-134">-Confirm</span></span>
<span data-ttu-id="9907d-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9907d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9907d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9907d-136">-WhatIf</span></span>
<span data-ttu-id="9907d-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9907d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9907d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9907d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9907d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9907d-139">CommonParameters</span></span>
<span data-ttu-id="9907d-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9907d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9907d-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9907d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9907d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9907d-142">INPUTS</span></span>

### <span data-ttu-id="9907d-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="9907d-143">None</span></span>

## <span data-ttu-id="9907d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9907d-144">OUTPUTS</span></span>

### <span data-ttu-id="9907d-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="9907d-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="9907d-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9907d-146">NOTES</span></span>

## <span data-ttu-id="9907d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9907d-147">RELATED LINKS</span></span>
