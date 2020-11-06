---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 034cca094bf6dd7d3911e3e705e03888f0ea10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503064"
---
# <span data-ttu-id="06d62-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06d62-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="06d62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06d62-102">SYNOPSIS</span></span>
<span data-ttu-id="06d62-103">A csomag-rögzítő erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="06d62-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06d62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06d62-104">SYNTAX</span></span>

### <span data-ttu-id="06d62-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06d62-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06d62-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="06d62-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06d62-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="06d62-107">DESCRIPTION</span></span>
<span data-ttu-id="06d62-108">A Remove-AzureRmNetworkWatcherPacketCapture eltávolítja a csomag-rögzítő erőforrást.</span><span class="sxs-lookup"><span data-stu-id="06d62-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="06d62-109">A Remove-AzureRmNetworkWatcherPacketCapture hívása ajánlott Stop-AzureRmNetworkWatcherPacketCapture hívás előtt.</span><span class="sxs-lookup"><span data-stu-id="06d62-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="06d62-110">Ha a csomag rögzítési munkamenete akkor fut, ha a Remove-AzureRmNetworkWatcherPacketCapture a csomagkapcsolt adatrögzítőt nem lehet menteni.</span><span class="sxs-lookup"><span data-stu-id="06d62-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="06d62-111">Ha a munkamenet megszűnik az Eltávolítás előtt, a program nem távolítja el a rögzítési adatot tartalmazó. Cap fájlt.</span><span class="sxs-lookup"><span data-stu-id="06d62-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="06d62-112">Példák</span><span class="sxs-lookup"><span data-stu-id="06d62-112">EXAMPLES</span></span>

### <span data-ttu-id="06d62-113">---Példa 1: a csomag rögzítési munkamenetének eltávolítása –</span><span class="sxs-lookup"><span data-stu-id="06d62-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="06d62-114">Ebben a példában eltávolítunk egy "PacketCaptureTest" nevű csomag-rögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="06d62-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="06d62-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06d62-115">PARAMETERS</span></span>

### <span data-ttu-id="06d62-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06d62-116">-AsJob</span></span>
<span data-ttu-id="06d62-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="06d62-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06d62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d62-118">-DefaultProfile</span></span>
<span data-ttu-id="06d62-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06d62-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06d62-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="06d62-120">-NetworkWatcher</span></span>
<span data-ttu-id="06d62-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="06d62-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="06d62-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="06d62-122">-NetworkWatcherName</span></span>
<span data-ttu-id="06d62-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="06d62-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="06d62-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="06d62-124">-PacketCaptureName</span></span>
<span data-ttu-id="06d62-125">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="06d62-125">The packet capture name.</span></span>

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

### <span data-ttu-id="06d62-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06d62-126">-PassThru</span></span>
<span data-ttu-id="06d62-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="06d62-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="06d62-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d62-128">-ResourceGroupName</span></span>
<span data-ttu-id="06d62-129">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="06d62-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="06d62-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06d62-130">-Confirm</span></span>
<span data-ttu-id="06d62-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06d62-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06d62-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d62-132">-WhatIf</span></span>
<span data-ttu-id="06d62-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06d62-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06d62-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06d62-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06d62-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d62-135">CommonParameters</span></span>
<span data-ttu-id="06d62-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06d62-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d62-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d62-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d62-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06d62-138">INPUTS</span></span>

### <span data-ttu-id="06d62-139">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="06d62-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="06d62-140">System. String</span><span class="sxs-lookup"><span data-stu-id="06d62-140">System.String</span></span>

## <span data-ttu-id="06d62-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06d62-141">OUTPUTS</span></span>

### <span data-ttu-id="06d62-142">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="06d62-142">System.Object</span></span>

## <span data-ttu-id="06d62-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06d62-143">NOTES</span></span>
<span data-ttu-id="06d62-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom, eltávolítás</span><span class="sxs-lookup"><span data-stu-id="06d62-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="06d62-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06d62-145">RELATED LINKS</span></span>

[<span data-ttu-id="06d62-146">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06d62-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06d62-147">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="06d62-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="06d62-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06d62-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06d62-149">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06d62-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06d62-150">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="06d62-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="06d62-151">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="06d62-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="06d62-152">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="06d62-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="06d62-153">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="06d62-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="06d62-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="06d62-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="06d62-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="06d62-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="06d62-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="06d62-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="06d62-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="06d62-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
