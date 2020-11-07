---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f250615837f4953f63a4c5ff5f0a0ea965691856
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843598"
---
# <span data-ttu-id="4e0cf-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e0cf-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="4e0cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0cf-103">Beállítja a folyamatábra erőforrás-naplózását.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="4e0cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e0cf-104">SYNTAX</span></span>

### <span data-ttu-id="4e0cf-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e0cf-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e0cf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4e0cf-106">SetByName</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e0cf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e0cf-107">DESCRIPTION</span></span>
<span data-ttu-id="4e0cf-108">A Set-AzNetworkWatcherConfigFlowLog beállítja a cél erőforráshoz tartozó folyamatábra naplózását.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-108">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="4e0cf-109">A megadható tulajdonságok: az adott erőforrásra vonatkozóan engedélyezve van-e a forgalom naplózása, a konfigurált tárterület-fiók a naplók küldéséhez és a naplók adatmegőrzési házirendjéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="4e0cf-110">Jelenleg hálózati biztonsági csoportok támogatottak a forgalom naplózásához.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="4e0cf-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4e0cf-111">EXAMPLES</span></span>

### <span data-ttu-id="4e0cf-112">---Példa 1: a forgalom naplózásának beállítása megadott NSG---</span><span class="sxs-lookup"><span data-stu-id="4e0cf-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="4e0cf-113">Ebben a példában a naplózási állapotot egy hálózati biztonsági csoporthoz konfiguráltuk.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="4e0cf-114">A válaszban láthatja, hogy a megadott NSG engedélyezve van a forgalom naplózása, és nincs adatmegőrzési házirend beállítva.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="4e0cf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e0cf-115">PARAMETERS</span></span>

### <span data-ttu-id="4e0cf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e0cf-116">-AsJob</span></span>
<span data-ttu-id="4e0cf-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4e0cf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e0cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0cf-118">-DefaultProfile</span></span>
<span data-ttu-id="4e0cf-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e0cf-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e0cf-120">-EnableFlowLog</span></span>
<span data-ttu-id="4e0cf-121">A forgalom naplózásának engedélyezésére/letiltására szolgáló jelölő</span><span class="sxs-lookup"><span data-stu-id="4e0cf-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0cf-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="4e0cf-122">-EnableRetention</span></span>
<span data-ttu-id="4e0cf-123">Jelölő az adatmegőrzés engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0cf-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e0cf-124">-NetworkWatcher</span></span>
<span data-ttu-id="4e0cf-125">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="4e0cf-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4e0cf-126">-NetworkWatcherName</span></span>
<span data-ttu-id="4e0cf-127">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="4e0cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e0cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="4e0cf-129">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4e0cf-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4e0cf-130">-RetentionInDays</span></span>
<span data-ttu-id="4e0cf-131">A átfolyási napló rekordjainak megtartására szolgáló napok száma.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="4e0cf-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4e0cf-132">-StorageAccountId</span></span>
<span data-ttu-id="4e0cf-133">Annak a tárolási fióknak az azonosítója, amely a folyamatábra tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="4e0cf-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4e0cf-134">-TargetResourceId</span></span>
<span data-ttu-id="4e0cf-135">A cél erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-135">The target resource ID.</span></span>

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

### <span data-ttu-id="4e0cf-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e0cf-136">-Confirm</span></span>
<span data-ttu-id="4e0cf-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0cf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e0cf-138">-WhatIf</span></span>
<span data-ttu-id="4e0cf-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e0cf-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e0cf-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0cf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0cf-141">CommonParameters</span></span>
<span data-ttu-id="4e0cf-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e0cf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0cf-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e0cf-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0cf-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e0cf-144">INPUTS</span></span>

### <span data-ttu-id="4e0cf-145">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e0cf-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4e0cf-146">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="4e0cf-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="4e0cf-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e0cf-147">OUTPUTS</span></span>

### <span data-ttu-id="4e0cf-148">Microsoft. Azure. commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e0cf-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="4e0cf-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e0cf-149">NOTES</span></span>
<span data-ttu-id="4e0cf-150">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, flow, naplók, flowlog, naplózás</span><span class="sxs-lookup"><span data-stu-id="4e0cf-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="4e0cf-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e0cf-151">RELATED LINKS</span></span>

[<span data-ttu-id="4e0cf-152">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4e0cf-152">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4e0cf-153">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e0cf-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4e0cf-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e0cf-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4e0cf-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e0cf-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4e0cf-156">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e0cf-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e0cf-157">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4e0cf-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4e0cf-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e0cf-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e0cf-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e0cf-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e0cf-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e0cf-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e0cf-161">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4e0cf-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4e0cf-162">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4e0cf-162">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4e0cf-163">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4e0cf-163">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4e0cf-164">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4e0cf-164">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4e0cf-165">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4e0cf-165">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4e0cf-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4e0cf-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
