---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: db3e3e529fd5c056acf793cd14280ef688c58a81
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333389"
---
# <span data-ttu-id="020c3-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="020c3-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="020c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="020c3-102">SYNOPSIS</span></span>
<span data-ttu-id="020c3-103">A korábban futtatott vagy éppen futó hibaelhárítási művelet hibaelhárítási eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="020c3-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="020c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="020c3-104">SYNTAX</span></span>

### <span data-ttu-id="020c3-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="020c3-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="020c3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="020c3-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="020c3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="020c3-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="020c3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="020c3-108">DESCRIPTION</span></span>
<span data-ttu-id="020c3-109">A Get-AzNetworkWatcherTroubleshootingResult parancsmag megkapja a hibaelhárítási eredményt a korábban futtatott vagy jelenleg futó Start-AzNetworkWatcherResourceTroubleshooting műveletből.</span><span class="sxs-lookup"><span data-stu-id="020c3-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="020c3-110">Ha a hibaelhárítási művelet folyamatban van, akkor a művelet néhány percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="020c3-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="020c3-111">Jelenleg a virtuális hálózati átjárók és kapcsolatok támogatottak.</span><span class="sxs-lookup"><span data-stu-id="020c3-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="020c3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="020c3-112">EXAMPLES</span></span>

### <span data-ttu-id="020c3-113">1. példa: Hibaelhárítás kezdése virtuális hálózati átjárón és az eredmény lekérése</span><span class="sxs-lookup"><span data-stu-id="020c3-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="020c3-114">A fenti minta megkezdi a hibaelhárítást egy virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="020c3-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="020c3-115">A művelet néhány percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="020c3-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="020c3-116">A hibaelhárítás elkezdődött, Get-AzNetworkWatcherTroubleshootingResult egy hívás az erőforráshoz, hogy beolvassa a hívás eredményét.</span><span class="sxs-lookup"><span data-stu-id="020c3-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="020c3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="020c3-117">PARAMETERS</span></span>

### <span data-ttu-id="020c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020c3-118">-DefaultProfile</span></span>
<span data-ttu-id="020c3-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="020c3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="020c3-120">-Location</span><span class="sxs-lookup"><span data-stu-id="020c3-120">-Location</span></span>
<span data-ttu-id="020c3-121">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="020c3-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="020c3-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="020c3-122">-NetworkWatcher</span></span>
<span data-ttu-id="020c3-123">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="020c3-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="020c3-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="020c3-124">-NetworkWatcherName</span></span>
<span data-ttu-id="020c3-125">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="020c3-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="020c3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="020c3-126">-ResourceGroupName</span></span>
<span data-ttu-id="020c3-127">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="020c3-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="020c3-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="020c3-128">-TargetResourceId</span></span>
<span data-ttu-id="020c3-129">A célerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="020c3-129">The target resource ID.</span></span>

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

### <span data-ttu-id="020c3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020c3-130">CommonParameters</span></span>
<span data-ttu-id="020c3-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="020c3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020c3-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="020c3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020c3-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="020c3-133">INPUTS</span></span>

### <span data-ttu-id="020c3-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="020c3-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="020c3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="020c3-135">System.String</span></span>

## <span data-ttu-id="020c3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="020c3-136">OUTPUTS</span></span>

### <span data-ttu-id="020c3-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="020c3-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="020c3-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="020c3-138">NOTES</span></span>
<span data-ttu-id="020c3-139">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, hibaelhárítás, VPN, kapcsolat</span><span class="sxs-lookup"><span data-stu-id="020c3-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="020c3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="020c3-140">RELATED LINKS</span></span>

[<span data-ttu-id="020c3-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="020c3-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="020c3-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="020c3-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="020c3-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="020c3-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="020c3-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="020c3-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="020c3-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="020c3-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="020c3-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="020c3-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="020c3-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="020c3-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="020c3-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="020c3-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="020c3-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="020c3-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="020c3-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="020c3-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="020c3-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="020c3-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="020c3-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="020c3-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="020c3-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="020c3-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="020c3-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="020c3-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="020c3-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="020c3-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="020c3-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="020c3-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="020c3-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="020c3-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="020c3-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="020c3-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="020c3-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="020c3-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="020c3-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="020c3-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="020c3-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="020c3-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="020c3-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="020c3-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="020c3-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="020c3-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="020c3-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="020c3-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="020c3-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="020c3-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="020c3-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="020c3-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="020c3-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="020c3-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
