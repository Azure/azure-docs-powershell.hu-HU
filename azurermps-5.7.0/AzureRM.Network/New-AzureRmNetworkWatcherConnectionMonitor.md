---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b8dd04fa4727465ee9b3be3eaf5e5e06a2243338
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680145"
---
# <span data-ttu-id="6a21d-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6a21d-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="6a21d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a21d-102">SYNOPSIS</span></span>
<span data-ttu-id="6a21d-103">Létrehoz egy kapcsolat monitort.</span><span class="sxs-lookup"><span data-stu-id="6a21d-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a21d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a21d-104">SYNTAX</span></span>

### <span data-ttu-id="6a21d-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a21d-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a21d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6a21d-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a21d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6a21d-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a21d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a21d-108">DESCRIPTION</span></span>
<span data-ttu-id="6a21d-109">A New-AzureRmNetworkWatcherConnectionMonitor parancsmag a megadott forrás-és rcreates-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a21d-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="6a21d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6a21d-110">EXAMPLES</span></span>

### <span data-ttu-id="6a21d-111">1. példa: kapcsolati monitor létrehozása VM-és internetes célhelyhez</span><span class="sxs-lookup"><span data-stu-id="6a21d-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
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

<span data-ttu-id="6a21d-112">Az New-AzureRmNetworkWatcherConnectionMonitor parancsmag létrehoz egy kapcsolat monitort egy adott forráshoz és célhoz.</span><span class="sxs-lookup"><span data-stu-id="6a21d-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="6a21d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a21d-113">PARAMETERS</span></span>

### <span data-ttu-id="6a21d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a21d-114">-AsJob</span></span>
<span data-ttu-id="6a21d-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6a21d-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a21d-116">-Confirm</span></span>
<span data-ttu-id="6a21d-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a21d-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a21d-118">-DefaultProfile</span></span>
<span data-ttu-id="6a21d-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a21d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6a21d-120">-DestinationAddress</span></span>
<span data-ttu-id="6a21d-121">A kapcsolat figyelője cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="6a21d-121">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6a21d-122">-DestinationPort</span></span>
<span data-ttu-id="6a21d-123">Célport.</span><span class="sxs-lookup"><span data-stu-id="6a21d-123">Destination port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="6a21d-124">-DestinationResourceId</span></span>
<span data-ttu-id="6a21d-125">A kapcsolat figyelési célhelyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a21d-125">The ID of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6a21d-126">-Force</span></span>
<span data-ttu-id="6a21d-127">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a21d-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="6a21d-128">-Location</span></span>
<span data-ttu-id="6a21d-129">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="6a21d-129">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6a21d-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="6a21d-131">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="6a21d-131">Monitoring interval in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a21d-132">-Name</span></span>
<span data-ttu-id="6a21d-133">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="6a21d-133">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6a21d-134">-NetworkWatcher</span></span>
<span data-ttu-id="6a21d-135">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6a21d-135">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6a21d-136">-NetworkWatcherName</span></span>
<span data-ttu-id="6a21d-137">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="6a21d-137">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a21d-138">-ResourceGroupName</span></span>
<span data-ttu-id="6a21d-139">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6a21d-139">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="6a21d-140">-SourcePort</span></span>
<span data-ttu-id="6a21d-141">Forrás port.</span><span class="sxs-lookup"><span data-stu-id="6a21d-141">Source port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6a21d-142">-SourceResourceId</span></span>
<span data-ttu-id="6a21d-143">A kapcsolat figyelője forrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a21d-143">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="6a21d-144">-Tag</span></span>
<span data-ttu-id="6a21d-145">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6a21d-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a21d-146">-WhatIf</span></span>
<span data-ttu-id="6a21d-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a21d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a21d-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a21d-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-149">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="6a21d-149">-ConfigureOnly</span></span>
<span data-ttu-id="6a21d-150">A kapcsolati monitor beállítása, de nem indul el</span><span class="sxs-lookup"><span data-stu-id="6a21d-150">Configure connection monitor, but do not start it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a21d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a21d-151">CommonParameters</span></span>
<span data-ttu-id="6a21d-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a21d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6a21d-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a21d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a21d-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a21d-154">INPUTS</span></span>

### <span data-ttu-id="6a21d-155">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6a21d-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6a21d-156">System. String</span><span class="sxs-lookup"><span data-stu-id="6a21d-156">System.String</span></span>

## <span data-ttu-id="6a21d-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a21d-157">OUTPUTS</span></span>

### <span data-ttu-id="6a21d-158">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="6a21d-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="6a21d-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a21d-159">NOTES</span></span>
<span data-ttu-id="6a21d-160">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="6a21d-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="6a21d-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a21d-161">RELATED LINKS</span></span>

[<span data-ttu-id="6a21d-162">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6a21d-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6a21d-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6a21d-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6a21d-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6a21d-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6a21d-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6a21d-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="6a21d-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6a21d-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="6a21d-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6a21d-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="6a21d-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6a21d-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="6a21d-169">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6a21d-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6a21d-170">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6a21d-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="6a21d-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6a21d-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6a21d-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6a21d-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6a21d-173">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6a21d-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6a21d-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6a21d-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6a21d-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6a21d-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="6a21d-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6a21d-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6a21d-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6a21d-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6a21d-178">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6a21d-178">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6a21d-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6a21d-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
