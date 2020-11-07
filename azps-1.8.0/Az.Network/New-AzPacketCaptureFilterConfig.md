---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 400b2b87576cf907802e831bc6272cadc5495e58
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670292"
---
# <span data-ttu-id="82913-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="82913-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="82913-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82913-102">SYNOPSIS</span></span>
<span data-ttu-id="82913-103">Új csomagkapcsolt rögzítési szűrő objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="82913-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="82913-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82913-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82913-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82913-105">DESCRIPTION</span></span>
<span data-ttu-id="82913-106">Az New-AzPacketCaptureFilterConfig parancsmag létrehoz egy új csomagkapcsolt rögzítési szűrő objektumot.</span><span class="sxs-lookup"><span data-stu-id="82913-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="82913-107">Ezzel az objektummal korlátozható, hogy milyen típusú csomagokat rögzít a program a csomag rögzítésekor a megadott feltételekkel.</span><span class="sxs-lookup"><span data-stu-id="82913-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="82913-108">A New-AzNetworkWatcherPacketCapture parancsmag több szűrő objektumot is elfogadhat a komponált rögzítési munkamenetek engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="82913-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="82913-109">Példák</span><span class="sxs-lookup"><span data-stu-id="82913-109">EXAMPLES</span></span>

### <span data-ttu-id="82913-110">Példa 1: több szűrőből álló csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="82913-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="82913-111">Ebben a példában a "PacketCaptureTest" nevű csomagot hozzuk létre több szűrővel és időkorlátozással.</span><span class="sxs-lookup"><span data-stu-id="82913-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="82913-112">A munkamenet befejezésekor a program a megadott tárterület-fiókba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="82913-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="82913-113">Megjegyzés: az Azure Network Watcher bővítménynek telepítve kell lennie a cél virtuális gépen a csomag rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="82913-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="82913-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82913-114">PARAMETERS</span></span>

### <span data-ttu-id="82913-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82913-115">-DefaultProfile</span></span>
<span data-ttu-id="82913-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82913-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82913-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="82913-117">-LocalIPAddress</span></span>
<span data-ttu-id="82913-118">A szűrni kívánt helyi IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="82913-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="82913-119">Példa bemenetekre: "127.0.0.1" az egyetlen cím bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="82913-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="82913-120">"127.0.0.1-127.0.0.255" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="82913-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="82913-121">"127.0.0.1; 127.0.0.5;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="82913-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="82913-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="82913-122">-LocalPort</span></span>
<span data-ttu-id="82913-123">A szűrni kívánt helyi IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="82913-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="82913-124">Példa bemenetekre: "127.0.0.1" az egyetlen cím bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="82913-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="82913-125">"127.0.0.1-127.0.0.255" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="82913-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="82913-126">"127.0.0.1; 127.0.0.5;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="82913-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="82913-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="82913-127">-Protocol</span></span>
<span data-ttu-id="82913-128">A szűréshez használandó procotol adja meg.</span><span class="sxs-lookup"><span data-stu-id="82913-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="82913-129">Elfogadható értékek "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="82913-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="82913-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="82913-130">-RemoteIPAddress</span></span>
<span data-ttu-id="82913-131">A szűrni kívánt távoli IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="82913-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="82913-132">Példa bemenetekre: "127.0.0.1" az egyetlen cím bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="82913-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="82913-133">"127.0.0.1-127.0.0.255" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="82913-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="82913-134">"127.0.0.1; 127.0.0.5;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="82913-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="82913-135">-TávoliPORT</span><span class="sxs-lookup"><span data-stu-id="82913-135">-RemotePort</span></span>
<span data-ttu-id="82913-136">A szűrni kívánt távoli portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="82913-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="82913-137">Távoli port – például bemenetek: "80" egy portos bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="82913-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="82913-138">"80-85" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="82913-138">"80-85" for range.</span></span>
<span data-ttu-id="82913-139">"80; 443;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="82913-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="82913-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82913-140">CommonParameters</span></span>
<span data-ttu-id="82913-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82913-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82913-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82913-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82913-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82913-143">INPUTS</span></span>

### <span data-ttu-id="82913-144">System. String</span><span class="sxs-lookup"><span data-stu-id="82913-144">System.String</span></span>

## <span data-ttu-id="82913-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82913-145">OUTPUTS</span></span>

### <span data-ttu-id="82913-146">Microsoft. Azure. commands. Network. models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="82913-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="82913-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82913-147">NOTES</span></span>
<span data-ttu-id="82913-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, csomag, rögzítés, forgalom, szűrő</span><span class="sxs-lookup"><span data-stu-id="82913-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="82913-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82913-149">RELATED LINKS</span></span>

[<span data-ttu-id="82913-150">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82913-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="82913-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82913-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="82913-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82913-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="82913-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="82913-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="82913-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="82913-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="82913-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="82913-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="82913-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="82913-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="82913-157">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82913-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82913-158">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="82913-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="82913-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82913-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82913-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82913-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82913-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82913-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82913-162">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="82913-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="82913-163">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="82913-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="82913-164">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="82913-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="82913-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82913-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="82913-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82913-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="82913-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82913-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="82913-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="82913-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="82913-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82913-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="82913-170">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82913-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="82913-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="82913-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="82913-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="82913-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="82913-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="82913-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="82913-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="82913-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="82913-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="82913-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="82913-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82913-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)