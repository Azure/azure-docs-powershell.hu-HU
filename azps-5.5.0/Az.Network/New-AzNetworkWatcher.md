---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 7c8f33d8339bb873b713acabd71ca57fe9107383
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202764"
---
# <span data-ttu-id="8a246-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a246-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="8a246-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a246-102">SYNOPSIS</span></span>
<span data-ttu-id="8a246-103">Létrehoz egy új Network Watcher erőforrást.</span><span class="sxs-lookup"><span data-stu-id="8a246-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="8a246-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8a246-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a246-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8a246-105">DESCRIPTION</span></span>
<span data-ttu-id="8a246-106">A New-AzNetworkWatcher parancsmag létrehoz egy új Network Watcher erőforrást.</span><span class="sxs-lookup"><span data-stu-id="8a246-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="8a246-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8a246-107">EXAMPLES</span></span>

### <span data-ttu-id="8a246-108">1. példa: Hálózatfigyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="8a246-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="8a246-109">Ebben a példában egy új Hálózatfigyelőt hoz létre egy újonnan létrehozott erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="8a246-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="8a246-110">Felhívjuk a figyelmét arra, hogy előfizetésenként régiónként csak egy Hálózati figyelőt lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="8a246-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="8a246-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a246-111">PARAMETERS</span></span>

### <span data-ttu-id="8a246-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a246-112">-DefaultProfile</span></span>
<span data-ttu-id="8a246-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a246-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a246-114">-Location</span><span class="sxs-lookup"><span data-stu-id="8a246-114">-Location</span></span>
<span data-ttu-id="8a246-115">Hely.</span><span class="sxs-lookup"><span data-stu-id="8a246-115">Location.</span></span>

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

### <span data-ttu-id="8a246-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8a246-116">-Name</span></span>
<span data-ttu-id="8a246-117">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="8a246-117">The network watcher name.</span></span>

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

### <span data-ttu-id="8a246-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a246-118">-ResourceGroupName</span></span>
<span data-ttu-id="8a246-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8a246-119">The resource group name.</span></span>

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

### <span data-ttu-id="8a246-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="8a246-120">-Tag</span></span>
<span data-ttu-id="8a246-121">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="8a246-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8a246-122">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="8a246-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8a246-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a246-123">-Confirm</span></span>
<span data-ttu-id="8a246-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8a246-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a246-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a246-125">-WhatIf</span></span>
<span data-ttu-id="8a246-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8a246-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a246-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8a246-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a246-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a246-128">CommonParameters</span></span>
<span data-ttu-id="8a246-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a246-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a246-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a246-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a246-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a246-131">INPUTS</span></span>

### <span data-ttu-id="8a246-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8a246-132">System.String</span></span>

### <span data-ttu-id="8a246-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8a246-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8a246-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a246-134">OUTPUTS</span></span>

### <span data-ttu-id="8a246-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a246-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="8a246-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8a246-136">NOTES</span></span>
<span data-ttu-id="8a246-137">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő</span><span class="sxs-lookup"><span data-stu-id="8a246-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="8a246-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a246-138">RELATED LINKS</span></span>

[<span data-ttu-id="8a246-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a246-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8a246-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a246-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8a246-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a246-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8a246-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8a246-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8a246-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8a246-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8a246-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8a246-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8a246-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8a246-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8a246-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a246-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a246-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8a246-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8a246-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a246-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a246-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a246-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a246-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a246-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a246-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a246-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8a246-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8a246-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8a246-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8a246-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8a246-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8a246-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8a246-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8a246-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8a246-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8a246-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8a246-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8a246-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8a246-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8a246-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8a246-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8a246-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8a246-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8a246-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8a246-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8a246-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8a246-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8a246-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8a246-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8a246-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8a246-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8a246-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8a246-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8a246-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
