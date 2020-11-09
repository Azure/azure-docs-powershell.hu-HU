---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 922026b14531cc1c65f60901914383b402d06889
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303518"
---
# <span data-ttu-id="0ef97-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0ef97-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="0ef97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ef97-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef97-103">Futó csomag rögzítési munkamenetének leállítása</span><span class="sxs-lookup"><span data-stu-id="0ef97-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="0ef97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ef97-104">SYNTAX</span></span>

### <span data-ttu-id="0ef97-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ef97-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ef97-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0ef97-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ef97-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0ef97-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ef97-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ef97-108">DESCRIPTION</span></span>
<span data-ttu-id="0ef97-109">A Stop-AzNetworkWatcherPacketCapture leállítja a futtatott csomag rögzítési munkamenetét.</span><span class="sxs-lookup"><span data-stu-id="0ef97-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="0ef97-110">Miután leállította a munkamenetet, a csomag rögzítésére szolgáló fájlt feltölti a rendszer, és a rendszer a VM-re menti a számítógépen, a konfigurációtól függően.</span><span class="sxs-lookup"><span data-stu-id="0ef97-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="0ef97-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0ef97-111">EXAMPLES</span></span>

### <span data-ttu-id="0ef97-112">Példa 1: a csomag rögzítési munkamenetének leállítása</span><span class="sxs-lookup"><span data-stu-id="0ef97-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="0ef97-113">Ebben a példában leállítjuk az "PacketCaptureTest" nevű futó csomag-rögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="0ef97-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="0ef97-114">Miután leállította a munkamenetet, a csomag rögzítésére szolgáló fájlt feltölti a rendszer, és a rendszer a VM-re menti a számítógépen, a konfigurációtól függően.</span><span class="sxs-lookup"><span data-stu-id="0ef97-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="0ef97-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ef97-115">PARAMETERS</span></span>

### <span data-ttu-id="0ef97-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ef97-116">-AsJob</span></span>
<span data-ttu-id="0ef97-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0ef97-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ef97-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef97-118">-DefaultProfile</span></span>
<span data-ttu-id="0ef97-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ef97-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ef97-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="0ef97-120">-Location</span></span>
<span data-ttu-id="0ef97-121">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="0ef97-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0ef97-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0ef97-122">-NetworkWatcher</span></span>
<span data-ttu-id="0ef97-123">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="0ef97-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="0ef97-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0ef97-124">-NetworkWatcherName</span></span>
<span data-ttu-id="0ef97-125">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="0ef97-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="0ef97-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="0ef97-126">-PacketCaptureName</span></span>
<span data-ttu-id="0ef97-127">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="0ef97-127">The packet capture name.</span></span>

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

### <span data-ttu-id="0ef97-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ef97-128">-PassThru</span></span>
<span data-ttu-id="0ef97-129">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0ef97-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="0ef97-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef97-130">-ResourceGroupName</span></span>
<span data-ttu-id="0ef97-131">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0ef97-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0ef97-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ef97-132">-Confirm</span></span>
<span data-ttu-id="0ef97-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ef97-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ef97-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef97-134">-WhatIf</span></span>
<span data-ttu-id="0ef97-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ef97-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ef97-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ef97-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ef97-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef97-137">CommonParameters</span></span>
<span data-ttu-id="0ef97-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ef97-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef97-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ef97-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef97-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ef97-140">INPUTS</span></span>

### <span data-ttu-id="0ef97-141">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0ef97-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0ef97-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0ef97-142">System.String</span></span>

## <span data-ttu-id="0ef97-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ef97-143">OUTPUTS</span></span>

### <span data-ttu-id="0ef97-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ef97-144">System.Boolean</span></span>

## <span data-ttu-id="0ef97-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ef97-145">NOTES</span></span>
<span data-ttu-id="0ef97-146">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="0ef97-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="0ef97-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ef97-147">RELATED LINKS</span></span>

[<span data-ttu-id="0ef97-148">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0ef97-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0ef97-149">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0ef97-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0ef97-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0ef97-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0ef97-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0ef97-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0ef97-152">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0ef97-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0ef97-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0ef97-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0ef97-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0ef97-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0ef97-155">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0ef97-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0ef97-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0ef97-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0ef97-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0ef97-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0ef97-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0ef97-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0ef97-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0ef97-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0ef97-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0ef97-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0ef97-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0ef97-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0ef97-162">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ef97-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0ef97-163">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0ef97-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0ef97-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0ef97-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0ef97-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0ef97-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0ef97-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0ef97-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0ef97-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0ef97-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0ef97-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0ef97-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0ef97-169">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0ef97-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0ef97-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0ef97-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0ef97-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0ef97-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0ef97-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0ef97-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0ef97-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0ef97-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0ef97-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0ef97-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
