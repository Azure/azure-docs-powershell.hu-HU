---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: f91dc3942241237ddf3841d276ea442361d89987
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849573"
---
# <span data-ttu-id="4d7cf-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d7cf-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="4d7cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7cf-103">Létrehoz egy új csomagkapcsolt adatrögzítő erőforrást, és a csomag rögzítési munkamenetét egy VM-eszközön indítja el.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d7cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d7cf-104">SYNTAX</span></span>

### <span data-ttu-id="4d7cf-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d7cf-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d7cf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4d7cf-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d7cf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d7cf-107">DESCRIPTION</span></span>
<span data-ttu-id="4d7cf-108">Az New-AzureRmNetworkWatcherPacketCapture parancsmag létrehoz egy új csomagkapcsolt adatrögzítő erőforrást, és egy csomag-rögzítési munkamenetet indít a VM-ben.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="4d7cf-109">A csomag-rögzítési munkamenetek hosszát időkorlátozással vagy méret korlátozással lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="4d7cf-110">Az egyes csomagokhoz rögzített adatmennyiség is konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="4d7cf-111">A szűrők alkalmazhatók az adott csomag-felvételi munkamenetre, így testre szabhatja a rögzített csomagok típusát.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="4d7cf-112">A szűrők a helyi és a távoli IP-címeken & a címtartomány, a helyi és távoli portok & a porttartomány, valamint a beragadni kívánt munkamenet-szintű protokoll korlátozását is korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="4d7cf-113">A szűrők elérhetők, és több szűrő is alkalmazható a rögzítés részletességének biztosítására.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="4d7cf-114">Példák</span><span class="sxs-lookup"><span data-stu-id="4d7cf-114">EXAMPLES</span></span>

### <span data-ttu-id="4d7cf-115">---Példa 1: több szűrőből álló csomag létrehozása---</span><span class="sxs-lookup"><span data-stu-id="4d7cf-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="4d7cf-116">Ebben a példában a "PacketCaptureTest" nevű csomagot hozzuk létre több szűrővel és időkorlátozással.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="4d7cf-117">A munkamenet befejezésekor a program a megadott tárterület-fiókba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="4d7cf-118">Megjegyzés: az Azure Network Watcher bővítménynek telepítve kell lennie a cél virtuális gépen a csomag rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="4d7cf-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d7cf-119">PARAMETERS</span></span>

### <span data-ttu-id="4d7cf-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d7cf-120">-AsJob</span></span>
<span data-ttu-id="4d7cf-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4d7cf-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d7cf-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="4d7cf-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="4d7cf-123">A csomagokat rögzítő bájtok száma.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-123">Bytes to capture per packet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7cf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d7cf-124">-DefaultProfile</span></span>
<span data-ttu-id="4d7cf-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d7cf-126">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="4d7cf-126">-Filter</span></span>
<span data-ttu-id="4d7cf-127">A csomagok rögzítési munkamenetének szűrői</span><span class="sxs-lookup"><span data-stu-id="4d7cf-127">Filters for packet capture session.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7cf-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="4d7cf-128">-LocalFilePath</span></span>
<span data-ttu-id="4d7cf-129">Helyi fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="4d7cf-129">Local file path.</span></span>

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

### <span data-ttu-id="4d7cf-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d7cf-130">-NetworkWatcher</span></span>
<span data-ttu-id="4d7cf-131">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="4d7cf-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4d7cf-132">-NetworkWatcherName</span></span>
<span data-ttu-id="4d7cf-133">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="4d7cf-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="4d7cf-134">-PacketCaptureName</span></span>
<span data-ttu-id="4d7cf-135">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-135">The packet capture name.</span></span>

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

### <span data-ttu-id="4d7cf-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d7cf-136">-ResourceGroupName</span></span>
<span data-ttu-id="4d7cf-137">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4d7cf-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4d7cf-138">-StorageAccountId</span></span>
<span data-ttu-id="4d7cf-139">Tárolási fiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-139">Storage account Id.</span></span>

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

### <span data-ttu-id="4d7cf-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="4d7cf-140">-StoragePath</span></span>
<span data-ttu-id="4d7cf-141">Tárterület elérési útja</span><span class="sxs-lookup"><span data-stu-id="4d7cf-141">Storage path.</span></span>

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

### <span data-ttu-id="4d7cf-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="4d7cf-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="4d7cf-143">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="4d7cf-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="4d7cf-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="4d7cf-145">Időkorlát másodpercben.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-145">Time limit in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7cf-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="4d7cf-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="4d7cf-147">Munkamenetenként összesen bájt.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-147">Total bytes per session.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7cf-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d7cf-148">-Confirm</span></span>
<span data-ttu-id="4d7cf-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7cf-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d7cf-150">-WhatIf</span></span>
<span data-ttu-id="4d7cf-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d7cf-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d7cf-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7cf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7cf-153">CommonParameters</span></span>
<span data-ttu-id="4d7cf-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d7cf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d7cf-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d7cf-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7cf-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d7cf-156">INPUTS</span></span>

### <span data-ttu-id="4d7cf-157">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d7cf-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4d7cf-158">System. String System. null \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="4d7cf-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="4d7cf-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d7cf-159">OUTPUTS</span></span>

### <span data-ttu-id="4d7cf-160">Microsoft. Azure. commands. Network. models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d7cf-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="4d7cf-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d7cf-161">NOTES</span></span>
<span data-ttu-id="4d7cf-162">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="4d7cf-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="4d7cf-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d7cf-163">RELATED LINKS</span></span>

[<span data-ttu-id="4d7cf-164">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4d7cf-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4d7cf-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d7cf-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d7cf-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d7cf-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d7cf-167">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d7cf-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d7cf-168">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d7cf-168">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d7cf-169">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d7cf-169">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d7cf-170">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d7cf-170">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d7cf-171">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4d7cf-171">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4d7cf-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4d7cf-172">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4d7cf-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4d7cf-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4d7cf-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4d7cf-174">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4d7cf-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4d7cf-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)


