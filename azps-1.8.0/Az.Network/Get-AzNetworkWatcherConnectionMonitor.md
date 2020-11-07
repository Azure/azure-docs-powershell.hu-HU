---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 0c59de4b0c6dfd7da196b4ec67999406a14e0d1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670524"
---
# <span data-ttu-id="0cf94-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0cf94-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="0cf94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0cf94-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf94-103">A megadott névvel vagy a kapcsolati figyelőket tartalmazó kapcsolat monitorát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0cf94-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="0cf94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0cf94-104">SYNTAX</span></span>

### <span data-ttu-id="0cf94-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0cf94-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf94-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0cf94-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf94-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0cf94-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cf94-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0cf94-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cf94-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0cf94-109">DESCRIPTION</span></span>
<span data-ttu-id="0cf94-110">A Get-AzNetworkWatcherConnectionMonitor parancsmag a megadott nevű vagy resourceId, illetve a megadott Hálózatfigyelő vagy-helynek megfelelő kapcsolati monitorokat tartalmazó kapcsolati monitort adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0cf94-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="0cf94-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0cf94-111">EXAMPLES</span></span>

### <span data-ttu-id="0cf94-112">Példa 1: a kapcsolat monitorjának beszerzése név szerint a megadott helyen</span><span class="sxs-lookup"><span data-stu-id="0cf94-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="0cf94-113">Ebben a példában a kapcsolat monitort a megadott helyen, név szerint szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="0cf94-113">In this example we get connection monitor by name in the specified location.</span></span>

### <span data-ttu-id="0cf94-114">2. példa: a kapcsolati monitorok szűréssel való beolvasása</span><span class="sxs-lookup"><span data-stu-id="0cf94-114">Example 2: Get connection monitors using filtering</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -ResourceGroupName NetworkWatcherRG -NetworkWatcherName NetworkWatcher_centraluseuap -Name cm*


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="0cf94-115">Ebben a példában bemutatjuk az összes olyan NetworkWatcher_centraluseuap-monitort, amely a "cm"-vel kezdődően jelenik meg</span><span class="sxs-lookup"><span data-stu-id="0cf94-115">In this example we get all connection monitors in NetworkWatcher_centraluseuap that start with "cm"</span></span>

## <span data-ttu-id="0cf94-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0cf94-116">PARAMETERS</span></span>

### <span data-ttu-id="0cf94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf94-117">-DefaultProfile</span></span>
<span data-ttu-id="0cf94-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cf94-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cf94-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="0cf94-119">-Location</span></span>
<span data-ttu-id="0cf94-120">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="0cf94-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0cf94-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0cf94-121">-Name</span></span>
<span data-ttu-id="0cf94-122">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="0cf94-122">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="0cf94-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0cf94-123">-NetworkWatcher</span></span>
<span data-ttu-id="0cf94-124">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="0cf94-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="0cf94-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0cf94-125">-NetworkWatcherName</span></span>
<span data-ttu-id="0cf94-126">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="0cf94-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="0cf94-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cf94-127">-ResourceGroupName</span></span>
<span data-ttu-id="0cf94-128">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0cf94-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0cf94-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cf94-129">-ResourceId</span></span>
<span data-ttu-id="0cf94-130">A kapcsolat figyelője erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0cf94-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="0cf94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf94-131">CommonParameters</span></span>
<span data-ttu-id="0cf94-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0cf94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf94-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0cf94-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf94-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cf94-134">INPUTS</span></span>

### <span data-ttu-id="0cf94-135">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0cf94-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0cf94-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf94-136">System.String</span></span>

## <span data-ttu-id="0cf94-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cf94-137">OUTPUTS</span></span>

### <span data-ttu-id="0cf94-138">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="0cf94-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="0cf94-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0cf94-139">NOTES</span></span>
<span data-ttu-id="0cf94-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="0cf94-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="0cf94-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cf94-141">RELATED LINKS</span></span>

[<span data-ttu-id="0cf94-142">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0cf94-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0cf94-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0cf94-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0cf94-144">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0cf94-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0cf94-145">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0cf94-145">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0cf94-146">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0cf94-146">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0cf94-147">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0cf94-147">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0cf94-148">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0cf94-148">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0cf94-149">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0cf94-149">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0cf94-150">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0cf94-150">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0cf94-151">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0cf94-151">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0cf94-152">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0cf94-152">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0cf94-153">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0cf94-153">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0cf94-154">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0cf94-154">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0cf94-155">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0cf94-155">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0cf94-156">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0cf94-156">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0cf94-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0cf94-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0cf94-158">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0cf94-158">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0cf94-159">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0cf94-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0cf94-160">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0cf94-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0cf94-161">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0cf94-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0cf94-162">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0cf94-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0cf94-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0cf94-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0cf94-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0cf94-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0cf94-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0cf94-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0cf94-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0cf94-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0cf94-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0cf94-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0cf94-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0cf94-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
