---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: d26f50768c561e05b4dc27ad829c063b73c5a336
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504843"
---
# <span data-ttu-id="3d5c1-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3d5c1-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="3d5c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5c1-103">A következő ugrást kapja egy VM-ből.</span><span class="sxs-lookup"><span data-stu-id="3d5c1-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d5c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d5c1-104">SYNTAX</span></span>

### <span data-ttu-id="3d5c1-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d5c1-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d5c1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3d5c1-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d5c1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d5c1-107">DESCRIPTION</span></span>
<span data-ttu-id="3d5c1-108">A Get-AzureRmNetworkWatcherNextHop parancsmag a VM következő ugrását kapja.</span><span class="sxs-lookup"><span data-stu-id="3d5c1-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="3d5c1-109">A következő ugrással megtekintheti, hogy milyen típusú Azure-erőforrás, az erőforráshoz társított IP-cím, valamint az útvonalért felelős útválasztási táblázat szabálya.</span><span class="sxs-lookup"><span data-stu-id="3d5c1-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="3d5c1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3d5c1-110">EXAMPLES</span></span>

### <span data-ttu-id="3d5c1-111">--– Példa 1: a következő ugrás beszerzése internetes IP-vel való kommunikáció során –</span><span class="sxs-lookup"><span data-stu-id="3d5c1-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="3d5c1-112">A következő ugrás a kimenő kommunikációhoz az elsődleges hálózati csatolóról a megadott virtuális Vachine a 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="3d5c1-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="3d5c1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d5c1-113">PARAMETERS</span></span>

### <span data-ttu-id="3d5c1-114">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="3d5c1-114">-DestinationIPAddress</span></span>
<span data-ttu-id="3d5c1-115">Cél IP-címe.</span><span class="sxs-lookup"><span data-stu-id="3d5c1-115">Destination IP address.</span></span>

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

### <span data-ttu-id="3d5c1-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d5c1-116">-NetworkWatcher</span></span>
<span data-ttu-id="3d5c1-117">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="3d5c1-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="3d5c1-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3d5c1-118">-NetworkWatcherName</span></span>
<span data-ttu-id="3d5c1-119">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="3d5c1-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="3d5c1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d5c1-120">-ResourceGroupName</span></span>
<span data-ttu-id="3d5c1-121">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3d5c1-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3d5c1-122">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="3d5c1-122">-SourceIPAddress</span></span>
<span data-ttu-id="3d5c1-123">Forrás IP-címe.</span><span class="sxs-lookup"><span data-stu-id="3d5c1-123">Source IP address.</span></span>

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

### <span data-ttu-id="3d5c1-124">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="3d5c1-124">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="3d5c1-125">A célként megadott hálózati csatoló azonosítója</span><span class="sxs-lookup"><span data-stu-id="3d5c1-125">Target network interface Id.</span></span>

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

### <span data-ttu-id="3d5c1-126">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="3d5c1-126">-TargetVirtualMachineId</span></span>
<span data-ttu-id="3d5c1-127">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3d5c1-127">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="3d5c1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d5c1-128">-DefaultProfile</span></span>
<span data-ttu-id="3d5c1-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d5c1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d5c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5c1-130">CommonParameters</span></span>
<span data-ttu-id="3d5c1-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d5c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5c1-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d5c1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5c1-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d5c1-133">INPUTS</span></span>

### <span data-ttu-id="3d5c1-134">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d5c1-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3d5c1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3d5c1-135">System.String</span></span>

## <span data-ttu-id="3d5c1-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d5c1-136">OUTPUTS</span></span>

### <span data-ttu-id="3d5c1-137">Microsoft. Azure. commands. Network. models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="3d5c1-137">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="3d5c1-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d5c1-138">NOTES</span></span>
<span data-ttu-id="3d5c1-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, következő, ugrás</span><span class="sxs-lookup"><span data-stu-id="3d5c1-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="3d5c1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d5c1-140">RELATED LINKS</span></span>

[<span data-ttu-id="3d5c1-141">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d5c1-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3d5c1-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d5c1-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3d5c1-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d5c1-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3d5c1-144">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3d5c1-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="3d5c1-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3d5c1-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3d5c1-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3d5c1-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="3d5c1-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3d5c1-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3d5c1-148">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d5c1-148">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d5c1-149">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3d5c1-149">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="3d5c1-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d5c1-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d5c1-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d5c1-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d5c1-152">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d5c1-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

