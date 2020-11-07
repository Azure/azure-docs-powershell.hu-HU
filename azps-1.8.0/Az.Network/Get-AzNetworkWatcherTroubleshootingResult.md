---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 4f8fcbc0e5eee5aea92493b54acc631ffd144d3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670506"
---
# <span data-ttu-id="de150-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="de150-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="de150-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de150-102">SYNOPSIS</span></span>
<span data-ttu-id="de150-103">A korábban futtatott vagy a jelenleg futó hibaelhárítási művelettől kapott hibaelhárítási eredményt kapja.</span><span class="sxs-lookup"><span data-stu-id="de150-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="de150-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de150-104">SYNTAX</span></span>

### <span data-ttu-id="de150-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="de150-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de150-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="de150-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de150-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="de150-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de150-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="de150-108">DESCRIPTION</span></span>
<span data-ttu-id="de150-109">A Get-AzNetworkWatcherTroubleshootingResult parancsmag a korábban futtatott vagy a jelenleg futó Start-AzNetworkWatcherResourceTroubleshooting műveletből kapja meg a hibaelhárítási találatokat.</span><span class="sxs-lookup"><span data-stu-id="de150-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="de150-110">Ha a hibaelhárítási művelet jelenleg folyamatban van, előfordulhat, hogy a művelet elvégzéséhez néhány percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="de150-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="de150-111">Jelenleg a virtuális hálózati átjárók és a kapcsolatok támogatottak.</span><span class="sxs-lookup"><span data-stu-id="de150-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="de150-112">Példák</span><span class="sxs-lookup"><span data-stu-id="de150-112">EXAMPLES</span></span>

### <span data-ttu-id="de150-113">Példa 1: hibaelhárítás indítása virtuális hálózati átjárón és az eredmény visszanyerése</span><span class="sxs-lookup"><span data-stu-id="de150-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="de150-114">A fenti példa egy virtuális hálózati átjáró hibaelhárítását indítja el.</span><span class="sxs-lookup"><span data-stu-id="de150-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="de150-115">A művelet elvégzéséhez néhány percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="de150-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="de150-116">A hibaelhárítást követően a hívás eredményének beolvasásához Get-AzNetworkWatcherTroubleshootingResult hívást kell kezdeményezni az erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="de150-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="de150-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de150-117">PARAMETERS</span></span>

### <span data-ttu-id="de150-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de150-118">-DefaultProfile</span></span>
<span data-ttu-id="de150-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de150-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de150-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="de150-120">-Location</span></span>
<span data-ttu-id="de150-121">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="de150-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="de150-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="de150-122">-NetworkWatcher</span></span>
<span data-ttu-id="de150-123">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="de150-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="de150-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="de150-124">-NetworkWatcherName</span></span>
<span data-ttu-id="de150-125">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="de150-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="de150-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de150-126">-ResourceGroupName</span></span>
<span data-ttu-id="de150-127">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="de150-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="de150-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="de150-128">-TargetResourceId</span></span>
<span data-ttu-id="de150-129">A cél erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="de150-129">The target resource ID.</span></span>

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

### <span data-ttu-id="de150-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de150-130">CommonParameters</span></span>
<span data-ttu-id="de150-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de150-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de150-132">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="de150-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de150-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de150-133">INPUTS</span></span>

### <span data-ttu-id="de150-134">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="de150-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="de150-135">System. String</span><span class="sxs-lookup"><span data-stu-id="de150-135">System.String</span></span>

## <span data-ttu-id="de150-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de150-136">OUTPUTS</span></span>

### <span data-ttu-id="de150-137">Microsoft. Azure. commands. Network. models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="de150-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="de150-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de150-138">NOTES</span></span>
<span data-ttu-id="de150-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, hibaelhárítás, VPN, kapcsolat</span><span class="sxs-lookup"><span data-stu-id="de150-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="de150-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de150-140">RELATED LINKS</span></span>

[<span data-ttu-id="de150-141">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="de150-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="de150-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="de150-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="de150-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="de150-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="de150-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="de150-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="de150-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="de150-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="de150-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="de150-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="de150-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="de150-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="de150-148">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="de150-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="de150-149">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="de150-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="de150-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="de150-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="de150-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="de150-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="de150-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="de150-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="de150-153">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="de150-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="de150-154">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="de150-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="de150-155">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="de150-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="de150-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de150-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="de150-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de150-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="de150-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de150-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="de150-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="de150-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="de150-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de150-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="de150-161">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de150-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="de150-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="de150-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="de150-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="de150-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="de150-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="de150-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="de150-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="de150-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="de150-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="de150-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="de150-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="de150-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
