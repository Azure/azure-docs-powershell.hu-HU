---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 44f81008b0693a4ff14a80a818e9d2514dfe0ebf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679876"
---
# <span data-ttu-id="fb56c-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fb56c-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="fb56c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb56c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb56c-103">Frissítheti a kapcsolat monitorát.</span><span class="sxs-lookup"><span data-stu-id="fb56c-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb56c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb56c-104">SYNTAX</span></span>

### <span data-ttu-id="fb56c-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb56c-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb56c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fb56c-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb56c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="fb56c-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb56c-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb56c-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb56c-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb56c-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb56c-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb56c-110">DESCRIPTION</span></span>
<span data-ttu-id="fb56c-111">A Set-AzureRmNetworkWatcherConnectionMonitor parancsmag frissíti a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="fb56c-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="fb56c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="fb56c-112">EXAMPLES</span></span>

### <span data-ttu-id="fb56c-113">1. példa: a kapcsolat monitorának frissítése</span><span class="sxs-lookup"><span data-stu-id="fb56c-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="fb56c-114">Ebben a példában frissítjük a meglévő kapcsolati monitort a destinationAddress módosításával és a címkék hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="fb56c-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="fb56c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb56c-115">PARAMETERS</span></span>

### <span data-ttu-id="fb56c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb56c-116">-AsJob</span></span>
<span data-ttu-id="fb56c-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fb56c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb56c-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb56c-118">-Confirm</span></span>
<span data-ttu-id="fb56c-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb56c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb56c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb56c-120">-DefaultProfile</span></span>
<span data-ttu-id="fb56c-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb56c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb56c-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="fb56c-122">-DestinationAddress</span></span>
<span data-ttu-id="fb56c-123">A kapcsolat figyelője cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="fb56c-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="fb56c-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="fb56c-124">-DestinationPort</span></span>
<span data-ttu-id="fb56c-125">Célport.</span><span class="sxs-lookup"><span data-stu-id="fb56c-125">Destination port.</span></span>

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

### <span data-ttu-id="fb56c-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="fb56c-126">-DestinationResourceId</span></span>
<span data-ttu-id="fb56c-127">A kapcsolat figyelési célhelyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fb56c-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="fb56c-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb56c-128">-InputObject</span></span>
<span data-ttu-id="fb56c-129">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="fb56c-129">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb56c-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="fb56c-130">-Location</span></span>
<span data-ttu-id="fb56c-131">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="fb56c-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="fb56c-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="fb56c-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="fb56c-133">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="fb56c-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="fb56c-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb56c-134">-Name</span></span>
<span data-ttu-id="fb56c-135">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="fb56c-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb56c-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fb56c-136">-NetworkWatcher</span></span>
<span data-ttu-id="fb56c-137">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="fb56c-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="fb56c-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fb56c-138">-NetworkWatcherName</span></span>
<span data-ttu-id="fb56c-139">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="fb56c-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="fb56c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb56c-140">-ResourceGroupName</span></span>
<span data-ttu-id="fb56c-141">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb56c-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fb56c-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb56c-142">-ResourceId</span></span>
<span data-ttu-id="fb56c-143">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fb56c-143">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb56c-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="fb56c-144">-SourcePort</span></span>
<span data-ttu-id="fb56c-145">Forrás port.</span><span class="sxs-lookup"><span data-stu-id="fb56c-145">Source port.</span></span>

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

### <span data-ttu-id="fb56c-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="fb56c-146">-SourceResourceId</span></span>
<span data-ttu-id="fb56c-147">A kapcsolat figyelője forrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fb56c-147">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb56c-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="fb56c-148">-Tag</span></span>
<span data-ttu-id="fb56c-149">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="fb56c-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fb56c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb56c-150">-WhatIf</span></span>
<span data-ttu-id="fb56c-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb56c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb56c-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb56c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb56c-153">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="fb56c-153">-ConfigureOnly</span></span>
<span data-ttu-id="fb56c-154">A kapcsolati monitor beállítása, de nem indul el</span><span class="sxs-lookup"><span data-stu-id="fb56c-154">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="fb56c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb56c-155">CommonParameters</span></span>
<span data-ttu-id="fb56c-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb56c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fb56c-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb56c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb56c-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb56c-158">INPUTS</span></span>

### <span data-ttu-id="fb56c-159">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fb56c-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="fb56c-160">System. String Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="fb56c-160">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="fb56c-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb56c-161">OUTPUTS</span></span>

### <span data-ttu-id="fb56c-162">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="fb56c-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="fb56c-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb56c-163">NOTES</span></span>
<span data-ttu-id="fb56c-164">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="fb56c-164">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="fb56c-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb56c-165">RELATED LINKS</span></span>

[<span data-ttu-id="fb56c-166">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fb56c-166">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="fb56c-167">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fb56c-167">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="fb56c-168">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fb56c-168">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="fb56c-169">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fb56c-169">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="fb56c-170">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fb56c-170">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="fb56c-171">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fb56c-171">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="fb56c-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fb56c-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="fb56c-173">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fb56c-173">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fb56c-174">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fb56c-174">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="fb56c-175">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fb56c-175">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fb56c-176">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fb56c-176">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fb56c-177">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fb56c-177">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fb56c-178">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fb56c-178">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fb56c-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fb56c-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="fb56c-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fb56c-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fb56c-181">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fb56c-181">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fb56c-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fb56c-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fb56c-183">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fb56c-183">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
