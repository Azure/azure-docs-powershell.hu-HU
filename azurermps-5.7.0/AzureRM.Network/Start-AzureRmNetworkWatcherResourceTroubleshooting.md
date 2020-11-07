---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermnetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 6c211bef936d6fa3077d066f7df190dbe6d4a47d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679276"
---
# <span data-ttu-id="16016-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="16016-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="16016-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16016-102">SYNOPSIS</span></span>
<span data-ttu-id="16016-103">Elindítja a hibaelhárítást egy hálózati erőforráson az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="16016-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16016-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16016-104">SYNTAX</span></span>

### <span data-ttu-id="16016-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16016-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16016-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="16016-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16016-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="16016-107">DESCRIPTION</span></span>
<span data-ttu-id="16016-108">Az Start-AzureRmNetworkWatcherResourceTroubleshooting parancsmag az Azure-ban egy hálózati erőforrás hibaelhárítását indítja el, és a potenciális problémákról és a mérséklésekről ad információt.</span><span class="sxs-lookup"><span data-stu-id="16016-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="16016-109">Jelenleg a virtuális hálózati átjárók és a kapcsolatok támogatottak.</span><span class="sxs-lookup"><span data-stu-id="16016-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="16016-110">Példák</span><span class="sxs-lookup"><span data-stu-id="16016-110">EXAMPLES</span></span>

### <span data-ttu-id="16016-111">---Példa 1: a hibaelhárítás indítása virtuális hálózati átjárón---</span><span class="sxs-lookup"><span data-stu-id="16016-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="16016-112">A fenti példa egy virtuális hálózati átjáró hibaelhárítását indítja el.</span><span class="sxs-lookup"><span data-stu-id="16016-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="16016-113">A művelet elvégzéséhez néhány percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="16016-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="16016-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16016-114">PARAMETERS</span></span>

### <span data-ttu-id="16016-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16016-115">-DefaultProfile</span></span>
<span data-ttu-id="16016-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16016-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16016-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16016-117">-NetworkWatcher</span></span>
<span data-ttu-id="16016-118">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="16016-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="16016-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="16016-119">-NetworkWatcherName</span></span>
<span data-ttu-id="16016-120">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="16016-120">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16016-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16016-121">-ResourceGroupName</span></span>
<span data-ttu-id="16016-122">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="16016-122">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16016-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="16016-123">-StorageId</span></span>
<span data-ttu-id="16016-124">A tárolási azonosító.</span><span class="sxs-lookup"><span data-stu-id="16016-124">The storage ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16016-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="16016-125">-StoragePath</span></span>
<span data-ttu-id="16016-126">A tárterület elérési útja.</span><span class="sxs-lookup"><span data-stu-id="16016-126">The storage path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16016-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="16016-127">-TargetResourceId</span></span>
<span data-ttu-id="16016-128">A hibaelhárításra szolgáló erőforrás erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="16016-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="16016-129">Példa formátum: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {kapcsolatnév}"</span><span class="sxs-lookup"><span data-stu-id="16016-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16016-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16016-130">CommonParameters</span></span>
<span data-ttu-id="16016-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16016-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16016-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16016-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16016-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16016-133">INPUTS</span></span>

### <span data-ttu-id="16016-134">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16016-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="16016-135">System. String</span><span class="sxs-lookup"><span data-stu-id="16016-135">System.String</span></span>

## <span data-ttu-id="16016-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16016-136">OUTPUTS</span></span>

### <span data-ttu-id="16016-137">Microsoft. Azure. commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="16016-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="16016-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16016-138">NOTES</span></span>
<span data-ttu-id="16016-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, hibaelhárítás, VPN, kapcsolat</span><span class="sxs-lookup"><span data-stu-id="16016-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="16016-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16016-140">RELATED LINKS</span></span>

[<span data-ttu-id="16016-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="16016-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="16016-142">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16016-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="16016-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16016-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="16016-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16016-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="16016-145">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16016-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16016-146">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="16016-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="16016-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16016-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16016-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16016-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16016-149">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16016-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16016-150">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="16016-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="16016-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="16016-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="16016-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="16016-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="16016-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="16016-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
