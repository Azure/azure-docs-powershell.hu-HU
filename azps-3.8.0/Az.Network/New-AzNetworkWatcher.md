---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: dbc1f3e942a95adf0cb56721ec1a2666da9b9188
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399039"
---
# <span data-ttu-id="b8323-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8323-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="b8323-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8323-102">SYNOPSIS</span></span>
<span data-ttu-id="b8323-103">Létrehoz egy új Network Watcher erőforrást.</span><span class="sxs-lookup"><span data-stu-id="b8323-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="b8323-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b8323-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8323-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b8323-105">DESCRIPTION</span></span>
<span data-ttu-id="b8323-106">A New-AzNetworkWatcher parancsmag létrehoz egy új Network Watcher erőforrást.</span><span class="sxs-lookup"><span data-stu-id="b8323-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="b8323-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b8323-107">EXAMPLES</span></span>

### <span data-ttu-id="b8323-108">1. példa: Hálózati figyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="b8323-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="b8323-109">Ebben a példában egy új Hálózatfigyelőt hoz létre egy újonnan létrehozott erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="b8323-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="b8323-110">Felhívjuk a figyelmét arra, hogy előfizetésenként régiónként csak egy Hálózati figyelőt lehet létrehozni.</span><span class="sxs-lookup"><span data-stu-id="b8323-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="b8323-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8323-111">PARAMETERS</span></span>

### <span data-ttu-id="b8323-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8323-112">-DefaultProfile</span></span>
<span data-ttu-id="b8323-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8323-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8323-114">-Location</span><span class="sxs-lookup"><span data-stu-id="b8323-114">-Location</span></span>
<span data-ttu-id="b8323-115">Hely.</span><span class="sxs-lookup"><span data-stu-id="b8323-115">Location.</span></span>

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

### <span data-ttu-id="b8323-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b8323-116">-Name</span></span>
<span data-ttu-id="b8323-117">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="b8323-117">The network watcher name.</span></span>

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

### <span data-ttu-id="b8323-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8323-118">-ResourceGroupName</span></span>
<span data-ttu-id="b8323-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b8323-119">The resource group name.</span></span>

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

### <span data-ttu-id="b8323-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="b8323-120">-Tag</span></span>
<span data-ttu-id="b8323-121">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="b8323-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b8323-122">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="b8323-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b8323-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8323-123">-Confirm</span></span>
<span data-ttu-id="b8323-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b8323-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8323-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8323-125">-WhatIf</span></span>
<span data-ttu-id="b8323-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b8323-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8323-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8323-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8323-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8323-128">CommonParameters</span></span>
<span data-ttu-id="b8323-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8323-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8323-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8323-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8323-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8323-131">INPUTS</span></span>

### <span data-ttu-id="b8323-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b8323-132">System.String</span></span>

### <span data-ttu-id="b8323-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b8323-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b8323-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8323-134">OUTPUTS</span></span>

### <span data-ttu-id="b8323-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8323-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="b8323-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b8323-136">NOTES</span></span>
<span data-ttu-id="b8323-137">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="b8323-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="b8323-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8323-138">RELATED LINKS</span></span>

[<span data-ttu-id="b8323-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8323-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b8323-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8323-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b8323-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8323-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b8323-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b8323-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b8323-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b8323-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b8323-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b8323-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b8323-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b8323-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b8323-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8323-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8323-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b8323-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b8323-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8323-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8323-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8323-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8323-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8323-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8323-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8323-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b8323-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b8323-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b8323-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b8323-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b8323-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8323-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8323-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8323-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8323-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8323-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8323-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b8323-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b8323-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8323-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8323-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8323-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8323-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b8323-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b8323-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b8323-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b8323-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b8323-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b8323-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b8323-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b8323-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b8323-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b8323-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8323-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
