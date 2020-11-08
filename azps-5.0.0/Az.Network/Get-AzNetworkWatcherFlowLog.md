---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5f4322ba81cdae5bdb0b33c2658a6d7934ed638d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186210"
---
# <span data-ttu-id="2801e-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2801e-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="2801e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2801e-102">SYNOPSIS</span></span>
<span data-ttu-id="2801e-103">Beolvashatja a folyamatábra erőforrását, vagy a megadott előfizetésben és régióban a forgalmi napló erőforrásainak listáját.</span><span class="sxs-lookup"><span data-stu-id="2801e-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="2801e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2801e-104">SYNTAX</span></span>

### <span data-ttu-id="2801e-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2801e-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2801e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2801e-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2801e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2801e-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2801e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2801e-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2801e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2801e-109">DESCRIPTION</span></span>
<span data-ttu-id="2801e-110">Beolvashatja a folyamatábra erőforrását, vagy a megadott előfizetésben és régióban a forgalmi napló erőforrásainak listáját.</span><span class="sxs-lookup"><span data-stu-id="2801e-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="2801e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2801e-111">EXAMPLES</span></span>

### <span data-ttu-id="2801e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2801e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="2801e-113">Név: pstest-azonosító:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid. hálózat/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETAG: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: sikerült hely: eastus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MySTorage: true RetentionPolicy: {"Days": 5, "enabled": true} formátum: {"type": "JSON", "version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"enabled": true; "workspaceId": "workspaceRegion": "eastus": "workspaceResourceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb"; "/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr": "oups"; "FlowLogsV2Demo": "OperationalInsights 60</span><span class="sxs-lookup"><span data-stu-id="2801e-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="2801e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2801e-114">PARAMETERS</span></span>

### <span data-ttu-id="2801e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2801e-115">-DefaultProfile</span></span>
<span data-ttu-id="2801e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2801e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2801e-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="2801e-117">-Location</span></span>
<span data-ttu-id="2801e-118">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="2801e-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2801e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2801e-119">-Name</span></span>
<span data-ttu-id="2801e-120">A folyamatábra neve.</span><span class="sxs-lookup"><span data-stu-id="2801e-120">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2801e-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2801e-121">-NetworkWatcher</span></span>
<span data-ttu-id="2801e-122">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="2801e-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="2801e-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2801e-123">-NetworkWatcherName</span></span>
<span data-ttu-id="2801e-124">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="2801e-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="2801e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2801e-125">-ResourceGroupName</span></span>
<span data-ttu-id="2801e-126">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2801e-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2801e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2801e-127">-ResourceId</span></span>
<span data-ttu-id="2801e-128">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2801e-128">Resource ID.</span></span>

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

### <span data-ttu-id="2801e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2801e-129">CommonParameters</span></span>
<span data-ttu-id="2801e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2801e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2801e-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2801e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2801e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2801e-132">INPUTS</span></span>

### <span data-ttu-id="2801e-133">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2801e-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2801e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2801e-134">System.String</span></span>

## <span data-ttu-id="2801e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2801e-135">OUTPUTS</span></span>

### <span data-ttu-id="2801e-136">Microsoft. Azure. commands. Network. models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="2801e-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="2801e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2801e-137">NOTES</span></span>

## <span data-ttu-id="2801e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2801e-138">RELATED LINKS</span></span>

[<span data-ttu-id="2801e-139">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2801e-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2801e-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2801e-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2801e-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2801e-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2801e-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2801e-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2801e-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2801e-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2801e-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2801e-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2801e-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2801e-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2801e-146">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2801e-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2801e-147">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2801e-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2801e-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2801e-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2801e-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2801e-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2801e-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2801e-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2801e-151">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2801e-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2801e-152">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2801e-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2801e-153">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2801e-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2801e-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2801e-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2801e-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2801e-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2801e-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2801e-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2801e-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2801e-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2801e-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2801e-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2801e-159">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2801e-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2801e-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2801e-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2801e-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2801e-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2801e-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2801e-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2801e-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2801e-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2801e-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2801e-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2801e-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2801e-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="2801e-166">Új – AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2801e-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="2801e-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2801e-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="2801e-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2801e-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
