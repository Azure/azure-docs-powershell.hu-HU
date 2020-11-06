---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 641678db33e8e7436bda103f95863aefbf31eb96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493109"
---
# <span data-ttu-id="e46b3-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e46b3-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="e46b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e46b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e46b3-103">A következő ugrást kapja egy VM-ből.</span><span class="sxs-lookup"><span data-stu-id="e46b3-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e46b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e46b3-104">SYNTAX</span></span>

### <span data-ttu-id="e46b3-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e46b3-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e46b3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e46b3-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e46b3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e46b3-107">DESCRIPTION</span></span>
<span data-ttu-id="e46b3-108">A Get-AzureRmNetworkWatcherNextHop parancsmag a VM következő ugrását kapja.</span><span class="sxs-lookup"><span data-stu-id="e46b3-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="e46b3-109">A következő ugrással megtekintheti, hogy milyen típusú Azure-erőforrás, az erőforráshoz társított IP-cím, valamint az útvonalért felelős útválasztási táblázat szabálya.</span><span class="sxs-lookup"><span data-stu-id="e46b3-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="e46b3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e46b3-110">EXAMPLES</span></span>

### <span data-ttu-id="e46b3-111">--– Példa 1: a következő ugrás beszerzése internetes IP-vel való kommunikáció során –</span><span class="sxs-lookup"><span data-stu-id="e46b3-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="e46b3-112">A következő ugrás a kimenő kommunikációhoz az elsődleges hálózati csatolóról a megadott virtuális Vachine a 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="e46b3-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="e46b3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e46b3-113">PARAMETERS</span></span>

### <span data-ttu-id="e46b3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e46b3-114">-AsJob</span></span>
<span data-ttu-id="e46b3-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e46b3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e46b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46b3-116">-DefaultProfile</span></span>
<span data-ttu-id="e46b3-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e46b3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e46b3-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="e46b3-118">-DestinationIPAddress</span></span>
<span data-ttu-id="e46b3-119">Cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="e46b3-119">Destination IP address.</span></span>

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

### <span data-ttu-id="e46b3-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e46b3-120">-NetworkWatcher</span></span>
<span data-ttu-id="e46b3-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="e46b3-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="e46b3-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e46b3-122">-NetworkWatcherName</span></span>
<span data-ttu-id="e46b3-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="e46b3-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="e46b3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e46b3-124">-ResourceGroupName</span></span>
<span data-ttu-id="e46b3-125">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e46b3-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e46b3-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="e46b3-126">-SourceIPAddress</span></span>
<span data-ttu-id="e46b3-127">Forrás IP-címe.</span><span class="sxs-lookup"><span data-stu-id="e46b3-127">Source IP address.</span></span>

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

### <span data-ttu-id="e46b3-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="e46b3-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="e46b3-129">A célként megadott hálózati csatoló azonosítója</span><span class="sxs-lookup"><span data-stu-id="e46b3-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="e46b3-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e46b3-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="e46b3-131">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e46b3-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="e46b3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46b3-132">CommonParameters</span></span>
<span data-ttu-id="e46b3-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e46b3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46b3-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e46b3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46b3-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e46b3-135">INPUTS</span></span>

### <span data-ttu-id="e46b3-136">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e46b3-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e46b3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e46b3-137">System.String</span></span>

## <span data-ttu-id="e46b3-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e46b3-138">OUTPUTS</span></span>

### <span data-ttu-id="e46b3-139">Microsoft. Azure. commands. Network. models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="e46b3-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="e46b3-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e46b3-140">NOTES</span></span>
<span data-ttu-id="e46b3-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, következő, ugrás</span><span class="sxs-lookup"><span data-stu-id="e46b3-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="e46b3-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e46b3-142">RELATED LINKS</span></span>

[<span data-ttu-id="e46b3-143">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e46b3-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e46b3-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e46b3-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e46b3-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e46b3-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e46b3-146">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e46b3-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="e46b3-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e46b3-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e46b3-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e46b3-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="e46b3-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e46b3-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e46b3-150">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e46b3-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e46b3-151">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e46b3-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="e46b3-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e46b3-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e46b3-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e46b3-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e46b3-154">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e46b3-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

