---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7554183d52b263f4eed470295a2574a3d1f487b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505327"
---
# <span data-ttu-id="65af4-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65af4-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="65af4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65af4-102">SYNOPSIS</span></span>
<span data-ttu-id="65af4-103">Létrehoz egy kapcsolat monitort.</span><span class="sxs-lookup"><span data-stu-id="65af4-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65af4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65af4-104">SYNTAX</span></span>

### <span data-ttu-id="65af4-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65af4-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65af4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="65af4-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65af4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="65af4-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65af4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="65af4-108">DESCRIPTION</span></span>
<span data-ttu-id="65af4-109">A New-AzureRmNetworkWatcherConnectionMonitor parancsmag a megadott forrás-és rcreates-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="65af4-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="65af4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="65af4-110">EXAMPLES</span></span>

### <span data-ttu-id="65af4-111">1. példa: kapcsolati monitor létrehozása VM-és internetes célhelyhez</span><span class="sxs-lookup"><span data-stu-id="65af4-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="65af4-112">Az New-AzureRmNetworkWatcherConnectionMonitor parancsmag létrehoz egy kapcsolat monitort egy adott forráshoz és célhoz.</span><span class="sxs-lookup"><span data-stu-id="65af4-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="65af4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65af4-113">PARAMETERS</span></span>

### <span data-ttu-id="65af4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65af4-114">-AsJob</span></span>
<span data-ttu-id="65af4-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65af4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65af4-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="65af4-116">-ConfigureOnly</span></span>
<span data-ttu-id="65af4-117">A kapcsolati monitor beállítása, de nem indul el</span><span class="sxs-lookup"><span data-stu-id="65af4-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="65af4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65af4-118">-DefaultProfile</span></span>
<span data-ttu-id="65af4-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65af4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65af4-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="65af4-120">-DestinationAddress</span></span>
<span data-ttu-id="65af4-121">A kapcsolat figyelője cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="65af4-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="65af4-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="65af4-122">-DestinationPort</span></span>
<span data-ttu-id="65af4-123">Célport.</span><span class="sxs-lookup"><span data-stu-id="65af4-123">Destination port.</span></span>

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

### <span data-ttu-id="65af4-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="65af4-124">-DestinationResourceId</span></span>
<span data-ttu-id="65af4-125">A kapcsolat figyelési célhelyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="65af4-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="65af4-126">-Force</span><span class="sxs-lookup"><span data-stu-id="65af4-126">-Force</span></span>
<span data-ttu-id="65af4-127">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65af4-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="65af4-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="65af4-128">-Location</span></span>
<span data-ttu-id="65af4-129">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="65af4-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="65af4-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="65af4-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="65af4-131">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="65af4-131">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="65af4-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65af4-132">-Name</span></span>
<span data-ttu-id="65af4-133">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="65af4-133">The connection monitor name.</span></span>

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

### <span data-ttu-id="65af4-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65af4-134">-NetworkWatcher</span></span>
<span data-ttu-id="65af4-135">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="65af4-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="65af4-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="65af4-136">-NetworkWatcherName</span></span>
<span data-ttu-id="65af4-137">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="65af4-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="65af4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65af4-138">-ResourceGroupName</span></span>
<span data-ttu-id="65af4-139">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="65af4-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="65af4-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="65af4-140">-SourcePort</span></span>
<span data-ttu-id="65af4-141">Forrás port.</span><span class="sxs-lookup"><span data-stu-id="65af4-141">Source port.</span></span>

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

### <span data-ttu-id="65af4-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="65af4-142">-SourceResourceId</span></span>
<span data-ttu-id="65af4-143">A kapcsolat figyelője forrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="65af4-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="65af4-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="65af4-144">-Tag</span></span>
<span data-ttu-id="65af4-145">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="65af4-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="65af4-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65af4-146">-Confirm</span></span>
<span data-ttu-id="65af4-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65af4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65af4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65af4-148">-WhatIf</span></span>
<span data-ttu-id="65af4-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65af4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65af4-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65af4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65af4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65af4-151">CommonParameters</span></span>
<span data-ttu-id="65af4-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65af4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65af4-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65af4-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65af4-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65af4-154">INPUTS</span></span>

### <span data-ttu-id="65af4-155">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65af4-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="65af4-156">Paraméterek: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65af4-156">Parameters: NetworkWatcher (ByValue)</span></span>

## <span data-ttu-id="65af4-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65af4-157">OUTPUTS</span></span>

### <span data-ttu-id="65af4-158">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="65af4-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="65af4-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65af4-159">NOTES</span></span>
<span data-ttu-id="65af4-160">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="65af4-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="65af4-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65af4-161">RELATED LINKS</span></span>

[<span data-ttu-id="65af4-162">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65af4-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="65af4-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65af4-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="65af4-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65af4-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="65af4-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="65af4-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="65af4-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="65af4-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="65af4-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="65af4-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="65af4-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="65af4-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="65af4-169">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65af4-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="65af4-170">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="65af4-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="65af4-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65af4-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="65af4-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65af4-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="65af4-173">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65af4-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="65af4-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65af4-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65af4-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="65af4-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="65af4-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65af4-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65af4-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65af4-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65af4-178">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65af4-178">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65af4-179">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65af4-179">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65af4-180">Új – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="65af4-180">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="65af4-181">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="65af4-181">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="65af4-182">Teszt-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="65af4-182">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="65af4-183">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="65af4-183">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="65af4-184">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="65af4-184">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="65af4-185">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="65af4-185">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="65af4-186">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="65af4-186">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="65af4-187">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="65af4-187">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="65af4-188">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="65af4-188">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
