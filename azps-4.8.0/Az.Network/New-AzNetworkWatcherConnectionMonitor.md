---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024610"
---
# <span data-ttu-id="1cb58-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1cb58-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="1cb58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cb58-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb58-103">Egy kapcsolat figyelése erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1cb58-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="1cb58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cb58-104">SYNTAX</span></span>

### <span data-ttu-id="1cb58-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1cb58-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cb58-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1cb58-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cb58-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="1cb58-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb58-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="1cb58-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb58-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1cb58-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb58-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="1cb58-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb58-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="1cb58-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb58-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cb58-112">DESCRIPTION</span></span>
<span data-ttu-id="1cb58-113">Az New-AzNetworkWatcherConnectionMonitor parancsmag létrehoz egy kapcsolat figyelése erőforrást a megadott forrás és cél (SingleSourcedestination-kapcsolat figyelője) vagy a vizsgált csoportok (MultiEndpointConnectionMonitor) beállítása között.</span><span class="sxs-lookup"><span data-stu-id="1cb58-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="1cb58-114">Példák</span><span class="sxs-lookup"><span data-stu-id="1cb58-114">EXAMPLES</span></span>

### <span data-ttu-id="1cb58-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1cb58-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="1cb58-116">Név: KK-azonosító:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/Providers/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 ETAG: W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState: a következő forrás: {"ResourceId": "/Subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/Providers/Microsoft. Számítási/virtualMachines/VM "," Port ": 0} cél: {" address ":" bing.com ";" Port ": 80} MonitoringIntervalInSeconds: 60 autostart: true kezdet: 1/12/2018 7:13:11 PM MonitoringStatus: futó hely: centraluseuap: Microsoft. Network/networkWatchers/connectionMonitors: {}</span><span class="sxs-lookup"><span data-stu-id="1cb58-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="1cb58-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cb58-117">PARAMETERS</span></span>

### <span data-ttu-id="1cb58-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cb58-118">-AsJob</span></span>
<span data-ttu-id="1cb58-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1cb58-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cb58-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="1cb58-120">-ConfigureOnly</span></span>
<span data-ttu-id="1cb58-121">A kapcsolati monitor beállítása, de nem indul el</span><span class="sxs-lookup"><span data-stu-id="1cb58-121">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="1cb58-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1cb58-122">-ConnectionMonitor</span></span>
<span data-ttu-id="1cb58-123">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="1cb58-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="1cb58-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb58-124">-DefaultProfile</span></span>
<span data-ttu-id="1cb58-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1cb58-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cb58-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="1cb58-126">-DestinationAddress</span></span>
<span data-ttu-id="1cb58-127">A kapcsolat figyelési célhelyének címe (IP vagy tartománynév).</span><span class="sxs-lookup"><span data-stu-id="1cb58-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="1cb58-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="1cb58-128">-DestinationPort</span></span>
<span data-ttu-id="1cb58-129">A kapcsolat figyelője által használt célport.</span><span class="sxs-lookup"><span data-stu-id="1cb58-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="1cb58-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="1cb58-130">-DestinationResourceId</span></span>
<span data-ttu-id="1cb58-131">A kapcsolat figyelője által célként használt erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1cb58-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="1cb58-132">-Force</span><span class="sxs-lookup"><span data-stu-id="1cb58-132">-Force</span></span>
<span data-ttu-id="1cb58-133">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1cb58-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1cb58-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="1cb58-134">-Location</span></span>
<span data-ttu-id="1cb58-135">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="1cb58-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1cb58-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1cb58-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="1cb58-137">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="1cb58-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="1cb58-138">Az alapértelmezett érték 60 másodperc.</span><span class="sxs-lookup"><span data-stu-id="1cb58-138">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="1cb58-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1cb58-139">-Name</span></span>
<span data-ttu-id="1cb58-140">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="1cb58-140">The connection monitor name.</span></span>

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

### <span data-ttu-id="1cb58-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1cb58-141">-NetworkWatcher</span></span>
<span data-ttu-id="1cb58-142">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="1cb58-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="1cb58-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1cb58-143">-NetworkWatcherName</span></span>
<span data-ttu-id="1cb58-144">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="1cb58-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="1cb58-145">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="1cb58-145">-Note</span></span>
<span data-ttu-id="1cb58-146">A kapcsolati monitorral társított megjegyzések.</span><span class="sxs-lookup"><span data-stu-id="1cb58-146">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="1cb58-147">-Output (kimenet)</span><span class="sxs-lookup"><span data-stu-id="1cb58-147">-Output</span></span>
<span data-ttu-id="1cb58-148">A képernyőn megjelenő kimeneti célhelyek ismertetése.</span><span class="sxs-lookup"><span data-stu-id="1cb58-148">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="1cb58-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb58-149">-ResourceGroupName</span></span>
<span data-ttu-id="1cb58-150">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1cb58-150">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1cb58-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="1cb58-151">-SourcePort</span></span>
<span data-ttu-id="1cb58-152">A Csatlakozáskezelő által használt forrás-port.</span><span class="sxs-lookup"><span data-stu-id="1cb58-152">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="1cb58-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="1cb58-153">-SourceResourceId</span></span>
<span data-ttu-id="1cb58-154">A forrásként használt erőforrás azonosítója a kapcsolat figyelője szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="1cb58-154">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="1cb58-155">-Címke</span><span class="sxs-lookup"><span data-stu-id="1cb58-155">-Tag</span></span>
<span data-ttu-id="1cb58-156">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="1cb58-156">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1cb58-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="1cb58-157">-TestGroup</span></span>
<span data-ttu-id="1cb58-158">A vizsgálati csoportok listája.</span><span class="sxs-lookup"><span data-stu-id="1cb58-158">The list of test groups.</span></span>

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

### <span data-ttu-id="1cb58-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1cb58-159">-Confirm</span></span>
<span data-ttu-id="1cb58-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1cb58-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb58-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb58-161">-WhatIf</span></span>
<span data-ttu-id="1cb58-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1cb58-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb58-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1cb58-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb58-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb58-164">CommonParameters</span></span>
<span data-ttu-id="1cb58-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cb58-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb58-166">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1cb58-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb58-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cb58-167">INPUTS</span></span>

### <span data-ttu-id="1cb58-168">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1cb58-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1cb58-169">System. String</span><span class="sxs-lookup"><span data-stu-id="1cb58-169">System.String</span></span>

### <span data-ttu-id="1cb58-170">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft. Azure. PowerShell. parancsmagok. Network, Version = 2.2.2.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1cb58-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1cb58-171">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. models. PSNetworkWatcherConnectionMonitorOutputObject, Microsoft. Azure. PowerShell. parancsmagok. Network, Version = 2.2.2.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1cb58-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1cb58-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cb58-172">OUTPUTS</span></span>

### <span data-ttu-id="1cb58-173">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="1cb58-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="1cb58-174">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="1cb58-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="1cb58-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cb58-175">NOTES</span></span>

## <span data-ttu-id="1cb58-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cb58-176">RELATED LINKS</span></span>
