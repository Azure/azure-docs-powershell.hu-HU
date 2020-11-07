---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 276cd57a51b6b457f2f4d205932cdbfabd7613b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843798"
---
# <span data-ttu-id="30825-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="30825-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="30825-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30825-102">SYNOPSIS</span></span>
<span data-ttu-id="30825-103">Hálózati figyelő eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="30825-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="30825-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30825-104">SYNTAX</span></span>

```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30825-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30825-105">DESCRIPTION</span></span>
<span data-ttu-id="30825-106">A Remove-AzNetworkWatcher parancsmag eltávolítja a Hálózatfigyelő-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="30825-106">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="30825-107">Példák</span><span class="sxs-lookup"><span data-stu-id="30825-107">EXAMPLES</span></span>

### <span data-ttu-id="30825-108">--------------------------Példa 1: Hálózatfigyelő létrehozása és törlése--------------------------</span><span class="sxs-lookup"><span data-stu-id="30825-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="30825-109">Ez a példa létrehoz egy hálózati figyelőt egy erőforráscsoporthoz, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="30825-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="30825-110">Fontos tudni, hogy az előfizetések régiónként csak egy Hálózatfigyelő hozható létre.</span><span class="sxs-lookup"><span data-stu-id="30825-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="30825-111">Ha a virtuális hálózat törlésekor a kérdését szeretné letiltani, használja a-Force jelölőt.</span><span class="sxs-lookup"><span data-stu-id="30825-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="30825-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30825-112">PARAMETERS</span></span>

### <span data-ttu-id="30825-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30825-113">-AsJob</span></span>
<span data-ttu-id="30825-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="30825-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30825-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30825-115">-DefaultProfile</span></span>
<span data-ttu-id="30825-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30825-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30825-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30825-117">-Name</span></span>
<span data-ttu-id="30825-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="30825-118">The resource name.</span></span>

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

### <span data-ttu-id="30825-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30825-119">-PassThru</span></span>
<span data-ttu-id="30825-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="30825-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="30825-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30825-121">-ResourceGroupName</span></span>
<span data-ttu-id="30825-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="30825-122">The resource group name.</span></span>

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

### <span data-ttu-id="30825-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="30825-123">-Confirm</span></span>
<span data-ttu-id="30825-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="30825-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30825-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30825-125">-WhatIf</span></span>
<span data-ttu-id="30825-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="30825-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30825-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30825-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30825-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30825-128">CommonParameters</span></span>
<span data-ttu-id="30825-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30825-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30825-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30825-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30825-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30825-131">INPUTS</span></span>

### <span data-ttu-id="30825-132">System. String</span><span class="sxs-lookup"><span data-stu-id="30825-132">System.String</span></span>

## <span data-ttu-id="30825-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30825-133">OUTPUTS</span></span>

### <span data-ttu-id="30825-134">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="30825-134">System.Object</span></span>

## <span data-ttu-id="30825-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30825-135">NOTES</span></span>
<span data-ttu-id="30825-136">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő</span><span class="sxs-lookup"><span data-stu-id="30825-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="30825-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30825-137">RELATED LINKS</span></span>

[<span data-ttu-id="30825-138">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="30825-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="30825-139">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="30825-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="30825-140">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="30825-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="30825-141">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="30825-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="30825-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="30825-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="30825-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="30825-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="30825-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="30825-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="30825-145">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="30825-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="30825-146">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="30825-146">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="30825-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="30825-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="30825-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="30825-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="30825-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="30825-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
