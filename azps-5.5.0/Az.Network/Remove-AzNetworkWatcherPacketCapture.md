---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: d6d11590699b52bb7245222ddaa01fbc42938d22
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415478"
---
# <span data-ttu-id="39296-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39296-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="39296-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39296-102">SYNOPSIS</span></span>
<span data-ttu-id="39296-103">Csomagrögzítési erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="39296-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="39296-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39296-104">SYNTAX</span></span>

### <span data-ttu-id="39296-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39296-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39296-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="39296-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39296-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="39296-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39296-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39296-108">DESCRIPTION</span></span>
<span data-ttu-id="39296-109">A Remove-AzNetworkWatcherPacketCapture eltávolítja a csomagrögzítési erőforrást.</span><span class="sxs-lookup"><span data-stu-id="39296-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="39296-110">Javasoljuk, hogy hívja fel Stop-AzNetworkWatcherPacketCapture Remove-AzNetworkWatcherPacketCapture hívást.</span><span class="sxs-lookup"><span data-stu-id="39296-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="39296-111">Ha a csomagrögzítési munkamenet akkor fut, Remove-AzNetworkWatcherPacketCapture a rendszer nem menti a csomagrögzítést.</span><span class="sxs-lookup"><span data-stu-id="39296-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="39296-112">Ha a munkamenet le van állítva az eltávolítás előtt, a rögzítési adatokat tartalmazó .cap fájl nem törlődik.</span><span class="sxs-lookup"><span data-stu-id="39296-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="39296-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39296-113">EXAMPLES</span></span>

### <span data-ttu-id="39296-114">1. példa: Csomagrögzítési munkamenet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="39296-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="39296-115">Ebben a példában eltávolítunk egy "PacketCaptureTest" nevű csomagrögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="39296-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="39296-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39296-116">PARAMETERS</span></span>

### <span data-ttu-id="39296-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39296-117">-AsJob</span></span>
<span data-ttu-id="39296-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="39296-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39296-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39296-119">-DefaultProfile</span></span>
<span data-ttu-id="39296-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39296-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39296-121">-Location</span><span class="sxs-lookup"><span data-stu-id="39296-121">-Location</span></span>
<span data-ttu-id="39296-122">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="39296-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="39296-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39296-123">-NetworkWatcher</span></span>
<span data-ttu-id="39296-124">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="39296-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="39296-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="39296-125">-NetworkWatcherName</span></span>
<span data-ttu-id="39296-126">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="39296-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="39296-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="39296-127">-PacketCaptureName</span></span>
<span data-ttu-id="39296-128">A csomagrögzítés neve.</span><span class="sxs-lookup"><span data-stu-id="39296-128">The packet capture name.</span></span>

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

### <span data-ttu-id="39296-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39296-129">-PassThru</span></span>
<span data-ttu-id="39296-130">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="39296-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="39296-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39296-131">-ResourceGroupName</span></span>
<span data-ttu-id="39296-132">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="39296-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="39296-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39296-133">-Confirm</span></span>
<span data-ttu-id="39296-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="39296-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39296-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39296-135">-WhatIf</span></span>
<span data-ttu-id="39296-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="39296-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39296-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39296-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39296-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39296-138">CommonParameters</span></span>
<span data-ttu-id="39296-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39296-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39296-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39296-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39296-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39296-141">INPUTS</span></span>

### <span data-ttu-id="39296-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39296-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="39296-143">System.String</span><span class="sxs-lookup"><span data-stu-id="39296-143">System.String</span></span>

## <span data-ttu-id="39296-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39296-144">OUTPUTS</span></span>

### <span data-ttu-id="39296-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39296-145">System.Boolean</span></span>

## <span data-ttu-id="39296-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39296-146">NOTES</span></span>
<span data-ttu-id="39296-147">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, csomag, rögzítés, forgalom, eltávolítás</span><span class="sxs-lookup"><span data-stu-id="39296-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="39296-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39296-148">RELATED LINKS</span></span>

[<span data-ttu-id="39296-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39296-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="39296-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39296-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="39296-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39296-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="39296-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="39296-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="39296-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="39296-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="39296-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="39296-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="39296-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="39296-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="39296-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39296-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39296-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="39296-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="39296-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39296-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39296-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39296-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39296-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39296-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39296-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="39296-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="39296-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="39296-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="39296-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="39296-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="39296-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39296-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39296-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39296-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39296-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39296-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39296-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="39296-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="39296-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39296-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39296-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39296-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39296-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="39296-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="39296-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="39296-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="39296-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="39296-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="39296-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="39296-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="39296-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="39296-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="39296-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39296-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
