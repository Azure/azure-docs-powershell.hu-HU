---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 307bb2c954526b744f31763f0d3a09d0163c8057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843509"
---
# <span data-ttu-id="901a8-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="901a8-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="901a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="901a8-102">SYNOPSIS</span></span>
<span data-ttu-id="901a8-103">Azt számítja ki, hogy a csomag engedélyezett vagy megtagadva van-e egy adott célhelyen.</span><span class="sxs-lookup"><span data-stu-id="901a8-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="901a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="901a8-104">SYNTAX</span></span>

### <span data-ttu-id="901a8-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="901a8-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="901a8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="901a8-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="901a8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="901a8-107">DESCRIPTION</span></span>
<span data-ttu-id="901a8-108">A Test-AzNetworkWatcherIPFlow parancsmag egy megadott VM-erőforráshoz és egy megadott irányú csomaghoz helyi és távoli, IP-címek és portok használatával, azt adja eredményül, hogy engedélyezett vagy megtagadta-e a csomagot.</span><span class="sxs-lookup"><span data-stu-id="901a8-108">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="901a8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="901a8-109">EXAMPLES</span></span>

### <span data-ttu-id="901a8-110">---Példa 1: fuss Test-AzNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="901a8-110">--- Example 1: Run Test-AzNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="901a8-111">Az előfizetéshez tartozó Közép-amerikai hálózati figyelő beszerzése, majd a VM és a hozzá tartozó hálózati illesztők beszerzése.</span><span class="sxs-lookup"><span data-stu-id="901a8-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="901a8-112">Ezután az első hálózati felületen az első IP-kapcsolaton futó IP-kapcsolaton keresztül futtatja a Test-AzNetworkWatcherIPFlowt egy internetes IP-kapcsolaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="901a8-112">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="901a8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="901a8-113">PARAMETERS</span></span>

### <span data-ttu-id="901a8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="901a8-114">-AsJob</span></span>
<span data-ttu-id="901a8-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="901a8-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901a8-116">-DefaultProfile</span></span>
<span data-ttu-id="901a8-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="901a8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-118">-Irány</span><span class="sxs-lookup"><span data-stu-id="901a8-118">-Direction</span></span>
<span data-ttu-id="901a8-119">Irányba.</span><span class="sxs-lookup"><span data-stu-id="901a8-119">Direction.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="901a8-120">-LocalIPAddress</span></span>
<span data-ttu-id="901a8-121">Helyi IP-cím.</span><span class="sxs-lookup"><span data-stu-id="901a8-121">Local IP Address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="901a8-122">-LocalPort</span></span>
<span data-ttu-id="901a8-123">Helyi port.</span><span class="sxs-lookup"><span data-stu-id="901a8-123">Local Port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="901a8-124">-NetworkWatcher</span></span>
<span data-ttu-id="901a8-125">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="901a8-125">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="901a8-126">-NetworkWatcherName</span></span>
<span data-ttu-id="901a8-127">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="901a8-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-128">-Protocol</span><span class="sxs-lookup"><span data-stu-id="901a8-128">-Protocol</span></span>
<span data-ttu-id="901a8-129">Protokoll.</span><span class="sxs-lookup"><span data-stu-id="901a8-129">Protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="901a8-130">-RemoteIPAddress</span></span>
<span data-ttu-id="901a8-131">Távoli IP-cím.</span><span class="sxs-lookup"><span data-stu-id="901a8-131">Remote IP Address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-132">-TávoliPORT</span><span class="sxs-lookup"><span data-stu-id="901a8-132">-RemotePort</span></span>
<span data-ttu-id="901a8-133">Távoli port.</span><span class="sxs-lookup"><span data-stu-id="901a8-133">Remote port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="901a8-134">-ResourceGroupName</span></span>
<span data-ttu-id="901a8-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="901a8-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="901a8-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="901a8-137">A célként megadott hálózati csatoló azonosítója</span><span class="sxs-lookup"><span data-stu-id="901a8-137">Target network interface Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="901a8-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="901a8-139">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="901a8-139">The target virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="901a8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901a8-140">CommonParameters</span></span>
<span data-ttu-id="901a8-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="901a8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901a8-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="901a8-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901a8-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="901a8-143">INPUTS</span></span>

### <span data-ttu-id="901a8-144">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="901a8-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="901a8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="901a8-145">System.String</span></span>

## <span data-ttu-id="901a8-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="901a8-146">OUTPUTS</span></span>

### <span data-ttu-id="901a8-147">Microsoft. Azure. commands. Network. models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="901a8-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="901a8-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="901a8-148">NOTES</span></span>
<span data-ttu-id="901a8-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, adatfolyam, IP</span><span class="sxs-lookup"><span data-stu-id="901a8-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="901a8-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="901a8-150">RELATED LINKS</span></span>

[<span data-ttu-id="901a8-151">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="901a8-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="901a8-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="901a8-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="901a8-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="901a8-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="901a8-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="901a8-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="901a8-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="901a8-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="901a8-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="901a8-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="901a8-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="901a8-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="901a8-158">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="901a8-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="901a8-159">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="901a8-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="901a8-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="901a8-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="901a8-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="901a8-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="901a8-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="901a8-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
