---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 8840fc454601880fd2d4ed8bf7b816f7f3d83e5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012787"
---
# <span data-ttu-id="39b72-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39b72-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="39b72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39b72-102">SYNOPSIS</span></span>
<span data-ttu-id="39b72-103">A kapcsolat figyelésének leállítása</span><span class="sxs-lookup"><span data-stu-id="39b72-103">Stop a connection monitor</span></span>

## <span data-ttu-id="39b72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39b72-104">SYNTAX</span></span>

### <span data-ttu-id="39b72-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39b72-105">SetByName (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39b72-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="39b72-106">SetByResource</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39b72-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="39b72-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39b72-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="39b72-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39b72-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="39b72-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39b72-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="39b72-110">DESCRIPTION</span></span>
<span data-ttu-id="39b72-111">A Stop-AzNetworkWatcherConnectionMonitor parancsmag leállítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="39b72-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="39b72-112">Példák</span><span class="sxs-lookup"><span data-stu-id="39b72-112">EXAMPLES</span></span>

### <span data-ttu-id="39b72-113">Példa 1: a kapcsolat figyelésének leállítása</span><span class="sxs-lookup"><span data-stu-id="39b72-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="39b72-114">Ebben a példában a kapcsolati monitor neve és a Hálózatfigyelő beállítás van megadva</span><span class="sxs-lookup"><span data-stu-id="39b72-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="39b72-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39b72-115">PARAMETERS</span></span>

### <span data-ttu-id="39b72-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39b72-116">-AsJob</span></span>
<span data-ttu-id="39b72-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="39b72-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39b72-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b72-118">-DefaultProfile</span></span>
<span data-ttu-id="39b72-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39b72-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39b72-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39b72-120">-InputObject</span></span>
<span data-ttu-id="39b72-121">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="39b72-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39b72-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="39b72-122">-Location</span></span>
<span data-ttu-id="39b72-123">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="39b72-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="39b72-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39b72-124">-Name</span></span>
<span data-ttu-id="39b72-125">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="39b72-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b72-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39b72-126">-NetworkWatcher</span></span>
<span data-ttu-id="39b72-127">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="39b72-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="39b72-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="39b72-128">-NetworkWatcherName</span></span>
<span data-ttu-id="39b72-129">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="39b72-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b72-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39b72-130">-PassThru</span></span>
<span data-ttu-id="39b72-131">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="39b72-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="39b72-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39b72-132">-ResourceGroupName</span></span>
<span data-ttu-id="39b72-133">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="39b72-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b72-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39b72-134">-ResourceId</span></span>
<span data-ttu-id="39b72-135">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="39b72-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39b72-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39b72-136">-Confirm</span></span>
<span data-ttu-id="39b72-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39b72-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39b72-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39b72-138">-WhatIf</span></span>
<span data-ttu-id="39b72-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39b72-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39b72-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39b72-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39b72-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b72-141">CommonParameters</span></span>
<span data-ttu-id="39b72-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39b72-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b72-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39b72-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b72-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39b72-144">INPUTS</span></span>

### <span data-ttu-id="39b72-145">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39b72-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="39b72-146">System. String</span><span class="sxs-lookup"><span data-stu-id="39b72-146">System.String</span></span>

### <span data-ttu-id="39b72-147">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="39b72-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="39b72-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39b72-148">OUTPUTS</span></span>

### <span data-ttu-id="39b72-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39b72-149">System.Boolean</span></span>

## <span data-ttu-id="39b72-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39b72-150">NOTES</span></span>
<span data-ttu-id="39b72-151">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="39b72-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="39b72-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39b72-152">RELATED LINKS</span></span>

[<span data-ttu-id="39b72-153">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39b72-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="39b72-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39b72-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="39b72-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="39b72-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="39b72-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="39b72-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="39b72-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="39b72-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="39b72-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="39b72-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="39b72-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="39b72-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="39b72-160">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39b72-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39b72-161">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="39b72-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="39b72-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39b72-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39b72-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39b72-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39b72-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="39b72-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="39b72-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39b72-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39b72-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="39b72-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="39b72-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39b72-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39b72-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39b72-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39b72-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39b72-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39b72-170">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39b72-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39b72-171">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="39b72-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="39b72-172">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="39b72-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="39b72-173">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="39b72-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="39b72-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="39b72-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="39b72-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="39b72-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="39b72-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="39b72-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="39b72-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="39b72-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="39b72-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="39b72-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="39b72-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="39b72-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
