---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 43dc48aaa58f086e6d05f45a81096612d3177a17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680127"
---
# <span data-ttu-id="b713b-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b713b-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="b713b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b713b-102">SYNOPSIS</span></span>
<span data-ttu-id="b713b-103">Futó csomag rögzítési munkamenetének leállítása</span><span class="sxs-lookup"><span data-stu-id="b713b-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b713b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b713b-104">SYNTAX</span></span>

### <span data-ttu-id="b713b-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b713b-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b713b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b713b-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b713b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b713b-107">DESCRIPTION</span></span>
<span data-ttu-id="b713b-108">A Stop-AzureRmNetworkWatcherPacketCapture leállítja a futtatott csomag rögzítési munkamenetét.</span><span class="sxs-lookup"><span data-stu-id="b713b-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="b713b-109">Miután leállította a munkamenetet, a csomag rögzítésére szolgáló fájlt feltölti a rendszer, és a rendszer a VM-re menti a számítógépen, a konfigurációtól függően.</span><span class="sxs-lookup"><span data-stu-id="b713b-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="b713b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b713b-110">EXAMPLES</span></span>

### <span data-ttu-id="b713b-111">---Példa 1: a csomag rögzítési munkamenetének leállítása---</span><span class="sxs-lookup"><span data-stu-id="b713b-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="b713b-112">Ebben a példában leállítjuk az "PacketCaptureTest" nevű futó csomag-rögzítési munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="b713b-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="b713b-113">Miután leállította a munkamenetet, a csomag rögzítésére szolgáló fájlt feltölti a rendszer, és a rendszer a VM-re menti a számítógépen, a konfigurációtól függően.</span><span class="sxs-lookup"><span data-stu-id="b713b-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="b713b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b713b-114">PARAMETERS</span></span>

### <span data-ttu-id="b713b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b713b-115">-AsJob</span></span>
<span data-ttu-id="b713b-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b713b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b713b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b713b-117">-DefaultProfile</span></span>
<span data-ttu-id="b713b-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b713b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b713b-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b713b-119">-NetworkWatcher</span></span>
<span data-ttu-id="b713b-120">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="b713b-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="b713b-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b713b-121">-NetworkWatcherName</span></span>
<span data-ttu-id="b713b-122">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="b713b-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="b713b-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="b713b-123">-PacketCaptureName</span></span>
<span data-ttu-id="b713b-124">A csomagot rögzítő név.</span><span class="sxs-lookup"><span data-stu-id="b713b-124">The packet capture name.</span></span>

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

### <span data-ttu-id="b713b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b713b-125">-PassThru</span></span>
<span data-ttu-id="b713b-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b713b-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b713b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b713b-127">-ResourceGroupName</span></span>
<span data-ttu-id="b713b-128">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b713b-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b713b-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b713b-129">-Confirm</span></span>
<span data-ttu-id="b713b-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b713b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b713b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b713b-131">-WhatIf</span></span>
<span data-ttu-id="b713b-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b713b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b713b-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b713b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b713b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b713b-134">CommonParameters</span></span>
<span data-ttu-id="b713b-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b713b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b713b-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b713b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b713b-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b713b-137">INPUTS</span></span>

### <span data-ttu-id="b713b-138">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b713b-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b713b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b713b-139">System.String</span></span>

## <span data-ttu-id="b713b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b713b-140">OUTPUTS</span></span>

### <span data-ttu-id="b713b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b713b-141">System.Boolean</span></span>

## <span data-ttu-id="b713b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b713b-142">NOTES</span></span>
<span data-ttu-id="b713b-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, csomag, rögzítés, forgalom</span><span class="sxs-lookup"><span data-stu-id="b713b-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="b713b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b713b-144">RELATED LINKS</span></span>

[<span data-ttu-id="b713b-145">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b713b-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b713b-146">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b713b-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="b713b-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b713b-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b713b-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b713b-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b713b-149">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b713b-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b713b-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b713b-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b713b-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b713b-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b713b-152">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b713b-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b713b-153">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b713b-153">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b713b-154">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b713b-154">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b713b-155">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b713b-155">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b713b-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b713b-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
