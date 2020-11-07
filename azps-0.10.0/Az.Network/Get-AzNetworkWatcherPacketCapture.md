---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 8e2e7a25b2c6e2c9eaa5e53234d7c1c9c3d0fa9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841562"
---
# <span data-ttu-id="878ef-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="878ef-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="878ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="878ef-102">SYNOPSIS</span></span>
<span data-ttu-id="878ef-103">Beolvassa a csomagkapcsolt erőforrás adatait és tulajdonságait és állapotát.</span><span class="sxs-lookup"><span data-stu-id="878ef-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="878ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="878ef-104">SYNTAX</span></span>

### <span data-ttu-id="878ef-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="878ef-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="878ef-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="878ef-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="878ef-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="878ef-107">DESCRIPTION</span></span>
<span data-ttu-id="878ef-108">A Get-AzNetworkWatcherPacketCapture a csomag-rögzítő erőforrás tulajdonságait és állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="878ef-108">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="878ef-109">Példák</span><span class="sxs-lookup"><span data-stu-id="878ef-109">EXAMPLES</span></span>

### <span data-ttu-id="878ef-110">---Példa 1: több szűrővel rendelkező csomag létrehozása és állapotának beolvasása---</span><span class="sxs-lookup"><span data-stu-id="878ef-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="878ef-111">Ebben a példában a "PacketCaptureTest" nevű csomagot hozzuk létre több szűrővel és időkorlátozással.</span><span class="sxs-lookup"><span data-stu-id="878ef-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="878ef-112">A munkamenet befejezésekor a program a megadott tárterület-fiókba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="878ef-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="878ef-113">Ezután hívja fel Get-AzNetworkWatcherPacketCapture a rögzítési munkamenet állapotának visszakereséséhez.</span><span class="sxs-lookup"><span data-stu-id="878ef-113">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="878ef-114">Megjegyzés: az Azure Network Watcher bővítménynek telepítve kell lennie a cél virtuális gépen a csomag rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="878ef-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="878ef-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="878ef-115">PARAMETERS</span></span>

### <span data-ttu-id="878ef-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="878ef-116">-AsJob</span></span>
<span data-ttu-id="878ef-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="878ef-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="878ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="878ef-118">-DefaultProfile</span></span>
<span data-ttu-id="878ef-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="878ef-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="878ef-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="878ef-120">-NetworkWatcher</span></span>
<span data-ttu-id="878ef-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="878ef-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="878ef-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="878ef-122">-NetworkWatcherName</span></span>
<span data-ttu-id="878ef-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="878ef-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="878ef-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="878ef-124">-PacketCaptureName</span></span>
<span data-ttu-id="878ef-125">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="878ef-125">The packet capture name.</span></span>

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

### <span data-ttu-id="878ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="878ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="878ef-127">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="878ef-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="878ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="878ef-128">CommonParameters</span></span>
<span data-ttu-id="878ef-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="878ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="878ef-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="878ef-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="878ef-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="878ef-131">INPUTS</span></span>

### <span data-ttu-id="878ef-132">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="878ef-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="878ef-133">System. String</span><span class="sxs-lookup"><span data-stu-id="878ef-133">System.String</span></span>

## <span data-ttu-id="878ef-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="878ef-134">OUTPUTS</span></span>

### <span data-ttu-id="878ef-135">Microsoft. Azure. commands. Network. models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="878ef-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="878ef-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="878ef-136">NOTES</span></span>
<span data-ttu-id="878ef-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="878ef-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="878ef-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="878ef-138">RELATED LINKS</span></span>

[<span data-ttu-id="878ef-139">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="878ef-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="878ef-140">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="878ef-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="878ef-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="878ef-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="878ef-142">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="878ef-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="878ef-143">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="878ef-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="878ef-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="878ef-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="878ef-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="878ef-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="878ef-146">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="878ef-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="878ef-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="878ef-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="878ef-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="878ef-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="878ef-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="878ef-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="878ef-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="878ef-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

