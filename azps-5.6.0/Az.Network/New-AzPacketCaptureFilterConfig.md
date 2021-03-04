---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: b3732167d26f35b0e3e8ac6c29f187138cde0b18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919570"
---
# <span data-ttu-id="f1d11-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f1d11-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="f1d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1d11-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d11-103">Új csomagrögzítési szűrőobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f1d11-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="f1d11-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f1d11-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1d11-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f1d11-105">DESCRIPTION</span></span>
<span data-ttu-id="f1d11-106">A New-AzPacketCaptureFilterConfig parancsmag létrehoz egy új csomagrögzítési szűrőobjektumot.</span><span class="sxs-lookup"><span data-stu-id="f1d11-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="f1d11-107">Ezzel az objektummal korlátozható a csomagrögzítési munkamenet során rögzített csomagok típusa a megadott feltételekkel.</span><span class="sxs-lookup"><span data-stu-id="f1d11-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="f1d11-108">A New-AzNetworkWatcherPacketCapture parancsmag több szűrőobjektumot is elfogadhat a kompatibilis rögzítési munkamenetek engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="f1d11-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="f1d11-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f1d11-109">EXAMPLES</span></span>

### <span data-ttu-id="f1d11-110">1. példa: Csomagrögzítés létrehozása több szűrővel</span><span class="sxs-lookup"><span data-stu-id="f1d11-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="f1d11-111">Ebben a példában létrehozunk egy "PacketCaptureTest" nevű csomagrögzítést több szűrővel és egy időkorláttal.</span><span class="sxs-lookup"><span data-stu-id="f1d11-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="f1d11-112">A munkamenet befejezése után a rendszer a megadott tárfiókba menti a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="f1d11-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="f1d11-113">Megjegyzés: Csomagrögzítések létrehozásához az Azure Network Watcher bővítményt telepíteni kell a cél virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="f1d11-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="f1d11-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1d11-114">PARAMETERS</span></span>

### <span data-ttu-id="f1d11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d11-115">-DefaultProfile</span></span>
<span data-ttu-id="f1d11-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1d11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1d11-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="f1d11-117">-LocalIPAddress</span></span>
<span data-ttu-id="f1d11-118">Megadja azt a helyi IP-címet, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="f1d11-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="f1d11-119">Példa: "127.0.0.1" egyetlen címbejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="f1d11-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="f1d11-120">"127.0.0.1-127.0.0.255" a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="f1d11-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="f1d11-121">"127.0.0.1;127.0.0.5;" több bejegyzés esetén.</span><span class="sxs-lookup"><span data-stu-id="f1d11-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="f1d11-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="f1d11-122">-LocalPort</span></span>
<span data-ttu-id="f1d11-123">Megadja azt a helyi IP-címet, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="f1d11-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="f1d11-124">Példa: "127.0.0.1" egyetlen címbejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="f1d11-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="f1d11-125">"127.0.0.1-127.0.0.255" a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="f1d11-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="f1d11-126">"127.0.0.1;127.0.0.5;" több bejegyzés esetén.</span><span class="sxs-lookup"><span data-stu-id="f1d11-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="f1d11-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f1d11-127">-Protocol</span></span>
<span data-ttu-id="f1d11-128">Azt a protokollt adja meg, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="f1d11-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="f1d11-129">Elfogadható értékek: "TCP","UDP","Any"</span><span class="sxs-lookup"><span data-stu-id="f1d11-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d11-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="f1d11-130">-RemoteIPAddress</span></span>
<span data-ttu-id="f1d11-131">Megadja azt a távoli IP-címet, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="f1d11-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="f1d11-132">Példa: "127.0.0.1" egyetlen címbejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="f1d11-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="f1d11-133">"127.0.0.1-127.0.0.255" a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="f1d11-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="f1d11-134">"127.0.0.1;127.0.0.5;" több bejegyzés esetén.</span><span class="sxs-lookup"><span data-stu-id="f1d11-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="f1d11-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="f1d11-135">-RemotePort</span></span>
<span data-ttu-id="f1d11-136">Megadja a távoli portot, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="f1d11-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="f1d11-137">Távoli port – Példa: "80" egyetlen port bejegyzéséhez.</span><span class="sxs-lookup"><span data-stu-id="f1d11-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="f1d11-138">"80-85" a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="f1d11-138">"80-85" for range.</span></span>
<span data-ttu-id="f1d11-139">"80;443;" több bejegyzés esetén.</span><span class="sxs-lookup"><span data-stu-id="f1d11-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="f1d11-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d11-140">CommonParameters</span></span>
<span data-ttu-id="f1d11-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1d11-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d11-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1d11-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d11-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1d11-143">INPUTS</span></span>

### <span data-ttu-id="f1d11-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f1d11-144">System.String</span></span>

## <span data-ttu-id="f1d11-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1d11-145">OUTPUTS</span></span>

### <span data-ttu-id="f1d11-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="f1d11-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="f1d11-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f1d11-147">NOTES</span></span>
<span data-ttu-id="f1d11-148">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, figyelő, csomag, rögzítés, forgalom, szűrés</span><span class="sxs-lookup"><span data-stu-id="f1d11-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="f1d11-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1d11-149">RELATED LINKS</span></span>

[<span data-ttu-id="f1d11-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f1d11-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f1d11-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f1d11-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f1d11-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f1d11-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f1d11-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f1d11-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f1d11-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f1d11-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f1d11-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f1d11-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f1d11-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f1d11-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f1d11-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1d11-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1d11-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f1d11-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f1d11-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1d11-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1d11-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1d11-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1d11-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1d11-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1d11-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1d11-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f1d11-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f1d11-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f1d11-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f1d11-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f1d11-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1d11-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f1d11-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1d11-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f1d11-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1d11-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f1d11-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f1d11-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f1d11-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1d11-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f1d11-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1d11-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f1d11-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f1d11-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f1d11-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f1d11-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f1d11-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f1d11-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f1d11-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f1d11-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f1d11-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f1d11-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f1d11-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f1d11-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
