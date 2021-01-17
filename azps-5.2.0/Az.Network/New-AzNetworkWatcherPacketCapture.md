---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: f6762b074c9b185d12666fb8ea92fcaf15a46b05
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329444"
---
# <span data-ttu-id="c6905-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c6905-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="c6905-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6905-102">SYNOPSIS</span></span>
<span data-ttu-id="c6905-103">Létrehoz egy új csomagrögzítési erőforrást, és elindít egy csomagrögzítési munkamenetet egy VM-en.</span><span class="sxs-lookup"><span data-stu-id="c6905-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="c6905-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c6905-104">SYNTAX</span></span>

### <span data-ttu-id="c6905-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6905-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6905-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c6905-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6905-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c6905-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6905-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c6905-108">DESCRIPTION</span></span>
<span data-ttu-id="c6905-109">A New-AzNetworkWatcherPacketCapture parancsmag létrehoz egy új csomagrögzítési erőforrást, és elindít egy csomagrögzítési munkamenetet egy VM-en.</span><span class="sxs-lookup"><span data-stu-id="c6905-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="c6905-110">A Csomagrögzítési munkamenetek hosszát időkényolhatja vagy méretkényolhatja.</span><span class="sxs-lookup"><span data-stu-id="c6905-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="c6905-111">Az egyes csomagokhoz rögzített adatok mennyisége is konfigurálható.</span><span class="sxs-lookup"><span data-stu-id="c6905-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="c6905-112">Szűrők alkalmazhatók egy adott csomagrögzítési munkamenetre, így testre szabhatja a rögzített csomagok típusát.</span><span class="sxs-lookup"><span data-stu-id="c6905-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="c6905-113">A szűrőkkel korlátozható a helyi és távoli IP-címek & címtartományok, helyi és távoli portok & porttartományok és a rögzített munkamenetszintű protokoll.</span><span class="sxs-lookup"><span data-stu-id="c6905-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="c6905-114">A szűrők kompatibilisek, és több szűrőt is alkalmazhat, hogy a felvétel részletes legyen.</span><span class="sxs-lookup"><span data-stu-id="c6905-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="c6905-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c6905-115">EXAMPLES</span></span>

### <span data-ttu-id="c6905-116">1. példa: Csomagrögzítés létrehozása több szűrővel</span><span class="sxs-lookup"><span data-stu-id="c6905-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="c6905-117">Ebben a példában létrehozunk egy "PacketCaptureTest" nevű csomagrögzítést több szűrővel és egy időkorláttal.</span><span class="sxs-lookup"><span data-stu-id="c6905-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="c6905-118">A munkamenet befejezése után a rendszer a megadott tárfiókba menti a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="c6905-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="c6905-119">Megjegyzés: Csomagrögzítések létrehozásához az Azure Network Watcher bővítményt telepíteni kell a cél virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="c6905-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="c6905-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6905-120">PARAMETERS</span></span>

### <span data-ttu-id="c6905-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6905-121">-AsJob</span></span>
<span data-ttu-id="c6905-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c6905-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6905-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="c6905-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="c6905-124">Csomagonként rögzítend bájt.</span><span class="sxs-lookup"><span data-stu-id="c6905-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="c6905-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6905-125">-DefaultProfile</span></span>
<span data-ttu-id="c6905-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6905-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6905-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="c6905-127">-Filter</span></span>
<span data-ttu-id="c6905-128">A csomagrögzítési munkamenet szűrői.</span><span class="sxs-lookup"><span data-stu-id="c6905-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="c6905-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="c6905-129">-LocalFilePath</span></span>
<span data-ttu-id="c6905-130">Helyi fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c6905-130">Local file path.</span></span>

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

### <span data-ttu-id="c6905-131">-Location</span><span class="sxs-lookup"><span data-stu-id="c6905-131">-Location</span></span>
<span data-ttu-id="c6905-132">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="c6905-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c6905-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c6905-133">-NetworkWatcher</span></span>
<span data-ttu-id="c6905-134">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="c6905-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="c6905-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c6905-135">-NetworkWatcherName</span></span>
<span data-ttu-id="c6905-136">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="c6905-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="c6905-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="c6905-137">-PacketCaptureName</span></span>
<span data-ttu-id="c6905-138">A csomagrögzítés neve.</span><span class="sxs-lookup"><span data-stu-id="c6905-138">The packet capture name.</span></span>

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

### <span data-ttu-id="c6905-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6905-139">-ResourceGroupName</span></span>
<span data-ttu-id="c6905-140">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6905-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c6905-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c6905-141">-StorageAccountId</span></span>
<span data-ttu-id="c6905-142">Tárfiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c6905-142">Storage account Id.</span></span>

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

### <span data-ttu-id="c6905-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="c6905-143">-StoragePath</span></span>
<span data-ttu-id="c6905-144">Tárterület elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c6905-144">Storage path.</span></span>

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

### <span data-ttu-id="c6905-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c6905-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="c6905-146">A cél virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c6905-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="c6905-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="c6905-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="c6905-148">Időkorlát másodpercben</span><span class="sxs-lookup"><span data-stu-id="c6905-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="c6905-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="c6905-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="c6905-150">Munkamenetenként összesen bájt.</span><span class="sxs-lookup"><span data-stu-id="c6905-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="c6905-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6905-151">-Confirm</span></span>
<span data-ttu-id="c6905-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c6905-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6905-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6905-153">-WhatIf</span></span>
<span data-ttu-id="c6905-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c6905-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6905-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6905-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6905-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6905-156">CommonParameters</span></span>
<span data-ttu-id="c6905-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6905-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6905-158">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6905-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6905-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6905-159">INPUTS</span></span>

### <span data-ttu-id="c6905-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c6905-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c6905-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c6905-161">System.String</span></span>

### <span data-ttu-id="c6905-162">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c6905-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c6905-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6905-163">OUTPUTS</span></span>

### <span data-ttu-id="c6905-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="c6905-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="c6905-165">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c6905-165">NOTES</span></span>
<span data-ttu-id="c6905-166">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="c6905-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="c6905-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6905-167">RELATED LINKS</span></span>

[<span data-ttu-id="c6905-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c6905-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c6905-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c6905-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c6905-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c6905-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c6905-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c6905-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c6905-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c6905-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c6905-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c6905-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c6905-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c6905-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c6905-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c6905-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c6905-176">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c6905-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c6905-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c6905-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c6905-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c6905-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c6905-179">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c6905-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c6905-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6905-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c6905-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c6905-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c6905-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c6905-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c6905-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6905-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c6905-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6905-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c6905-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6905-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c6905-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c6905-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c6905-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6905-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c6905-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6905-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c6905-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c6905-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c6905-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c6905-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c6905-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c6905-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c6905-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c6905-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c6905-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c6905-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c6905-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c6905-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


