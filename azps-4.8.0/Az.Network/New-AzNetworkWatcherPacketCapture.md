---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: f6762b074c9b185d12666fb8ea92fcaf15a46b05
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182989"
---
# <span data-ttu-id="2c9ce-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c9ce-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="2c9ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9ce-103">Létrehoz egy új csomagkapcsolt adatrögzítő erőforrást, és a csomag rögzítési munkamenetét egy VM-eszközön indítja el.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="2c9ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c9ce-104">SYNTAX</span></span>

### <span data-ttu-id="2c9ce-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c9ce-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c9ce-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2c9ce-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c9ce-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2c9ce-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c9ce-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c9ce-108">DESCRIPTION</span></span>
<span data-ttu-id="2c9ce-109">Az New-AzNetworkWatcherPacketCapture parancsmag létrehoz egy új csomagkapcsolt adatrögzítő erőforrást, és egy csomag-rögzítési munkamenetet indít a VM-ben.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="2c9ce-110">A csomag-rögzítési munkamenetek hosszát időkorlátozással vagy méret korlátozással lehet konfigurálni.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="2c9ce-111">Az egyes csomagokhoz rögzített adatmennyiség is konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="2c9ce-112">A szűrők alkalmazhatók az adott csomag-felvételi munkamenetre, így testre szabhatja a rögzített csomagok típusát.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="2c9ce-113">A szűrők a helyi és a távoli IP-címeken & a címtartomány, a helyi és távoli portok & a porttartomány, valamint a beragadni kívánt munkamenet-szintű protokoll korlátozását is korlátozhatja.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="2c9ce-114">A szűrők elérhetők, és több szűrő is alkalmazható a rögzítés részletességének biztosítására.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="2c9ce-115">Példák</span><span class="sxs-lookup"><span data-stu-id="2c9ce-115">EXAMPLES</span></span>

### <span data-ttu-id="2c9ce-116">Példa 1: több szűrőből álló csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="2c9ce-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="2c9ce-117">Ebben a példában a "PacketCaptureTest" nevű csomagot hozzuk létre több szűrővel és időkorlátozással.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="2c9ce-118">A munkamenet befejezésekor a program a megadott tárterület-fiókba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="2c9ce-119">Megjegyzés: az Azure Network Watcher bővítménynek telepítve kell lennie a cél virtuális gépen a csomag rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="2c9ce-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c9ce-120">PARAMETERS</span></span>

### <span data-ttu-id="2c9ce-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c9ce-121">-AsJob</span></span>
<span data-ttu-id="2c9ce-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2c9ce-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9ce-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="2c9ce-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="2c9ce-124">A csomagokat rögzítő bájtok száma.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-124">Bytes to capture per packet.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9ce-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9ce-125">-DefaultProfile</span></span>
<span data-ttu-id="2c9ce-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9ce-127">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="2c9ce-127">-Filter</span></span>
<span data-ttu-id="2c9ce-128">A csomagok rögzítési munkamenetének szűrői</span><span class="sxs-lookup"><span data-stu-id="2c9ce-128">Filters for packet capture session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9ce-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="2c9ce-129">-LocalFilePath</span></span>
<span data-ttu-id="2c9ce-130">Helyi fájl elérési útja</span><span class="sxs-lookup"><span data-stu-id="2c9ce-130">Local file path.</span></span>

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

### <span data-ttu-id="2c9ce-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="2c9ce-131">-Location</span></span>
<span data-ttu-id="2c9ce-132">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-132">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9ce-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c9ce-133">-NetworkWatcher</span></span>
<span data-ttu-id="2c9ce-134">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="2c9ce-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2c9ce-135">-NetworkWatcherName</span></span>
<span data-ttu-id="2c9ce-136">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="2c9ce-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="2c9ce-137">-PacketCaptureName</span></span>
<span data-ttu-id="2c9ce-138">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-138">The packet capture name.</span></span>

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

### <span data-ttu-id="2c9ce-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c9ce-139">-ResourceGroupName</span></span>
<span data-ttu-id="2c9ce-140">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2c9ce-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2c9ce-141">-StorageAccountId</span></span>
<span data-ttu-id="2c9ce-142">Tárolási fiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-142">Storage account Id.</span></span>

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

### <span data-ttu-id="2c9ce-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="2c9ce-143">-StoragePath</span></span>
<span data-ttu-id="2c9ce-144">Tárterület elérési útja</span><span class="sxs-lookup"><span data-stu-id="2c9ce-144">Storage path.</span></span>

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

### <span data-ttu-id="2c9ce-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2c9ce-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2c9ce-146">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="2c9ce-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="2c9ce-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="2c9ce-148">Időkorlát másodpercben.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-148">Time limit in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9ce-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="2c9ce-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="2c9ce-150">Munkamenetenként összesen bájt.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-150">Total bytes per session.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9ce-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c9ce-151">-Confirm</span></span>
<span data-ttu-id="2c9ce-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9ce-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c9ce-153">-WhatIf</span></span>
<span data-ttu-id="2c9ce-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c9ce-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c9ce-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c9ce-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9ce-156">CommonParameters</span></span>
<span data-ttu-id="2c9ce-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c9ce-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9ce-158">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9ce-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9ce-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c9ce-159">INPUTS</span></span>

### <span data-ttu-id="2c9ce-160">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c9ce-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2c9ce-161">System. String</span><span class="sxs-lookup"><span data-stu-id="2c9ce-161">System.String</span></span>

### <span data-ttu-id="2c9ce-162">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2c9ce-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2c9ce-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c9ce-163">OUTPUTS</span></span>

### <span data-ttu-id="2c9ce-164">Microsoft. Azure. commands. Network. models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="2c9ce-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="2c9ce-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c9ce-165">NOTES</span></span>
<span data-ttu-id="2c9ce-166">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="2c9ce-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="2c9ce-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c9ce-167">RELATED LINKS</span></span>

[<span data-ttu-id="2c9ce-168">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c9ce-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2c9ce-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c9ce-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2c9ce-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c9ce-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2c9ce-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2c9ce-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2c9ce-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2c9ce-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2c9ce-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2c9ce-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2c9ce-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2c9ce-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2c9ce-175">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c9ce-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c9ce-176">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2c9ce-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2c9ce-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c9ce-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c9ce-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c9ce-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c9ce-179">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c9ce-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c9ce-180">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c9ce-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2c9ce-181">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2c9ce-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2c9ce-182">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2c9ce-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2c9ce-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c9ce-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c9ce-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c9ce-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c9ce-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c9ce-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c9ce-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2c9ce-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2c9ce-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c9ce-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c9ce-188">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c9ce-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c9ce-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2c9ce-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2c9ce-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2c9ce-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2c9ce-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2c9ce-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2c9ce-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2c9ce-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2c9ce-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2c9ce-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2c9ce-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c9ce-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


