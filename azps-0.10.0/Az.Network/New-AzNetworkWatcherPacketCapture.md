---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 6844db506ee8a55c7d0c16f54946e35349059ae4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841285"
---
# <span data-ttu-id="ba285-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba285-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="ba285-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba285-102">SYNOPSIS</span></span>
<span data-ttu-id="ba285-103">Létrehoz egy új csomagkapcsolt adatrögzítő erőforrást, és a csomag rögzítési munkamenetét egy VM-eszközön indítja el.</span><span class="sxs-lookup"><span data-stu-id="ba285-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="ba285-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba285-104">SYNTAX</span></span>

### <span data-ttu-id="ba285-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba285-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba285-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ba285-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba285-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba285-107">DESCRIPTION</span></span>
<span data-ttu-id="ba285-108">Az New-AzNetworkWatcherPacketCapture parancsmag létrehoz egy új csomagkapcsolt adatrögzítő erőforrást, és egy csomag-rögzítési munkamenetet indít a VM-ben.</span><span class="sxs-lookup"><span data-stu-id="ba285-108">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="ba285-109">A csomag-rögzítési munkamenetek hosszát időkorlátozással vagy méret korlátozással lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="ba285-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="ba285-110">Az egyes csomagokhoz rögzített adatmennyiség is konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="ba285-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="ba285-111">A szűrők alkalmazhatók az adott csomag-felvételi munkamenetre, így testre szabhatja a rögzített csomagok típusát.</span><span class="sxs-lookup"><span data-stu-id="ba285-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="ba285-112">A szűrők a helyi és a távoli IP-címeken & a címtartomány, a helyi és távoli portok & a porttartomány, valamint a beragadni kívánt munkamenet-szintű protokoll korlátozását is korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="ba285-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="ba285-113">A szűrők elérhetők, és több szűrő is alkalmazható a rögzítés részletességének biztosítására.</span><span class="sxs-lookup"><span data-stu-id="ba285-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="ba285-114">Példák</span><span class="sxs-lookup"><span data-stu-id="ba285-114">EXAMPLES</span></span>

### <span data-ttu-id="ba285-115">---Példa 1: több szűrőből álló csomag létrehozása---</span><span class="sxs-lookup"><span data-stu-id="ba285-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="ba285-116">Ebben a példában a "PacketCaptureTest" nevű csomagot hozzuk létre több szűrővel és időkorlátozással.</span><span class="sxs-lookup"><span data-stu-id="ba285-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="ba285-117">A munkamenet befejezésekor a program a megadott tárterület-fiókba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="ba285-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="ba285-118">Megjegyzés: az Azure Network Watcher bővítménynek telepítve kell lennie a cél virtuális gépen a csomag rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="ba285-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="ba285-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba285-119">PARAMETERS</span></span>

### <span data-ttu-id="ba285-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba285-120">-AsJob</span></span>
<span data-ttu-id="ba285-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ba285-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba285-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="ba285-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="ba285-123">A csomagokat rögzítő bájtok száma.</span><span class="sxs-lookup"><span data-stu-id="ba285-123">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="ba285-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba285-124">-DefaultProfile</span></span>
<span data-ttu-id="ba285-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba285-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba285-126">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="ba285-126">-Filter</span></span>
<span data-ttu-id="ba285-127">A csomagok rögzítési munkamenetének szűrői</span><span class="sxs-lookup"><span data-stu-id="ba285-127">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="ba285-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="ba285-128">-LocalFilePath</span></span>
<span data-ttu-id="ba285-129">Helyi fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="ba285-129">Local file path.</span></span>

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

### <span data-ttu-id="ba285-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba285-130">-NetworkWatcher</span></span>
<span data-ttu-id="ba285-131">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ba285-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="ba285-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ba285-132">-NetworkWatcherName</span></span>
<span data-ttu-id="ba285-133">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="ba285-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="ba285-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="ba285-134">-PacketCaptureName</span></span>
<span data-ttu-id="ba285-135">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="ba285-135">The packet capture name.</span></span>

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

### <span data-ttu-id="ba285-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba285-136">-ResourceGroupName</span></span>
<span data-ttu-id="ba285-137">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba285-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ba285-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ba285-138">-StorageAccountId</span></span>
<span data-ttu-id="ba285-139">Tárolási fiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ba285-139">Storage account Id.</span></span>

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

### <span data-ttu-id="ba285-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="ba285-140">-StoragePath</span></span>
<span data-ttu-id="ba285-141">Tárterület elérési útja</span><span class="sxs-lookup"><span data-stu-id="ba285-141">Storage path.</span></span>

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

### <span data-ttu-id="ba285-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ba285-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="ba285-143">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ba285-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="ba285-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="ba285-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="ba285-145">Időkorlát másodpercben.</span><span class="sxs-lookup"><span data-stu-id="ba285-145">Time limit in seconds.</span></span>

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

### <span data-ttu-id="ba285-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="ba285-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="ba285-147">Munkamenetenként összesen bájt.</span><span class="sxs-lookup"><span data-stu-id="ba285-147">Total bytes per session.</span></span>

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

### <span data-ttu-id="ba285-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba285-148">-Confirm</span></span>
<span data-ttu-id="ba285-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba285-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba285-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba285-150">-WhatIf</span></span>
<span data-ttu-id="ba285-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba285-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba285-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba285-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba285-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba285-153">CommonParameters</span></span>
<span data-ttu-id="ba285-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba285-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba285-155">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba285-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba285-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba285-156">INPUTS</span></span>

### <span data-ttu-id="ba285-157">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba285-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ba285-158">System. String System. null \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="ba285-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="ba285-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba285-159">OUTPUTS</span></span>

### <span data-ttu-id="ba285-160">Microsoft. Azure. commands. Network. models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba285-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="ba285-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba285-161">NOTES</span></span>
<span data-ttu-id="ba285-162">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="ba285-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="ba285-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba285-163">RELATED LINKS</span></span>

[<span data-ttu-id="ba285-164">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ba285-164">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ba285-165">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba285-165">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ba285-166">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba285-166">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ba285-167">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ba285-167">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ba285-168">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba285-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ba285-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba285-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ba285-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ba285-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ba285-171">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ba285-171">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ba285-172">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ba285-172">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ba285-173">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ba285-173">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ba285-174">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ba285-174">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ba285-175">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ba285-175">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)


