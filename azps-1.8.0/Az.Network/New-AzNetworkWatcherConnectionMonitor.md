---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7c6ad774c7b260424821b37837882bab0b47bd53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670299"
---
# <span data-ttu-id="23c26-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23c26-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="23c26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23c26-102">SYNOPSIS</span></span>
<span data-ttu-id="23c26-103">Létrehoz egy kapcsolat monitort.</span><span class="sxs-lookup"><span data-stu-id="23c26-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="23c26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23c26-104">SYNTAX</span></span>

### <span data-ttu-id="23c26-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23c26-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23c26-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="23c26-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23c26-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="23c26-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23c26-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="23c26-108">DESCRIPTION</span></span>
<span data-ttu-id="23c26-109">A New-AzNetworkWatcherConnectionMonitor parancsmag a megadott forrás-és rcreates-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="23c26-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="23c26-110">Példák</span><span class="sxs-lookup"><span data-stu-id="23c26-110">EXAMPLES</span></span>

### <span data-ttu-id="23c26-111">1. példa: kapcsolati monitor létrehozása VM-és internetes célhelyhez</span><span class="sxs-lookup"><span data-stu-id="23c26-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="23c26-112">Az New-AzNetworkWatcherConnectionMonitor parancsmag létrehoz egy kapcsolat monitort egy adott forráshoz és célhoz.</span><span class="sxs-lookup"><span data-stu-id="23c26-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="23c26-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23c26-113">PARAMETERS</span></span>

### <span data-ttu-id="23c26-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23c26-114">-AsJob</span></span>
<span data-ttu-id="23c26-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="23c26-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23c26-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="23c26-116">-ConfigureOnly</span></span>
<span data-ttu-id="23c26-117">A kapcsolati monitor beállítása, de nem indul el</span><span class="sxs-lookup"><span data-stu-id="23c26-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="23c26-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c26-118">-DefaultProfile</span></span>
<span data-ttu-id="23c26-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23c26-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23c26-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="23c26-120">-DestinationAddress</span></span>
<span data-ttu-id="23c26-121">A kapcsolat figyelője cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="23c26-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="23c26-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="23c26-122">-DestinationPort</span></span>
<span data-ttu-id="23c26-123">Célport.</span><span class="sxs-lookup"><span data-stu-id="23c26-123">Destination port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23c26-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="23c26-124">-DestinationResourceId</span></span>
<span data-ttu-id="23c26-125">A kapcsolat figyelési célhelyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="23c26-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="23c26-126">-Force</span><span class="sxs-lookup"><span data-stu-id="23c26-126">-Force</span></span>
<span data-ttu-id="23c26-127">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23c26-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23c26-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="23c26-128">-Location</span></span>
<span data-ttu-id="23c26-129">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="23c26-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="23c26-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="23c26-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="23c26-131">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="23c26-131">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23c26-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23c26-132">-Name</span></span>
<span data-ttu-id="23c26-133">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="23c26-133">The connection monitor name.</span></span>

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

### <span data-ttu-id="23c26-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23c26-134">-NetworkWatcher</span></span>
<span data-ttu-id="23c26-135">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="23c26-135">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23c26-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="23c26-136">-NetworkWatcherName</span></span>
<span data-ttu-id="23c26-137">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="23c26-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="23c26-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c26-138">-ResourceGroupName</span></span>
<span data-ttu-id="23c26-139">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="23c26-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="23c26-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="23c26-140">-SourcePort</span></span>
<span data-ttu-id="23c26-141">Forrás port.</span><span class="sxs-lookup"><span data-stu-id="23c26-141">Source port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23c26-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="23c26-142">-SourceResourceId</span></span>
<span data-ttu-id="23c26-143">A kapcsolat figyelője forrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="23c26-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="23c26-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="23c26-144">-Tag</span></span>
<span data-ttu-id="23c26-145">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="23c26-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23c26-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="23c26-146">-Confirm</span></span>
<span data-ttu-id="23c26-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23c26-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23c26-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23c26-148">-WhatIf</span></span>
<span data-ttu-id="23c26-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="23c26-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23c26-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23c26-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23c26-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c26-151">CommonParameters</span></span>
<span data-ttu-id="23c26-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23c26-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c26-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23c26-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c26-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23c26-154">INPUTS</span></span>

### <span data-ttu-id="23c26-155">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23c26-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="23c26-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23c26-156">OUTPUTS</span></span>

### <span data-ttu-id="23c26-157">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="23c26-157">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="23c26-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23c26-158">NOTES</span></span>
<span data-ttu-id="23c26-159">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="23c26-159">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="23c26-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23c26-160">RELATED LINKS</span></span>

[<span data-ttu-id="23c26-161">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23c26-161">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="23c26-162">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23c26-162">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="23c26-163">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23c26-163">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="23c26-164">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="23c26-164">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="23c26-165">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="23c26-165">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="23c26-166">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="23c26-166">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="23c26-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="23c26-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="23c26-168">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23c26-168">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23c26-169">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="23c26-169">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="23c26-170">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23c26-170">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23c26-171">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23c26-171">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23c26-172">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23c26-172">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23c26-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23c26-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23c26-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="23c26-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="23c26-175">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23c26-175">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23c26-176">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23c26-176">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23c26-177">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23c26-177">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23c26-178">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23c26-178">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23c26-179">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c26-179">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="23c26-180">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="23c26-180">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="23c26-181">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="23c26-181">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="23c26-182">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="23c26-182">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="23c26-183">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23c26-183">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23c26-184">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="23c26-184">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="23c26-185">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="23c26-185">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="23c26-186">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="23c26-186">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="23c26-187">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="23c26-187">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
