---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 4c6a1e179cf0c6086035488d092232e85c570637
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495084"
---
# <span data-ttu-id="9c5e7-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9c5e7-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="9c5e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5e7-103">A következő ugrást kapja egy VM-ből.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c5e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c5e7-104">SYNTAX</span></span>

### <span data-ttu-id="9c5e7-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c5e7-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c5e7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9c5e7-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c5e7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9c5e7-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c5e7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c5e7-108">DESCRIPTION</span></span>
<span data-ttu-id="9c5e7-109">A Get-AzureRmNetworkWatcherNextHop parancsmag a VM következő ugrását kapja.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-109">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="9c5e7-110">A következő ugrással megtekintheti, hogy milyen típusú Azure-erőforrás, az erőforráshoz társított IP-cím, valamint az útvonalért felelős útválasztási táblázat szabálya.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="9c5e7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9c5e7-111">EXAMPLES</span></span>

### <span data-ttu-id="9c5e7-112">1. példa: a következő ugrás beszerzése internetes IP-címekkel való kommunikációkor</span><span class="sxs-lookup"><span data-stu-id="9c5e7-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="9c5e7-113">A következő ugrás a kimenő kommunikációhoz az elsődleges hálózati csatolóról a megadott virtuális Vachine a 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="9c5e7-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="9c5e7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c5e7-114">PARAMETERS</span></span>

### <span data-ttu-id="9c5e7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c5e7-115">-AsJob</span></span>
<span data-ttu-id="9c5e7-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9c5e7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c5e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5e7-117">-DefaultProfile</span></span>
<span data-ttu-id="9c5e7-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c5e7-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="9c5e7-119">-DestinationIPAddress</span></span>
<span data-ttu-id="9c5e7-120">Cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-120">Destination IP address.</span></span>

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

### <span data-ttu-id="9c5e7-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="9c5e7-121">-Location</span></span>
<span data-ttu-id="9c5e7-122">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9c5e7-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9c5e7-123">-NetworkWatcher</span></span>
<span data-ttu-id="9c5e7-124">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="9c5e7-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9c5e7-125">-NetworkWatcherName</span></span>
<span data-ttu-id="9c5e7-126">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="9c5e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c5e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c5e7-128">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9c5e7-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="9c5e7-129">-SourceIPAddress</span></span>
<span data-ttu-id="9c5e7-130">Forrás IP-címe.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-130">Source IP address.</span></span>

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

### <span data-ttu-id="9c5e7-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="9c5e7-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="9c5e7-132">A célként megadott hálózati csatoló azonosítója</span><span class="sxs-lookup"><span data-stu-id="9c5e7-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="9c5e7-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="9c5e7-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="9c5e7-134">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9c5e7-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="9c5e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5e7-135">CommonParameters</span></span>
<span data-ttu-id="9c5e7-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c5e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5e7-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5e7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5e7-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c5e7-138">INPUTS</span></span>

### <span data-ttu-id="9c5e7-139">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9c5e7-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9c5e7-140">Paraméterek: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9c5e7-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="9c5e7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9c5e7-141">System.String</span></span>
<span data-ttu-id="9c5e7-142">Paraméterek: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9c5e7-142">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="9c5e7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c5e7-143">OUTPUTS</span></span>

### <span data-ttu-id="9c5e7-144">Microsoft. Azure. commands. Network. models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="9c5e7-144">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="9c5e7-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c5e7-145">NOTES</span></span>
<span data-ttu-id="9c5e7-146">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, következő, ugrás</span><span class="sxs-lookup"><span data-stu-id="9c5e7-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="9c5e7-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c5e7-147">RELATED LINKS</span></span>

[<span data-ttu-id="9c5e7-148">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9c5e7-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9c5e7-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9c5e7-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9c5e7-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9c5e7-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9c5e7-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9c5e7-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="9c5e7-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9c5e7-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9c5e7-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9c5e7-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="9c5e7-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9c5e7-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9c5e7-155">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9c5e7-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9c5e7-156">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9c5e7-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="9c5e7-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9c5e7-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9c5e7-158">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9c5e7-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9c5e7-159">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9c5e7-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9c5e7-160">Új – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c5e7-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9c5e7-161">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9c5e7-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="9c5e7-162">Teszt-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9c5e7-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="9c5e7-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c5e7-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9c5e7-164">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c5e7-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9c5e7-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c5e7-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9c5e7-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9c5e7-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9c5e7-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c5e7-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9c5e7-168">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c5e7-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9c5e7-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9c5e7-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9c5e7-170">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9c5e7-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9c5e7-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9c5e7-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9c5e7-172">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9c5e7-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9c5e7-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9c5e7-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="9c5e7-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c5e7-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
