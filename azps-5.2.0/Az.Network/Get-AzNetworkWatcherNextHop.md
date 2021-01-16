---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: cf120e8e9ca9e0dad8f4d430c7f207d40fcfab3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358510"
---
# <span data-ttu-id="2502b-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2502b-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="2502b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2502b-102">SYNOPSIS</span></span>
<span data-ttu-id="2502b-103">A következő ugrás egy VM-ről.</span><span class="sxs-lookup"><span data-stu-id="2502b-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="2502b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2502b-104">SYNTAX</span></span>

### <span data-ttu-id="2502b-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2502b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2502b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2502b-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2502b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2502b-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2502b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2502b-108">DESCRIPTION</span></span>
<span data-ttu-id="2502b-109">A Get-AzNetworkWatcherNextHop parancsmag a következő ugrást egy VM-től kapja.</span><span class="sxs-lookup"><span data-stu-id="2502b-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="2502b-110">A következő ugrással megtekintheti az Azure-erőforrás típusát, az erőforrás társított IP-címét és az útvonalért felelős útválasztási táblaszabályt.</span><span class="sxs-lookup"><span data-stu-id="2502b-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="2502b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2502b-111">EXAMPLES</span></span>

### <span data-ttu-id="2502b-112">1. példa: A következő ugrás az internetes IP-címekkel való kommunikáció során</span><span class="sxs-lookup"><span data-stu-id="2502b-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="2502b-113">A következő ugrás a megadott virtuális gép elsődleges hálózati felületéről a 204.79.197.200-as (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="2502b-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="2502b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2502b-114">PARAMETERS</span></span>

### <span data-ttu-id="2502b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2502b-115">-AsJob</span></span>
<span data-ttu-id="2502b-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2502b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2502b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2502b-117">-DefaultProfile</span></span>
<span data-ttu-id="2502b-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2502b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2502b-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="2502b-119">-DestinationIPAddress</span></span>
<span data-ttu-id="2502b-120">Cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="2502b-120">Destination IP address.</span></span>

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

### <span data-ttu-id="2502b-121">-Location</span><span class="sxs-lookup"><span data-stu-id="2502b-121">-Location</span></span>
<span data-ttu-id="2502b-122">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="2502b-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2502b-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2502b-123">-NetworkWatcher</span></span>
<span data-ttu-id="2502b-124">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="2502b-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="2502b-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2502b-125">-NetworkWatcherName</span></span>
<span data-ttu-id="2502b-126">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="2502b-126">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2502b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2502b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2502b-128">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2502b-128">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2502b-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="2502b-129">-SourceIPAddress</span></span>
<span data-ttu-id="2502b-130">Forrás IP-címe.</span><span class="sxs-lookup"><span data-stu-id="2502b-130">Source IP address.</span></span>

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

### <span data-ttu-id="2502b-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="2502b-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="2502b-132">Célhálózati felület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2502b-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="2502b-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2502b-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2502b-134">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2502b-134">The target virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2502b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2502b-135">CommonParameters</span></span>
<span data-ttu-id="2502b-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2502b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2502b-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2502b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2502b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2502b-138">INPUTS</span></span>

### <span data-ttu-id="2502b-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2502b-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2502b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2502b-140">System.String</span></span>

## <span data-ttu-id="2502b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2502b-141">OUTPUTS</span></span>

### <span data-ttu-id="2502b-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="2502b-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="2502b-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2502b-143">NOTES</span></span>
<span data-ttu-id="2502b-144">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="2502b-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="2502b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2502b-145">RELATED LINKS</span></span>

[<span data-ttu-id="2502b-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2502b-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2502b-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2502b-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2502b-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2502b-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2502b-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2502b-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2502b-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2502b-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2502b-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2502b-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2502b-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2502b-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2502b-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2502b-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2502b-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2502b-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2502b-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2502b-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2502b-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2502b-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2502b-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2502b-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2502b-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2502b-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2502b-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2502b-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2502b-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2502b-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2502b-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2502b-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2502b-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2502b-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2502b-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2502b-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2502b-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2502b-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2502b-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2502b-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2502b-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2502b-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2502b-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2502b-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2502b-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2502b-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2502b-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2502b-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2502b-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2502b-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2502b-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2502b-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2502b-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2502b-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
