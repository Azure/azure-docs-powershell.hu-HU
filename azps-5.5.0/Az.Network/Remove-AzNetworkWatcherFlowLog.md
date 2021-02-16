---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5c8532502e4e74b94a9d0c1e252c8d1cea9ddad8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411228"
---
# <span data-ttu-id="03685-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="03685-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="03685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03685-102">SYNOPSIS</span></span>
<span data-ttu-id="03685-103">Törli a megadott folyamatnapló-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="03685-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="03685-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03685-104">SYNTAX</span></span>

### <span data-ttu-id="03685-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03685-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03685-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="03685-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03685-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="03685-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03685-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="03685-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03685-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="03685-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03685-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03685-110">DESCRIPTION</span></span>
<span data-ttu-id="03685-111">Törli a megadott folyamatnapló-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="03685-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="03685-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03685-112">EXAMPLES</span></span>

### <span data-ttu-id="03685-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="03685-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="03685-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03685-114">PARAMETERS</span></span>

### <span data-ttu-id="03685-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03685-115">-AsJob</span></span>
<span data-ttu-id="03685-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="03685-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03685-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03685-117">-DefaultProfile</span></span>
<span data-ttu-id="03685-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03685-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03685-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03685-119">-InputObject</span></span>
<span data-ttu-id="03685-120">Folyamatnapló-objektum.</span><span class="sxs-lookup"><span data-stu-id="03685-120">Flow log object.</span></span>

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

### <span data-ttu-id="03685-121">-Location</span><span class="sxs-lookup"><span data-stu-id="03685-121">-Location</span></span>
<span data-ttu-id="03685-122">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="03685-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="03685-123">-Name</span><span class="sxs-lookup"><span data-stu-id="03685-123">-Name</span></span>
<span data-ttu-id="03685-124">A folyamatnapló neve.</span><span class="sxs-lookup"><span data-stu-id="03685-124">The flow log name.</span></span>

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

### <span data-ttu-id="03685-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03685-125">-NetworkWatcher</span></span>
<span data-ttu-id="03685-126">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="03685-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="03685-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="03685-127">-NetworkWatcherName</span></span>
<span data-ttu-id="03685-128">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="03685-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="03685-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03685-129">-PassThru</span></span>
<span data-ttu-id="03685-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="03685-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="03685-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03685-131">-ResourceGroupName</span></span>
<span data-ttu-id="03685-132">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03685-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="03685-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03685-133">-ResourceId</span></span>
<span data-ttu-id="03685-134">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="03685-134">Resource ID.</span></span>

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

### <span data-ttu-id="03685-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03685-135">-Confirm</span></span>
<span data-ttu-id="03685-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03685-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03685-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03685-137">-WhatIf</span></span>
<span data-ttu-id="03685-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03685-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03685-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03685-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03685-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03685-140">CommonParameters</span></span>
<span data-ttu-id="03685-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03685-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03685-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03685-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03685-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03685-143">INPUTS</span></span>

### <span data-ttu-id="03685-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03685-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="03685-145">System.String</span><span class="sxs-lookup"><span data-stu-id="03685-145">System.String</span></span>

### <span data-ttu-id="03685-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="03685-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="03685-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03685-147">OUTPUTS</span></span>

### <span data-ttu-id="03685-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03685-148">System.Boolean</span></span>

## <span data-ttu-id="03685-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03685-149">NOTES</span></span>

## <span data-ttu-id="03685-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03685-150">RELATED LINKS</span></span>

[<span data-ttu-id="03685-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03685-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="03685-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03685-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="03685-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03685-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="03685-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="03685-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="03685-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="03685-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="03685-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="03685-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="03685-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="03685-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="03685-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03685-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03685-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="03685-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="03685-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03685-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03685-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03685-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03685-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03685-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03685-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="03685-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="03685-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="03685-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="03685-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="03685-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="03685-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03685-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03685-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03685-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03685-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03685-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03685-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="03685-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="03685-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03685-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03685-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03685-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03685-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="03685-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="03685-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="03685-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="03685-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="03685-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="03685-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="03685-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="03685-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="03685-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="03685-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03685-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03685-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="03685-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="03685-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="03685-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="03685-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="03685-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)
