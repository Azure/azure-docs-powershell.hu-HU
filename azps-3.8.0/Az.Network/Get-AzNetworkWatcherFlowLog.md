---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 8296a680db76e1e7b3aedb15896f41ad0fba8e2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845937"
---
# <span data-ttu-id="63ea1-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="63ea1-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="63ea1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="63ea1-103">Beolvashatja a folyamatábra erőforrását, vagy a megadott előfizetésben és régióban a forgalmi napló erőforrásainak listáját.</span><span class="sxs-lookup"><span data-stu-id="63ea1-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="63ea1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63ea1-104">SYNTAX</span></span>

### <span data-ttu-id="63ea1-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63ea1-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63ea1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="63ea1-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63ea1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="63ea1-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63ea1-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="63ea1-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63ea1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="63ea1-109">DESCRIPTION</span></span>
<span data-ttu-id="63ea1-110">Beolvashatja a folyamatábra erőforrását, vagy a megadott előfizetésben és régióban a forgalmi napló erőforrásainak listáját.</span><span class="sxs-lookup"><span data-stu-id="63ea1-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="63ea1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="63ea1-111">EXAMPLES</span></span>

### <span data-ttu-id="63ea1-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="63ea1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="63ea1-113">Név: pstest-azonosító:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid. hálózat/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETAG: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: sikerült hely: eastus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MySTorage: true RetentionPolicy: {"Days": 5, "enabled": true} formátum: {"type": "JSON", "version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"enabled": true; "workspaceId": "workspaceRegion": "eastus": "workspaceResourceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb"; "/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr": "oups"; "FlowLogsV2Demo": "OperationalInsights 60</span><span class="sxs-lookup"><span data-stu-id="63ea1-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="63ea1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63ea1-114">PARAMETERS</span></span>

### <span data-ttu-id="63ea1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ea1-115">-DefaultProfile</span></span>
<span data-ttu-id="63ea1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63ea1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63ea1-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="63ea1-117">-Location</span></span>
<span data-ttu-id="63ea1-118">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="63ea1-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="63ea1-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63ea1-119">-Name</span></span>
<span data-ttu-id="63ea1-120">A folyamatábra neve.</span><span class="sxs-lookup"><span data-stu-id="63ea1-120">The flow log name.</span></span>

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

### <span data-ttu-id="63ea1-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63ea1-121">-NetworkWatcher</span></span>
<span data-ttu-id="63ea1-122">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="63ea1-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="63ea1-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="63ea1-123">-NetworkWatcherName</span></span>
<span data-ttu-id="63ea1-124">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="63ea1-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="63ea1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63ea1-125">-ResourceGroupName</span></span>
<span data-ttu-id="63ea1-126">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="63ea1-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="63ea1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63ea1-127">-ResourceId</span></span>
<span data-ttu-id="63ea1-128">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="63ea1-128">Resource ID.</span></span>

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

### <span data-ttu-id="63ea1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ea1-129">CommonParameters</span></span>
<span data-ttu-id="63ea1-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63ea1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ea1-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="63ea1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ea1-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63ea1-132">INPUTS</span></span>

### <span data-ttu-id="63ea1-133">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63ea1-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="63ea1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="63ea1-134">System.String</span></span>

## <span data-ttu-id="63ea1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63ea1-135">OUTPUTS</span></span>

### <span data-ttu-id="63ea1-136">Microsoft. Azure. commands. Network. models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="63ea1-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="63ea1-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63ea1-137">NOTES</span></span>

## <span data-ttu-id="63ea1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63ea1-138">RELATED LINKS</span></span>

[<span data-ttu-id="63ea1-139">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63ea1-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="63ea1-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63ea1-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="63ea1-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="63ea1-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="63ea1-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="63ea1-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="63ea1-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="63ea1-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="63ea1-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="63ea1-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="63ea1-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="63ea1-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="63ea1-146">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63ea1-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63ea1-147">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="63ea1-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="63ea1-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63ea1-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63ea1-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63ea1-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63ea1-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="63ea1-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="63ea1-151">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="63ea1-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="63ea1-152">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="63ea1-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="63ea1-153">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="63ea1-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="63ea1-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63ea1-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="63ea1-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63ea1-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="63ea1-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63ea1-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="63ea1-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="63ea1-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="63ea1-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63ea1-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="63ea1-159">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63ea1-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="63ea1-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="63ea1-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="63ea1-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="63ea1-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="63ea1-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="63ea1-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="63ea1-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="63ea1-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="63ea1-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="63ea1-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="63ea1-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="63ea1-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="63ea1-166">Új – AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="63ea1-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog)

[<span data-ttu-id="63ea1-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="63ea1-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="63ea1-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="63ea1-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog)
