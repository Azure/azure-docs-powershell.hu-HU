---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: c4d31de526132974defc6b3d28542e1ec8de4c67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843514"
---
# <span data-ttu-id="d0b7f-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0b7f-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d0b7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b7f-103">Futó csomag rögzítési munkamenetének leállítása</span><span class="sxs-lookup"><span data-stu-id="d0b7f-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="d0b7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0b7f-104">SYNTAX</span></span>

### <span data-ttu-id="d0b7f-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0b7f-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0b7f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d0b7f-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0b7f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0b7f-107">DESCRIPTION</span></span>
<span data-ttu-id="d0b7f-108">A Stop-AzNetworkWatcherPacketCapture leállítja a futtatott csomag rögzítési munkamenetét.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-108">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="d0b7f-109">Miután leállította a munkamenetet, a csomag rögzítésére szolgáló fájlt feltölti a rendszer, és a rendszer a VM-re menti a számítógépen, a konfigurációtól függően.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="d0b7f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d0b7f-110">EXAMPLES</span></span>

### <span data-ttu-id="d0b7f-111">---Példa 1: a csomag rögzítési munkamenetének leállítása---</span><span class="sxs-lookup"><span data-stu-id="d0b7f-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="d0b7f-112">Ebben a példában leállítjuk az "PacketCaptureTest" nevű futó csomag-rögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="d0b7f-113">Miután leállította a munkamenetet, a csomag rögzítésére szolgáló fájlt feltölti a rendszer, és a rendszer a VM-re menti a számítógépen, a konfigurációtól függően.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="d0b7f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0b7f-114">PARAMETERS</span></span>

### <span data-ttu-id="d0b7f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0b7f-115">-AsJob</span></span>
<span data-ttu-id="d0b7f-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d0b7f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0b7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b7f-117">-DefaultProfile</span></span>
<span data-ttu-id="d0b7f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0b7f-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0b7f-119">-NetworkWatcher</span></span>
<span data-ttu-id="d0b7f-120">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="d0b7f-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d0b7f-121">-NetworkWatcherName</span></span>
<span data-ttu-id="d0b7f-122">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="d0b7f-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d0b7f-123">-PacketCaptureName</span></span>
<span data-ttu-id="d0b7f-124">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-124">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0b7f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0b7f-125">-PassThru</span></span>
<span data-ttu-id="d0b7f-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d0b7f-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d0b7f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0b7f-127">-ResourceGroupName</span></span>
<span data-ttu-id="d0b7f-128">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d0b7f-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d0b7f-129">-Confirm</span></span>
<span data-ttu-id="d0b7f-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0b7f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0b7f-131">-WhatIf</span></span>
<span data-ttu-id="d0b7f-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0b7f-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0b7f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b7f-134">CommonParameters</span></span>
<span data-ttu-id="d0b7f-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0b7f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b7f-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b7f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b7f-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0b7f-137">INPUTS</span></span>

### <span data-ttu-id="d0b7f-138">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0b7f-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d0b7f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d0b7f-139">System.String</span></span>

## <span data-ttu-id="d0b7f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0b7f-140">OUTPUTS</span></span>

### <span data-ttu-id="d0b7f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0b7f-141">System.Boolean</span></span>

## <span data-ttu-id="d0b7f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0b7f-142">NOTES</span></span>
<span data-ttu-id="d0b7f-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="d0b7f-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="d0b7f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0b7f-144">RELATED LINKS</span></span>

[<span data-ttu-id="d0b7f-145">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0b7f-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0b7f-146">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d0b7f-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d0b7f-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0b7f-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0b7f-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0b7f-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0b7f-149">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0b7f-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d0b7f-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0b7f-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d0b7f-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0b7f-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d0b7f-152">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d0b7f-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d0b7f-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d0b7f-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d0b7f-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d0b7f-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d0b7f-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d0b7f-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d0b7f-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d0b7f-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
