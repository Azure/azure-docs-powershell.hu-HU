---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: c1ea29572bb42bea0c7e64c3ec818fe2f2d0ed0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845941"
---
# <span data-ttu-id="bac2d-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bac2d-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="bac2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bac2d-102">SYNOPSIS</span></span>
<span data-ttu-id="bac2d-103">A Hálózatfigyelő tulajdonságait kapja meg</span><span class="sxs-lookup"><span data-stu-id="bac2d-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="bac2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bac2d-104">SYNTAX</span></span>

### <span data-ttu-id="bac2d-105">Lista</span><span class="sxs-lookup"><span data-stu-id="bac2d-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bac2d-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bac2d-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bac2d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bac2d-107">DESCRIPTION</span></span>
<span data-ttu-id="bac2d-108">A Get-AzNetworkWatcher parancsmag egy vagy több Azure Network Watcher-erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="bac2d-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="bac2d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bac2d-109">EXAMPLES</span></span>

### <span data-ttu-id="bac2d-110">Példa 1: hálózati figyelő beszerzése</span><span class="sxs-lookup"><span data-stu-id="bac2d-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="bac2d-111">A NetworkWatcher_westcentralus nevű Hálózatfigyelőt kapja az erőforráscsoport NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="bac2d-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="bac2d-112">2. példa: szűrést használó hálózati figyelők listázása</span><span class="sxs-lookup"><span data-stu-id="bac2d-112">Example 2: List Network Watchers using filtering</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher*

Name              : NetworkWatcher_westcentralus1
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus1
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded

Name              : NetworkWatcher_westcentralus2
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus2
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="bac2d-113">A "NetworkWatcher" kezdetű hálózati figyelők beolvasása</span><span class="sxs-lookup"><span data-stu-id="bac2d-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="bac2d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bac2d-114">PARAMETERS</span></span>

### <span data-ttu-id="bac2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac2d-115">-DefaultProfile</span></span>
<span data-ttu-id="bac2d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bac2d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bac2d-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="bac2d-117">-Location</span></span>
<span data-ttu-id="bac2d-118">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="bac2d-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bac2d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bac2d-119">-Name</span></span>
<span data-ttu-id="bac2d-120">A Hálózatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="bac2d-120">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="bac2d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bac2d-121">-ResourceGroupName</span></span>
<span data-ttu-id="bac2d-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="bac2d-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="bac2d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac2d-123">CommonParameters</span></span>
<span data-ttu-id="bac2d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bac2d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac2d-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bac2d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac2d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bac2d-126">INPUTS</span></span>

### <span data-ttu-id="bac2d-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="bac2d-127">None</span></span>

## <span data-ttu-id="bac2d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bac2d-128">OUTPUTS</span></span>

### <span data-ttu-id="bac2d-129">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bac2d-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="bac2d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bac2d-130">NOTES</span></span>
<span data-ttu-id="bac2d-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="bac2d-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="bac2d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bac2d-132">RELATED LINKS</span></span>

[<span data-ttu-id="bac2d-133">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bac2d-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bac2d-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bac2d-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bac2d-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bac2d-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bac2d-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bac2d-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bac2d-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bac2d-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bac2d-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bac2d-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bac2d-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bac2d-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="bac2d-140">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bac2d-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bac2d-141">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bac2d-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bac2d-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bac2d-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bac2d-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bac2d-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bac2d-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bac2d-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bac2d-145">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="bac2d-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="bac2d-146">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bac2d-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bac2d-147">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="bac2d-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="bac2d-148">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bac2d-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bac2d-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bac2d-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bac2d-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bac2d-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bac2d-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bac2d-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="bac2d-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bac2d-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bac2d-153">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bac2d-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bac2d-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bac2d-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="bac2d-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="bac2d-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="bac2d-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="bac2d-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="bac2d-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="bac2d-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="bac2d-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="bac2d-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="bac2d-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bac2d-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
