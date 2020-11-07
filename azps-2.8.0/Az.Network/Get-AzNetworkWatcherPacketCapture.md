---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: dc8093a9e508084639fe64b68378cf44f41aa67d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837568"
---
# <span data-ttu-id="62e6a-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="62e6a-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="62e6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="62e6a-103">Beolvassa a csomagkapcsolt erőforrás adatait és tulajdonságait és állapotát.</span><span class="sxs-lookup"><span data-stu-id="62e6a-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="62e6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62e6a-104">SYNTAX</span></span>

### <span data-ttu-id="62e6a-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="62e6a-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62e6a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="62e6a-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62e6a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="62e6a-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62e6a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="62e6a-108">DESCRIPTION</span></span>
<span data-ttu-id="62e6a-109">A Get-AzNetworkWatcherPacketCapture a csomag-rögzítő erőforrás tulajdonságait és állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="62e6a-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="62e6a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="62e6a-110">EXAMPLES</span></span>

### <span data-ttu-id="62e6a-111">Példa 1: csomag-rögzítés létrehozása több szűrővel és az állapot beolvasása</span><span class="sxs-lookup"><span data-stu-id="62e6a-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="62e6a-112">Ebben a példában a "PacketCaptureTest" nevű csomagot hozzuk létre több szűrővel és időkorlátozással.</span><span class="sxs-lookup"><span data-stu-id="62e6a-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="62e6a-113">A munkamenet befejezésekor a program a megadott tárterület-fiókba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="62e6a-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="62e6a-114">Ezután hívja fel Get-AzNetworkWatcherPacketCapture a rögzítési munkamenet állapotának visszakereséséhez.</span><span class="sxs-lookup"><span data-stu-id="62e6a-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="62e6a-115">Megjegyzés: az Azure Network Watcher bővítménynek telepítve kell lennie a cél virtuális gépen a csomag rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="62e6a-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="62e6a-116">Ha közvetlenül a New-AzNetworkWatcherPacketCapture parancson keresztül hoz létre a csomagra mutató hivatkozást, az nem minden tulajdonsággal fog rendelkezni.</span><span class="sxs-lookup"><span data-stu-id="62e6a-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="62e6a-117">A csomag rögzítésének összes tulajdonságát a Get-AzNetworkWatcherPacketCapture parancs hívásával érheti el.</span><span class="sxs-lookup"><span data-stu-id="62e6a-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="62e6a-118">2. példa: több szűrővel rendelkező csomag létrehozása és állapotának lekérése</span><span class="sxs-lookup"><span data-stu-id="62e6a-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="62e6a-119">Ez a parancsmag minden olyan PacketCaptures visszaadott, amely a "PacketCapture" kezdetű a NW1-hálózati figyelőben.</span><span class="sxs-lookup"><span data-stu-id="62e6a-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="62e6a-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62e6a-120">PARAMETERS</span></span>

### <span data-ttu-id="62e6a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62e6a-121">-AsJob</span></span>
<span data-ttu-id="62e6a-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="62e6a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62e6a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e6a-123">-DefaultProfile</span></span>
<span data-ttu-id="62e6a-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62e6a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62e6a-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="62e6a-125">-Location</span></span>
<span data-ttu-id="62e6a-126">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="62e6a-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="62e6a-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62e6a-127">-NetworkWatcher</span></span>
<span data-ttu-id="62e6a-128">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="62e6a-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="62e6a-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="62e6a-129">-NetworkWatcherName</span></span>
<span data-ttu-id="62e6a-130">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="62e6a-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="62e6a-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="62e6a-131">-PacketCaptureName</span></span>
<span data-ttu-id="62e6a-132">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="62e6a-132">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="62e6a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e6a-133">-ResourceGroupName</span></span>
<span data-ttu-id="62e6a-134">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="62e6a-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="62e6a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e6a-135">CommonParameters</span></span>
<span data-ttu-id="62e6a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62e6a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e6a-137">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="62e6a-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e6a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62e6a-138">INPUTS</span></span>

### <span data-ttu-id="62e6a-139">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62e6a-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="62e6a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="62e6a-140">System.String</span></span>

## <span data-ttu-id="62e6a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62e6a-141">OUTPUTS</span></span>

### <span data-ttu-id="62e6a-142">Microsoft. Azure. commands. Network. models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="62e6a-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="62e6a-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62e6a-143">NOTES</span></span>
<span data-ttu-id="62e6a-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="62e6a-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="62e6a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62e6a-145">RELATED LINKS</span></span>

[<span data-ttu-id="62e6a-146">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62e6a-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="62e6a-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62e6a-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="62e6a-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62e6a-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="62e6a-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="62e6a-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="62e6a-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="62e6a-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="62e6a-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="62e6a-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="62e6a-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="62e6a-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="62e6a-153">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="62e6a-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="62e6a-154">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="62e6a-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="62e6a-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="62e6a-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="62e6a-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="62e6a-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="62e6a-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="62e6a-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="62e6a-158">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="62e6a-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="62e6a-159">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="62e6a-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="62e6a-160">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="62e6a-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="62e6a-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="62e6a-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="62e6a-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="62e6a-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="62e6a-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="62e6a-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="62e6a-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="62e6a-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="62e6a-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="62e6a-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="62e6a-166">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="62e6a-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="62e6a-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="62e6a-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="62e6a-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="62e6a-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="62e6a-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="62e6a-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="62e6a-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="62e6a-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="62e6a-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="62e6a-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="62e6a-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="62e6a-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

