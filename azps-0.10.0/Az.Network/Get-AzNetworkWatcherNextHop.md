---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 02e24fd35fbe2e5aec5fc8b6ed73d3608d07c5b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841566"
---
# <span data-ttu-id="468a2-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="468a2-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="468a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="468a2-102">SYNOPSIS</span></span>
<span data-ttu-id="468a2-103">A következő ugrást kapja egy VM-ből.</span><span class="sxs-lookup"><span data-stu-id="468a2-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="468a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="468a2-104">SYNTAX</span></span>

### <span data-ttu-id="468a2-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="468a2-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="468a2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="468a2-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="468a2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="468a2-107">DESCRIPTION</span></span>
<span data-ttu-id="468a2-108">A Get-AzNetworkWatcherNextHop parancsmag a VM következő ugrását kapja.</span><span class="sxs-lookup"><span data-stu-id="468a2-108">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="468a2-109">A következő ugrással megtekintheti, hogy milyen típusú Azure-erőforrás, az erőforráshoz társított IP-cím, valamint az útvonalért felelős útválasztási táblázat szabálya.</span><span class="sxs-lookup"><span data-stu-id="468a2-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="468a2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="468a2-110">EXAMPLES</span></span>

### <span data-ttu-id="468a2-111">--– Példa 1: a következő ugrás beszerzése internetes IP-vel való kommunikáció során –</span><span class="sxs-lookup"><span data-stu-id="468a2-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="468a2-112">A következő ugrás a kimenő kommunikációhoz az elsődleges hálózati csatolóról a megadott virtuális Vachine a 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="468a2-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="468a2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="468a2-113">PARAMETERS</span></span>

### <span data-ttu-id="468a2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="468a2-114">-AsJob</span></span>
<span data-ttu-id="468a2-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="468a2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="468a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468a2-116">-DefaultProfile</span></span>
<span data-ttu-id="468a2-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="468a2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="468a2-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="468a2-118">-DestinationIPAddress</span></span>
<span data-ttu-id="468a2-119">Cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="468a2-119">Destination IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="468a2-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="468a2-120">-NetworkWatcher</span></span>
<span data-ttu-id="468a2-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="468a2-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="468a2-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="468a2-122">-NetworkWatcherName</span></span>
<span data-ttu-id="468a2-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="468a2-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="468a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="468a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="468a2-125">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="468a2-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="468a2-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="468a2-126">-SourceIPAddress</span></span>
<span data-ttu-id="468a2-127">Forrás IP-címe.</span><span class="sxs-lookup"><span data-stu-id="468a2-127">Source IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="468a2-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="468a2-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="468a2-129">A célként megadott hálózati csatoló azonosítója</span><span class="sxs-lookup"><span data-stu-id="468a2-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="468a2-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="468a2-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="468a2-131">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="468a2-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="468a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468a2-132">CommonParameters</span></span>
<span data-ttu-id="468a2-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="468a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468a2-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="468a2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468a2-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="468a2-135">INPUTS</span></span>

### <span data-ttu-id="468a2-136">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="468a2-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="468a2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="468a2-137">System.String</span></span>

## <span data-ttu-id="468a2-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="468a2-138">OUTPUTS</span></span>

### <span data-ttu-id="468a2-139">Microsoft. Azure. commands. Network. models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="468a2-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="468a2-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="468a2-140">NOTES</span></span>
<span data-ttu-id="468a2-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, következő, ugrás</span><span class="sxs-lookup"><span data-stu-id="468a2-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="468a2-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="468a2-142">RELATED LINKS</span></span>

[<span data-ttu-id="468a2-143">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="468a2-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="468a2-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="468a2-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="468a2-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="468a2-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="468a2-146">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="468a2-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="468a2-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="468a2-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="468a2-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="468a2-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="468a2-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="468a2-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="468a2-150">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="468a2-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="468a2-151">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="468a2-151">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="468a2-152">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="468a2-152">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="468a2-153">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="468a2-153">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="468a2-154">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="468a2-154">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

