---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c4e70253a42fc577ba283919fb3ab2eeb9701c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838294"
---
# <span data-ttu-id="ca635-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ca635-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="ca635-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca635-102">SYNOPSIS</span></span>
<span data-ttu-id="ca635-103">Kapcsolati monitor indítása</span><span class="sxs-lookup"><span data-stu-id="ca635-103">Start a connection monitor</span></span>

## <span data-ttu-id="ca635-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca635-104">SYNTAX</span></span>

### <span data-ttu-id="ca635-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca635-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca635-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ca635-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca635-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ca635-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca635-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ca635-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca635-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="ca635-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca635-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca635-110">DESCRIPTION</span></span>
<span data-ttu-id="ca635-111">A Start-AzNetworkWatcherConnectionMonitor parancsmag elindítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="ca635-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="ca635-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ca635-112">EXAMPLES</span></span>

### <span data-ttu-id="ca635-113">1. példa: egy kapcsolat monitorjának indítása</span><span class="sxs-lookup"><span data-stu-id="ca635-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="ca635-114">Ebben a példában a kapcsolat monitort a név és a Hálózatfigyelő paranccsal indíthatja el.</span><span class="sxs-lookup"><span data-stu-id="ca635-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="ca635-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca635-115">PARAMETERS</span></span>

### <span data-ttu-id="ca635-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca635-116">-AsJob</span></span>
<span data-ttu-id="ca635-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ca635-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca635-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca635-118">-DefaultProfile</span></span>
<span data-ttu-id="ca635-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca635-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca635-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca635-120">-InputObject</span></span>
<span data-ttu-id="ca635-121">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="ca635-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="ca635-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="ca635-122">-Location</span></span>
<span data-ttu-id="ca635-123">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="ca635-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ca635-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca635-124">-Name</span></span>
<span data-ttu-id="ca635-125">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="ca635-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="ca635-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ca635-126">-NetworkWatcher</span></span>
<span data-ttu-id="ca635-127">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ca635-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="ca635-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ca635-128">-NetworkWatcherName</span></span>
<span data-ttu-id="ca635-129">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="ca635-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="ca635-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca635-130">-PassThru</span></span>
<span data-ttu-id="ca635-131">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ca635-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="ca635-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca635-132">-ResourceGroupName</span></span>
<span data-ttu-id="ca635-133">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ca635-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ca635-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca635-134">-ResourceId</span></span>
<span data-ttu-id="ca635-135">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ca635-135">Resource ID.</span></span>

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

### <span data-ttu-id="ca635-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca635-136">-Confirm</span></span>
<span data-ttu-id="ca635-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca635-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca635-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca635-138">-WhatIf</span></span>
<span data-ttu-id="ca635-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca635-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca635-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca635-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca635-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca635-141">CommonParameters</span></span>
<span data-ttu-id="ca635-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca635-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca635-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca635-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca635-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca635-144">INPUTS</span></span>

### <span data-ttu-id="ca635-145">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ca635-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ca635-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ca635-146">System.String</span></span>

### <span data-ttu-id="ca635-147">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="ca635-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="ca635-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca635-148">OUTPUTS</span></span>

### <span data-ttu-id="ca635-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca635-149">System.Boolean</span></span>

## <span data-ttu-id="ca635-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca635-150">NOTES</span></span>
<span data-ttu-id="ca635-151">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="ca635-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="ca635-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca635-152">RELATED LINKS</span></span>

[<span data-ttu-id="ca635-153">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ca635-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ca635-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ca635-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ca635-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ca635-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ca635-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ca635-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ca635-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ca635-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ca635-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ca635-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ca635-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ca635-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ca635-160">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ca635-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ca635-161">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ca635-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ca635-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ca635-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ca635-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ca635-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ca635-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ca635-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ca635-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ca635-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ca635-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ca635-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="ca635-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ca635-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ca635-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ca635-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ca635-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ca635-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ca635-170">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ca635-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ca635-171">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca635-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ca635-172">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ca635-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ca635-173">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ca635-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ca635-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ca635-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ca635-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ca635-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ca635-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ca635-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ca635-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ca635-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ca635-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ca635-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ca635-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ca635-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
