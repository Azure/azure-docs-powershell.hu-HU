---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7e3836f2c546c5ba3ad2ee4a2845e7c813601dda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838336"
---
# <span data-ttu-id="cfdb8-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfdb8-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="cfdb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfdb8-102">SYNOPSIS</span></span>
<span data-ttu-id="cfdb8-103">Frissítheti a kapcsolat monitorát.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-103">Update a connection monitor.</span></span>

## <span data-ttu-id="cfdb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfdb8-104">SYNTAX</span></span>

### <span data-ttu-id="cfdb8-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cfdb8-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cfdb8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cfdb8-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cfdb8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cfdb8-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfdb8-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cfdb8-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfdb8-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="cfdb8-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfdb8-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfdb8-110">DESCRIPTION</span></span>
<span data-ttu-id="cfdb8-111">A Set-AzNetworkWatcherConnectionMonitor parancsmag frissíti a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="cfdb8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="cfdb8-112">EXAMPLES</span></span>

### <span data-ttu-id="cfdb8-113">1. példa: a kapcsolat monitorának frissítése</span><span class="sxs-lookup"><span data-stu-id="cfdb8-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="cfdb8-114">Ebben a példában frissítjük a meglévő kapcsolati monitort a destinationAddress módosításával és a címkék hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="cfdb8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfdb8-115">PARAMETERS</span></span>

### <span data-ttu-id="cfdb8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfdb8-116">-AsJob</span></span>
<span data-ttu-id="cfdb8-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cfdb8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfdb8-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="cfdb8-118">-ConfigureOnly</span></span>
<span data-ttu-id="cfdb8-119">A kapcsolati monitor beállítása, de nem indul el</span><span class="sxs-lookup"><span data-stu-id="cfdb8-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="cfdb8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfdb8-120">-DefaultProfile</span></span>
<span data-ttu-id="cfdb8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfdb8-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="cfdb8-122">-DestinationAddress</span></span>
<span data-ttu-id="cfdb8-123">A kapcsolat figyelője cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="cfdb8-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="cfdb8-124">-DestinationPort</span></span>
<span data-ttu-id="cfdb8-125">Célport.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-125">Destination port.</span></span>

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

### <span data-ttu-id="cfdb8-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="cfdb8-126">-DestinationResourceId</span></span>
<span data-ttu-id="cfdb8-127">A kapcsolat figyelési célhelyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="cfdb8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfdb8-128">-InputObject</span></span>
<span data-ttu-id="cfdb8-129">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="cfdb8-129">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdb8-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="cfdb8-130">-Location</span></span>
<span data-ttu-id="cfdb8-131">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cfdb8-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="cfdb8-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="cfdb8-133">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="cfdb8-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="cfdb8-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cfdb8-134">-Name</span></span>
<span data-ttu-id="cfdb8-135">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-135">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdb8-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cfdb8-136">-NetworkWatcher</span></span>
<span data-ttu-id="cfdb8-137">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="cfdb8-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cfdb8-138">-NetworkWatcherName</span></span>
<span data-ttu-id="cfdb8-139">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="cfdb8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfdb8-140">-ResourceGroupName</span></span>
<span data-ttu-id="cfdb8-141">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cfdb8-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfdb8-142">-ResourceId</span></span>
<span data-ttu-id="cfdb8-143">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-143">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdb8-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="cfdb8-144">-SourcePort</span></span>
<span data-ttu-id="cfdb8-145">Forrás port.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-145">Source port.</span></span>

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

### <span data-ttu-id="cfdb8-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="cfdb8-146">-SourceResourceId</span></span>
<span data-ttu-id="cfdb8-147">A kapcsolat figyelője forrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="cfdb8-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="cfdb8-148">-Tag</span></span>
<span data-ttu-id="cfdb8-149">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cfdb8-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cfdb8-150">-Confirm</span></span>
<span data-ttu-id="cfdb8-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfdb8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfdb8-152">-WhatIf</span></span>
<span data-ttu-id="cfdb8-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfdb8-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfdb8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfdb8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfdb8-155">CommonParameters</span></span>
<span data-ttu-id="cfdb8-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfdb8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfdb8-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfdb8-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfdb8-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfdb8-158">INPUTS</span></span>

### <span data-ttu-id="cfdb8-159">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cfdb8-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="cfdb8-160">System. String</span><span class="sxs-lookup"><span data-stu-id="cfdb8-160">System.String</span></span>

### <span data-ttu-id="cfdb8-161">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="cfdb8-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="cfdb8-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfdb8-162">OUTPUTS</span></span>

### <span data-ttu-id="cfdb8-163">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="cfdb8-163">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="cfdb8-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfdb8-164">NOTES</span></span>
<span data-ttu-id="cfdb8-165">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="cfdb8-165">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="cfdb8-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfdb8-166">RELATED LINKS</span></span>

[<span data-ttu-id="cfdb8-167">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cfdb8-167">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cfdb8-168">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cfdb8-168">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cfdb8-169">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cfdb8-169">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cfdb8-170">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cfdb8-170">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cfdb8-171">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cfdb8-171">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cfdb8-172">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cfdb8-172">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="cfdb8-173">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cfdb8-173">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cfdb8-174">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cfdb8-174">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cfdb8-175">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cfdb8-175">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cfdb8-176">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cfdb8-176">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cfdb8-177">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cfdb8-177">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cfdb8-178">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cfdb8-178">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cfdb8-179">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfdb8-179">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfdb8-180">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cfdb8-180">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="cfdb8-181">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfdb8-181">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfdb8-182">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfdb8-182">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfdb8-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfdb8-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfdb8-184">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfdb8-184">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfdb8-185">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfdb8-185">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cfdb8-186">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cfdb8-186">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cfdb8-187">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cfdb8-187">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="cfdb8-188">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cfdb8-188">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cfdb8-189">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfdb8-189">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfdb8-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cfdb8-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cfdb8-191">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cfdb8-191">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cfdb8-192">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cfdb8-192">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cfdb8-193">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cfdb8-193">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
