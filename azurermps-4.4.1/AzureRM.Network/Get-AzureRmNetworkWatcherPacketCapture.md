---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 4cf1cb9149c0f821ad0e6164cd7c817b12ccc147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494832"
---
# <span data-ttu-id="759a2-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="759a2-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="759a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="759a2-102">SYNOPSIS</span></span>
<span data-ttu-id="759a2-103">Beolvassa a csomagkapcsolt erőforrás adatait és tulajdonságait és állapotát.</span><span class="sxs-lookup"><span data-stu-id="759a2-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="759a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="759a2-104">SYNTAX</span></span>

### <span data-ttu-id="759a2-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="759a2-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="759a2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="759a2-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="759a2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="759a2-107">DESCRIPTION</span></span>
<span data-ttu-id="759a2-108">A Get-AzureRmNetworkWatcherPacketCapture a csomag-rögzítő erőforrás tulajdonságait és állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="759a2-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="759a2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="759a2-109">EXAMPLES</span></span>

### <span data-ttu-id="759a2-110">---Példa 1: több szűrővel rendelkező csomag létrehozása és állapotának beolvasása---</span><span class="sxs-lookup"><span data-stu-id="759a2-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="759a2-111">Ebben a példában a "PacketCaptureTest" nevű csomagot hozzuk létre több szűrővel és időkorlátozással.</span><span class="sxs-lookup"><span data-stu-id="759a2-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="759a2-112">A munkamenet befejezésekor a program a megadott tárterület-fiókba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="759a2-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="759a2-113">Ezután hívja fel Get-AzureRmNetworkWatcherPacketCapture a rögzítési munkamenet állapotának visszakereséséhez.</span><span class="sxs-lookup"><span data-stu-id="759a2-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="759a2-114">Megjegyzés: az Azure Network Watcher bővítménynek telepítve kell lennie a cél virtuális gépen a csomag rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="759a2-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="759a2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="759a2-115">PARAMETERS</span></span>

### <span data-ttu-id="759a2-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="759a2-116">-NetworkWatcher</span></span>
<span data-ttu-id="759a2-117">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="759a2-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="759a2-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="759a2-118">-NetworkWatcherName</span></span>
<span data-ttu-id="759a2-119">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="759a2-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="759a2-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="759a2-120">-PacketCaptureName</span></span>
<span data-ttu-id="759a2-121">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="759a2-121">The packet capture name.</span></span>

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

### <span data-ttu-id="759a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="759a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="759a2-123">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="759a2-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="759a2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="759a2-124">-DefaultProfile</span></span>
<span data-ttu-id="759a2-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="759a2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="759a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="759a2-126">CommonParameters</span></span>
<span data-ttu-id="759a2-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="759a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="759a2-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="759a2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="759a2-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="759a2-129">INPUTS</span></span>

### <span data-ttu-id="759a2-130">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="759a2-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="759a2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="759a2-131">System.String</span></span>

## <span data-ttu-id="759a2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="759a2-132">OUTPUTS</span></span>

### <span data-ttu-id="759a2-133">Microsoft. Azure. commands. Network. models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="759a2-133">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="759a2-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="759a2-134">NOTES</span></span>
<span data-ttu-id="759a2-135">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="759a2-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="759a2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="759a2-136">RELATED LINKS</span></span>

[<span data-ttu-id="759a2-137">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="759a2-137">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="759a2-138">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="759a2-138">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="759a2-139">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="759a2-139">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="759a2-140">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="759a2-140">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="759a2-141">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="759a2-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="759a2-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="759a2-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="759a2-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="759a2-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="759a2-144">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="759a2-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="759a2-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="759a2-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="759a2-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="759a2-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="759a2-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="759a2-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="759a2-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="759a2-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

