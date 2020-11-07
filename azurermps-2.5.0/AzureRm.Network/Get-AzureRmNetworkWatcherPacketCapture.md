---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: aeadada7c6e2e2d7cb94a484e7ca3223e03b4426
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848458"
---
# <span data-ttu-id="66076-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="66076-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="66076-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66076-102">SYNOPSIS</span></span>
<span data-ttu-id="66076-103">Beolvassa a csomagkapcsolt erőforrás adatait és tulajdonságait és állapotát.</span><span class="sxs-lookup"><span data-stu-id="66076-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66076-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66076-104">SYNTAX</span></span>

### <span data-ttu-id="66076-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66076-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66076-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="66076-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66076-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="66076-107">DESCRIPTION</span></span>
<span data-ttu-id="66076-108">A Get-AzureRmNetworkWatcherPacketCapture a csomag-rögzítő erőforrás tulajdonságait és állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="66076-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="66076-109">Példák</span><span class="sxs-lookup"><span data-stu-id="66076-109">EXAMPLES</span></span>

### <span data-ttu-id="66076-110">---Példa 1: több szűrővel rendelkező csomag létrehozása és állapotának beolvasása---</span><span class="sxs-lookup"><span data-stu-id="66076-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="66076-111">Ebben a példában a "PacketCaptureTest" nevű csomagot hozzuk létre több szűrővel és időkorlátozással.</span><span class="sxs-lookup"><span data-stu-id="66076-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="66076-112">A munkamenet befejezésekor a program a megadott tárterület-fiókba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="66076-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="66076-113">Ezután hívja fel Get-AzureRmNetworkWatcherPacketCapture a rögzítési munkamenet állapotának visszakereséséhez.</span><span class="sxs-lookup"><span data-stu-id="66076-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="66076-114">Megjegyzés: az Azure Network Watcher bővítménynek telepítve kell lennie a cél virtuális gépen a csomag rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="66076-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="66076-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66076-115">PARAMETERS</span></span>

### <span data-ttu-id="66076-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66076-116">-AsJob</span></span>
<span data-ttu-id="66076-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="66076-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66076-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66076-118">-DefaultProfile</span></span>
<span data-ttu-id="66076-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66076-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66076-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66076-120">-NetworkWatcher</span></span>
<span data-ttu-id="66076-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="66076-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="66076-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="66076-122">-NetworkWatcherName</span></span>
<span data-ttu-id="66076-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="66076-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="66076-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="66076-124">-PacketCaptureName</span></span>
<span data-ttu-id="66076-125">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="66076-125">The packet capture name.</span></span>

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

### <span data-ttu-id="66076-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66076-126">-ResourceGroupName</span></span>
<span data-ttu-id="66076-127">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="66076-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="66076-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66076-128">CommonParameters</span></span>
<span data-ttu-id="66076-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66076-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66076-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66076-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66076-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66076-131">INPUTS</span></span>

### <span data-ttu-id="66076-132">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66076-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="66076-133">System. String</span><span class="sxs-lookup"><span data-stu-id="66076-133">System.String</span></span>

## <span data-ttu-id="66076-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66076-134">OUTPUTS</span></span>

### <span data-ttu-id="66076-135">Microsoft. Azure. commands. Network. models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="66076-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="66076-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66076-136">NOTES</span></span>
<span data-ttu-id="66076-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="66076-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="66076-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66076-138">RELATED LINKS</span></span>

[<span data-ttu-id="66076-139">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="66076-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="66076-140">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="66076-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="66076-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="66076-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="66076-142">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="66076-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="66076-143">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66076-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="66076-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66076-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="66076-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="66076-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="66076-146">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="66076-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="66076-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="66076-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="66076-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="66076-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="66076-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="66076-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="66076-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="66076-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

