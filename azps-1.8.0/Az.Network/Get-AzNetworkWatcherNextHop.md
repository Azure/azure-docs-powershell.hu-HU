---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 51fea717c352f00b4f356e6bb07b730cdeb60966
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670521"
---
# <span data-ttu-id="611ba-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="611ba-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="611ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="611ba-102">SYNOPSIS</span></span>
<span data-ttu-id="611ba-103">A következő ugrást kapja egy VM-ből.</span><span class="sxs-lookup"><span data-stu-id="611ba-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="611ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="611ba-104">SYNTAX</span></span>

### <span data-ttu-id="611ba-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="611ba-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="611ba-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="611ba-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="611ba-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="611ba-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="611ba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="611ba-108">DESCRIPTION</span></span>
<span data-ttu-id="611ba-109">A Get-AzNetworkWatcherNextHop parancsmag a VM következő ugrását kapja.</span><span class="sxs-lookup"><span data-stu-id="611ba-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="611ba-110">A következő ugrással megtekintheti, hogy milyen típusú Azure-erőforrás, az erőforráshoz társított IP-cím, valamint az útvonalért felelős útválasztási táblázat szabálya.</span><span class="sxs-lookup"><span data-stu-id="611ba-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="611ba-111">Példák</span><span class="sxs-lookup"><span data-stu-id="611ba-111">EXAMPLES</span></span>

### <span data-ttu-id="611ba-112">1. példa: a következő ugrás beszerzése internetes IP-címekkel való kommunikációkor</span><span class="sxs-lookup"><span data-stu-id="611ba-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
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

<span data-ttu-id="611ba-113">A következő ugrás a kimenő kommunikációhoz az elsődleges hálózati csatolóról a megadott virtuális Vachine a 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="611ba-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="611ba-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="611ba-114">PARAMETERS</span></span>

### <span data-ttu-id="611ba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="611ba-115">-AsJob</span></span>
<span data-ttu-id="611ba-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="611ba-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="611ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="611ba-117">-DefaultProfile</span></span>
<span data-ttu-id="611ba-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="611ba-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="611ba-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="611ba-119">-DestinationIPAddress</span></span>
<span data-ttu-id="611ba-120">Cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="611ba-120">Destination IP address.</span></span>

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

### <span data-ttu-id="611ba-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="611ba-121">-Location</span></span>
<span data-ttu-id="611ba-122">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="611ba-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="611ba-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="611ba-123">-NetworkWatcher</span></span>
<span data-ttu-id="611ba-124">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="611ba-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="611ba-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="611ba-125">-NetworkWatcherName</span></span>
<span data-ttu-id="611ba-126">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="611ba-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="611ba-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="611ba-127">-ResourceGroupName</span></span>
<span data-ttu-id="611ba-128">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="611ba-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="611ba-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="611ba-129">-SourceIPAddress</span></span>
<span data-ttu-id="611ba-130">Forrás IP-címe.</span><span class="sxs-lookup"><span data-stu-id="611ba-130">Source IP address.</span></span>

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

### <span data-ttu-id="611ba-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="611ba-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="611ba-132">A célként megadott hálózati csatoló azonosítója</span><span class="sxs-lookup"><span data-stu-id="611ba-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="611ba-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="611ba-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="611ba-134">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="611ba-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="611ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611ba-135">CommonParameters</span></span>
<span data-ttu-id="611ba-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="611ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611ba-137">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="611ba-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611ba-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="611ba-138">INPUTS</span></span>

### <span data-ttu-id="611ba-139">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="611ba-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="611ba-140">System. String</span><span class="sxs-lookup"><span data-stu-id="611ba-140">System.String</span></span>

## <span data-ttu-id="611ba-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="611ba-141">OUTPUTS</span></span>

### <span data-ttu-id="611ba-142">Microsoft. Azure. commands. Network. models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="611ba-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="611ba-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="611ba-143">NOTES</span></span>
<span data-ttu-id="611ba-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, következő, ugrás</span><span class="sxs-lookup"><span data-stu-id="611ba-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="611ba-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="611ba-145">RELATED LINKS</span></span>

[<span data-ttu-id="611ba-146">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="611ba-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="611ba-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="611ba-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="611ba-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="611ba-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="611ba-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="611ba-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="611ba-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="611ba-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="611ba-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="611ba-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="611ba-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="611ba-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="611ba-153">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="611ba-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="611ba-154">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="611ba-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="611ba-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="611ba-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="611ba-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="611ba-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="611ba-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="611ba-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="611ba-158">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="611ba-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="611ba-159">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="611ba-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="611ba-160">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="611ba-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="611ba-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="611ba-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="611ba-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="611ba-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="611ba-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="611ba-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="611ba-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="611ba-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="611ba-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="611ba-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="611ba-166">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="611ba-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="611ba-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="611ba-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="611ba-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="611ba-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="611ba-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="611ba-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="611ba-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="611ba-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="611ba-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="611ba-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="611ba-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="611ba-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
