---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: a72f494518b3a511eac3e4b1a92330f666bbca64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843526"
---
# <span data-ttu-id="f7101-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f7101-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="f7101-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7101-102">SYNOPSIS</span></span>
<span data-ttu-id="f7101-103">Elindítja a hibaelhárítást egy hálózati erőforráson az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="f7101-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="f7101-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7101-104">SYNTAX</span></span>

### <span data-ttu-id="f7101-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7101-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7101-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f7101-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7101-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7101-107">DESCRIPTION</span></span>
<span data-ttu-id="f7101-108">Az Start-AzNetworkWatcherResourceTroubleshooting parancsmag az Azure-ban egy hálózati erőforrás hibaelhárítását indítja el, és a potenciális problémákról és a mérséklésekről ad információt.</span><span class="sxs-lookup"><span data-stu-id="f7101-108">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="f7101-109">Jelenleg a virtuális hálózati átjárók és a kapcsolatok támogatottak.</span><span class="sxs-lookup"><span data-stu-id="f7101-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="f7101-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f7101-110">EXAMPLES</span></span>

### <span data-ttu-id="f7101-111">---Példa 1: a hibaelhárítás indítása virtuális hálózati átjárón---</span><span class="sxs-lookup"><span data-stu-id="f7101-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="f7101-112">A fenti példa egy virtuális hálózati átjáró hibaelhárítását indítja el.</span><span class="sxs-lookup"><span data-stu-id="f7101-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="f7101-113">A művelet elvégzéséhez néhány percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="f7101-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="f7101-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7101-114">PARAMETERS</span></span>

### <span data-ttu-id="f7101-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7101-115">-DefaultProfile</span></span>
<span data-ttu-id="f7101-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7101-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7101-117">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7101-117">-NetworkWatcher</span></span>
<span data-ttu-id="f7101-118">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="f7101-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="f7101-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f7101-119">-NetworkWatcherName</span></span>
<span data-ttu-id="f7101-120">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="f7101-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="f7101-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7101-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7101-122">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7101-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f7101-123">-StorageId</span><span class="sxs-lookup"><span data-stu-id="f7101-123">-StorageId</span></span>
<span data-ttu-id="f7101-124">A tárolási azonosító.</span><span class="sxs-lookup"><span data-stu-id="f7101-124">The storage ID.</span></span>

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

### <span data-ttu-id="f7101-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="f7101-125">-StoragePath</span></span>
<span data-ttu-id="f7101-126">A tárterület elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f7101-126">The storage path.</span></span>

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

### <span data-ttu-id="f7101-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f7101-127">-TargetResourceId</span></span>
<span data-ttu-id="f7101-128">A hibaelhárításra szolgáló erőforrás erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7101-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="f7101-129">Példa formátum: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {kapcsolatnév}"</span><span class="sxs-lookup"><span data-stu-id="f7101-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="f7101-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7101-130">CommonParameters</span></span>
<span data-ttu-id="f7101-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7101-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7101-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7101-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7101-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7101-133">INPUTS</span></span>

### <span data-ttu-id="f7101-134">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7101-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f7101-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f7101-135">System.String</span></span>

## <span data-ttu-id="f7101-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7101-136">OUTPUTS</span></span>

### <span data-ttu-id="f7101-137">Microsoft. Azure. commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="f7101-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="f7101-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7101-138">NOTES</span></span>
<span data-ttu-id="f7101-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, hibaelhárítás, VPN, kapcsolat</span><span class="sxs-lookup"><span data-stu-id="f7101-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="f7101-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7101-140">RELATED LINKS</span></span>

[<span data-ttu-id="f7101-141">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f7101-141">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f7101-142">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7101-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f7101-143">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7101-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f7101-144">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f7101-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f7101-145">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7101-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7101-146">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f7101-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f7101-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7101-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7101-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7101-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7101-149">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f7101-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f7101-150">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f7101-150">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f7101-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f7101-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f7101-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f7101-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f7101-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f7101-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
