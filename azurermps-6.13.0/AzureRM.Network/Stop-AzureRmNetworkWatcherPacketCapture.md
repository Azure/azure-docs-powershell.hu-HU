---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: fc78481ceeec796fe4a498bf76092955adb1639a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498271"
---
# <span data-ttu-id="7608c-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7608c-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="7608c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7608c-102">SYNOPSIS</span></span>
<span data-ttu-id="7608c-103">Futó csomag rögzítési munkamenetének leállítása</span><span class="sxs-lookup"><span data-stu-id="7608c-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7608c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7608c-104">SYNTAX</span></span>

### <span data-ttu-id="7608c-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7608c-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7608c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7608c-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7608c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7608c-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7608c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7608c-108">DESCRIPTION</span></span>
<span data-ttu-id="7608c-109">A Stop-AzureRmNetworkWatcherPacketCapture leállítja a futtatott csomag rögzítési munkamenetét.</span><span class="sxs-lookup"><span data-stu-id="7608c-109">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="7608c-110">Miután leállította a munkamenetet, a csomag rögzítésére szolgáló fájlt feltölti a rendszer, és a rendszer a VM-re menti a számítógépen, a konfigurációtól függően.</span><span class="sxs-lookup"><span data-stu-id="7608c-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="7608c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7608c-111">EXAMPLES</span></span>

### <span data-ttu-id="7608c-112">Példa 1: a csomag rögzítési munkamenetének leállítása</span><span class="sxs-lookup"><span data-stu-id="7608c-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="7608c-113">Ebben a példában leállítjuk az "PacketCaptureTest" nevű futó csomag-rögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="7608c-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="7608c-114">Miután leállította a munkamenetet, a csomag rögzítésére szolgáló fájlt feltölti a rendszer, és a rendszer a VM-re menti a számítógépen, a konfigurációtól függően.</span><span class="sxs-lookup"><span data-stu-id="7608c-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="7608c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7608c-115">PARAMETERS</span></span>

### <span data-ttu-id="7608c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7608c-116">-AsJob</span></span>
<span data-ttu-id="7608c-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7608c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7608c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7608c-118">-DefaultProfile</span></span>
<span data-ttu-id="7608c-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7608c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7608c-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="7608c-120">-Location</span></span>
<span data-ttu-id="7608c-121">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="7608c-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7608c-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7608c-122">-NetworkWatcher</span></span>
<span data-ttu-id="7608c-123">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="7608c-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="7608c-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7608c-124">-NetworkWatcherName</span></span>
<span data-ttu-id="7608c-125">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="7608c-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="7608c-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="7608c-126">-PacketCaptureName</span></span>
<span data-ttu-id="7608c-127">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="7608c-127">The packet capture name.</span></span>

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

### <span data-ttu-id="7608c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7608c-128">-PassThru</span></span>
<span data-ttu-id="7608c-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7608c-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7608c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7608c-130">-ResourceGroupName</span></span>
<span data-ttu-id="7608c-131">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7608c-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7608c-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7608c-132">-Confirm</span></span>
<span data-ttu-id="7608c-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7608c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7608c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7608c-134">-WhatIf</span></span>
<span data-ttu-id="7608c-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7608c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7608c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7608c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7608c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7608c-137">CommonParameters</span></span>
<span data-ttu-id="7608c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7608c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7608c-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7608c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7608c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7608c-140">INPUTS</span></span>

### <span data-ttu-id="7608c-141">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7608c-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7608c-142">Paraméterek: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7608c-142">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="7608c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7608c-143">System.String</span></span>
<span data-ttu-id="7608c-144">Paraméterek: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7608c-144">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="7608c-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7608c-145">OUTPUTS</span></span>

### <span data-ttu-id="7608c-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7608c-146">System.Boolean</span></span>

## <span data-ttu-id="7608c-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7608c-147">NOTES</span></span>
<span data-ttu-id="7608c-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="7608c-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="7608c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7608c-149">RELATED LINKS</span></span>

[<span data-ttu-id="7608c-150">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7608c-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7608c-151">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7608c-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7608c-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7608c-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7608c-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7608c-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7608c-154">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7608c-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7608c-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7608c-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7608c-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7608c-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7608c-157">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7608c-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7608c-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7608c-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7608c-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7608c-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7608c-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7608c-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7608c-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7608c-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7608c-162">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7608c-162">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7608c-163">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7608c-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7608c-164">Új – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7608c-164">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7608c-165">Teszt-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7608c-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="7608c-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7608c-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7608c-167">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7608c-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7608c-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7608c-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7608c-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7608c-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7608c-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7608c-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7608c-171">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7608c-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7608c-172">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7608c-172">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7608c-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7608c-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7608c-174">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7608c-174">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7608c-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7608c-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="7608c-176">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7608c-176">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
