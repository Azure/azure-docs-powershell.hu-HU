---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: dd88c40876bf3ceb5f90a7088f5943fcf5f18ce8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358523"
---
# <span data-ttu-id="8ab9c-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8ab9c-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="8ab9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ab9c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab9c-103">Egy erőforrás folyamatnaplózási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="8ab9c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ab9c-104">SYNTAX</span></span>

### <span data-ttu-id="8ab9c-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ab9c-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ab9c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8ab9c-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ab9c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8ab9c-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ab9c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ab9c-108">DESCRIPTION</span></span>
<span data-ttu-id="8ab9c-109">A Get-AzNetworkWatcherFlowLogStatus parancsmag egy erőforrás folyamatnaplózási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="8ab9c-110">Az állapot tartalmazza, hogy engedélyezve van-e a folyamatnaplózás az erőforráshoz, a konfigurált tárfiók naplók küldésekor, valamint a naplók adatmegőrzési házirende.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="8ab9c-111">A hálózati biztonsági csoportok jelenleg a folyamatnaplózásban támogatottak.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="8ab9c-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ab9c-112">EXAMPLES</span></span>

### <span data-ttu-id="8ab9c-113">1. példa: Folyamatnaplózási állapot lekérte egy megadott NSG-hez</span><span class="sxs-lookup"><span data-stu-id="8ab9c-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                     "Format"         : {
                       "Type ": "Json",
                       "Version": 1
                     }
                   }
```

<span data-ttu-id="8ab9c-114">Ebben a példában egy hálózati biztonsági csoport folyamatnaplózási állapotát mutatjuk be.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="8ab9c-115">A megadott NSG-ben engedélyezve van a folyamatnaplózás, az alapértelmezett formátum, és nincs beállítva adatmegőrzési házirend.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="8ab9c-116">2. példa: Folyamatnaplózás és forgalomelemzési állapot lekérte egy megadott NSG-hez</span><span class="sxs-lookup"><span data-stu-id="8ab9c-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="8ab9c-117">Ebben a példában egy hálózati biztonsági csoport folyamatnaplózási és forgalomelemzési állapotát mutatjuk be.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="8ab9c-118">A megadott NSG-ben engedélyezve van a folyamatnaplózás, és engedélyezve van a Forgalomelemzés, az alapértelmezett formátum, és nincs beállítva adatmegőrzési házirend.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="8ab9c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ab9c-119">PARAMETERS</span></span>

### <span data-ttu-id="8ab9c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ab9c-120">-AsJob</span></span>
<span data-ttu-id="8ab9c-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8ab9c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ab9c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab9c-122">-DefaultProfile</span></span>
<span data-ttu-id="8ab9c-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ab9c-124">-Location</span><span class="sxs-lookup"><span data-stu-id="8ab9c-124">-Location</span></span>
<span data-ttu-id="8ab9c-125">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8ab9c-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ab9c-126">-NetworkWatcher</span></span>
<span data-ttu-id="8ab9c-127">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="8ab9c-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8ab9c-128">-NetworkWatcherName</span></span>
<span data-ttu-id="8ab9c-129">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab9c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ab9c-130">-ResourceGroupName</span></span>
<span data-ttu-id="8ab9c-131">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8ab9c-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8ab9c-132">-TargetResourceId</span></span>
<span data-ttu-id="8ab9c-133">A célerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-133">The target resource ID.</span></span>

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

### <span data-ttu-id="8ab9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab9c-134">CommonParameters</span></span>
<span data-ttu-id="8ab9c-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ab9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab9c-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ab9c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab9c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ab9c-137">INPUTS</span></span>

### <span data-ttu-id="8ab9c-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ab9c-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="8ab9c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8ab9c-139">System.String</span></span>

## <span data-ttu-id="8ab9c-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ab9c-140">OUTPUTS</span></span>

### <span data-ttu-id="8ab9c-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="8ab9c-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="8ab9c-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ab9c-142">NOTES</span></span>
<span data-ttu-id="8ab9c-143">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, figyelő, folyamat, naplók, folyamatábra, naplózás</span><span class="sxs-lookup"><span data-stu-id="8ab9c-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="8ab9c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ab9c-144">RELATED LINKS</span></span>

[<span data-ttu-id="8ab9c-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ab9c-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8ab9c-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ab9c-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8ab9c-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ab9c-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8ab9c-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8ab9c-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8ab9c-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8ab9c-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8ab9c-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8ab9c-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8ab9c-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8ab9c-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8ab9c-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ab9c-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ab9c-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8ab9c-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8ab9c-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ab9c-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ab9c-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ab9c-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ab9c-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ab9c-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ab9c-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ab9c-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8ab9c-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8ab9c-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8ab9c-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8ab9c-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8ab9c-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ab9c-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ab9c-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ab9c-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ab9c-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ab9c-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ab9c-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8ab9c-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8ab9c-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ab9c-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ab9c-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ab9c-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ab9c-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8ab9c-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8ab9c-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8ab9c-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8ab9c-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8ab9c-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8ab9c-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8ab9c-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8ab9c-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8ab9c-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8ab9c-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ab9c-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
