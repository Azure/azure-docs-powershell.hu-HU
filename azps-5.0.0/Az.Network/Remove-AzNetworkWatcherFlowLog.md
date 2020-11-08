---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 9906af7da12f76650ebbe45ff764da78c90ef340
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185957"
---
# <span data-ttu-id="1af4f-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="1af4f-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="1af4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1af4f-102">SYNOPSIS</span></span>
<span data-ttu-id="1af4f-103">Törli a megadott folyamatábra-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="1af4f-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="1af4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1af4f-104">SYNTAX</span></span>

### <span data-ttu-id="1af4f-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1af4f-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af4f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1af4f-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af4f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1af4f-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af4f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1af4f-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af4f-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="1af4f-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1af4f-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="1af4f-110">DESCRIPTION</span></span>
<span data-ttu-id="1af4f-111">Törli a megadott folyamatábra-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="1af4f-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="1af4f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="1af4f-112">EXAMPLES</span></span>

### <span data-ttu-id="1af4f-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1af4f-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="1af4f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1af4f-114">PARAMETERS</span></span>

### <span data-ttu-id="1af4f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1af4f-115">-AsJob</span></span>
<span data-ttu-id="1af4f-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1af4f-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af4f-117">-DefaultProfile</span></span>
<span data-ttu-id="1af4f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1af4f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1af4f-119">-InputObject</span></span>
<span data-ttu-id="1af4f-120">Flow log objektum.</span><span class="sxs-lookup"><span data-stu-id="1af4f-120">Flow log object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="1af4f-121">-Location</span></span>
<span data-ttu-id="1af4f-122">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="1af4f-122">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1af4f-123">-Name</span></span>
<span data-ttu-id="1af4f-124">A folyamatábra neve.</span><span class="sxs-lookup"><span data-stu-id="1af4f-124">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1af4f-125">-NetworkWatcher</span></span>
<span data-ttu-id="1af4f-126">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="1af4f-126">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1af4f-127">-NetworkWatcherName</span></span>
<span data-ttu-id="1af4f-128">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="1af4f-128">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1af4f-129">-PassThru</span></span>
<span data-ttu-id="1af4f-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1af4f-130">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af4f-131">-ResourceGroupName</span></span>
<span data-ttu-id="1af4f-132">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1af4f-132">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af4f-133">-ResourceId</span></span>
<span data-ttu-id="1af4f-134">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="1af4f-134">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1af4f-135">-Confirm</span></span>
<span data-ttu-id="1af4f-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1af4f-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af4f-137">-WhatIf</span></span>
<span data-ttu-id="1af4f-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1af4f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af4f-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1af4f-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1af4f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af4f-140">CommonParameters</span></span>
<span data-ttu-id="1af4f-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1af4f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af4f-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1af4f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af4f-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1af4f-143">INPUTS</span></span>

### <span data-ttu-id="1af4f-144">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1af4f-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1af4f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="1af4f-145">System.String</span></span>

### <span data-ttu-id="1af4f-146">Microsoft. Azure. commands. Network. models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="1af4f-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="1af4f-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1af4f-147">OUTPUTS</span></span>

### <span data-ttu-id="1af4f-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1af4f-148">System.Boolean</span></span>

## <span data-ttu-id="1af4f-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1af4f-149">NOTES</span></span>

## <span data-ttu-id="1af4f-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1af4f-150">RELATED LINKS</span></span>

[<span data-ttu-id="1af4f-151">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1af4f-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1af4f-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1af4f-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1af4f-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1af4f-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1af4f-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1af4f-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1af4f-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1af4f-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1af4f-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1af4f-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1af4f-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1af4f-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1af4f-158">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1af4f-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1af4f-159">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1af4f-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1af4f-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1af4f-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1af4f-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1af4f-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1af4f-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1af4f-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1af4f-163">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1af4f-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1af4f-164">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1af4f-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1af4f-165">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1af4f-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1af4f-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1af4f-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1af4f-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1af4f-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1af4f-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1af4f-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1af4f-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1af4f-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1af4f-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1af4f-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1af4f-171">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1af4f-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1af4f-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1af4f-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1af4f-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1af4f-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1af4f-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1af4f-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1af4f-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1af4f-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1af4f-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1af4f-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1af4f-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1af4f-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="1af4f-178">Új – AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="1af4f-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="1af4f-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="1af4f-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="1af4f-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="1af4f-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)
