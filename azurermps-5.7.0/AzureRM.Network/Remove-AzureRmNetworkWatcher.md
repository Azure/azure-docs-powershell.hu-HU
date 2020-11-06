---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: 4fd6da3388b4058a3aa4bee2fe918fb063c8fd6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497528"
---
# <span data-ttu-id="cd9c4-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd9c4-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="cd9c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd9c4-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9c4-103">Hálózati figyelő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd9c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd9c4-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd9c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd9c4-105">DESCRIPTION</span></span>
<span data-ttu-id="cd9c4-106">A Remove-AzureRmNetworkWatcher parancsmag eltávolítja a Hálózatfigyelő-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="cd9c4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd9c4-107">EXAMPLES</span></span>

### <span data-ttu-id="cd9c4-108">--------------------------Példa 1: Hálózatfigyelő létrehozása és törlése--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd9c4-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="cd9c4-109">Ez a példa létrehoz egy hálózati figyelőt egy erőforráscsoporthoz, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="cd9c4-110">Fontos tudni, hogy az előfizetések régiónként csak egy Hálózatfigyelő hozható létre.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="cd9c4-111">Ha a virtuális hálózat törlésekor a kérdését szeretné letiltani, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="cd9c4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd9c4-112">PARAMETERS</span></span>

### <span data-ttu-id="cd9c4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd9c4-113">-AsJob</span></span>
<span data-ttu-id="cd9c4-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cd9c4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd9c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9c4-115">-DefaultProfile</span></span>
<span data-ttu-id="cd9c4-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd9c4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd9c4-117">-Name</span></span>
<span data-ttu-id="cd9c4-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd9c4-119">-PassThru</span></span>
<span data-ttu-id="cd9c4-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cd9c4-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd9c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="cd9c4-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-122">The resource group name.</span></span>

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

### <span data-ttu-id="cd9c4-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd9c4-123">-Confirm</span></span>
<span data-ttu-id="cd9c4-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9c4-125">-WhatIf</span></span>
<span data-ttu-id="cd9c4-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd9c4-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd9c4-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9c4-128">CommonParameters</span></span>
<span data-ttu-id="cd9c4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd9c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9c4-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9c4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9c4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd9c4-131">INPUTS</span></span>

### <span data-ttu-id="cd9c4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cd9c4-132">System.String</span></span>

## <span data-ttu-id="cd9c4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd9c4-133">OUTPUTS</span></span>

### <span data-ttu-id="cd9c4-134">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="cd9c4-134">System.Object</span></span>

## <span data-ttu-id="cd9c4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd9c4-135">NOTES</span></span>
<span data-ttu-id="cd9c4-136">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="cd9c4-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="cd9c4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd9c4-137">RELATED LINKS</span></span>

[<span data-ttu-id="cd9c4-138">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd9c4-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cd9c4-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd9c4-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cd9c4-140">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd9c4-140">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd9c4-141">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cd9c4-141">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="cd9c4-142">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd9c4-142">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd9c4-143">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd9c4-143">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd9c4-144">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd9c4-144">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd9c4-145">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cd9c4-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="cd9c4-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cd9c4-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="cd9c4-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cd9c4-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cd9c4-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cd9c4-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="cd9c4-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cd9c4-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
