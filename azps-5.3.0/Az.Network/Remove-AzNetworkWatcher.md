---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479956"
---
# <span data-ttu-id="e3989-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3989-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="e3989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3989-102">SYNOPSIS</span></span>
<span data-ttu-id="e3989-103">Eltávolítja a hálózati figyelőt.</span><span class="sxs-lookup"><span data-stu-id="e3989-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="e3989-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3989-104">SYNTAX</span></span>

### <span data-ttu-id="e3989-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e3989-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3989-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e3989-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3989-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e3989-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3989-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3989-108">DESCRIPTION</span></span>
<span data-ttu-id="e3989-109">A Remove-AzNetworkWatcher parancsmag eltávolítja a Hálózati figyelő erőforrást.</span><span class="sxs-lookup"><span data-stu-id="e3989-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="e3989-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3989-110">EXAMPLES</span></span>

### <span data-ttu-id="e3989-111">1. példa: Hálózati figyelő létrehozása és törlése</span><span class="sxs-lookup"><span data-stu-id="e3989-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="e3989-112">Ebben a példában egy hálózati figyelőt hoz létre egy erőforráscsoportban, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="e3989-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e3989-113">Felhívjuk a figyelmét arra, hogy előfizetésenként régiónként csak egy Hálózati figyelőt lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="e3989-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="e3989-114">A -Force jelölővel elrejtheti a parancssort a virtuális hálózat törlésekor.</span><span class="sxs-lookup"><span data-stu-id="e3989-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="e3989-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3989-115">PARAMETERS</span></span>

### <span data-ttu-id="e3989-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3989-116">-AsJob</span></span>
<span data-ttu-id="e3989-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e3989-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3989-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3989-118">-DefaultProfile</span></span>
<span data-ttu-id="e3989-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3989-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3989-120">-Location</span><span class="sxs-lookup"><span data-stu-id="e3989-120">-Location</span></span>
<span data-ttu-id="e3989-121">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="e3989-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e3989-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e3989-122">-Name</span></span>
<span data-ttu-id="e3989-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e3989-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3989-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3989-124">-NetworkWatcher</span></span>
<span data-ttu-id="e3989-125">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="e3989-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="e3989-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3989-126">-PassThru</span></span>
<span data-ttu-id="e3989-127">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="e3989-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="e3989-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3989-128">-ResourceGroupName</span></span>
<span data-ttu-id="e3989-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3989-129">The resource group name.</span></span>

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

### <span data-ttu-id="e3989-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3989-130">-Confirm</span></span>
<span data-ttu-id="e3989-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e3989-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3989-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3989-132">-WhatIf</span></span>
<span data-ttu-id="e3989-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e3989-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3989-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3989-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3989-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3989-135">CommonParameters</span></span>
<span data-ttu-id="e3989-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3989-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3989-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3989-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3989-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3989-138">INPUTS</span></span>

### <span data-ttu-id="e3989-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3989-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e3989-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e3989-140">System.String</span></span>

## <span data-ttu-id="e3989-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3989-141">OUTPUTS</span></span>

### <span data-ttu-id="e3989-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3989-142">System.Boolean</span></span>

## <span data-ttu-id="e3989-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3989-143">NOTES</span></span>
<span data-ttu-id="e3989-144">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="e3989-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="e3989-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3989-145">RELATED LINKS</span></span>

[<span data-ttu-id="e3989-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3989-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e3989-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3989-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e3989-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3989-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e3989-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e3989-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e3989-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e3989-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e3989-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e3989-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e3989-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e3989-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e3989-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3989-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3989-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e3989-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e3989-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3989-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3989-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3989-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3989-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3989-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3989-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3989-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e3989-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e3989-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e3989-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e3989-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e3989-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3989-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e3989-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3989-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e3989-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3989-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e3989-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e3989-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e3989-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3989-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e3989-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3989-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e3989-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e3989-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e3989-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e3989-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e3989-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e3989-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e3989-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e3989-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e3989-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e3989-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e3989-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3989-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
