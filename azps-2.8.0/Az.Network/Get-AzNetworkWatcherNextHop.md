---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: c9c530d6677617f8969237759e172b757c14f256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837302"
---
# <span data-ttu-id="d73f6-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d73f6-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="d73f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d73f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d73f6-103">A következő ugrást kapja egy VM-ből.</span><span class="sxs-lookup"><span data-stu-id="d73f6-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="d73f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d73f6-104">SYNTAX</span></span>

### <span data-ttu-id="d73f6-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d73f6-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d73f6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d73f6-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d73f6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d73f6-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d73f6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d73f6-108">DESCRIPTION</span></span>
<span data-ttu-id="d73f6-109">A Get-AzNetworkWatcherNextHop parancsmag a VM következő ugrását kapja.</span><span class="sxs-lookup"><span data-stu-id="d73f6-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="d73f6-110">A következő ugrással megtekintheti, hogy milyen típusú Azure-erőforrás, az erőforráshoz társított IP-cím, valamint az útvonalért felelős útválasztási táblázat szabálya.</span><span class="sxs-lookup"><span data-stu-id="d73f6-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="d73f6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d73f6-111">EXAMPLES</span></span>

### <span data-ttu-id="d73f6-112">1. példa: a következő ugrás beszerzése internetes IP-címekkel való kommunikációkor</span><span class="sxs-lookup"><span data-stu-id="d73f6-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
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

<span data-ttu-id="d73f6-113">A következő ugrást kapja a kimenő kommunikációhoz a megadott virtuális gép elsődleges hálózati felületéről a 204.79.197.200 (www.bing.com).</span><span class="sxs-lookup"><span data-stu-id="d73f6-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="d73f6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d73f6-114">PARAMETERS</span></span>

### <span data-ttu-id="d73f6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d73f6-115">-AsJob</span></span>
<span data-ttu-id="d73f6-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d73f6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d73f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d73f6-117">-DefaultProfile</span></span>
<span data-ttu-id="d73f6-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d73f6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d73f6-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="d73f6-119">-DestinationIPAddress</span></span>
<span data-ttu-id="d73f6-120">Cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="d73f6-120">Destination IP address.</span></span>

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

### <span data-ttu-id="d73f6-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="d73f6-121">-Location</span></span>
<span data-ttu-id="d73f6-122">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="d73f6-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d73f6-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d73f6-123">-NetworkWatcher</span></span>
<span data-ttu-id="d73f6-124">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="d73f6-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="d73f6-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d73f6-125">-NetworkWatcherName</span></span>
<span data-ttu-id="d73f6-126">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="d73f6-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="d73f6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d73f6-127">-ResourceGroupName</span></span>
<span data-ttu-id="d73f6-128">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d73f6-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d73f6-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="d73f6-129">-SourceIPAddress</span></span>
<span data-ttu-id="d73f6-130">Forrás IP-címe.</span><span class="sxs-lookup"><span data-stu-id="d73f6-130">Source IP address.</span></span>

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

### <span data-ttu-id="d73f6-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="d73f6-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="d73f6-132">A célként megadott hálózati csatoló azonosítója</span><span class="sxs-lookup"><span data-stu-id="d73f6-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="d73f6-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d73f6-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d73f6-134">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d73f6-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="d73f6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d73f6-135">CommonParameters</span></span>
<span data-ttu-id="d73f6-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d73f6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d73f6-137">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d73f6-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d73f6-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d73f6-138">INPUTS</span></span>

### <span data-ttu-id="d73f6-139">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d73f6-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d73f6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d73f6-140">System.String</span></span>

## <span data-ttu-id="d73f6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d73f6-141">OUTPUTS</span></span>

### <span data-ttu-id="d73f6-142">Microsoft. Azure. commands. Network. models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="d73f6-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="d73f6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d73f6-143">NOTES</span></span>
<span data-ttu-id="d73f6-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, következő, ugrás</span><span class="sxs-lookup"><span data-stu-id="d73f6-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="d73f6-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d73f6-145">RELATED LINKS</span></span>

[<span data-ttu-id="d73f6-146">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d73f6-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d73f6-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d73f6-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d73f6-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d73f6-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d73f6-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d73f6-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d73f6-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d73f6-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d73f6-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d73f6-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d73f6-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d73f6-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d73f6-153">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d73f6-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d73f6-154">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d73f6-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d73f6-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d73f6-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d73f6-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d73f6-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d73f6-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d73f6-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d73f6-158">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d73f6-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d73f6-159">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d73f6-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d73f6-160">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d73f6-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d73f6-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d73f6-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d73f6-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d73f6-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d73f6-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d73f6-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d73f6-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d73f6-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d73f6-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d73f6-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d73f6-166">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d73f6-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d73f6-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d73f6-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d73f6-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d73f6-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d73f6-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d73f6-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d73f6-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d73f6-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d73f6-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d73f6-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d73f6-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d73f6-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
