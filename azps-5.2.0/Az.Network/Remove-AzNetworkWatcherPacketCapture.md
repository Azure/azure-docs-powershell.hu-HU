---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: e22b9d85bbc17897742fa2ac0cbdf3e2d8187d5b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328071"
---
# <span data-ttu-id="b9e2f-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9e2f-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="b9e2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e2f-103">Csomagrögzítési erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="b9e2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b9e2f-104">SYNTAX</span></span>

### <span data-ttu-id="b9e2f-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9e2f-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e2f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b9e2f-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e2f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b9e2f-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e2f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b9e2f-108">DESCRIPTION</span></span>
<span data-ttu-id="b9e2f-109">A Remove-AzNetworkWatcherPacketCapture eltávolítja a csomagrögzítési erőforrást.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="b9e2f-110">Javasoljuk, hogy hívja fel Stop-AzNetworkWatcherPacketCapture Remove-AzNetworkWatcherPacketCapture hívást.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="b9e2f-111">Ha a csomagrögzítési munkamenet akkor fut, Remove-AzNetworkWatcherPacketCapture a rendszer nem menti a csomagrögzítést.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="b9e2f-112">Ha a munkamenet le van állítva a rögzítési adatokat tartalmazó .cap fájl eltávolítása előtt, a rendszer nem távolítja el.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="b9e2f-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b9e2f-113">EXAMPLES</span></span>

### <span data-ttu-id="b9e2f-114">1. példa: Csomagrögzítési munkamenet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b9e2f-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="b9e2f-115">Ebben a példában eltávolítunk egy "PacketCaptureTest" nevű csomagrögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="b9e2f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9e2f-116">PARAMETERS</span></span>

### <span data-ttu-id="b9e2f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9e2f-117">-AsJob</span></span>
<span data-ttu-id="b9e2f-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b9e2f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9e2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e2f-119">-DefaultProfile</span></span>
<span data-ttu-id="b9e2f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9e2f-121">-Location</span><span class="sxs-lookup"><span data-stu-id="b9e2f-121">-Location</span></span>
<span data-ttu-id="b9e2f-122">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b9e2f-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9e2f-123">-NetworkWatcher</span></span>
<span data-ttu-id="b9e2f-124">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="b9e2f-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b9e2f-125">-NetworkWatcherName</span></span>
<span data-ttu-id="b9e2f-126">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="b9e2f-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="b9e2f-127">-PacketCaptureName</span></span>
<span data-ttu-id="b9e2f-128">A csomagrögzítés neve.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-128">The packet capture name.</span></span>

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

### <span data-ttu-id="b9e2f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9e2f-129">-PassThru</span></span>
<span data-ttu-id="b9e2f-130">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="b9e2f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e2f-131">-ResourceGroupName</span></span>
<span data-ttu-id="b9e2f-132">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b9e2f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9e2f-133">-Confirm</span></span>
<span data-ttu-id="b9e2f-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e2f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e2f-135">-WhatIf</span></span>
<span data-ttu-id="b9e2f-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e2f-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e2f-138">CommonParameters</span></span>
<span data-ttu-id="b9e2f-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e2f-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e2f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e2f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9e2f-141">INPUTS</span></span>

### <span data-ttu-id="b9e2f-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9e2f-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b9e2f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b9e2f-143">System.String</span></span>

## <span data-ttu-id="b9e2f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9e2f-144">OUTPUTS</span></span>

### <span data-ttu-id="b9e2f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9e2f-145">System.Boolean</span></span>

## <span data-ttu-id="b9e2f-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b9e2f-146">NOTES</span></span>
<span data-ttu-id="b9e2f-147">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, csomag, rögzítés, forgalom, eltávolítás</span><span class="sxs-lookup"><span data-stu-id="b9e2f-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="b9e2f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9e2f-148">RELATED LINKS</span></span>

[<span data-ttu-id="b9e2f-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9e2f-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b9e2f-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9e2f-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b9e2f-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b9e2f-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b9e2f-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b9e2f-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b9e2f-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b9e2f-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b9e2f-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b9e2f-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b9e2f-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b9e2f-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b9e2f-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9e2f-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9e2f-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b9e2f-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b9e2f-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9e2f-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9e2f-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9e2f-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9e2f-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b9e2f-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b9e2f-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9e2f-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b9e2f-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b9e2f-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b9e2f-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b9e2f-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b9e2f-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9e2f-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9e2f-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9e2f-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9e2f-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9e2f-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9e2f-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b9e2f-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b9e2f-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9e2f-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9e2f-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9e2f-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b9e2f-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b9e2f-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b9e2f-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b9e2f-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b9e2f-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b9e2f-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b9e2f-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b9e2f-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b9e2f-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b9e2f-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b9e2f-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b9e2f-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
