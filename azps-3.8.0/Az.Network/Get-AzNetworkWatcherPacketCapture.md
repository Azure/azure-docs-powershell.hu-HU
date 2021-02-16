---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: e836bb8738b594e09c65568cc0f454a476db9d34
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408882"
---
# <span data-ttu-id="a2d93-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2d93-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a2d93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2d93-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d93-103">Információkat és tulajdonságokat, valamint a csomagrögzítési erőforrás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a2d93-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="a2d93-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2d93-104">SYNTAX</span></span>

### <span data-ttu-id="a2d93-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2d93-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2d93-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a2d93-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2d93-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a2d93-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2d93-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2d93-108">DESCRIPTION</span></span>
<span data-ttu-id="a2d93-109">A Get-AzNetworkWatcherPacketCapture csomagrögzítési erőforrás tulajdonságait és állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a2d93-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="a2d93-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2d93-110">EXAMPLES</span></span>

### <span data-ttu-id="a2d93-111">1. példa: Több szűrővel rendelkező csomagrögzítés létrehozása és állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="a2d93-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a2d93-112">Ebben a példában létrehozunk egy "PacketCaptureTest" nevű csomagrögzítést több szűrővel és egy időkorláttal.</span><span class="sxs-lookup"><span data-stu-id="a2d93-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="a2d93-113">A munkamenet befejezése után a rendszer a megadott tárfiókba menti a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="a2d93-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="a2d93-114">Ezután felhívjuk a Get-AzNetworkWatcherPacketCapture, hogy lekérjük a rögzítési munkamenet állapotát.</span><span class="sxs-lookup"><span data-stu-id="a2d93-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="a2d93-115">Megjegyzés: Csomagrögzítések létrehozásához az Azure Network Watcher bővítményt telepíteni kell a cél virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="a2d93-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="a2d93-116">Ha közvetlenül a New-AzNetworkWatcherPacketCapture parancsból hoz létre hivatkozást a csomagrögzítésre, nem lesz minden tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="a2d93-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="a2d93-117">A csomagrögzítés összes tulajdonságát úgy kaphatja meg, hogy felhívja a Get-AzNetworkWatcherPacketCapture parancsot.</span><span class="sxs-lookup"><span data-stu-id="a2d93-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="a2d93-118">2. példa: Több szűrővel rendelkező csomagrögzítés létrehozása és állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="a2d93-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="a2d93-119">Ez a parancsmag az nw1 Network Watcherben a "PacketCapture" kezdetű összes PacketCapture-et visszaadja.</span><span class="sxs-lookup"><span data-stu-id="a2d93-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="a2d93-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2d93-120">PARAMETERS</span></span>

### <span data-ttu-id="a2d93-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2d93-121">-AsJob</span></span>
<span data-ttu-id="a2d93-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a2d93-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2d93-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d93-123">-DefaultProfile</span></span>
<span data-ttu-id="a2d93-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2d93-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2d93-125">-Location</span><span class="sxs-lookup"><span data-stu-id="a2d93-125">-Location</span></span>
<span data-ttu-id="a2d93-126">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="a2d93-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a2d93-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2d93-127">-NetworkWatcher</span></span>
<span data-ttu-id="a2d93-128">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="a2d93-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="a2d93-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a2d93-129">-NetworkWatcherName</span></span>
<span data-ttu-id="a2d93-130">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="a2d93-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="a2d93-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a2d93-131">-PacketCaptureName</span></span>
<span data-ttu-id="a2d93-132">A csomagrögzítés neve.</span><span class="sxs-lookup"><span data-stu-id="a2d93-132">The packet capture name.</span></span>

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

### <span data-ttu-id="a2d93-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d93-133">-ResourceGroupName</span></span>
<span data-ttu-id="a2d93-134">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2d93-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a2d93-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d93-135">CommonParameters</span></span>
<span data-ttu-id="a2d93-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d93-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d93-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2d93-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d93-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2d93-138">INPUTS</span></span>

### <span data-ttu-id="a2d93-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2d93-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a2d93-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a2d93-140">System.String</span></span>

## <span data-ttu-id="a2d93-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2d93-141">OUTPUTS</span></span>

### <span data-ttu-id="a2d93-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a2d93-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="a2d93-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2d93-143">NOTES</span></span>
<span data-ttu-id="a2d93-144">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="a2d93-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="a2d93-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2d93-145">RELATED LINKS</span></span>

[<span data-ttu-id="a2d93-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2d93-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a2d93-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2d93-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a2d93-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a2d93-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a2d93-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a2d93-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a2d93-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a2d93-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a2d93-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a2d93-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a2d93-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a2d93-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a2d93-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2d93-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2d93-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a2d93-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a2d93-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2d93-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2d93-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2d93-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2d93-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a2d93-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a2d93-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2d93-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a2d93-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a2d93-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a2d93-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a2d93-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a2d93-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2d93-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2d93-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2d93-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2d93-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2d93-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2d93-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a2d93-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a2d93-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2d93-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2d93-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2d93-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a2d93-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a2d93-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a2d93-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a2d93-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a2d93-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a2d93-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a2d93-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a2d93-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a2d93-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a2d93-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a2d93-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a2d93-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

