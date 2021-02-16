---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b98ebe6bfe1bbae1f88c49799f875f56cee52698
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400331"
---
# <span data-ttu-id="a06c6-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a06c6-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a06c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a06c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a06c6-103">Információkat és tulajdonságokat, valamint a csomagrögzítési erőforrás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a06c6-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="a06c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a06c6-104">SYNTAX</span></span>

### <span data-ttu-id="a06c6-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a06c6-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a06c6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a06c6-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a06c6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a06c6-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a06c6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a06c6-108">DESCRIPTION</span></span>
<span data-ttu-id="a06c6-109">A Get-AzNetworkWatcherPacketCapture csomagrögzítési erőforrás tulajdonságait és állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a06c6-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="a06c6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a06c6-110">EXAMPLES</span></span>

### <span data-ttu-id="a06c6-111">1. példa: Több szűrővel rendelkező csomagrögzítés létrehozása és állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="a06c6-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a06c6-112">Ebben a példában létrehozunk egy "PacketCaptureTest" nevű csomagrögzítést több szűrővel és egy időkorláttal.</span><span class="sxs-lookup"><span data-stu-id="a06c6-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="a06c6-113">A munkamenet befejezése után a rendszer a megadott tárfiókba menti a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="a06c6-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="a06c6-114">Ezután felhívjuk a Get-AzNetworkWatcherPacketCapture, hogy lekérjük a rögzítési munkamenet állapotát.</span><span class="sxs-lookup"><span data-stu-id="a06c6-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="a06c6-115">Megjegyzés: Csomagrögzítések létrehozásához az Azure Network Watcher bővítményt telepíteni kell a cél virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="a06c6-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

### <span data-ttu-id="a06c6-116">2. példa: Több szűrővel rendelkező csomagrögzítés létrehozása és állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="a06c6-116">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="a06c6-117">Ez a parancsmag az nw1 Network Watcherben a "PacketCapture" kezdetű összes PacketCapture-et visszaadja.</span><span class="sxs-lookup"><span data-stu-id="a06c6-117">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="a06c6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a06c6-118">PARAMETERS</span></span>

### <span data-ttu-id="a06c6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a06c6-119">-AsJob</span></span>
<span data-ttu-id="a06c6-120">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a06c6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a06c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06c6-121">-DefaultProfile</span></span>
<span data-ttu-id="a06c6-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a06c6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a06c6-123">-Location</span><span class="sxs-lookup"><span data-stu-id="a06c6-123">-Location</span></span>
<span data-ttu-id="a06c6-124">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="a06c6-124">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a06c6-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a06c6-125">-NetworkWatcher</span></span>
<span data-ttu-id="a06c6-126">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="a06c6-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="a06c6-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a06c6-127">-NetworkWatcherName</span></span>
<span data-ttu-id="a06c6-128">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="a06c6-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="a06c6-129">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a06c6-129">-PacketCaptureName</span></span>
<span data-ttu-id="a06c6-130">A csomagrögzítés neve.</span><span class="sxs-lookup"><span data-stu-id="a06c6-130">The packet capture name.</span></span>

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

### <span data-ttu-id="a06c6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06c6-131">-ResourceGroupName</span></span>
<span data-ttu-id="a06c6-132">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a06c6-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a06c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06c6-133">CommonParameters</span></span>
<span data-ttu-id="a06c6-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06c6-135">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a06c6-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06c6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a06c6-136">INPUTS</span></span>

### <span data-ttu-id="a06c6-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a06c6-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a06c6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a06c6-138">System.String</span></span>

## <span data-ttu-id="a06c6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a06c6-139">OUTPUTS</span></span>

### <span data-ttu-id="a06c6-140">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a06c6-140">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="a06c6-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a06c6-141">NOTES</span></span>
<span data-ttu-id="a06c6-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="a06c6-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="a06c6-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a06c6-143">RELATED LINKS</span></span>

[<span data-ttu-id="a06c6-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a06c6-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a06c6-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a06c6-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a06c6-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a06c6-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a06c6-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a06c6-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a06c6-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a06c6-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a06c6-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a06c6-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a06c6-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a06c6-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a06c6-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a06c6-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a06c6-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a06c6-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a06c6-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a06c6-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a06c6-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a06c6-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a06c6-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a06c6-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a06c6-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a06c6-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a06c6-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a06c6-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a06c6-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a06c6-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a06c6-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a06c6-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a06c6-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a06c6-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a06c6-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a06c6-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a06c6-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a06c6-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a06c6-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a06c6-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a06c6-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a06c6-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a06c6-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a06c6-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a06c6-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a06c6-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a06c6-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a06c6-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a06c6-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a06c6-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a06c6-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a06c6-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a06c6-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a06c6-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

