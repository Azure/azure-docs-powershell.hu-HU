---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: c3d1e7e3a76a2561c77c8d580b7365f8fd2e6fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841554"
---
# <span data-ttu-id="ac926-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ac926-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="ac926-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac926-102">SYNOPSIS</span></span>
<span data-ttu-id="ac926-103">A korábban futtatott vagy a jelenleg futó hibaelhárítási művelettől kapott hibaelhárítási eredményt kapja.</span><span class="sxs-lookup"><span data-stu-id="ac926-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="ac926-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac926-104">SYNTAX</span></span>

### <span data-ttu-id="ac926-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac926-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac926-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ac926-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac926-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac926-107">DESCRIPTION</span></span>
<span data-ttu-id="ac926-108">A Get-AzNetworkWatcherTroubleshootingResult parancsmag a korábban futtatott vagy a jelenleg futó Start-AzNetworkWatcherResourceTroubleshooting műveletből kapja meg a hibaelhárítási találatokat.</span><span class="sxs-lookup"><span data-stu-id="ac926-108">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="ac926-109">Ha a hibaelhárítási művelet jelenleg folyamatban van, előfordulhat, hogy a művelet elvégzéséhez néhány percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="ac926-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="ac926-110">Jelenleg a virtuális hálózati átjárók és a kapcsolatok támogatottak.</span><span class="sxs-lookup"><span data-stu-id="ac926-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="ac926-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ac926-111">EXAMPLES</span></span>

### <span data-ttu-id="ac926-112">---Példa 1: a hibaelhárítás indítása virtuális hálózati átjárón és a találatok beolvasása---</span><span class="sxs-lookup"><span data-stu-id="ac926-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="ac926-113">A fenti példa egy virtuális hálózati átjáró hibaelhárítását indítja el.</span><span class="sxs-lookup"><span data-stu-id="ac926-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="ac926-114">A művelet elvégzéséhez néhány percet is igénybe vehet.</span><span class="sxs-lookup"><span data-stu-id="ac926-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="ac926-115">A hibaelhárítást követően a hívás eredményének beolvasásához Get-AzNetworkWatcherTroubleshootingResult hívást kell kezdeményezni az erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="ac926-115">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="ac926-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac926-116">PARAMETERS</span></span>

### <span data-ttu-id="ac926-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac926-117">-DefaultProfile</span></span>
<span data-ttu-id="ac926-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac926-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac926-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac926-119">-NetworkWatcher</span></span>
<span data-ttu-id="ac926-120">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ac926-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="ac926-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ac926-121">-NetworkWatcherName</span></span>
<span data-ttu-id="ac926-122">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="ac926-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="ac926-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac926-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac926-124">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac926-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ac926-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ac926-125">-TargetResourceId</span></span>
<span data-ttu-id="ac926-126">A cél erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ac926-126">The target resource ID.</span></span>

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

### <span data-ttu-id="ac926-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac926-127">CommonParameters</span></span>
<span data-ttu-id="ac926-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac926-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac926-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac926-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac926-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac926-130">INPUTS</span></span>

### <span data-ttu-id="ac926-131">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac926-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ac926-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ac926-132">System.String</span></span>

## <span data-ttu-id="ac926-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac926-133">OUTPUTS</span></span>

### <span data-ttu-id="ac926-134">Microsoft. Azure. commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="ac926-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="ac926-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac926-135">NOTES</span></span>
<span data-ttu-id="ac926-136">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, hibaelhárítás, VPN, kapcsolat</span><span class="sxs-lookup"><span data-stu-id="ac926-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="ac926-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac926-137">RELATED LINKS</span></span>

[<span data-ttu-id="ac926-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ac926-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ac926-139">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac926-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ac926-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac926-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ac926-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac926-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ac926-142">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac926-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac926-143">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ac926-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ac926-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac926-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac926-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac926-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac926-146">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac926-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac926-147">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ac926-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ac926-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ac926-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ac926-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ac926-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ac926-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ac926-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
