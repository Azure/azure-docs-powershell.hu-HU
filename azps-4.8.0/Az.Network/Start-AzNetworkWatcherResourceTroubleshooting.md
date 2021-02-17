---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5f707b4e6a2610f8a62ce807c5549ee03e6697d8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409086"
---
# <span data-ttu-id="9bd4f-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9bd4f-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="9bd4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd4f-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd4f-103">Hibaelhárítást kezd egy hálózati erőforrással az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="9bd4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9bd4f-104">SYNTAX</span></span>

### <span data-ttu-id="9bd4f-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9bd4f-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd4f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9bd4f-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd4f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9bd4f-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bd4f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9bd4f-108">DESCRIPTION</span></span>
<span data-ttu-id="9bd4f-109">A Start-AzNetworkWatcherResourceTroubleshooting parancsmag megkezdi egy hálózati erőforrás hibaelhárítását az Azure-ban, és a lehetséges problémákról és megoldásokról ad információkat.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="9bd4f-110">Jelenleg a virtuális hálózati átjárók és kapcsolatok támogatottak.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="9bd4f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9bd4f-111">EXAMPLES</span></span>

### <span data-ttu-id="9bd4f-112">1. példa: Hibaelhárítás kezdése virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="9bd4f-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="9bd4f-113">A fenti minta megkezdi a hibaelhárítást egy virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="9bd4f-114">A művelet néhány percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="9bd4f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bd4f-115">PARAMETERS</span></span>

### <span data-ttu-id="9bd4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd4f-116">-DefaultProfile</span></span>
<span data-ttu-id="9bd4f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bd4f-118">-Location</span><span class="sxs-lookup"><span data-stu-id="9bd4f-118">-Location</span></span>
<span data-ttu-id="9bd4f-119">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9bd4f-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9bd4f-120">-NetworkWatcher</span></span>
<span data-ttu-id="9bd4f-121">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="9bd4f-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9bd4f-122">-NetworkWatcherName</span></span>
<span data-ttu-id="9bd4f-123">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="9bd4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="9bd4f-125">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9bd4f-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="9bd4f-126">-StorageId</span></span>
<span data-ttu-id="9bd4f-127">A tárterület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-127">The storage ID.</span></span>

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

### <span data-ttu-id="9bd4f-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="9bd4f-128">-StoragePath</span></span>
<span data-ttu-id="9bd4f-129">A tárterület elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-129">The storage path.</span></span>

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

### <span data-ttu-id="9bd4f-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9bd4f-130">-TargetResourceId</span></span>
<span data-ttu-id="9bd4f-131">Megadja a hibaelhárításhoz szükséges erőforrás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="9bd4f-132">Példaformátum: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="9bd4f-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="9bd4f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd4f-133">CommonParameters</span></span>
<span data-ttu-id="9bd4f-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd4f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd4f-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd4f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd4f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9bd4f-136">INPUTS</span></span>

### <span data-ttu-id="9bd4f-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9bd4f-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9bd4f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9bd4f-138">System.String</span></span>

## <span data-ttu-id="9bd4f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bd4f-139">OUTPUTS</span></span>

### <span data-ttu-id="9bd4f-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9bd4f-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="9bd4f-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9bd4f-141">NOTES</span></span>
<span data-ttu-id="9bd4f-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, hibaelhárítás, VPN, kapcsolat</span><span class="sxs-lookup"><span data-stu-id="9bd4f-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="9bd4f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bd4f-143">RELATED LINKS</span></span>

[<span data-ttu-id="9bd4f-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9bd4f-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9bd4f-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9bd4f-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9bd4f-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9bd4f-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9bd4f-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9bd4f-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9bd4f-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9bd4f-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9bd4f-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9bd4f-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9bd4f-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9bd4f-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9bd4f-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9bd4f-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9bd4f-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9bd4f-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9bd4f-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9bd4f-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9bd4f-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9bd4f-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9bd4f-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9bd4f-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9bd4f-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bd4f-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9bd4f-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9bd4f-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9bd4f-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9bd4f-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9bd4f-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bd4f-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9bd4f-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bd4f-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9bd4f-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bd4f-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9bd4f-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9bd4f-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9bd4f-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bd4f-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9bd4f-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bd4f-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9bd4f-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9bd4f-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9bd4f-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9bd4f-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9bd4f-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9bd4f-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9bd4f-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9bd4f-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9bd4f-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9bd4f-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="9bd4f-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bd4f-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
