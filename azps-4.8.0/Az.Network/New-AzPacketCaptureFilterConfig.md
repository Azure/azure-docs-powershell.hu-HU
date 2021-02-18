---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: d7dac006abf09ec7c80d4a7e7659405936a8d20e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409647"
---
# <span data-ttu-id="16ec1-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="16ec1-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="16ec1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="16ec1-103">Új csomagrögzítési szűrőobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="16ec1-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="16ec1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="16ec1-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16ec1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="16ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="16ec1-106">A New-AzPacketCaptureFilterConfig parancsmag létrehoz egy új csomagrögzítési szűrőobjektumot.</span><span class="sxs-lookup"><span data-stu-id="16ec1-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="16ec1-107">Ezzel az objektummal korlátozható a csomagrögzítési munkamenet során rögzített csomagok típusa a megadott feltételekkel.</span><span class="sxs-lookup"><span data-stu-id="16ec1-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="16ec1-108">A New-AzNetworkWatcherPacketCapture parancsmag több szűrőobjektumot is elfogadhat a kompatibilis rögzítési munkamenetek engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="16ec1-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="16ec1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="16ec1-109">EXAMPLES</span></span>

### <span data-ttu-id="16ec1-110">1. példa: Csomagrögzítés létrehozása több szűrővel</span><span class="sxs-lookup"><span data-stu-id="16ec1-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="16ec1-111">Ebben a példában létrehozunk egy "PacketCaptureTest" nevű csomagrögzítést több szűrővel és egy időkorláttal.</span><span class="sxs-lookup"><span data-stu-id="16ec1-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="16ec1-112">A munkamenet befejezése után a rendszer a megadott tárfiókba menti a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="16ec1-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="16ec1-113">Megjegyzés: Csomagrögzítések létrehozásához az Azure Network Watcher bővítményt telepíteni kell a cél virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="16ec1-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="16ec1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16ec1-114">PARAMETERS</span></span>

### <span data-ttu-id="16ec1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ec1-115">-DefaultProfile</span></span>
<span data-ttu-id="16ec1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16ec1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ec1-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="16ec1-117">-LocalIPAddress</span></span>
<span data-ttu-id="16ec1-118">Megadja azt a helyi IP-címet, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="16ec1-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="16ec1-119">Példa: "127.0.0.1" egyetlen címbejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="16ec1-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="16ec1-120">"127.0.0.1-127.0.0.255" a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="16ec1-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="16ec1-121">"127.0.0.1;127.0.0.5;" több bejegyzés esetén.</span><span class="sxs-lookup"><span data-stu-id="16ec1-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="16ec1-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="16ec1-122">-LocalPort</span></span>
<span data-ttu-id="16ec1-123">Megadja azt a helyi IP-címet, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="16ec1-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="16ec1-124">Példa: "127.0.0.1" egyetlen címbejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="16ec1-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="16ec1-125">"127.0.0.1-127.0.0.255" a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="16ec1-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="16ec1-126">"127.0.0.1;127.0.0.5;" több bejegyzés esetén.</span><span class="sxs-lookup"><span data-stu-id="16ec1-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="16ec1-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="16ec1-127">-Protocol</span></span>
<span data-ttu-id="16ec1-128">Azt a protokollt adja meg, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="16ec1-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="16ec1-129">Elfogadható értékek: "TCP","UDP","Any"</span><span class="sxs-lookup"><span data-stu-id="16ec1-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="16ec1-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="16ec1-130">-RemoteIPAddress</span></span>
<span data-ttu-id="16ec1-131">Megadja azt a távoli IP-címet, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="16ec1-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="16ec1-132">Példa: "127.0.0.1" egyetlen címbejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="16ec1-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="16ec1-133">"127.0.0.1-127.0.0.255" a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="16ec1-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="16ec1-134">"127.0.0.1;127.0.0.5;" több bejegyzés esetén.</span><span class="sxs-lookup"><span data-stu-id="16ec1-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="16ec1-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="16ec1-135">-RemotePort</span></span>
<span data-ttu-id="16ec1-136">Megadja a távoli portot, amely alapján szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="16ec1-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="16ec1-137">Távoli port – Példa: "80" egyetlen port bejegyzéséhez.</span><span class="sxs-lookup"><span data-stu-id="16ec1-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="16ec1-138">"80-85" a tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="16ec1-138">"80-85" for range.</span></span>
<span data-ttu-id="16ec1-139">"80;443;" több bejegyzés esetén.</span><span class="sxs-lookup"><span data-stu-id="16ec1-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="16ec1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ec1-140">CommonParameters</span></span>
<span data-ttu-id="16ec1-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ec1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ec1-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ec1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ec1-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16ec1-143">INPUTS</span></span>

### <span data-ttu-id="16ec1-144">System.String</span><span class="sxs-lookup"><span data-stu-id="16ec1-144">System.String</span></span>

## <span data-ttu-id="16ec1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16ec1-145">OUTPUTS</span></span>

### <span data-ttu-id="16ec1-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="16ec1-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="16ec1-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="16ec1-147">NOTES</span></span>
<span data-ttu-id="16ec1-148">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, figyelő, csomag, rögzítés, forgalom, szűrés</span><span class="sxs-lookup"><span data-stu-id="16ec1-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="16ec1-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16ec1-149">RELATED LINKS</span></span>

[<span data-ttu-id="16ec1-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16ec1-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="16ec1-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16ec1-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="16ec1-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16ec1-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="16ec1-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="16ec1-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="16ec1-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="16ec1-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="16ec1-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="16ec1-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="16ec1-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="16ec1-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="16ec1-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16ec1-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16ec1-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="16ec1-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="16ec1-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16ec1-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16ec1-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16ec1-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16ec1-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16ec1-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16ec1-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="16ec1-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="16ec1-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="16ec1-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="16ec1-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="16ec1-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="16ec1-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16ec1-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="16ec1-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16ec1-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="16ec1-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16ec1-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="16ec1-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="16ec1-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="16ec1-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16ec1-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="16ec1-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16ec1-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="16ec1-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="16ec1-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="16ec1-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="16ec1-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="16ec1-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="16ec1-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="16ec1-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="16ec1-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="16ec1-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="16ec1-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="16ec1-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16ec1-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
