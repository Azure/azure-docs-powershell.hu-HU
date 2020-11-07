---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b3095aace7fa8e1959e51ef64aa92b6d2bcaffba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843793"
---
# <span data-ttu-id="6a177-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6a177-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="6a177-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a177-102">SYNOPSIS</span></span>
<span data-ttu-id="6a177-103">A csomag-rögzítő erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="6a177-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="6a177-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a177-104">SYNTAX</span></span>

### <span data-ttu-id="6a177-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a177-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a177-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6a177-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a177-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a177-107">DESCRIPTION</span></span>
<span data-ttu-id="6a177-108">A Remove-AzNetworkWatcherPacketCapture eltávolítja a csomag-rögzítő erőforrást.</span><span class="sxs-lookup"><span data-stu-id="6a177-108">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="6a177-109">A Remove-AzNetworkWatcherPacketCapture hívása ajánlott Stop-AzNetworkWatcherPacketCapture hívás előtt.</span><span class="sxs-lookup"><span data-stu-id="6a177-109">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="6a177-110">Ha a csomag rögzítési munkamenete akkor fut, ha a Remove-AzNetworkWatcherPacketCapture a csomagkapcsolt adatrögzítőt nem lehet menteni.</span><span class="sxs-lookup"><span data-stu-id="6a177-110">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="6a177-111">Ha a munkamenet megszűnik az Eltávolítás előtt, a program nem távolítja el a rögzítési adatot tartalmazó. Cap fájlt.</span><span class="sxs-lookup"><span data-stu-id="6a177-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="6a177-112">Példák</span><span class="sxs-lookup"><span data-stu-id="6a177-112">EXAMPLES</span></span>

### <span data-ttu-id="6a177-113">---Példa 1: a csomag rögzítési munkamenetének eltávolítása –</span><span class="sxs-lookup"><span data-stu-id="6a177-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="6a177-114">Ebben a példában eltávolítunk egy "PacketCaptureTest" nevű csomag-rögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="6a177-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="6a177-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a177-115">PARAMETERS</span></span>

### <span data-ttu-id="6a177-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a177-116">-AsJob</span></span>
<span data-ttu-id="6a177-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6a177-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a177-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a177-118">-DefaultProfile</span></span>
<span data-ttu-id="6a177-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a177-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a177-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6a177-120">-NetworkWatcher</span></span>
<span data-ttu-id="6a177-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6a177-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="6a177-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6a177-122">-NetworkWatcherName</span></span>
<span data-ttu-id="6a177-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="6a177-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="6a177-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="6a177-124">-PacketCaptureName</span></span>
<span data-ttu-id="6a177-125">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="6a177-125">The packet capture name.</span></span>

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

### <span data-ttu-id="6a177-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a177-126">-PassThru</span></span>
<span data-ttu-id="6a177-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6a177-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6a177-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a177-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a177-129">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6a177-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6a177-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a177-130">-Confirm</span></span>
<span data-ttu-id="6a177-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a177-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a177-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a177-132">-WhatIf</span></span>
<span data-ttu-id="6a177-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a177-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a177-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a177-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a177-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a177-135">CommonParameters</span></span>
<span data-ttu-id="6a177-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a177-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a177-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a177-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a177-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a177-138">INPUTS</span></span>

### <span data-ttu-id="6a177-139">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6a177-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6a177-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6a177-140">System.String</span></span>

## <span data-ttu-id="6a177-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a177-141">OUTPUTS</span></span>

### <span data-ttu-id="6a177-142">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="6a177-142">System.Object</span></span>

## <span data-ttu-id="6a177-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a177-143">NOTES</span></span>
<span data-ttu-id="6a177-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom, eltávolítás</span><span class="sxs-lookup"><span data-stu-id="6a177-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="6a177-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a177-145">RELATED LINKS</span></span>

[<span data-ttu-id="6a177-146">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6a177-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6a177-147">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6a177-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6a177-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6a177-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6a177-149">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6a177-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6a177-150">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6a177-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6a177-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6a177-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6a177-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6a177-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6a177-153">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6a177-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6a177-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6a177-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6a177-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6a177-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6a177-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6a177-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6a177-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6a177-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
