---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: e8ce107453a447ef2da4cb8528b2f3e1f24a3ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494804"
---
# <span data-ttu-id="c0efb-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c0efb-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="c0efb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0efb-102">SYNOPSIS</span></span>
<span data-ttu-id="c0efb-103">Beállítja a folyamatábra erőforrás-naplózását.</span><span class="sxs-lookup"><span data-stu-id="c0efb-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0efb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0efb-104">SYNTAX</span></span>

### <span data-ttu-id="c0efb-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0efb-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0efb-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c0efb-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0efb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0efb-107">DESCRIPTION</span></span>
<span data-ttu-id="c0efb-108">A Set-AzureRmNetworkWatcherConfigFlowLog beállítja a cél erőforráshoz tartozó folyamatábra naplózását.</span><span class="sxs-lookup"><span data-stu-id="c0efb-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="c0efb-109">A megadható tulajdonságok: az adott erőforrásra vonatkozóan engedélyezve van-e a forgalom naplózása, a konfigurált tárterület-fiók a naplók küldéséhez és a naplók adatmegőrzési házirendjéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="c0efb-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="c0efb-110">Jelenleg hálózati biztonsági csoportok támogatottak a forgalom naplózásához.</span><span class="sxs-lookup"><span data-stu-id="c0efb-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="c0efb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c0efb-111">EXAMPLES</span></span>

### <span data-ttu-id="c0efb-112">---Példa 1: a forgalom naplózásának beállítása megadott NSG---</span><span class="sxs-lookup"><span data-stu-id="c0efb-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="c0efb-113">Ebben a példában a naplózási állapotot egy hálózati biztonsági csoporthoz konfiguráltuk.</span><span class="sxs-lookup"><span data-stu-id="c0efb-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="c0efb-114">A válaszban láthatja, hogy a megadott NSG engedélyezve van a forgalom naplózása, és nincs adatmegőrzési házirend beállítva.</span><span class="sxs-lookup"><span data-stu-id="c0efb-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="c0efb-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0efb-115">PARAMETERS</span></span>

### <span data-ttu-id="c0efb-116">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="c0efb-116">-EnableFlowLog</span></span>
<span data-ttu-id="c0efb-117">A forgalom naplózásának engedélyezésére/letiltására szolgáló jelölő</span><span class="sxs-lookup"><span data-stu-id="c0efb-117">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0efb-118">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="c0efb-118">-EnableRetention</span></span>
<span data-ttu-id="c0efb-119">Jelölő az adatmegőrzés engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="c0efb-119">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0efb-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0efb-120">-NetworkWatcher</span></span>
<span data-ttu-id="c0efb-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="c0efb-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="c0efb-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c0efb-122">-NetworkWatcherName</span></span>
<span data-ttu-id="c0efb-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="c0efb-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="c0efb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0efb-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0efb-125">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c0efb-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c0efb-126">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c0efb-126">-RetentionInDays</span></span>
<span data-ttu-id="c0efb-127">A átfolyási napló rekordjainak megtartására szolgáló napok száma.</span><span class="sxs-lookup"><span data-stu-id="c0efb-127">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0efb-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c0efb-128">-StorageAccountId</span></span>
<span data-ttu-id="c0efb-129">Annak a tárolási fióknak az azonosítója, amely a folyamatábra tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="c0efb-129">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="c0efb-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c0efb-130">-TargetResourceId</span></span>
<span data-ttu-id="c0efb-131">A cél erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c0efb-131">The target resource ID.</span></span>

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

### <span data-ttu-id="c0efb-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0efb-132">-Confirm</span></span>
<span data-ttu-id="c0efb-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0efb-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0efb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0efb-134">-WhatIf</span></span>
<span data-ttu-id="c0efb-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0efb-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0efb-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0efb-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0efb-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0efb-137">-DefaultProfile</span></span>
<span data-ttu-id="c0efb-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0efb-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0efb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0efb-139">CommonParameters</span></span>
<span data-ttu-id="c0efb-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0efb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0efb-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0efb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0efb-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0efb-142">INPUTS</span></span>

### <span data-ttu-id="c0efb-143">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0efb-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c0efb-144">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="c0efb-144">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="c0efb-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0efb-145">OUTPUTS</span></span>

### <span data-ttu-id="c0efb-146">Microsoft. Azure. commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="c0efb-146">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="c0efb-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0efb-147">NOTES</span></span>
<span data-ttu-id="c0efb-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, flow, naplók, flowlog, naplózás</span><span class="sxs-lookup"><span data-stu-id="c0efb-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="c0efb-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0efb-149">RELATED LINKS</span></span>

[<span data-ttu-id="c0efb-150">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c0efb-150">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c0efb-151">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0efb-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0efb-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0efb-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0efb-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0efb-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0efb-154">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0efb-154">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0efb-155">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c0efb-155">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c0efb-156">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0efb-156">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0efb-157">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0efb-157">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0efb-158">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0efb-158">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0efb-159">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c0efb-159">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c0efb-160">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c0efb-160">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c0efb-161">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c0efb-161">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c0efb-162">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c0efb-162">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c0efb-163">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c0efb-163">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c0efb-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c0efb-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
