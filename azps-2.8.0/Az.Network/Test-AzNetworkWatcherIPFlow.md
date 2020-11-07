---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 61946fcf8023fa46e6296bb976fd474f5021a195
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838271"
---
# <span data-ttu-id="8b2a6-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8b2a6-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="8b2a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b2a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2a6-103">Azt számítja ki, hogy a csomag engedélyezett vagy megtagadva van-e egy adott célhelyen.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="8b2a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b2a6-104">SYNTAX</span></span>

### <span data-ttu-id="8b2a6-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8b2a6-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b2a6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8b2a6-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b2a6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8b2a6-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b2a6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b2a6-108">DESCRIPTION</span></span>
<span data-ttu-id="8b2a6-109">A Test-AzNetworkWatcherIPFlow parancsmag egy megadott VM-erőforráshoz és egy megadott irányú csomaghoz helyi és távoli, IP-címek és portok használatával, azt adja eredményül, hogy engedélyezett vagy megtagadta-e a csomagot.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="8b2a6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8b2a6-110">EXAMPLES</span></span>

### <span data-ttu-id="8b2a6-111">1. példa: Test-AzNetworkWatcherIPFlow futtatása</span><span class="sxs-lookup"><span data-stu-id="8b2a6-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="8b2a6-112">Itt kapja meg az előfizetéshez tartozó Közép-amerikai hálózati figyelőt, majd megkapja a VM-et és a hozzá tartozó hálózati csatolókat.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="8b2a6-113">Ezután az első hálózati felületen az első IP-kapcsolaton futó IP-kapcsolaton keresztül futtatja a Test-AzNetworkWatcherIPFlowt egy internetes IP-kapcsolaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="8b2a6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b2a6-114">PARAMETERS</span></span>

### <span data-ttu-id="8b2a6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b2a6-115">-AsJob</span></span>
<span data-ttu-id="8b2a6-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8b2a6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b2a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2a6-117">-DefaultProfile</span></span>
<span data-ttu-id="8b2a6-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b2a6-119">-Irány</span><span class="sxs-lookup"><span data-stu-id="8b2a6-119">-Direction</span></span>
<span data-ttu-id="8b2a6-120">Irányba.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-120">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b2a6-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="8b2a6-121">-LocalIPAddress</span></span>
<span data-ttu-id="8b2a6-122">Helyi IP-cím.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-122">Local IP Address.</span></span>

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

### <span data-ttu-id="8b2a6-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="8b2a6-123">-LocalPort</span></span>
<span data-ttu-id="8b2a6-124">Helyi port.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-124">Local Port.</span></span>

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

### <span data-ttu-id="8b2a6-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="8b2a6-125">-Location</span></span>
<span data-ttu-id="8b2a6-126">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8b2a6-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8b2a6-127">-NetworkWatcher</span></span>
<span data-ttu-id="8b2a6-128">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="8b2a6-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8b2a6-129">-NetworkWatcherName</span></span>
<span data-ttu-id="8b2a6-130">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="8b2a6-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8b2a6-131">-Protocol</span></span>
<span data-ttu-id="8b2a6-132">Protokoll.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-132">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b2a6-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="8b2a6-133">-RemoteIPAddress</span></span>
<span data-ttu-id="8b2a6-134">Távoli IP-cím.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="8b2a6-135">-TávoliPORT</span><span class="sxs-lookup"><span data-stu-id="8b2a6-135">-RemotePort</span></span>
<span data-ttu-id="8b2a6-136">Távoli port.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-136">Remote port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b2a6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b2a6-137">-ResourceGroupName</span></span>
<span data-ttu-id="8b2a6-138">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8b2a6-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="8b2a6-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="8b2a6-140">A célként megadott hálózati csatoló azonosítója</span><span class="sxs-lookup"><span data-stu-id="8b2a6-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="8b2a6-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="8b2a6-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="8b2a6-142">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8b2a6-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="8b2a6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2a6-143">CommonParameters</span></span>
<span data-ttu-id="8b2a6-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b2a6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2a6-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b2a6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2a6-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b2a6-146">INPUTS</span></span>

### <span data-ttu-id="8b2a6-147">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8b2a6-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="8b2a6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8b2a6-148">System.String</span></span>

## <span data-ttu-id="8b2a6-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b2a6-149">OUTPUTS</span></span>

### <span data-ttu-id="8b2a6-150">Microsoft. Azure. commands. Network. models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="8b2a6-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="8b2a6-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b2a6-151">NOTES</span></span>
<span data-ttu-id="8b2a6-152">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, adatfolyam, IP</span><span class="sxs-lookup"><span data-stu-id="8b2a6-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="8b2a6-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b2a6-153">RELATED LINKS</span></span>

[<span data-ttu-id="8b2a6-154">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8b2a6-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8b2a6-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8b2a6-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8b2a6-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8b2a6-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8b2a6-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8b2a6-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8b2a6-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8b2a6-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8b2a6-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8b2a6-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8b2a6-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8b2a6-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8b2a6-161">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8b2a6-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8b2a6-162">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8b2a6-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8b2a6-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8b2a6-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8b2a6-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8b2a6-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8b2a6-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8b2a6-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8b2a6-166">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b2a6-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8b2a6-167">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8b2a6-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8b2a6-168">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8b2a6-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8b2a6-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8b2a6-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8b2a6-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8b2a6-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8b2a6-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8b2a6-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8b2a6-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8b2a6-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8b2a6-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8b2a6-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8b2a6-174">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8b2a6-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8b2a6-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8b2a6-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8b2a6-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8b2a6-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8b2a6-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8b2a6-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8b2a6-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8b2a6-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8b2a6-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8b2a6-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="8b2a6-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8b2a6-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
