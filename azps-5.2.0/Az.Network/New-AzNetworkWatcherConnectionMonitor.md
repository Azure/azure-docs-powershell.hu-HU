---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334469"
---
# <span data-ttu-id="183f9-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="183f9-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="183f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="183f9-102">SYNOPSIS</span></span>
<span data-ttu-id="183f9-103">Kapcsolatfigyelő erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="183f9-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="183f9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="183f9-104">SYNTAX</span></span>

### <span data-ttu-id="183f9-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="183f9-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="183f9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="183f9-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="183f9-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="183f9-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="183f9-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="183f9-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="183f9-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="183f9-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="183f9-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="183f9-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="183f9-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="183f9-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="183f9-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="183f9-112">DESCRIPTION</span></span>
<span data-ttu-id="183f9-113">A New-AzNetworkWatcherConnectionMonitor parancsmag kapcsolatfigyelő erőforrást hoz létre a megadott forrás- és célhelyhez (SingleSourcedestination kapcsolatfigyelő) vagy tesztcsoportokhoz (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="183f9-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="183f9-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="183f9-114">EXAMPLES</span></span>

### <span data-ttu-id="183f9-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="183f9-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="183f9-116">Név: cm Id : /subscriptions/00000000-0000-0000-00000-0000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState: Sikeres forrás: { "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft. Compute/virtualMachines/vm", "Port": 0 } Destination: { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds: 60 AutoStart: True StartTime : 2018.01.12.07:13:11 PM MonitoringStatus: Running Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags: : {}</span><span class="sxs-lookup"><span data-stu-id="183f9-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="183f9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="183f9-117">PARAMETERS</span></span>

### <span data-ttu-id="183f9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="183f9-118">-AsJob</span></span>
<span data-ttu-id="183f9-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="183f9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="183f9-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="183f9-120">-ConfigureOnly</span></span>
<span data-ttu-id="183f9-121">A kapcsolatfigyelő beállítása, de nem indul el</span><span class="sxs-lookup"><span data-stu-id="183f9-121">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="183f9-122">-ConnectionMonitor</span></span>
<span data-ttu-id="183f9-123">Kapcsolatfigyelő objektum.</span><span class="sxs-lookup"><span data-stu-id="183f9-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183f9-124">-DefaultProfile</span></span>
<span data-ttu-id="183f9-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="183f9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="183f9-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="183f9-126">-DestinationAddress</span></span>
<span data-ttu-id="183f9-127">A kapcsolatfigyelő célhelyének címe (IP vagy tartománynév).</span><span class="sxs-lookup"><span data-stu-id="183f9-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="183f9-128">-DestinationPort</span></span>
<span data-ttu-id="183f9-129">A kapcsolatfigyelő által használt célport.</span><span class="sxs-lookup"><span data-stu-id="183f9-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="183f9-130">-DestinationResourceId</span></span>
<span data-ttu-id="183f9-131">A kapcsolatfigyelő által célként használt erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="183f9-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-132">-Force</span><span class="sxs-lookup"><span data-stu-id="183f9-132">-Force</span></span>
<span data-ttu-id="183f9-133">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="183f9-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="183f9-134">-Location</span><span class="sxs-lookup"><span data-stu-id="183f9-134">-Location</span></span>
<span data-ttu-id="183f9-135">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="183f9-135">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="183f9-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="183f9-137">Figyelési időköz másodpercben</span><span class="sxs-lookup"><span data-stu-id="183f9-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="183f9-138">Az alapértelmezett érték 60 másodperc.</span><span class="sxs-lookup"><span data-stu-id="183f9-138">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-139">-Name</span><span class="sxs-lookup"><span data-stu-id="183f9-139">-Name</span></span>
<span data-ttu-id="183f9-140">A kapcsolatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="183f9-140">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="183f9-141">-NetworkWatcher</span></span>
<span data-ttu-id="183f9-142">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="183f9-142">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="183f9-143">-NetworkWatcherName</span></span>
<span data-ttu-id="183f9-144">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="183f9-144">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-145">-Note</span><span class="sxs-lookup"><span data-stu-id="183f9-145">-Note</span></span>
<span data-ttu-id="183f9-146">A kapcsolatfigyelővel társított jegyzetek.</span><span class="sxs-lookup"><span data-stu-id="183f9-146">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-147">-Kimenet</span><span class="sxs-lookup"><span data-stu-id="183f9-147">-Output</span></span>
<span data-ttu-id="183f9-148">A kapcsolatfigyelő kimeneti célhelyét ismerteti.</span><span class="sxs-lookup"><span data-stu-id="183f9-148">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="183f9-149">-ResourceGroupName</span></span>
<span data-ttu-id="183f9-150">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="183f9-150">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="183f9-151">-SourcePort</span></span>
<span data-ttu-id="183f9-152">A kapcsolatfigyelő által használt forrásport.</span><span class="sxs-lookup"><span data-stu-id="183f9-152">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="183f9-153">-SourceResourceId</span></span>
<span data-ttu-id="183f9-154">A kapcsolatfigyelő által forrásként használt erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="183f9-154">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="183f9-155">-Tag</span></span>
<span data-ttu-id="183f9-156">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="183f9-156">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="183f9-157">-TestGroup</span></span>
<span data-ttu-id="183f9-158">A tesztcsoportok listája.</span><span class="sxs-lookup"><span data-stu-id="183f9-158">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183f9-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="183f9-159">-Confirm</span></span>
<span data-ttu-id="183f9-160">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="183f9-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="183f9-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="183f9-161">-WhatIf</span></span>
<span data-ttu-id="183f9-162">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="183f9-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="183f9-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="183f9-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="183f9-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183f9-164">CommonParameters</span></span>
<span data-ttu-id="183f9-165">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="183f9-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183f9-166">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="183f9-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183f9-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="183f9-167">INPUTS</span></span>

### <span data-ttu-id="183f9-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="183f9-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="183f9-169">System.String</span><span class="sxs-lookup"><span data-stu-id="183f9-169">System.String</span></span>

### <span data-ttu-id="183f9-170">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="183f9-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="183f9-171">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="183f9-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="183f9-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="183f9-172">OUTPUTS</span></span>

### <span data-ttu-id="183f9-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="183f9-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="183f9-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="183f9-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="183f9-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="183f9-175">NOTES</span></span>

## <span data-ttu-id="183f9-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="183f9-176">RELATED LINKS</span></span>
