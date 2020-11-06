---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
ms.openlocfilehash: 36a584be829cd3d85d900c1e0b251dc7d49e95e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496380"
---
# <span data-ttu-id="3e956-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3e956-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="3e956-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e956-102">SYNOPSIS</span></span>
<span data-ttu-id="3e956-103">A megadott forrású VM és rendeltetési hely kapcsolati adatait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3e956-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e956-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e956-104">SYNTAX</span></span>

### <span data-ttu-id="3e956-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e956-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e956-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3e956-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e956-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e956-107">DESCRIPTION</span></span>
<span data-ttu-id="3e956-108">A Test-AzureRmNetworkWatcherConnectivity parancsmag a megadott forrású VM és a célhely kapcsolati adatait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3e956-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="3e956-109">Ha a forrás és a cél közötti kapcsolat nem hozható létre, a parancsmag részleteket ad meg a problémáról.</span><span class="sxs-lookup"><span data-stu-id="3e956-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="3e956-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3e956-110">EXAMPLES</span></span>

### <span data-ttu-id="3e956-111">---------------Példa 1: tesztelje a Hálózatfigyelő egy VM-kapcsolatát egy webhelyre---------------</span><span class="sxs-lookup"><span data-stu-id="3e956-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="3e956-112">Ebben a példában a VM-től az Azure-www.bing.com való kapcsolatot teszteljük.</span><span class="sxs-lookup"><span data-stu-id="3e956-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="3e956-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e956-113">PARAMETERS</span></span>

### <span data-ttu-id="3e956-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e956-114">-AsJob</span></span>
<span data-ttu-id="3e956-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3e956-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e956-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e956-116">-DefaultProfile</span></span>
<span data-ttu-id="3e956-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e956-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e956-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="3e956-118">-DestinationAddress</span></span>
<span data-ttu-id="3e956-119">Annak az erőforrásnak az IP-címe vagy URI-azonosítója, amelyhez csatlakozási kísérletet tesz.</span><span class="sxs-lookup"><span data-stu-id="3e956-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e956-120">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="3e956-120">-DestinationId</span></span>
<span data-ttu-id="3e956-121">Annak az erőforrásnak az azonosítója, amelyhez csatlakozási kísérletet fog tenni.</span><span class="sxs-lookup"><span data-stu-id="3e956-121">The ID of the resource to which a connection attempt will be made.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e956-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3e956-122">-DestinationPort</span></span>
<span data-ttu-id="3e956-123">Annak a portnak a végrehajtása, amelyen ellenőrizni fogja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="3e956-123">Port on which check connectivity will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e956-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3e956-124">-NetworkWatcher</span></span>
<span data-ttu-id="3e956-125">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="3e956-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="3e956-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3e956-126">-NetworkWatcherName</span></span>
<span data-ttu-id="3e956-127">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="3e956-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e956-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e956-128">-ResourceGroupName</span></span>
<span data-ttu-id="3e956-129">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e956-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3e956-130">-SourceId forrásazonosító</span><span class="sxs-lookup"><span data-stu-id="3e956-130">-SourceId</span></span>
<span data-ttu-id="3e956-131">Annak az erőforrásnak az azonosítója, amelyből a kapcsolódási ellenőrzést kezdeményezni kívánja.</span><span class="sxs-lookup"><span data-stu-id="3e956-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="3e956-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="3e956-132">-SourcePort</span></span>
<span data-ttu-id="3e956-133">Annak a forrásnak a portja, amelyből a kapcsolódási ellenőrzést végrehajtja.</span><span class="sxs-lookup"><span data-stu-id="3e956-133">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e956-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e956-134">CommonParameters</span></span>
<span data-ttu-id="3e956-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e956-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e956-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e956-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e956-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e956-137">INPUTS</span></span>

### <span data-ttu-id="3e956-138">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3e956-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3e956-139">System. String System. Int32</span><span class="sxs-lookup"><span data-stu-id="3e956-139">System.String System.Int32</span></span>

## <span data-ttu-id="3e956-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e956-140">OUTPUTS</span></span>

### <span data-ttu-id="3e956-141">Microsoft. Azure. commands. Network. models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="3e956-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="3e956-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e956-142">NOTES</span></span>
<span data-ttu-id="3e956-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, hálózati figyelő</span><span class="sxs-lookup"><span data-stu-id="3e956-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="3e956-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e956-144">RELATED LINKS</span></span>

<span data-ttu-id="3e956-145">[Új – AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="3e956-145">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="3e956-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="3e956-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="3e956-147">[Új – AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Új – AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="3e956-147">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
