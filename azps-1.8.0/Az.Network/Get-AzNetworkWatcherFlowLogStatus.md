---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: cdc97ff5e528e58aa088950f5272e7689f35b10e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670523"
---
# <span data-ttu-id="64449-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="64449-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="64449-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64449-102">SYNOPSIS</span></span>
<span data-ttu-id="64449-103">Beolvassa egy erőforrás átfolyási naplózási állapotát.</span><span class="sxs-lookup"><span data-stu-id="64449-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="64449-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64449-104">SYNTAX</span></span>

### <span data-ttu-id="64449-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64449-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64449-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="64449-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64449-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="64449-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64449-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="64449-108">DESCRIPTION</span></span>
<span data-ttu-id="64449-109">A Get-AzNetworkWatcherFlowLogStatus parancsmag az erőforrás átfolyási naplózási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="64449-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="64449-110">Az állapot azt is tartalmazza, hogy engedélyezve van-e a forgalom naplózása a megadott erőforráshoz, a konfigurált tárterület-fiók a naplók küldéséhez és a naplók adatmegőrzési házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="64449-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="64449-111">Jelenleg hálózati biztonsági csoportok támogatottak a forgalom naplózásához.</span><span class="sxs-lookup"><span data-stu-id="64449-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="64449-112">Példák</span><span class="sxs-lookup"><span data-stu-id="64449-112">EXAMPLES</span></span>

### <span data-ttu-id="64449-113">Példa 1: a forgalom naplózási állapotának beszerzése megadott NSG</span><span class="sxs-lookup"><span data-stu-id="64449-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
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

<span data-ttu-id="64449-114">Ebben a példában bemutatjuk egy hálózati biztonsági csoport átfolyás naplózási állapotát.</span><span class="sxs-lookup"><span data-stu-id="64449-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="64449-115">A megadott NSG engedélyezve van a folyamat naplózása, az alapértelmezett formátum és a nincs adatmegőrzési házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="64449-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="64449-116">2. példa: a forgalom naplózása és a forgalmi statisztika állapotának beszerzése egy megadott NSG</span><span class="sxs-lookup"><span data-stu-id="64449-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
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

<span data-ttu-id="64449-117">Ebben a példában bemutatjuk a forgalom naplózása és a forgalmi statisztika állapotát egy hálózati biztonsági csoport számára.</span><span class="sxs-lookup"><span data-stu-id="64449-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="64449-118">A megadott NSG a forgalom naplózása és a forgalmi statisztika engedélyezve van, az alapértelmezett formátum és a nincs adatmegőrzési házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="64449-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="64449-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64449-119">PARAMETERS</span></span>

### <span data-ttu-id="64449-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64449-120">-AsJob</span></span>
<span data-ttu-id="64449-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="64449-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64449-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64449-122">-DefaultProfile</span></span>
<span data-ttu-id="64449-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64449-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64449-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="64449-124">-Location</span></span>
<span data-ttu-id="64449-125">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="64449-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="64449-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64449-126">-NetworkWatcher</span></span>
<span data-ttu-id="64449-127">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="64449-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="64449-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="64449-128">-NetworkWatcherName</span></span>
<span data-ttu-id="64449-129">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="64449-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="64449-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64449-130">-ResourceGroupName</span></span>
<span data-ttu-id="64449-131">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="64449-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="64449-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="64449-132">-TargetResourceId</span></span>
<span data-ttu-id="64449-133">A cél erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="64449-133">The target resource ID.</span></span>

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

### <span data-ttu-id="64449-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64449-134">CommonParameters</span></span>
<span data-ttu-id="64449-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64449-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64449-136">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="64449-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64449-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64449-137">INPUTS</span></span>

### <span data-ttu-id="64449-138">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64449-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="64449-139">System. String</span><span class="sxs-lookup"><span data-stu-id="64449-139">System.String</span></span>

## <span data-ttu-id="64449-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64449-140">OUTPUTS</span></span>

### <span data-ttu-id="64449-141">Microsoft. Azure. commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="64449-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="64449-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64449-142">NOTES</span></span>
<span data-ttu-id="64449-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, flow, naplók, flowlog, naplózás</span><span class="sxs-lookup"><span data-stu-id="64449-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="64449-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64449-144">RELATED LINKS</span></span>

[<span data-ttu-id="64449-145">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64449-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="64449-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64449-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="64449-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64449-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="64449-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="64449-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="64449-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="64449-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="64449-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="64449-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="64449-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="64449-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="64449-152">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64449-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64449-153">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="64449-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="64449-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64449-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64449-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64449-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64449-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64449-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64449-157">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="64449-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="64449-158">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="64449-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="64449-159">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="64449-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="64449-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64449-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64449-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64449-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64449-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64449-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64449-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="64449-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="64449-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64449-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64449-165">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64449-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64449-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="64449-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="64449-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="64449-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="64449-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="64449-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="64449-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="64449-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="64449-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="64449-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="64449-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64449-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
