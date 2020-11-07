---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
ms.openlocfilehash: 96d3bea781b0c595b54387a9b07b085f173d7b0a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848781"
---
# <span data-ttu-id="89cd9-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="89cd9-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="89cd9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="89cd9-103">Beolvassa egy erőforrás átfolyási naplózási állapotát.</span><span class="sxs-lookup"><span data-stu-id="89cd9-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89cd9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89cd9-104">SYNTAX</span></span>

### <span data-ttu-id="89cd9-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89cd9-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89cd9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="89cd9-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89cd9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="89cd9-107">DESCRIPTION</span></span>
<span data-ttu-id="89cd9-108">A Get-AzureRmNetworkWatcherFlowLogStatus parancsmag az erőforrás átfolyási naplózási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="89cd9-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="89cd9-109">Az állapot azt is tartalmazza, hogy engedélyezve van-e a forgalom naplózása a megadott erőforráshoz, a konfigurált tárterület-fiók a naplók küldéséhez és a naplók adatmegőrzési házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="89cd9-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="89cd9-110">Jelenleg hálózati biztonsági csoportok támogatottak a forgalom naplózásához.</span><span class="sxs-lookup"><span data-stu-id="89cd9-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="89cd9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="89cd9-111">EXAMPLES</span></span>

### <span data-ttu-id="89cd9-112">---Példa 1: a forgalom naplózási állapotának beszerzése megadott NSG---</span><span class="sxs-lookup"><span data-stu-id="89cd9-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="89cd9-113">Ebben a példában bemutatjuk egy hálózati biztonsági csoport átfolyás naplózási állapotát.</span><span class="sxs-lookup"><span data-stu-id="89cd9-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="89cd9-114">A megadott NSG engedélyezve van a folyamatok naplózása, és nincs adatmegőrzési házirend beállítva.</span><span class="sxs-lookup"><span data-stu-id="89cd9-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="89cd9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89cd9-115">PARAMETERS</span></span>

### <span data-ttu-id="89cd9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89cd9-116">-AsJob</span></span>
<span data-ttu-id="89cd9-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="89cd9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89cd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89cd9-118">-DefaultProfile</span></span>
<span data-ttu-id="89cd9-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89cd9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89cd9-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89cd9-120">-NetworkWatcher</span></span>
<span data-ttu-id="89cd9-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="89cd9-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="89cd9-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="89cd9-122">-NetworkWatcherName</span></span>
<span data-ttu-id="89cd9-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="89cd9-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="89cd9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89cd9-124">-ResourceGroupName</span></span>
<span data-ttu-id="89cd9-125">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="89cd9-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="89cd9-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="89cd9-126">-TargetResourceId</span></span>
<span data-ttu-id="89cd9-127">A cél erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="89cd9-127">The target resource ID.</span></span>

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

### <span data-ttu-id="89cd9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89cd9-128">CommonParameters</span></span>
<span data-ttu-id="89cd9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89cd9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89cd9-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89cd9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89cd9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89cd9-131">INPUTS</span></span>

### <span data-ttu-id="89cd9-132">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89cd9-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="89cd9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="89cd9-133">System.String</span></span>

## <span data-ttu-id="89cd9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89cd9-134">OUTPUTS</span></span>

### <span data-ttu-id="89cd9-135">Microsoft. Azure. commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="89cd9-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="89cd9-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89cd9-136">NOTES</span></span>
<span data-ttu-id="89cd9-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, flow, naplók, flowlog, naplózás</span><span class="sxs-lookup"><span data-stu-id="89cd9-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="89cd9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89cd9-138">RELATED LINKS</span></span>

[<span data-ttu-id="89cd9-139">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="89cd9-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="89cd9-140">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89cd9-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="89cd9-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89cd9-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="89cd9-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89cd9-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="89cd9-143">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89cd9-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89cd9-144">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="89cd9-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="89cd9-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89cd9-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89cd9-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89cd9-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89cd9-147">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89cd9-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89cd9-148">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="89cd9-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="89cd9-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="89cd9-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="89cd9-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="89cd9-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="89cd9-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="89cd9-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="89cd9-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="89cd9-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="89cd9-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="89cd9-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
