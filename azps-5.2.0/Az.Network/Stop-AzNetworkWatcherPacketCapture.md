---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 922026b14531cc1c65f60901914383b402d06889
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363451"
---
# <span data-ttu-id="49f3d-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49f3d-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="49f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="49f3d-103">A futó csomagrögzítési munkamenet leállítja</span><span class="sxs-lookup"><span data-stu-id="49f3d-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="49f3d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49f3d-104">SYNTAX</span></span>

### <span data-ttu-id="49f3d-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49f3d-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f3d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="49f3d-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49f3d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="49f3d-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49f3d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49f3d-108">DESCRIPTION</span></span>
<span data-ttu-id="49f3d-109">A Stop-AzNetworkWatcherPacketCapture leállít egy futó csomagrögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="49f3d-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="49f3d-110">Miután leállt a munkamenet, a csomagrögzítő fájl feltöltődik a tárhelyre, és/vagy helyileg menti a virtuális gépre a konfigurációtól függően.</span><span class="sxs-lookup"><span data-stu-id="49f3d-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="49f3d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49f3d-111">EXAMPLES</span></span>

### <span data-ttu-id="49f3d-112">1. példa: Csomagrögzítési munkamenet befejezése</span><span class="sxs-lookup"><span data-stu-id="49f3d-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="49f3d-113">Ebben a példában leállítunk egy "PacketCaptureTest" nevű csomagrögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="49f3d-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="49f3d-114">Miután leállt a munkamenet, a csomagrögzítő fájl feltöltődik a tárhelyre, és/vagy helyileg menti a virtuális gépre a konfigurációtól függően.</span><span class="sxs-lookup"><span data-stu-id="49f3d-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="49f3d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49f3d-115">PARAMETERS</span></span>

### <span data-ttu-id="49f3d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49f3d-116">-AsJob</span></span>
<span data-ttu-id="49f3d-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="49f3d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49f3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f3d-118">-DefaultProfile</span></span>
<span data-ttu-id="49f3d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49f3d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49f3d-120">-Location</span><span class="sxs-lookup"><span data-stu-id="49f3d-120">-Location</span></span>
<span data-ttu-id="49f3d-121">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="49f3d-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="49f3d-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49f3d-122">-NetworkWatcher</span></span>
<span data-ttu-id="49f3d-123">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="49f3d-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="49f3d-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="49f3d-124">-NetworkWatcherName</span></span>
<span data-ttu-id="49f3d-125">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="49f3d-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="49f3d-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="49f3d-126">-PacketCaptureName</span></span>
<span data-ttu-id="49f3d-127">A csomagrögzítés neve.</span><span class="sxs-lookup"><span data-stu-id="49f3d-127">The packet capture name.</span></span>

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

### <span data-ttu-id="49f3d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49f3d-128">-PassThru</span></span>
<span data-ttu-id="49f3d-129">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="49f3d-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="49f3d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f3d-130">-ResourceGroupName</span></span>
<span data-ttu-id="49f3d-131">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="49f3d-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="49f3d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49f3d-132">-Confirm</span></span>
<span data-ttu-id="49f3d-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="49f3d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49f3d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f3d-134">-WhatIf</span></span>
<span data-ttu-id="49f3d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="49f3d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49f3d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49f3d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49f3d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f3d-137">CommonParameters</span></span>
<span data-ttu-id="49f3d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f3d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f3d-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f3d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f3d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49f3d-140">INPUTS</span></span>

### <span data-ttu-id="49f3d-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49f3d-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="49f3d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="49f3d-142">System.String</span></span>

## <span data-ttu-id="49f3d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49f3d-143">OUTPUTS</span></span>

### <span data-ttu-id="49f3d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49f3d-144">System.Boolean</span></span>

## <span data-ttu-id="49f3d-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49f3d-145">NOTES</span></span>
<span data-ttu-id="49f3d-146">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="49f3d-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="49f3d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49f3d-147">RELATED LINKS</span></span>

[<span data-ttu-id="49f3d-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49f3d-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49f3d-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="49f3d-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="49f3d-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49f3d-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49f3d-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49f3d-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49f3d-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49f3d-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="49f3d-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49f3d-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="49f3d-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49f3d-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="49f3d-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="49f3d-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="49f3d-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="49f3d-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="49f3d-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="49f3d-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="49f3d-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="49f3d-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="49f3d-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="49f3d-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="49f3d-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="49f3d-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="49f3d-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49f3d-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49f3d-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="49f3d-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="49f3d-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="49f3d-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="49f3d-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49f3d-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49f3d-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49f3d-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49f3d-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49f3d-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49f3d-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="49f3d-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="49f3d-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49f3d-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49f3d-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49f3d-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49f3d-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="49f3d-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="49f3d-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="49f3d-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="49f3d-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="49f3d-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="49f3d-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="49f3d-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="49f3d-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49f3d-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
