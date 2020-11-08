---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: bb686440cbde0f68659ad77137eae2644f2dcd3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014063"
---
# <span data-ttu-id="0fa05-101">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0fa05-101">Remove-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="0fa05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fa05-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa05-103">A kapcsolat figyelésének megszüntetése</span><span class="sxs-lookup"><span data-stu-id="0fa05-103">Remove connection monitor.</span></span>

## <span data-ttu-id="0fa05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fa05-104">SYNTAX</span></span>

### <span data-ttu-id="0fa05-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0fa05-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0fa05-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0fa05-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fa05-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0fa05-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fa05-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0fa05-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fa05-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="0fa05-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fa05-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fa05-110">DESCRIPTION</span></span>
<span data-ttu-id="0fa05-111">A Remove-AzNetworkWatcherConnectionMonitor parancsmag eltávolítja a megadott kapcsolati monitort.</span><span class="sxs-lookup"><span data-stu-id="0fa05-111">The remove-AzNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="0fa05-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0fa05-112">EXAMPLES</span></span>

### <span data-ttu-id="0fa05-113">1. példa: a megadott kapcsolati monitor eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0fa05-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="0fa05-114">Ebben a példában töröljük a kapcsolat monitor helyét és nevét.</span><span class="sxs-lookup"><span data-stu-id="0fa05-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="0fa05-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fa05-115">PARAMETERS</span></span>

### <span data-ttu-id="0fa05-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fa05-116">-AsJob</span></span>
<span data-ttu-id="0fa05-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0fa05-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fa05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa05-118">-DefaultProfile</span></span>
<span data-ttu-id="0fa05-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fa05-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fa05-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fa05-120">-InputObject</span></span>
<span data-ttu-id="0fa05-121">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="0fa05-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="0fa05-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="0fa05-122">-Location</span></span>
<span data-ttu-id="0fa05-123">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="0fa05-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0fa05-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0fa05-124">-Name</span></span>
<span data-ttu-id="0fa05-125">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="0fa05-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="0fa05-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0fa05-126">-NetworkWatcher</span></span>
<span data-ttu-id="0fa05-127">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="0fa05-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="0fa05-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0fa05-128">-NetworkWatcherName</span></span>
<span data-ttu-id="0fa05-129">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="0fa05-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="0fa05-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fa05-130">-PassThru</span></span>
<span data-ttu-id="0fa05-131">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="0fa05-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="0fa05-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa05-132">-ResourceGroupName</span></span>
<span data-ttu-id="0fa05-133">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0fa05-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0fa05-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fa05-134">-ResourceId</span></span>
<span data-ttu-id="0fa05-135">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0fa05-135">Resource ID.</span></span>

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

### <span data-ttu-id="0fa05-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0fa05-136">-Confirm</span></span>
<span data-ttu-id="0fa05-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fa05-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fa05-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fa05-138">-WhatIf</span></span>
<span data-ttu-id="0fa05-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fa05-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fa05-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fa05-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fa05-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa05-141">CommonParameters</span></span>
<span data-ttu-id="0fa05-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fa05-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa05-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fa05-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa05-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fa05-144">INPUTS</span></span>

### <span data-ttu-id="0fa05-145">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0fa05-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0fa05-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0fa05-146">System.String</span></span>

### <span data-ttu-id="0fa05-147">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="0fa05-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="0fa05-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fa05-148">OUTPUTS</span></span>

### <span data-ttu-id="0fa05-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fa05-149">System.Boolean</span></span>

## <span data-ttu-id="0fa05-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fa05-150">NOTES</span></span>
<span data-ttu-id="0fa05-151">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, kapcsolat figyelője</span><span class="sxs-lookup"><span data-stu-id="0fa05-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="0fa05-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fa05-152">RELATED LINKS</span></span>

[<span data-ttu-id="0fa05-153">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0fa05-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0fa05-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0fa05-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0fa05-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0fa05-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0fa05-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0fa05-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0fa05-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0fa05-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0fa05-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0fa05-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0fa05-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0fa05-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0fa05-160">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0fa05-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0fa05-161">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0fa05-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0fa05-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0fa05-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0fa05-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0fa05-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0fa05-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0fa05-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0fa05-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0fa05-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0fa05-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0fa05-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0fa05-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0fa05-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0fa05-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0fa05-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0fa05-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0fa05-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0fa05-170">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0fa05-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0fa05-171">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fa05-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0fa05-172">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0fa05-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0fa05-173">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0fa05-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0fa05-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0fa05-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0fa05-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0fa05-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0fa05-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0fa05-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0fa05-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0fa05-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0fa05-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0fa05-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0fa05-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0fa05-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
