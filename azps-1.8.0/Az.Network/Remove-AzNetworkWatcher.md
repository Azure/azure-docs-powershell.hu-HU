---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: b06540e1f03058fd36302616d22375270b521b8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670132"
---
# <span data-ttu-id="6c7be-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c7be-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="6c7be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c7be-102">SYNOPSIS</span></span>
<span data-ttu-id="6c7be-103">Hálózati figyelő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="6c7be-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="6c7be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c7be-104">SYNTAX</span></span>

### <span data-ttu-id="6c7be-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6c7be-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c7be-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6c7be-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c7be-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6c7be-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c7be-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c7be-108">DESCRIPTION</span></span>
<span data-ttu-id="6c7be-109">A Remove-AzNetworkWatcher parancsmag eltávolítja a Hálózatfigyelő-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6c7be-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="6c7be-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6c7be-110">EXAMPLES</span></span>

### <span data-ttu-id="6c7be-111">Példa 1: Hálózatfigyelő létrehozása és törlése</span><span class="sxs-lookup"><span data-stu-id="6c7be-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="6c7be-112">Ez a példa létrehoz egy hálózati figyelőt egy erőforráscsoporthoz, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="6c7be-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="6c7be-113">Fontos tudni, hogy az előfizetések régiónként csak egy Hálózatfigyelő hozható létre.</span><span class="sxs-lookup"><span data-stu-id="6c7be-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="6c7be-114">Ha a virtuális hálózat törlésekor a kérdését szeretné letiltani, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="6c7be-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="6c7be-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c7be-115">PARAMETERS</span></span>

### <span data-ttu-id="6c7be-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c7be-116">-AsJob</span></span>
<span data-ttu-id="6c7be-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6c7be-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c7be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c7be-118">-DefaultProfile</span></span>
<span data-ttu-id="6c7be-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c7be-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c7be-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="6c7be-120">-Location</span></span>
<span data-ttu-id="6c7be-121">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="6c7be-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6c7be-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6c7be-122">-Name</span></span>
<span data-ttu-id="6c7be-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="6c7be-123">The resource name.</span></span>

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

### <span data-ttu-id="6c7be-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c7be-124">-NetworkWatcher</span></span>
<span data-ttu-id="6c7be-125">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6c7be-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="6c7be-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c7be-126">-PassThru</span></span>
<span data-ttu-id="6c7be-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6c7be-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="6c7be-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c7be-128">-ResourceGroupName</span></span>
<span data-ttu-id="6c7be-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6c7be-129">The resource group name.</span></span>

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

### <span data-ttu-id="6c7be-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c7be-130">-Confirm</span></span>
<span data-ttu-id="6c7be-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c7be-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c7be-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c7be-132">-WhatIf</span></span>
<span data-ttu-id="6c7be-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c7be-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c7be-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c7be-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c7be-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c7be-135">CommonParameters</span></span>
<span data-ttu-id="6c7be-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c7be-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c7be-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c7be-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c7be-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c7be-138">INPUTS</span></span>

### <span data-ttu-id="6c7be-139">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c7be-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="6c7be-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6c7be-140">System.String</span></span>

## <span data-ttu-id="6c7be-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c7be-141">OUTPUTS</span></span>

### <span data-ttu-id="6c7be-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c7be-142">System.Boolean</span></span>

## <span data-ttu-id="6c7be-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c7be-143">NOTES</span></span>
<span data-ttu-id="6c7be-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="6c7be-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="6c7be-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c7be-145">RELATED LINKS</span></span>

[<span data-ttu-id="6c7be-146">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c7be-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6c7be-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c7be-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6c7be-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c7be-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6c7be-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6c7be-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6c7be-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6c7be-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6c7be-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6c7be-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6c7be-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6c7be-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6c7be-153">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c7be-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c7be-154">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6c7be-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6c7be-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c7be-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c7be-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c7be-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c7be-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c7be-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c7be-158">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c7be-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6c7be-159">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6c7be-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6c7be-160">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6c7be-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6c7be-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c7be-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6c7be-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c7be-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6c7be-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c7be-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6c7be-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6c7be-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6c7be-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c7be-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6c7be-166">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c7be-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6c7be-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6c7be-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6c7be-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6c7be-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6c7be-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6c7be-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6c7be-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6c7be-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6c7be-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6c7be-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="6c7be-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6c7be-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
