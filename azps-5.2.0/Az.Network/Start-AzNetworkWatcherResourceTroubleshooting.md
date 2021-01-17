---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 0776b10a14236ac4806ccc166f24b1dd5a3ee3de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336558"
---
# <span data-ttu-id="cdb43-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cdb43-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="cdb43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdb43-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb43-103">Hibaelhárítást kezd egy hálózati erőforrással az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="cdb43-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="cdb43-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cdb43-104">SYNTAX</span></span>

### <span data-ttu-id="cdb43-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cdb43-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdb43-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cdb43-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdb43-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cdb43-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdb43-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cdb43-108">DESCRIPTION</span></span>
<span data-ttu-id="cdb43-109">A Start-AzNetworkWatcherResourceTroubleshooting parancsmag megkezdi egy hálózati erőforrás hibaelhárítását az Azure-ban, és a lehetséges problémákról és megoldásokról ad információkat.</span><span class="sxs-lookup"><span data-stu-id="cdb43-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="cdb43-110">Jelenleg a virtuális hálózati átjárók és kapcsolatok támogatottak.</span><span class="sxs-lookup"><span data-stu-id="cdb43-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="cdb43-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cdb43-111">EXAMPLES</span></span>

### <span data-ttu-id="cdb43-112">1. példa: Hibaelhárítás kezdése virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="cdb43-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="cdb43-113">A fenti minta megkezdi a hibaelhárítást egy virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="cdb43-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="cdb43-114">A művelet néhány percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="cdb43-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="cdb43-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdb43-115">PARAMETERS</span></span>

### <span data-ttu-id="cdb43-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb43-116">-DefaultProfile</span></span>
<span data-ttu-id="cdb43-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdb43-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdb43-118">-Location</span><span class="sxs-lookup"><span data-stu-id="cdb43-118">-Location</span></span>
<span data-ttu-id="cdb43-119">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="cdb43-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cdb43-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdb43-120">-NetworkWatcher</span></span>
<span data-ttu-id="cdb43-121">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="cdb43-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="cdb43-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cdb43-122">-NetworkWatcherName</span></span>
<span data-ttu-id="cdb43-123">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="cdb43-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="cdb43-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb43-124">-ResourceGroupName</span></span>
<span data-ttu-id="cdb43-125">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cdb43-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cdb43-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="cdb43-126">-StorageId</span></span>
<span data-ttu-id="cdb43-127">A tárterület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cdb43-127">The storage ID.</span></span>

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

### <span data-ttu-id="cdb43-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="cdb43-128">-StoragePath</span></span>
<span data-ttu-id="cdb43-129">A tárterület elérési útja.</span><span class="sxs-lookup"><span data-stu-id="cdb43-129">The storage path.</span></span>

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

### <span data-ttu-id="cdb43-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb43-130">-TargetResourceId</span></span>
<span data-ttu-id="cdb43-131">Megadja a hibaelhárításhoz szükséges erőforrás erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="cdb43-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="cdb43-132">Példaformátum: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="cdb43-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="cdb43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb43-133">CommonParameters</span></span>
<span data-ttu-id="cdb43-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb43-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb43-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb43-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdb43-136">INPUTS</span></span>

### <span data-ttu-id="cdb43-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdb43-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="cdb43-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cdb43-138">System.String</span></span>

## <span data-ttu-id="cdb43-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdb43-139">OUTPUTS</span></span>

### <span data-ttu-id="cdb43-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cdb43-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="cdb43-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cdb43-141">NOTES</span></span>
<span data-ttu-id="cdb43-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, hibaelhárítás, VPN, kapcsolat</span><span class="sxs-lookup"><span data-stu-id="cdb43-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="cdb43-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdb43-143">RELATED LINKS</span></span>

[<span data-ttu-id="cdb43-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdb43-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cdb43-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdb43-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cdb43-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdb43-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cdb43-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cdb43-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cdb43-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cdb43-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cdb43-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cdb43-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="cdb43-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cdb43-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cdb43-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdb43-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdb43-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cdb43-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cdb43-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdb43-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdb43-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdb43-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdb43-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdb43-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdb43-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdb43-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cdb43-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cdb43-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cdb43-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cdb43-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="cdb43-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb43-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cdb43-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb43-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cdb43-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb43-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cdb43-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cdb43-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cdb43-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb43-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cdb43-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb43-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cdb43-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cdb43-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cdb43-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cdb43-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cdb43-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cdb43-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cdb43-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cdb43-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cdb43-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cdb43-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="cdb43-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb43-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
