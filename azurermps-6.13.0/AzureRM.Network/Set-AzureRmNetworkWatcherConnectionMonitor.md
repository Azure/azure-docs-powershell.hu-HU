---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5c7709c234ba762e5b87418cc0e9b3fc4637ac11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672923"
---
# <span data-ttu-id="86e73-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86e73-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="86e73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86e73-102">SYNOPSIS</span></span>
<span data-ttu-id="86e73-103">Frissítheti a kapcsolat monitorát.</span><span class="sxs-lookup"><span data-stu-id="86e73-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86e73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86e73-104">SYNTAX</span></span>

### <span data-ttu-id="86e73-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86e73-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86e73-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="86e73-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86e73-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="86e73-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86e73-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="86e73-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86e73-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="86e73-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e73-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="86e73-110">DESCRIPTION</span></span>
<span data-ttu-id="86e73-111">A Set-AzureRmNetworkWatcherConnectionMonitor parancsmag frissíti a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="86e73-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="86e73-112">Példák</span><span class="sxs-lookup"><span data-stu-id="86e73-112">EXAMPLES</span></span>

### <span data-ttu-id="86e73-113">1. példa: a kapcsolat monitorának frissítése</span><span class="sxs-lookup"><span data-stu-id="86e73-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="86e73-114">Ebben a példában frissítjük a meglévő kapcsolati monitort a destinationAddress módosításával és a címkék hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="86e73-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="86e73-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86e73-115">PARAMETERS</span></span>

### <span data-ttu-id="86e73-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86e73-116">-AsJob</span></span>
<span data-ttu-id="86e73-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="86e73-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86e73-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="86e73-118">-ConfigureOnly</span></span>
<span data-ttu-id="86e73-119">A kapcsolati monitor beállítása, de nem indul el</span><span class="sxs-lookup"><span data-stu-id="86e73-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="86e73-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e73-120">-DefaultProfile</span></span>
<span data-ttu-id="86e73-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86e73-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86e73-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="86e73-122">-DestinationAddress</span></span>
<span data-ttu-id="86e73-123">A kapcsolat figyelője cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="86e73-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="86e73-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="86e73-124">-DestinationPort</span></span>
<span data-ttu-id="86e73-125">Célport.</span><span class="sxs-lookup"><span data-stu-id="86e73-125">Destination port.</span></span>

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

### <span data-ttu-id="86e73-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="86e73-126">-DestinationResourceId</span></span>
<span data-ttu-id="86e73-127">A kapcsolat figyelési célhelyének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="86e73-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="86e73-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86e73-128">-InputObject</span></span>
<span data-ttu-id="86e73-129">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="86e73-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="86e73-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="86e73-130">-Location</span></span>
<span data-ttu-id="86e73-131">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="86e73-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="86e73-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="86e73-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="86e73-133">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="86e73-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="86e73-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86e73-134">-Name</span></span>
<span data-ttu-id="86e73-135">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="86e73-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="86e73-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86e73-136">-NetworkWatcher</span></span>
<span data-ttu-id="86e73-137">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="86e73-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="86e73-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="86e73-138">-NetworkWatcherName</span></span>
<span data-ttu-id="86e73-139">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="86e73-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="86e73-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e73-140">-ResourceGroupName</span></span>
<span data-ttu-id="86e73-141">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86e73-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="86e73-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86e73-142">-ResourceId</span></span>
<span data-ttu-id="86e73-143">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="86e73-143">Resource ID.</span></span>

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

### <span data-ttu-id="86e73-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="86e73-144">-SourcePort</span></span>
<span data-ttu-id="86e73-145">Forrás port.</span><span class="sxs-lookup"><span data-stu-id="86e73-145">Source port.</span></span>

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

### <span data-ttu-id="86e73-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="86e73-146">-SourceResourceId</span></span>
<span data-ttu-id="86e73-147">A kapcsolat figyelője forrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="86e73-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="86e73-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="86e73-148">-Tag</span></span>
<span data-ttu-id="86e73-149">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="86e73-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="86e73-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86e73-150">-Confirm</span></span>
<span data-ttu-id="86e73-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86e73-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86e73-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e73-152">-WhatIf</span></span>
<span data-ttu-id="86e73-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86e73-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86e73-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86e73-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86e73-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e73-155">CommonParameters</span></span>
<span data-ttu-id="86e73-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86e73-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e73-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86e73-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e73-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86e73-158">INPUTS</span></span>

### <span data-ttu-id="86e73-159">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86e73-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="86e73-160">Paraméterek: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="86e73-160">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="86e73-161">System. String</span><span class="sxs-lookup"><span data-stu-id="86e73-161">System.String</span></span>

### <span data-ttu-id="86e73-162">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="86e73-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="86e73-163">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="86e73-163">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="86e73-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86e73-164">OUTPUTS</span></span>

### <span data-ttu-id="86e73-165">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="86e73-165">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="86e73-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86e73-166">NOTES</span></span>
<span data-ttu-id="86e73-167">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="86e73-167">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="86e73-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86e73-168">RELATED LINKS</span></span>

[<span data-ttu-id="86e73-169">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86e73-169">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="86e73-170">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86e73-170">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="86e73-171">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86e73-171">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="86e73-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="86e73-172">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="86e73-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="86e73-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="86e73-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="86e73-174">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="86e73-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="86e73-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="86e73-176">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86e73-176">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="86e73-177">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="86e73-177">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="86e73-178">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86e73-178">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="86e73-179">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86e73-179">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="86e73-180">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86e73-180">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="86e73-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86e73-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="86e73-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="86e73-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="86e73-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86e73-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="86e73-184">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86e73-184">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="86e73-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86e73-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="86e73-186">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86e73-186">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="86e73-187">Új – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="86e73-187">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="86e73-188">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="86e73-188">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="86e73-189">Teszt-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="86e73-189">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="86e73-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="86e73-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="86e73-191">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86e73-191">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="86e73-192">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="86e73-192">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="86e73-193">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="86e73-193">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="86e73-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="86e73-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="86e73-195">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="86e73-195">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
