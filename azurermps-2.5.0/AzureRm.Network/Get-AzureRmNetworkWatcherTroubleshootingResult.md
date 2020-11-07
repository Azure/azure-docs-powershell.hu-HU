---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
ms.openlocfilehash: a2caff32969ac771140bd8c6a5a3b142f4d61485
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849206"
---
# <span data-ttu-id="7a76c-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7a76c-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="7a76c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a76c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a76c-103">A korábban futtatott vagy a jelenleg futó hibaelhárítási művelettől kapott hibaelhárítási eredményt kapja.</span><span class="sxs-lookup"><span data-stu-id="7a76c-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a76c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a76c-104">SYNTAX</span></span>

### <span data-ttu-id="7a76c-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a76c-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a76c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7a76c-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a76c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a76c-107">DESCRIPTION</span></span>
<span data-ttu-id="7a76c-108">A Get-AzureRmNetworkWatcherTroubleshootingResult parancsmag a korábban futtatott vagy a jelenleg futó Start-AzureRmNetworkWatcherResourceTroubleshooting műveletből kapja meg a hibaelhárítási találatokat.</span><span class="sxs-lookup"><span data-stu-id="7a76c-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="7a76c-109">Ha a hibaelhárítási művelet jelenleg folyamatban van, előfordulhat, hogy a művelet elvégzéséhez néhány percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="7a76c-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="7a76c-110">Jelenleg a virtuális hálózati átjárók és a kapcsolatok támogatottak.</span><span class="sxs-lookup"><span data-stu-id="7a76c-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="7a76c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7a76c-111">EXAMPLES</span></span>

### <span data-ttu-id="7a76c-112">---Példa 1: a hibaelhárítás indítása virtuális hálózati átjárón és a találatok beolvasása---</span><span class="sxs-lookup"><span data-stu-id="7a76c-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="7a76c-113">A fenti példa egy virtuális hálózati átjáró hibaelhárítását indítja el.</span><span class="sxs-lookup"><span data-stu-id="7a76c-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="7a76c-114">A művelet elvégzéséhez néhány percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="7a76c-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="7a76c-115">A hibaelhárítást követően a hívás eredményének beolvasásához Get-AzureRmNetworkWatcherTroubleshootingResult hívást kell kezdeményezni az erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="7a76c-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="7a76c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a76c-116">PARAMETERS</span></span>

### <span data-ttu-id="7a76c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a76c-117">-DefaultProfile</span></span>
<span data-ttu-id="7a76c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a76c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a76c-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a76c-119">-NetworkWatcher</span></span>
<span data-ttu-id="7a76c-120">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="7a76c-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="7a76c-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7a76c-121">-NetworkWatcherName</span></span>
<span data-ttu-id="7a76c-122">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="7a76c-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="7a76c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a76c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a76c-124">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a76c-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7a76c-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7a76c-125">-TargetResourceId</span></span>
<span data-ttu-id="7a76c-126">A cél erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7a76c-126">The target resource ID.</span></span>

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

### <span data-ttu-id="7a76c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a76c-127">CommonParameters</span></span>
<span data-ttu-id="7a76c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a76c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a76c-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a76c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a76c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a76c-130">INPUTS</span></span>

### <span data-ttu-id="7a76c-131">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a76c-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7a76c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7a76c-132">System.String</span></span>

## <span data-ttu-id="7a76c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a76c-133">OUTPUTS</span></span>

### <span data-ttu-id="7a76c-134">Microsoft. Azure. commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="7a76c-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="7a76c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a76c-135">NOTES</span></span>
<span data-ttu-id="7a76c-136">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, hibaelhárítás, VPN, kapcsolat</span><span class="sxs-lookup"><span data-stu-id="7a76c-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="7a76c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a76c-137">RELATED LINKS</span></span>

[<span data-ttu-id="7a76c-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7a76c-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7a76c-139">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a76c-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7a76c-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a76c-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7a76c-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a76c-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7a76c-142">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a76c-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a76c-143">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7a76c-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7a76c-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a76c-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a76c-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a76c-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a76c-146">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a76c-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a76c-147">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7a76c-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7a76c-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7a76c-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7a76c-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7a76c-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7a76c-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7a76c-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
