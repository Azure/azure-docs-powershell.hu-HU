---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: ee92fd78d3a69b38620b2af543e01db7569d3b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492458"
---
# <span data-ttu-id="82ad0-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82ad0-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="82ad0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="82ad0-103">Hálózati figyelő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="82ad0-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ad0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82ad0-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ad0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82ad0-105">DESCRIPTION</span></span>
<span data-ttu-id="82ad0-106">A Remove-AzureRmNetworkWatcher parancsmag eltávolítja a Hálózatfigyelő-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="82ad0-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="82ad0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="82ad0-107">EXAMPLES</span></span>

### <span data-ttu-id="82ad0-108">--------------------------Példa 1: Hálózatfigyelő létrehozása és törlése--------------------------</span><span class="sxs-lookup"><span data-stu-id="82ad0-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="82ad0-109">Ez a példa létrehoz egy hálózati figyelőt egy erőforráscsoporthoz, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="82ad0-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="82ad0-110">Fontos tudni, hogy az előfizetések régiónként csak egy Hálózatfigyelő hozható létre.</span><span class="sxs-lookup"><span data-stu-id="82ad0-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="82ad0-111">Ha a virtuális hálózat törlésekor a kérdését szeretné letiltani, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="82ad0-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="82ad0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82ad0-112">PARAMETERS</span></span>

### <span data-ttu-id="82ad0-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="82ad0-113">-Name</span></span>
<span data-ttu-id="82ad0-114">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="82ad0-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ad0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82ad0-115">-PassThru</span></span>
<span data-ttu-id="82ad0-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="82ad0-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ad0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ad0-117">-ResourceGroupName</span></span>
<span data-ttu-id="82ad0-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="82ad0-118">The resource group name.</span></span>

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

### <span data-ttu-id="82ad0-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="82ad0-119">-Confirm</span></span>
<span data-ttu-id="82ad0-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="82ad0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ad0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ad0-121">-WhatIf</span></span>
<span data-ttu-id="82ad0-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="82ad0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82ad0-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82ad0-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ad0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ad0-124">-DefaultProfile</span></span>
<span data-ttu-id="82ad0-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82ad0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82ad0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ad0-126">CommonParameters</span></span>
<span data-ttu-id="82ad0-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82ad0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ad0-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ad0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ad0-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82ad0-129">INPUTS</span></span>

### <span data-ttu-id="82ad0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="82ad0-130">System.String</span></span>

## <span data-ttu-id="82ad0-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82ad0-131">OUTPUTS</span></span>

### <span data-ttu-id="82ad0-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="82ad0-132">System.Object</span></span>

## <span data-ttu-id="82ad0-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82ad0-133">NOTES</span></span>
<span data-ttu-id="82ad0-134">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="82ad0-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="82ad0-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82ad0-135">RELATED LINKS</span></span>

[<span data-ttu-id="82ad0-136">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82ad0-136">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="82ad0-137">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82ad0-137">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="82ad0-138">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82ad0-138">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82ad0-139">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="82ad0-139">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="82ad0-140">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82ad0-140">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82ad0-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82ad0-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82ad0-142">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82ad0-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82ad0-143">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="82ad0-143">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="82ad0-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="82ad0-144">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="82ad0-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="82ad0-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="82ad0-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="82ad0-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="82ad0-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="82ad0-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
