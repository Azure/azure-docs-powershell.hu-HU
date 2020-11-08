---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172905"
---
# <span data-ttu-id="c3fb3-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c3fb3-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="c3fb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fb3-103">Hálózati figyelő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="c3fb3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3fb3-104">SYNTAX</span></span>

### <span data-ttu-id="c3fb3-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c3fb3-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3fb3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c3fb3-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3fb3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c3fb3-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3fb3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3fb3-108">DESCRIPTION</span></span>
<span data-ttu-id="c3fb3-109">A Remove-AzNetworkWatcher parancsmag eltávolítja a Hálózatfigyelő-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="c3fb3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c3fb3-110">EXAMPLES</span></span>

### <span data-ttu-id="c3fb3-111">Példa 1: Hálózatfigyelő létrehozása és törlése</span><span class="sxs-lookup"><span data-stu-id="c3fb3-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="c3fb3-112">Ez a példa létrehoz egy hálózati figyelőt egy erőforráscsoporthoz, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c3fb3-113">Fontos tudni, hogy az előfizetések régiónként csak egy Hálózatfigyelő hozható létre.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="c3fb3-114">Ha a virtuális hálózat törlésekor a kérdését szeretné letiltani, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="c3fb3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3fb3-115">PARAMETERS</span></span>

### <span data-ttu-id="c3fb3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3fb3-116">-AsJob</span></span>
<span data-ttu-id="c3fb3-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c3fb3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3fb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fb3-118">-DefaultProfile</span></span>
<span data-ttu-id="c3fb3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3fb3-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="c3fb3-120">-Location</span></span>
<span data-ttu-id="c3fb3-121">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c3fb3-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3fb3-122">-Name</span></span>
<span data-ttu-id="c3fb3-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-123">The resource name.</span></span>

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

### <span data-ttu-id="c3fb3-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c3fb3-124">-NetworkWatcher</span></span>
<span data-ttu-id="c3fb3-125">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="c3fb3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3fb3-126">-PassThru</span></span>
<span data-ttu-id="c3fb3-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="c3fb3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3fb3-128">-ResourceGroupName</span></span>
<span data-ttu-id="c3fb3-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-129">The resource group name.</span></span>

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

### <span data-ttu-id="c3fb3-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3fb3-130">-Confirm</span></span>
<span data-ttu-id="c3fb3-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3fb3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3fb3-132">-WhatIf</span></span>
<span data-ttu-id="c3fb3-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3fb3-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3fb3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3fb3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fb3-135">CommonParameters</span></span>
<span data-ttu-id="c3fb3-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3fb3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fb3-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3fb3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fb3-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3fb3-138">INPUTS</span></span>

### <span data-ttu-id="c3fb3-139">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c3fb3-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c3fb3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c3fb3-140">System.String</span></span>

## <span data-ttu-id="c3fb3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3fb3-141">OUTPUTS</span></span>

### <span data-ttu-id="c3fb3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3fb3-142">System.Boolean</span></span>

## <span data-ttu-id="c3fb3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3fb3-143">NOTES</span></span>
<span data-ttu-id="c3fb3-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="c3fb3-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="c3fb3-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3fb3-145">RELATED LINKS</span></span>

[<span data-ttu-id="c3fb3-146">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c3fb3-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c3fb3-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c3fb3-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c3fb3-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c3fb3-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c3fb3-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c3fb3-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c3fb3-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c3fb3-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c3fb3-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c3fb3-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c3fb3-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c3fb3-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c3fb3-153">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3fb3-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c3fb3-154">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c3fb3-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c3fb3-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3fb3-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c3fb3-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3fb3-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c3fb3-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3fb3-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c3fb3-158">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3fb3-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c3fb3-159">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c3fb3-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c3fb3-160">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c3fb3-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c3fb3-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3fb3-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c3fb3-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3fb3-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c3fb3-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3fb3-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c3fb3-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c3fb3-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c3fb3-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3fb3-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c3fb3-166">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3fb3-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c3fb3-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c3fb3-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c3fb3-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c3fb3-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c3fb3-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c3fb3-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c3fb3-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c3fb3-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c3fb3-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c3fb3-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c3fb3-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3fb3-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
