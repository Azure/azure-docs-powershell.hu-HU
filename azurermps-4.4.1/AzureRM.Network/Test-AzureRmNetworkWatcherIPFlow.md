---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6e9700f91a9d6f8db5983604a0146f9d864dafd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504907"
---
# <span data-ttu-id="84b22-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="84b22-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="84b22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84b22-102">SYNOPSIS</span></span>
<span data-ttu-id="84b22-103">Azt számítja ki, hogy a csomag engedélyezett vagy megtagadva van-e egy adott célhelyen.</span><span class="sxs-lookup"><span data-stu-id="84b22-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84b22-104">SYNTAX</span></span>

### <span data-ttu-id="84b22-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84b22-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84b22-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="84b22-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84b22-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="84b22-107">DESCRIPTION</span></span>
<span data-ttu-id="84b22-108">A Test-AzureRmNetworkWatcherIPFlow parancsmag egy megadott VM-erőforráshoz és egy megadott irányú csomaghoz helyi és távoli, IP-címek és portok használatával, azt adja eredményül, hogy engedélyezett vagy megtagadta-e a csomagot.</span><span class="sxs-lookup"><span data-stu-id="84b22-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="84b22-109">Példák</span><span class="sxs-lookup"><span data-stu-id="84b22-109">EXAMPLES</span></span>

### <span data-ttu-id="84b22-110">---Példa 1: fuss Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="84b22-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="84b22-111">Az előfizetéshez tartozó Közép-amerikai hálózati figyelő beszerzése, majd a VM és a hozzá tartozó hálózati illesztők beszerzése.</span><span class="sxs-lookup"><span data-stu-id="84b22-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="84b22-112">Ezután az első hálózati felületen az első IP-kapcsolaton futó IP-kapcsolaton keresztül futtatja a Test-AzureRmNetworkWatcherIPFlowt egy internetes IP-kapcsolaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="84b22-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="84b22-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84b22-113">PARAMETERS</span></span>

### <span data-ttu-id="84b22-114">-Irány</span><span class="sxs-lookup"><span data-stu-id="84b22-114">-Direction</span></span>
<span data-ttu-id="84b22-115">Irányba.</span><span class="sxs-lookup"><span data-stu-id="84b22-115">Direction.</span></span>

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

### <span data-ttu-id="84b22-116">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="84b22-116">-LocalIPAddress</span></span>
<span data-ttu-id="84b22-117">Helyi IP-cím.</span><span class="sxs-lookup"><span data-stu-id="84b22-117">Local IP Address.</span></span>

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

### <span data-ttu-id="84b22-118">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="84b22-118">-LocalPort</span></span>
<span data-ttu-id="84b22-119">Helyi port.</span><span class="sxs-lookup"><span data-stu-id="84b22-119">Local Port.</span></span>

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

### <span data-ttu-id="84b22-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b22-120">-NetworkWatcher</span></span>
<span data-ttu-id="84b22-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="84b22-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="84b22-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="84b22-122">-NetworkWatcherName</span></span>
<span data-ttu-id="84b22-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="84b22-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="84b22-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="84b22-124">-Protocol</span></span>
<span data-ttu-id="84b22-125">Protokoll.</span><span class="sxs-lookup"><span data-stu-id="84b22-125">Protocol.</span></span>

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

### <span data-ttu-id="84b22-126">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="84b22-126">-RemoteIPAddress</span></span>
<span data-ttu-id="84b22-127">Távoli IP-cím.</span><span class="sxs-lookup"><span data-stu-id="84b22-127">Remote IP Address.</span></span>

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

### <span data-ttu-id="84b22-128">-TávoliPORT</span><span class="sxs-lookup"><span data-stu-id="84b22-128">-RemotePort</span></span>
<span data-ttu-id="84b22-129">Távoli port.</span><span class="sxs-lookup"><span data-stu-id="84b22-129">Remote port.</span></span>

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

### <span data-ttu-id="84b22-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b22-130">-ResourceGroupName</span></span>
<span data-ttu-id="84b22-131">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="84b22-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="84b22-132">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="84b22-132">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="84b22-133">A célként megadott hálózati csatoló azonosítója</span><span class="sxs-lookup"><span data-stu-id="84b22-133">Target network interface Id.</span></span>

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

### <span data-ttu-id="84b22-134">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="84b22-134">-TargetVirtualMachineId</span></span>
<span data-ttu-id="84b22-135">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="84b22-135">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="84b22-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b22-136">-DefaultProfile</span></span>
<span data-ttu-id="84b22-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84b22-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84b22-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b22-138">CommonParameters</span></span>
<span data-ttu-id="84b22-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84b22-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b22-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b22-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b22-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84b22-141">INPUTS</span></span>

### <span data-ttu-id="84b22-142">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b22-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="84b22-143">System. String</span><span class="sxs-lookup"><span data-stu-id="84b22-143">System.String</span></span>

## <span data-ttu-id="84b22-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84b22-144">OUTPUTS</span></span>

### <span data-ttu-id="84b22-145">Microsoft. Azure. commands. Network. models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="84b22-145">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="84b22-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84b22-146">NOTES</span></span>
<span data-ttu-id="84b22-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, adatfolyam, IP</span><span class="sxs-lookup"><span data-stu-id="84b22-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="84b22-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84b22-148">RELATED LINKS</span></span>

[<span data-ttu-id="84b22-149">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b22-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="84b22-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b22-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="84b22-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b22-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="84b22-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="84b22-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="84b22-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="84b22-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="84b22-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="84b22-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="84b22-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="84b22-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="84b22-156">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b22-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b22-157">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="84b22-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="84b22-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b22-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b22-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b22-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b22-160">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b22-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
