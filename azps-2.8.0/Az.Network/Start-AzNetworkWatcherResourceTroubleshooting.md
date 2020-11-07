---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5399c97f076f1402b20b91798d2db215d00af8b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838290"
---
# <span data-ttu-id="d922d-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d922d-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="d922d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d922d-102">SYNOPSIS</span></span>
<span data-ttu-id="d922d-103">Elindítja a hibaelhárítást egy hálózati erőforráson az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d922d-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="d922d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d922d-104">SYNTAX</span></span>

### <span data-ttu-id="d922d-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d922d-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d922d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d922d-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d922d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d922d-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d922d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d922d-108">DESCRIPTION</span></span>
<span data-ttu-id="d922d-109">Az Start-AzNetworkWatcherResourceTroubleshooting parancsmag az Azure-ban egy hálózati erőforrás hibaelhárítását indítja el, és a potenciális problémákról és a mérséklésekről ad információt.</span><span class="sxs-lookup"><span data-stu-id="d922d-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="d922d-110">Jelenleg a virtuális hálózati átjárók és a kapcsolatok támogatottak.</span><span class="sxs-lookup"><span data-stu-id="d922d-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="d922d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d922d-111">EXAMPLES</span></span>

### <span data-ttu-id="d922d-112">1. példa: hibaelhárítás indítása virtuális hálózati átjárón</span><span class="sxs-lookup"><span data-stu-id="d922d-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="d922d-113">A fenti példa egy virtuális hálózati átjáró hibaelhárítását indítja el.</span><span class="sxs-lookup"><span data-stu-id="d922d-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="d922d-114">A művelet elvégzéséhez néhány percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="d922d-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="d922d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d922d-115">PARAMETERS</span></span>

### <span data-ttu-id="d922d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d922d-116">-DefaultProfile</span></span>
<span data-ttu-id="d922d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d922d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d922d-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="d922d-118">-Location</span></span>
<span data-ttu-id="d922d-119">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="d922d-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d922d-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d922d-120">-NetworkWatcher</span></span>
<span data-ttu-id="d922d-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="d922d-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="d922d-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d922d-122">-NetworkWatcherName</span></span>
<span data-ttu-id="d922d-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="d922d-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="d922d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d922d-124">-ResourceGroupName</span></span>
<span data-ttu-id="d922d-125">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d922d-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d922d-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="d922d-126">-StorageId</span></span>
<span data-ttu-id="d922d-127">A tárolási azonosító.</span><span class="sxs-lookup"><span data-stu-id="d922d-127">The storage ID.</span></span>

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

### <span data-ttu-id="d922d-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="d922d-128">-StoragePath</span></span>
<span data-ttu-id="d922d-129">A tárterület elérési útja.</span><span class="sxs-lookup"><span data-stu-id="d922d-129">The storage path.</span></span>

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

### <span data-ttu-id="d922d-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d922d-130">-TargetResourceId</span></span>
<span data-ttu-id="d922d-131">A hibaelhárításra szolgáló erőforrás erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d922d-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="d922d-132">Példa formátum: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {kapcsolatnév}"</span><span class="sxs-lookup"><span data-stu-id="d922d-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="d922d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d922d-133">CommonParameters</span></span>
<span data-ttu-id="d922d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d922d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d922d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d922d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d922d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d922d-136">INPUTS</span></span>

### <span data-ttu-id="d922d-137">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d922d-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d922d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d922d-138">System.String</span></span>

## <span data-ttu-id="d922d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d922d-139">OUTPUTS</span></span>

### <span data-ttu-id="d922d-140">Microsoft. Azure. commands. Network. models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d922d-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="d922d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d922d-141">NOTES</span></span>
<span data-ttu-id="d922d-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, hibaelhárítás, VPN, kapcsolat</span><span class="sxs-lookup"><span data-stu-id="d922d-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="d922d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d922d-143">RELATED LINKS</span></span>

[<span data-ttu-id="d922d-144">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d922d-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d922d-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d922d-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d922d-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d922d-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d922d-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d922d-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d922d-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d922d-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d922d-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d922d-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d922d-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d922d-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d922d-151">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d922d-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d922d-152">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d922d-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d922d-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d922d-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d922d-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d922d-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d922d-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d922d-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d922d-156">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d922d-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d922d-157">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d922d-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d922d-158">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d922d-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d922d-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d922d-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d922d-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d922d-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d922d-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d922d-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d922d-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d922d-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d922d-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d922d-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d922d-164">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d922d-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d922d-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d922d-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d922d-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d922d-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d922d-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d922d-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d922d-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d922d-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d922d-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d922d-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d922d-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d922d-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)