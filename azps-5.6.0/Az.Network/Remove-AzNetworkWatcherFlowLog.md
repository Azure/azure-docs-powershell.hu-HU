---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 292a916794184edb8100d38feaa0fe23536d8a0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940050"
---
# <span data-ttu-id="adc91-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="adc91-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="adc91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc91-102">SYNOPSIS</span></span>
<span data-ttu-id="adc91-103">Törli a megadott folyamatnapló-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="adc91-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="adc91-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="adc91-104">SYNTAX</span></span>

### <span data-ttu-id="adc91-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="adc91-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adc91-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="adc91-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adc91-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="adc91-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adc91-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="adc91-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adc91-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="adc91-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adc91-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="adc91-110">DESCRIPTION</span></span>
<span data-ttu-id="adc91-111">Törli a megadott folyamatnapló-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="adc91-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="adc91-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="adc91-112">EXAMPLES</span></span>

### <span data-ttu-id="adc91-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="adc91-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="adc91-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adc91-114">PARAMETERS</span></span>

### <span data-ttu-id="adc91-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="adc91-115">-AsJob</span></span>
<span data-ttu-id="adc91-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="adc91-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="adc91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc91-117">-DefaultProfile</span></span>
<span data-ttu-id="adc91-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adc91-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adc91-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adc91-119">-InputObject</span></span>
<span data-ttu-id="adc91-120">Folyamatnapló objektum.</span><span class="sxs-lookup"><span data-stu-id="adc91-120">Flow log object.</span></span>

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

### <span data-ttu-id="adc91-121">-Location</span><span class="sxs-lookup"><span data-stu-id="adc91-121">-Location</span></span>
<span data-ttu-id="adc91-122">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="adc91-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="adc91-123">-Name</span><span class="sxs-lookup"><span data-stu-id="adc91-123">-Name</span></span>
<span data-ttu-id="adc91-124">A folyamatnapló neve.</span><span class="sxs-lookup"><span data-stu-id="adc91-124">The flow log name.</span></span>

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

### <span data-ttu-id="adc91-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="adc91-125">-NetworkWatcher</span></span>
<span data-ttu-id="adc91-126">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="adc91-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="adc91-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="adc91-127">-NetworkWatcherName</span></span>
<span data-ttu-id="adc91-128">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="adc91-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="adc91-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adc91-129">-PassThru</span></span>
<span data-ttu-id="adc91-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="adc91-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="adc91-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc91-131">-ResourceGroupName</span></span>
<span data-ttu-id="adc91-132">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="adc91-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="adc91-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adc91-133">-ResourceId</span></span>
<span data-ttu-id="adc91-134">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="adc91-134">Resource ID.</span></span>

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

### <span data-ttu-id="adc91-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adc91-135">-Confirm</span></span>
<span data-ttu-id="adc91-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="adc91-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adc91-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc91-137">-WhatIf</span></span>
<span data-ttu-id="adc91-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="adc91-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adc91-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="adc91-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adc91-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc91-140">CommonParameters</span></span>
<span data-ttu-id="adc91-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc91-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc91-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adc91-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc91-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adc91-143">INPUTS</span></span>

### <span data-ttu-id="adc91-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="adc91-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="adc91-145">System.String</span><span class="sxs-lookup"><span data-stu-id="adc91-145">System.String</span></span>

### <span data-ttu-id="adc91-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="adc91-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="adc91-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adc91-147">OUTPUTS</span></span>

### <span data-ttu-id="adc91-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="adc91-148">System.Boolean</span></span>

## <span data-ttu-id="adc91-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="adc91-149">NOTES</span></span>

## <span data-ttu-id="adc91-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adc91-150">RELATED LINKS</span></span>

[<span data-ttu-id="adc91-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="adc91-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="adc91-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="adc91-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="adc91-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="adc91-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="adc91-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="adc91-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="adc91-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="adc91-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="adc91-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="adc91-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="adc91-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="adc91-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="adc91-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="adc91-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="adc91-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="adc91-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="adc91-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="adc91-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="adc91-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="adc91-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="adc91-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="adc91-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="adc91-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="adc91-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="adc91-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="adc91-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="adc91-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="adc91-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="adc91-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="adc91-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="adc91-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="adc91-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="adc91-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="adc91-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="adc91-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="adc91-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="adc91-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="adc91-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="adc91-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="adc91-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="adc91-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="adc91-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="adc91-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="adc91-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="adc91-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="adc91-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="adc91-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="adc91-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="adc91-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="adc91-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="adc91-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="adc91-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="adc91-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="adc91-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="adc91-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="adc91-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="adc91-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="adc91-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)
