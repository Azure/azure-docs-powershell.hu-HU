---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2f855175065f743bdfec5fb8dc9c917af262b05b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841569"
---
# <span data-ttu-id="3019b-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3019b-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="3019b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3019b-102">SYNOPSIS</span></span>
<span data-ttu-id="3019b-103">Beolvassa egy erőforrás átfolyási naplózási állapotát.</span><span class="sxs-lookup"><span data-stu-id="3019b-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="3019b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3019b-104">SYNTAX</span></span>

### <span data-ttu-id="3019b-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3019b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3019b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3019b-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3019b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3019b-107">DESCRIPTION</span></span>
<span data-ttu-id="3019b-108">A Get-AzNetworkWatcherFlowLogStatus parancsmag az erőforrás átfolyási naplózási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3019b-108">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="3019b-109">Az állapot azt is tartalmazza, hogy engedélyezve van-e a forgalom naplózása a megadott erőforráshoz, a konfigurált tárterület-fiók a naplók küldéséhez és a naplók adatmegőrzési házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="3019b-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="3019b-110">Jelenleg hálózati biztonsági csoportok támogatottak a forgalom naplózásához.</span><span class="sxs-lookup"><span data-stu-id="3019b-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="3019b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3019b-111">EXAMPLES</span></span>

### <span data-ttu-id="3019b-112">---Példa 1: a forgalom naplózási állapotának beszerzése megadott NSG---</span><span class="sxs-lookup"><span data-stu-id="3019b-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="3019b-113">Ebben a példában bemutatjuk egy hálózati biztonsági csoport átfolyás naplózási állapotát.</span><span class="sxs-lookup"><span data-stu-id="3019b-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="3019b-114">A megadott NSG engedélyezve van a folyamatok naplózása, és nincs adatmegőrzési házirend beállítva.</span><span class="sxs-lookup"><span data-stu-id="3019b-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="3019b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3019b-115">PARAMETERS</span></span>

### <span data-ttu-id="3019b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3019b-116">-AsJob</span></span>
<span data-ttu-id="3019b-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3019b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3019b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3019b-118">-DefaultProfile</span></span>
<span data-ttu-id="3019b-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3019b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3019b-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3019b-120">-NetworkWatcher</span></span>
<span data-ttu-id="3019b-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="3019b-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="3019b-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3019b-122">-NetworkWatcherName</span></span>
<span data-ttu-id="3019b-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="3019b-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="3019b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3019b-124">-ResourceGroupName</span></span>
<span data-ttu-id="3019b-125">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3019b-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3019b-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3019b-126">-TargetResourceId</span></span>
<span data-ttu-id="3019b-127">A cél erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3019b-127">The target resource ID.</span></span>

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

### <span data-ttu-id="3019b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3019b-128">CommonParameters</span></span>
<span data-ttu-id="3019b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3019b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3019b-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3019b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3019b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3019b-131">INPUTS</span></span>

### <span data-ttu-id="3019b-132">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3019b-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3019b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3019b-133">System.String</span></span>

## <span data-ttu-id="3019b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3019b-134">OUTPUTS</span></span>

### <span data-ttu-id="3019b-135">Microsoft. Azure. commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="3019b-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="3019b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3019b-136">NOTES</span></span>
<span data-ttu-id="3019b-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, flow, naplók, flowlog, naplózás</span><span class="sxs-lookup"><span data-stu-id="3019b-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="3019b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3019b-138">RELATED LINKS</span></span>

[<span data-ttu-id="3019b-139">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3019b-139">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3019b-140">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3019b-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3019b-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3019b-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3019b-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3019b-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3019b-143">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3019b-143">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3019b-144">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3019b-144">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3019b-145">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3019b-145">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3019b-146">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3019b-146">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3019b-147">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3019b-147">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3019b-148">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3019b-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3019b-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3019b-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3019b-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3019b-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3019b-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3019b-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3019b-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3019b-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3019b-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3019b-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
