---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 8be10fd630bbc9d4e1952150728d144b5f552fe6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918481"
---
# <span data-ttu-id="78a52-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="78a52-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="78a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a52-102">SYNOPSIS</span></span>
<span data-ttu-id="78a52-103">Visszaadja, hogy a csomag engedélyezett-e vagy megtagadható-e egy adott célhelyhez vagy egy adott célhelytől.</span><span class="sxs-lookup"><span data-stu-id="78a52-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="78a52-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="78a52-104">SYNTAX</span></span>

### <span data-ttu-id="78a52-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78a52-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a52-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="78a52-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a52-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="78a52-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78a52-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="78a52-108">DESCRIPTION</span></span>
<span data-ttu-id="78a52-109">A Test-AzNetworkWatcherIPFlow egy adott VM-erőforráshoz és egy helyi és távoli IP-címeket és portokat használó meghatározott irányú csomaghoz megadott parancsmag visszaadja, hogy a csomag engedélyezett vagy megtagadható-e.</span><span class="sxs-lookup"><span data-stu-id="78a52-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="78a52-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="78a52-110">EXAMPLES</span></span>

### <span data-ttu-id="78a52-111">1. példa: Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="78a52-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="78a52-112">Megkapja a Network Watchert az Egyesült Államok nyugati részén, ezért az előfizetésért, majd a VM-et és a hozzá tartozó hálózati felületekhez tartozót.</span><span class="sxs-lookup"><span data-stu-id="78a52-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="78a52-113">Ezután az első Hálózati felület esetén Test-AzNetworkWatcherIPFlow az első hálózati felületről származó IP-címet használva kimenő kapcsolatot létesít egy IP-hálózathoz az interneten.</span><span class="sxs-lookup"><span data-stu-id="78a52-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="78a52-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78a52-114">PARAMETERS</span></span>

### <span data-ttu-id="78a52-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78a52-115">-AsJob</span></span>
<span data-ttu-id="78a52-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="78a52-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78a52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a52-117">-DefaultProfile</span></span>
<span data-ttu-id="78a52-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78a52-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78a52-119">-Irány</span><span class="sxs-lookup"><span data-stu-id="78a52-119">-Direction</span></span>
<span data-ttu-id="78a52-120">Irány.</span><span class="sxs-lookup"><span data-stu-id="78a52-120">Direction.</span></span>

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

### <span data-ttu-id="78a52-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="78a52-121">-LocalIPAddress</span></span>
<span data-ttu-id="78a52-122">Helyi IP-cím.</span><span class="sxs-lookup"><span data-stu-id="78a52-122">Local IP Address.</span></span>

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

### <span data-ttu-id="78a52-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="78a52-123">-LocalPort</span></span>
<span data-ttu-id="78a52-124">Helyi port.</span><span class="sxs-lookup"><span data-stu-id="78a52-124">Local Port.</span></span>

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

### <span data-ttu-id="78a52-125">-Location</span><span class="sxs-lookup"><span data-stu-id="78a52-125">-Location</span></span>
<span data-ttu-id="78a52-126">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="78a52-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="78a52-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78a52-127">-NetworkWatcher</span></span>
<span data-ttu-id="78a52-128">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="78a52-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="78a52-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="78a52-129">-NetworkWatcherName</span></span>
<span data-ttu-id="78a52-130">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="78a52-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="78a52-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="78a52-131">-Protocol</span></span>
<span data-ttu-id="78a52-132">Protokoll.</span><span class="sxs-lookup"><span data-stu-id="78a52-132">Protocol.</span></span>

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

### <span data-ttu-id="78a52-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="78a52-133">-RemoteIPAddress</span></span>
<span data-ttu-id="78a52-134">Távoli IP-cím.</span><span class="sxs-lookup"><span data-stu-id="78a52-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="78a52-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="78a52-135">-RemotePort</span></span>
<span data-ttu-id="78a52-136">Távoli port.</span><span class="sxs-lookup"><span data-stu-id="78a52-136">Remote port.</span></span>

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

### <span data-ttu-id="78a52-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a52-137">-ResourceGroupName</span></span>
<span data-ttu-id="78a52-138">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="78a52-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="78a52-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="78a52-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="78a52-140">Célhálózati felület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="78a52-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="78a52-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="78a52-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="78a52-142">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="78a52-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="78a52-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a52-143">CommonParameters</span></span>
<span data-ttu-id="78a52-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a52-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a52-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a52-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a52-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78a52-146">INPUTS</span></span>

### <span data-ttu-id="78a52-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78a52-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="78a52-148">System.String</span><span class="sxs-lookup"><span data-stu-id="78a52-148">System.String</span></span>

## <span data-ttu-id="78a52-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78a52-149">OUTPUTS</span></span>

### <span data-ttu-id="78a52-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="78a52-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="78a52-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="78a52-151">NOTES</span></span>
<span data-ttu-id="78a52-152">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, folyamat, ip</span><span class="sxs-lookup"><span data-stu-id="78a52-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="78a52-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78a52-153">RELATED LINKS</span></span>

[<span data-ttu-id="78a52-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78a52-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="78a52-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78a52-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="78a52-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78a52-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="78a52-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="78a52-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="78a52-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="78a52-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="78a52-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="78a52-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="78a52-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="78a52-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="78a52-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78a52-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78a52-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="78a52-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="78a52-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78a52-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78a52-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78a52-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78a52-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78a52-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78a52-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="78a52-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="78a52-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="78a52-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="78a52-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="78a52-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="78a52-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78a52-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78a52-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78a52-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78a52-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78a52-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78a52-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="78a52-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="78a52-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78a52-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78a52-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78a52-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78a52-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="78a52-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="78a52-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="78a52-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="78a52-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="78a52-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="78a52-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="78a52-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="78a52-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="78a52-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="78a52-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78a52-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
