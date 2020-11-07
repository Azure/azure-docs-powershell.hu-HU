---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermnetworkwatcherresourcetroubleshooting
schema: 2.0.0
ms.openlocfilehash: 411b70fb6018b71b1c1c7fbf67816d0c86e6d3b6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848690"
---
# <span data-ttu-id="167b6-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="167b6-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="167b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="167b6-102">SYNOPSIS</span></span>
<span data-ttu-id="167b6-103">Elindítja a hibaelhárítást egy hálózati erőforráson az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="167b6-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="167b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="167b6-104">SYNTAX</span></span>

### <span data-ttu-id="167b6-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="167b6-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="167b6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="167b6-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="167b6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="167b6-107">DESCRIPTION</span></span>
<span data-ttu-id="167b6-108">Az Start-AzureRmNetworkWatcherResourceTroubleshooting parancsmag az Azure-ban egy hálózati erőforrás hibaelhárítását indítja el, és a potenciális problémákról és a mérséklésekről ad információt.</span><span class="sxs-lookup"><span data-stu-id="167b6-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="167b6-109">Jelenleg a virtuális hálózati átjárók és a kapcsolatok támogatottak.</span><span class="sxs-lookup"><span data-stu-id="167b6-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="167b6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="167b6-110">EXAMPLES</span></span>

### <span data-ttu-id="167b6-111">---Példa 1: a hibaelhárítás indítása virtuális hálózati átjárón---</span><span class="sxs-lookup"><span data-stu-id="167b6-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="167b6-112">A fenti példa egy virtuális hálózati átjáró hibaelhárítását indítja el.</span><span class="sxs-lookup"><span data-stu-id="167b6-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="167b6-113">A művelet elvégzéséhez néhány percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="167b6-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="167b6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="167b6-114">PARAMETERS</span></span>

### <span data-ttu-id="167b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167b6-115">-DefaultProfile</span></span>
<span data-ttu-id="167b6-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="167b6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="167b6-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="167b6-117">-NetworkWatcher</span></span>
<span data-ttu-id="167b6-118">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="167b6-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="167b6-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="167b6-119">-NetworkWatcherName</span></span>
<span data-ttu-id="167b6-120">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="167b6-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="167b6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="167b6-121">-ResourceGroupName</span></span>
<span data-ttu-id="167b6-122">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="167b6-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="167b6-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="167b6-123">-StorageId</span></span>
<span data-ttu-id="167b6-124">A tárolási azonosító.</span><span class="sxs-lookup"><span data-stu-id="167b6-124">The storage ID.</span></span>

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

### <span data-ttu-id="167b6-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="167b6-125">-StoragePath</span></span>
<span data-ttu-id="167b6-126">A tárterület elérési útja.</span><span class="sxs-lookup"><span data-stu-id="167b6-126">The storage path.</span></span>

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

### <span data-ttu-id="167b6-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="167b6-127">-TargetResourceId</span></span>
<span data-ttu-id="167b6-128">A hibaelhárításra szolgáló erőforrás erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="167b6-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="167b6-129">Példa formátum: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {kapcsolatnév}"</span><span class="sxs-lookup"><span data-stu-id="167b6-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="167b6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167b6-130">CommonParameters</span></span>
<span data-ttu-id="167b6-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="167b6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167b6-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="167b6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167b6-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="167b6-133">INPUTS</span></span>

### <span data-ttu-id="167b6-134">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="167b6-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="167b6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="167b6-135">System.String</span></span>

## <span data-ttu-id="167b6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="167b6-136">OUTPUTS</span></span>

### <span data-ttu-id="167b6-137">Microsoft. Azure. commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="167b6-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="167b6-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="167b6-138">NOTES</span></span>
<span data-ttu-id="167b6-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, hibaelhárítás, VPN, kapcsolat</span><span class="sxs-lookup"><span data-stu-id="167b6-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="167b6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="167b6-140">RELATED LINKS</span></span>

[<span data-ttu-id="167b6-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="167b6-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="167b6-142">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="167b6-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="167b6-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="167b6-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="167b6-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="167b6-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="167b6-145">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="167b6-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="167b6-146">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="167b6-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="167b6-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="167b6-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="167b6-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="167b6-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="167b6-149">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="167b6-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="167b6-150">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="167b6-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="167b6-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="167b6-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="167b6-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="167b6-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="167b6-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="167b6-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
