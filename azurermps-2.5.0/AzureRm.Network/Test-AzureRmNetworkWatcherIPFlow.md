---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
ms.openlocfilehash: 6147697826dbc475c5871acab1f037af21c2b84d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848661"
---
# <span data-ttu-id="ec34e-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ec34e-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="ec34e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec34e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec34e-103">Azt számítja ki, hogy a csomag engedélyezett vagy megtagadva van-e egy adott célhelyen.</span><span class="sxs-lookup"><span data-stu-id="ec34e-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec34e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec34e-104">SYNTAX</span></span>

### <span data-ttu-id="ec34e-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec34e-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec34e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ec34e-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec34e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec34e-107">DESCRIPTION</span></span>
<span data-ttu-id="ec34e-108">A Test-AzureRmNetworkWatcherIPFlow parancsmag egy megadott VM-erőforráshoz és egy megadott irányú csomaghoz helyi és távoli, IP-címek és portok használatával, azt adja eredményül, hogy engedélyezett vagy megtagadta-e a csomagot.</span><span class="sxs-lookup"><span data-stu-id="ec34e-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="ec34e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ec34e-109">EXAMPLES</span></span>

### <span data-ttu-id="ec34e-110">---Példa 1: fuss Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="ec34e-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="ec34e-111">Az előfizetéshez tartozó Közép-amerikai hálózati figyelő beszerzése, majd a VM és a hozzá tartozó hálózati illesztők beszerzése.</span><span class="sxs-lookup"><span data-stu-id="ec34e-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="ec34e-112">Ezután az első hálózati felületen az első IP-kapcsolaton futó IP-kapcsolaton keresztül futtatja a Test-AzureRmNetworkWatcherIPFlowt egy internetes IP-kapcsolaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="ec34e-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="ec34e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec34e-113">PARAMETERS</span></span>

### <span data-ttu-id="ec34e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec34e-114">-AsJob</span></span>
<span data-ttu-id="ec34e-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ec34e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec34e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec34e-116">-DefaultProfile</span></span>
<span data-ttu-id="ec34e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec34e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec34e-118">-Irány</span><span class="sxs-lookup"><span data-stu-id="ec34e-118">-Direction</span></span>
<span data-ttu-id="ec34e-119">Irányba.</span><span class="sxs-lookup"><span data-stu-id="ec34e-119">Direction.</span></span>

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

### <span data-ttu-id="ec34e-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="ec34e-120">-LocalIPAddress</span></span>
<span data-ttu-id="ec34e-121">Helyi IP-cím.</span><span class="sxs-lookup"><span data-stu-id="ec34e-121">Local IP Address.</span></span>

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

### <span data-ttu-id="ec34e-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="ec34e-122">-LocalPort</span></span>
<span data-ttu-id="ec34e-123">Helyi port.</span><span class="sxs-lookup"><span data-stu-id="ec34e-123">Local Port.</span></span>

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

### <span data-ttu-id="ec34e-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec34e-124">-NetworkWatcher</span></span>
<span data-ttu-id="ec34e-125">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ec34e-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="ec34e-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ec34e-126">-NetworkWatcherName</span></span>
<span data-ttu-id="ec34e-127">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="ec34e-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="ec34e-128">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ec34e-128">-Protocol</span></span>
<span data-ttu-id="ec34e-129">Protokoll.</span><span class="sxs-lookup"><span data-stu-id="ec34e-129">Protocol.</span></span>

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

### <span data-ttu-id="ec34e-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="ec34e-130">-RemoteIPAddress</span></span>
<span data-ttu-id="ec34e-131">Távoli IP-cím.</span><span class="sxs-lookup"><span data-stu-id="ec34e-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="ec34e-132">-TávoliPORT</span><span class="sxs-lookup"><span data-stu-id="ec34e-132">-RemotePort</span></span>
<span data-ttu-id="ec34e-133">Távoli port.</span><span class="sxs-lookup"><span data-stu-id="ec34e-133">Remote port.</span></span>

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

### <span data-ttu-id="ec34e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec34e-134">-ResourceGroupName</span></span>
<span data-ttu-id="ec34e-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ec34e-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ec34e-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="ec34e-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="ec34e-137">A célként megadott hálózati csatoló azonosítója</span><span class="sxs-lookup"><span data-stu-id="ec34e-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="ec34e-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ec34e-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="ec34e-139">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec34e-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="ec34e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec34e-140">CommonParameters</span></span>
<span data-ttu-id="ec34e-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec34e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec34e-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec34e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec34e-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec34e-143">INPUTS</span></span>

### <span data-ttu-id="ec34e-144">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec34e-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ec34e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ec34e-145">System.String</span></span>

## <span data-ttu-id="ec34e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec34e-146">OUTPUTS</span></span>

### <span data-ttu-id="ec34e-147">Microsoft. Azure. commands. Network. models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="ec34e-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="ec34e-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec34e-148">NOTES</span></span>
<span data-ttu-id="ec34e-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, adatfolyam, IP</span><span class="sxs-lookup"><span data-stu-id="ec34e-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="ec34e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec34e-150">RELATED LINKS</span></span>

[<span data-ttu-id="ec34e-151">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec34e-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ec34e-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec34e-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ec34e-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ec34e-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ec34e-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ec34e-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ec34e-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ec34e-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ec34e-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ec34e-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ec34e-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ec34e-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ec34e-158">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec34e-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec34e-159">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ec34e-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ec34e-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec34e-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec34e-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec34e-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ec34e-162">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ec34e-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
