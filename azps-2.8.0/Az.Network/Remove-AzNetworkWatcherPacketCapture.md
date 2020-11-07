---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: d99b085f5137c9f18d4dda50fce0654954266f37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837841"
---
# <span data-ttu-id="70f30-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70f30-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="70f30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70f30-102">SYNOPSIS</span></span>
<span data-ttu-id="70f30-103">A csomag-rögzítő erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="70f30-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="70f30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70f30-104">SYNTAX</span></span>

### <span data-ttu-id="70f30-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70f30-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f30-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="70f30-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f30-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="70f30-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70f30-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="70f30-108">DESCRIPTION</span></span>
<span data-ttu-id="70f30-109">A Remove-AzNetworkWatcherPacketCapture eltávolítja a csomag-rögzítő erőforrást.</span><span class="sxs-lookup"><span data-stu-id="70f30-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="70f30-110">A Remove-AzNetworkWatcherPacketCapture hívása ajánlott Stop-AzNetworkWatcherPacketCapture hívás előtt.</span><span class="sxs-lookup"><span data-stu-id="70f30-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="70f30-111">Ha a csomag rögzítési munkamenete akkor fut, ha a Remove-AzNetworkWatcherPacketCapture a csomagkapcsolt adatrögzítőt nem lehet menteni.</span><span class="sxs-lookup"><span data-stu-id="70f30-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="70f30-112">Ha a munkamenet megszűnik az Eltávolítás előtt, a program nem távolítja el a rögzítési adatot tartalmazó. Cap fájlt.</span><span class="sxs-lookup"><span data-stu-id="70f30-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="70f30-113">Példák</span><span class="sxs-lookup"><span data-stu-id="70f30-113">EXAMPLES</span></span>

### <span data-ttu-id="70f30-114">1. példa: a csomag rögzítési munkamenetének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="70f30-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="70f30-115">Ebben a példában eltávolítunk egy "PacketCaptureTest" nevű csomag-rögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="70f30-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="70f30-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70f30-116">PARAMETERS</span></span>

### <span data-ttu-id="70f30-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70f30-117">-AsJob</span></span>
<span data-ttu-id="70f30-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="70f30-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70f30-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f30-119">-DefaultProfile</span></span>
<span data-ttu-id="70f30-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70f30-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70f30-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="70f30-121">-Location</span></span>
<span data-ttu-id="70f30-122">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="70f30-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="70f30-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70f30-123">-NetworkWatcher</span></span>
<span data-ttu-id="70f30-124">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="70f30-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="70f30-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="70f30-125">-NetworkWatcherName</span></span>
<span data-ttu-id="70f30-126">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="70f30-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="70f30-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="70f30-127">-PacketCaptureName</span></span>
<span data-ttu-id="70f30-128">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="70f30-128">The packet capture name.</span></span>

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

### <span data-ttu-id="70f30-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70f30-129">-PassThru</span></span>
<span data-ttu-id="70f30-130">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="70f30-130">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f30-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f30-131">-ResourceGroupName</span></span>
<span data-ttu-id="70f30-132">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="70f30-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="70f30-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70f30-133">-Confirm</span></span>
<span data-ttu-id="70f30-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70f30-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f30-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f30-135">-WhatIf</span></span>
<span data-ttu-id="70f30-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70f30-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70f30-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70f30-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70f30-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f30-138">CommonParameters</span></span>
<span data-ttu-id="70f30-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70f30-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f30-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f30-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f30-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70f30-141">INPUTS</span></span>

### <span data-ttu-id="70f30-142">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70f30-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="70f30-143">System. String</span><span class="sxs-lookup"><span data-stu-id="70f30-143">System.String</span></span>

## <span data-ttu-id="70f30-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70f30-144">OUTPUTS</span></span>

### <span data-ttu-id="70f30-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70f30-145">System.Boolean</span></span>

## <span data-ttu-id="70f30-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70f30-146">NOTES</span></span>
<span data-ttu-id="70f30-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom, eltávolítás</span><span class="sxs-lookup"><span data-stu-id="70f30-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="70f30-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70f30-148">RELATED LINKS</span></span>

[<span data-ttu-id="70f30-149">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70f30-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="70f30-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70f30-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="70f30-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="70f30-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="70f30-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="70f30-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="70f30-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="70f30-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="70f30-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="70f30-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="70f30-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="70f30-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="70f30-156">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70f30-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70f30-157">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="70f30-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="70f30-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70f30-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70f30-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70f30-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70f30-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="70f30-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="70f30-161">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="70f30-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="70f30-162">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="70f30-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="70f30-163">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="70f30-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="70f30-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70f30-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70f30-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70f30-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70f30-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70f30-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70f30-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="70f30-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="70f30-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70f30-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70f30-169">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70f30-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="70f30-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="70f30-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="70f30-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="70f30-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="70f30-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="70f30-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="70f30-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="70f30-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="70f30-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="70f30-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="70f30-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="70f30-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
