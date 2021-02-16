---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: cf5d5cba1b824af3187b681c7c87f26e4970b197
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402762"
---
# <span data-ttu-id="b70fb-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b70fb-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="b70fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b70fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b70fb-103">A Hálózati figyelő tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="b70fb-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="b70fb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b70fb-104">SYNTAX</span></span>

### <span data-ttu-id="b70fb-105">Lista</span><span class="sxs-lookup"><span data-stu-id="b70fb-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b70fb-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b70fb-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b70fb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b70fb-107">DESCRIPTION</span></span>
<span data-ttu-id="b70fb-108">A Get-AzNetworkWatcher parancsmag egy vagy több Azure Network Watcher-erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="b70fb-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="b70fb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b70fb-109">EXAMPLES</span></span>

### <span data-ttu-id="b70fb-110">1. példa: Hálózati figyelő lekérte</span><span class="sxs-lookup"><span data-stu-id="b70fb-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="b70fb-111">A NetworkWatcherRG erőforráscsoportban NetworkWatcher_westcentralus a Network WatcherRG nevű hálózatfigyelőt.</span><span class="sxs-lookup"><span data-stu-id="b70fb-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="b70fb-112">2. példa: Hálózati figyelőlista szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="b70fb-112">Example 2: List Network Watchers using filtering</span></span>
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

<span data-ttu-id="b70fb-113">A "NetworkWatcher" kezdetnek megfelelő hálózati figyelőket kapja meg</span><span class="sxs-lookup"><span data-stu-id="b70fb-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="b70fb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b70fb-114">PARAMETERS</span></span>

### <span data-ttu-id="b70fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70fb-115">-DefaultProfile</span></span>
<span data-ttu-id="b70fb-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b70fb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b70fb-117">-Location</span><span class="sxs-lookup"><span data-stu-id="b70fb-117">-Location</span></span>
<span data-ttu-id="b70fb-118">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="b70fb-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b70fb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b70fb-119">-Name</span></span>
<span data-ttu-id="b70fb-120">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="b70fb-120">The network watcher name.</span></span>

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

### <span data-ttu-id="b70fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b70fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="b70fb-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b70fb-122">The resource group name.</span></span>

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

### <span data-ttu-id="b70fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70fb-123">CommonParameters</span></span>
<span data-ttu-id="b70fb-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b70fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70fb-125">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b70fb-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70fb-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b70fb-126">INPUTS</span></span>

### <span data-ttu-id="b70fb-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="b70fb-127">None</span></span>

## <span data-ttu-id="b70fb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b70fb-128">OUTPUTS</span></span>

### <span data-ttu-id="b70fb-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b70fb-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="b70fb-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b70fb-130">NOTES</span></span>
<span data-ttu-id="b70fb-131">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő</span><span class="sxs-lookup"><span data-stu-id="b70fb-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="b70fb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b70fb-132">RELATED LINKS</span></span>

[<span data-ttu-id="b70fb-133">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b70fb-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b70fb-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b70fb-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b70fb-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b70fb-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b70fb-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b70fb-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b70fb-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b70fb-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b70fb-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b70fb-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b70fb-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b70fb-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b70fb-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b70fb-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b70fb-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b70fb-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b70fb-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b70fb-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b70fb-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b70fb-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b70fb-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b70fb-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b70fb-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b70fb-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b70fb-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b70fb-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b70fb-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b70fb-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b70fb-148">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b70fb-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b70fb-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b70fb-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b70fb-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b70fb-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b70fb-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b70fb-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b70fb-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b70fb-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b70fb-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b70fb-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b70fb-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b70fb-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b70fb-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b70fb-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b70fb-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b70fb-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b70fb-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b70fb-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b70fb-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b70fb-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b70fb-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b70fb-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
