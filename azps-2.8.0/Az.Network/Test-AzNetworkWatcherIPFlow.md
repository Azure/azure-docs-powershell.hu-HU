---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 1d4bcd95ba526b8fc2d9c9bdc94e5fed3c042940
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408338"
---
# <span data-ttu-id="1d197-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1d197-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="1d197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d197-102">SYNOPSIS</span></span>
<span data-ttu-id="1d197-103">Visszaadja, hogy a csomag engedélyezett-e vagy megtagadható-e egy adott célhelyhez vagy egy adott célhelytől.</span><span class="sxs-lookup"><span data-stu-id="1d197-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="1d197-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d197-104">SYNTAX</span></span>

### <span data-ttu-id="1d197-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d197-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d197-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1d197-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d197-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1d197-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d197-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d197-108">DESCRIPTION</span></span>
<span data-ttu-id="1d197-109">A Test-AzNetworkWatcherIPFlow egy adott VM-erőforráshoz és egy helyi és távoli IP-címeket és portokat használó meghatározott irányú csomaghoz megadott parancsmag visszaadja, hogy a csomag engedélyezett vagy megtagadható-e.</span><span class="sxs-lookup"><span data-stu-id="1d197-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="1d197-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d197-110">EXAMPLES</span></span>

### <span data-ttu-id="1d197-111">1. példa: Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1d197-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="1d197-112">Megkapja a Network Watchert az Amerikai Egyesült Államok nyugati részén, ezt az előfizetést, majd a VM-et és a hozzá tartozó hálózati felületekhez tartozót.</span><span class="sxs-lookup"><span data-stu-id="1d197-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="1d197-113">Ezután az első Hálózati felület esetén Test-AzNetworkWatcherIPFlow az első hálózati felületről származó IP-címet használva kimenő kapcsolatot létesít egy IP-hálózathoz az interneten.</span><span class="sxs-lookup"><span data-stu-id="1d197-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="1d197-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d197-114">PARAMETERS</span></span>

### <span data-ttu-id="1d197-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d197-115">-AsJob</span></span>
<span data-ttu-id="1d197-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1d197-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d197-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d197-117">-DefaultProfile</span></span>
<span data-ttu-id="1d197-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d197-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d197-119">-Irány</span><span class="sxs-lookup"><span data-stu-id="1d197-119">-Direction</span></span>
<span data-ttu-id="1d197-120">Irány.</span><span class="sxs-lookup"><span data-stu-id="1d197-120">Direction.</span></span>

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

### <span data-ttu-id="1d197-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="1d197-121">-LocalIPAddress</span></span>
<span data-ttu-id="1d197-122">Helyi IP-cím.</span><span class="sxs-lookup"><span data-stu-id="1d197-122">Local IP Address.</span></span>

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

### <span data-ttu-id="1d197-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="1d197-123">-LocalPort</span></span>
<span data-ttu-id="1d197-124">Helyi port.</span><span class="sxs-lookup"><span data-stu-id="1d197-124">Local Port.</span></span>

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

### <span data-ttu-id="1d197-125">-Location</span><span class="sxs-lookup"><span data-stu-id="1d197-125">-Location</span></span>
<span data-ttu-id="1d197-126">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="1d197-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1d197-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d197-127">-NetworkWatcher</span></span>
<span data-ttu-id="1d197-128">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="1d197-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="1d197-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1d197-129">-NetworkWatcherName</span></span>
<span data-ttu-id="1d197-130">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="1d197-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="1d197-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1d197-131">-Protocol</span></span>
<span data-ttu-id="1d197-132">Protokoll.</span><span class="sxs-lookup"><span data-stu-id="1d197-132">Protocol.</span></span>

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

### <span data-ttu-id="1d197-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="1d197-133">-RemoteIPAddress</span></span>
<span data-ttu-id="1d197-134">Távoli IP-cím.</span><span class="sxs-lookup"><span data-stu-id="1d197-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="1d197-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="1d197-135">-RemotePort</span></span>
<span data-ttu-id="1d197-136">Távoli port.</span><span class="sxs-lookup"><span data-stu-id="1d197-136">Remote port.</span></span>

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

### <span data-ttu-id="1d197-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d197-137">-ResourceGroupName</span></span>
<span data-ttu-id="1d197-138">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1d197-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1d197-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="1d197-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="1d197-140">Célhálózati felület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1d197-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="1d197-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="1d197-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="1d197-142">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1d197-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="1d197-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d197-143">CommonParameters</span></span>
<span data-ttu-id="1d197-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d197-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d197-145">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d197-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d197-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d197-146">INPUTS</span></span>

### <span data-ttu-id="1d197-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d197-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1d197-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1d197-148">System.String</span></span>

## <span data-ttu-id="1d197-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d197-149">OUTPUTS</span></span>

### <span data-ttu-id="1d197-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="1d197-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="1d197-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d197-151">NOTES</span></span>
<span data-ttu-id="1d197-152">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, folyamat, ip</span><span class="sxs-lookup"><span data-stu-id="1d197-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="1d197-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d197-153">RELATED LINKS</span></span>

[<span data-ttu-id="1d197-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d197-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1d197-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d197-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1d197-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1d197-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1d197-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1d197-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1d197-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1d197-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1d197-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1d197-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1d197-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1d197-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1d197-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d197-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1d197-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1d197-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1d197-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d197-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1d197-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d197-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1d197-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1d197-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1d197-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d197-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1d197-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1d197-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1d197-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1d197-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1d197-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1d197-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1d197-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1d197-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1d197-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1d197-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1d197-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1d197-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1d197-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1d197-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1d197-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1d197-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1d197-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1d197-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1d197-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1d197-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1d197-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1d197-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1d197-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1d197-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1d197-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1d197-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1d197-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1d197-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
