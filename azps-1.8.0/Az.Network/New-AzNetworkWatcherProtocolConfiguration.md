---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: b7c16c529bb8e3a45d45c31dd985f43f138aee6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670295"
---
# <span data-ttu-id="9b436-101">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b436-101">New-AzNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="9b436-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b436-102">SYNOPSIS</span></span>
<span data-ttu-id="9b436-103">Új protokoll-konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="9b436-103">Creates a new protocol configuration object.</span></span>

## <span data-ttu-id="9b436-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b436-104">SYNTAX</span></span>

```
New-AzNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b436-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b436-105">DESCRIPTION</span></span>
<span data-ttu-id="9b436-106">Az New-AzNetworkWatcherProtocolConfiguration parancsmag új protokoll-konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9b436-106">The New-AzNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="9b436-107">Ezzel az objektummal korlátozhatja a protokoll Confiuration a connecitivity-ellenőrzés során a megadott feltételek teljesülése esetén.</span><span class="sxs-lookup"><span data-stu-id="9b436-107">This object is used to restrict the protocol confiuration during a connecitivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="9b436-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9b436-108">EXAMPLES</span></span>

### <span data-ttu-id="9b436-109">1. példa: a Hálózatfigyelő-kapcsolat tesztelése VM-ről egy olyan webhelyre, amelyen a protokoll konfigurációja van</span><span class="sxs-lookup"><span data-stu-id="9b436-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="9b436-110">Ebben a példában a VM-től az Azure-www.bing.com való kapcsolatot teszteljük.</span><span class="sxs-lookup"><span data-stu-id="9b436-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="9b436-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b436-111">PARAMETERS</span></span>

### <span data-ttu-id="9b436-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b436-112">-DefaultProfile</span></span>
<span data-ttu-id="9b436-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b436-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b436-114">-Header</span><span class="sxs-lookup"><span data-stu-id="9b436-114">-Header</span></span>
<span data-ttu-id="9b436-115">HTTP-fejlécek listája</span><span class="sxs-lookup"><span data-stu-id="9b436-115">list of HTTP headers</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b436-116">-Módszer</span><span class="sxs-lookup"><span data-stu-id="9b436-116">-Method</span></span>
<span data-ttu-id="9b436-117">HTTP-módszer</span><span class="sxs-lookup"><span data-stu-id="9b436-117">HTTP method</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b436-118">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9b436-118">-Protocol</span></span>
<span data-ttu-id="9b436-119">Procotol típusa</span><span class="sxs-lookup"><span data-stu-id="9b436-119">Procotol type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b436-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="9b436-120">-ValidStatusCode</span></span>
<span data-ttu-id="9b436-121">érvényes állapotkódok</span><span class="sxs-lookup"><span data-stu-id="9b436-121">valid status codes</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b436-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b436-122">CommonParameters</span></span>
<span data-ttu-id="9b436-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b436-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b436-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b436-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b436-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b436-125">INPUTS</span></span>

### <span data-ttu-id="9b436-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="9b436-126">None</span></span>

## <span data-ttu-id="9b436-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b436-127">OUTPUTS</span></span>

### <span data-ttu-id="9b436-128">Microsoft. Azure. commands. Network. models. PSNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b436-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="9b436-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b436-129">NOTES</span></span>
<span data-ttu-id="9b436-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, csomag, rögzítés, forgalom, szűrő</span><span class="sxs-lookup"><span data-stu-id="9b436-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="9b436-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b436-131">RELATED LINKS</span></span>

[<span data-ttu-id="9b436-132">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b436-132">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9b436-133">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b436-133">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9b436-134">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b436-134">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9b436-135">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9b436-135">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9b436-136">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9b436-136">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9b436-137">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9b436-137">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9b436-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9b436-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9b436-139">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b436-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b436-140">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9b436-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9b436-141">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b436-141">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b436-142">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b436-142">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b436-143">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b436-143">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9b436-144">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b436-144">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9b436-145">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9b436-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9b436-146">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9b436-146">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9b436-147">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b436-147">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9b436-148">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b436-148">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9b436-149">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b436-149">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9b436-150">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9b436-150">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9b436-151">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b436-151">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9b436-152">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b436-152">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9b436-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9b436-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9b436-154">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9b436-154">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9b436-155">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9b436-155">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9b436-156">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9b436-156">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9b436-157">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9b436-157">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="9b436-158">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b436-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
