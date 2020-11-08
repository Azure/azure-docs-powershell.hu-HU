---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 7c8f33d8339bb873b713acabd71ca57fe9107383
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024612"
---
# <span data-ttu-id="f865e-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f865e-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="f865e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f865e-102">SYNOPSIS</span></span>
<span data-ttu-id="f865e-103">Új Hálózatfigyelő-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="f865e-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="f865e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f865e-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f865e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f865e-105">DESCRIPTION</span></span>
<span data-ttu-id="f865e-106">Az New-AzNetworkWatcher parancsmag új Hálózatfigyelő-erőforrást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f865e-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="f865e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f865e-107">EXAMPLES</span></span>

### <span data-ttu-id="f865e-108">Példa 1: Hálózatfigyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="f865e-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="f865e-109">Ebben a példában egy új hálózati figyelőt hoz létre egy újonnan létrehozott erőforráscsoport belsejében.</span><span class="sxs-lookup"><span data-stu-id="f865e-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="f865e-110">Fontos tudni, hogy az előfizetések régiónként csak egy Hálózatfigyelő hozható létre.</span><span class="sxs-lookup"><span data-stu-id="f865e-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="f865e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f865e-111">PARAMETERS</span></span>

### <span data-ttu-id="f865e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f865e-112">-DefaultProfile</span></span>
<span data-ttu-id="f865e-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f865e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f865e-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="f865e-114">-Location</span></span>
<span data-ttu-id="f865e-115">Helyre.</span><span class="sxs-lookup"><span data-stu-id="f865e-115">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f865e-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f865e-116">-Name</span></span>
<span data-ttu-id="f865e-117">A Hálózatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="f865e-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f865e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f865e-118">-ResourceGroupName</span></span>
<span data-ttu-id="f865e-119">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f865e-119">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f865e-120">-Címke</span><span class="sxs-lookup"><span data-stu-id="f865e-120">-Tag</span></span>
<span data-ttu-id="f865e-121">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="f865e-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f865e-122">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="f865e-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f865e-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f865e-123">-Confirm</span></span>
<span data-ttu-id="f865e-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f865e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f865e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f865e-125">-WhatIf</span></span>
<span data-ttu-id="f865e-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f865e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f865e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f865e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f865e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f865e-128">CommonParameters</span></span>
<span data-ttu-id="f865e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f865e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f865e-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f865e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f865e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f865e-131">INPUTS</span></span>

### <span data-ttu-id="f865e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f865e-132">System.String</span></span>

### <span data-ttu-id="f865e-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f865e-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f865e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f865e-134">OUTPUTS</span></span>

### <span data-ttu-id="f865e-135">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f865e-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="f865e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f865e-136">NOTES</span></span>
<span data-ttu-id="f865e-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="f865e-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="f865e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f865e-138">RELATED LINKS</span></span>

[<span data-ttu-id="f865e-139">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f865e-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f865e-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f865e-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f865e-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f865e-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f865e-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f865e-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f865e-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f865e-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f865e-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f865e-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f865e-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f865e-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f865e-146">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f865e-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f865e-147">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f865e-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f865e-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f865e-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f865e-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f865e-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f865e-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f865e-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f865e-151">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f865e-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f865e-152">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f865e-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f865e-153">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f865e-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f865e-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f865e-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f865e-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f865e-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f865e-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f865e-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f865e-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f865e-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f865e-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f865e-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f865e-159">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f865e-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f865e-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f865e-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f865e-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f865e-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f865e-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f865e-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f865e-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f865e-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f865e-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f865e-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f865e-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f865e-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
