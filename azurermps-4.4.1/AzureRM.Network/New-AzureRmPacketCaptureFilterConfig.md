---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: ad6d2baaccdc17ec6ca414ae4b0cee84db20c94b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494831"
---
# <span data-ttu-id="89444-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="89444-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="89444-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89444-102">SYNOPSIS</span></span>
<span data-ttu-id="89444-103">Új csomagkapcsolt rögzítési szűrő objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="89444-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89444-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89444-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89444-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89444-105">DESCRIPTION</span></span>
<span data-ttu-id="89444-106">Az New-AzureRmPacketCaptureFilterConfig parancsmag létrehoz egy új csomagkapcsolt rögzítési szűrő objektumot.</span><span class="sxs-lookup"><span data-stu-id="89444-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="89444-107">Ezzel az objektummal korlátozható, hogy milyen típusú csomagokat rögzít a program a csomag rögzítésekor a megadott feltételekkel.</span><span class="sxs-lookup"><span data-stu-id="89444-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="89444-108">A New-AzureRmNetworkWatcherPacketCapture parancsmag több szűrő objektumot is elfogadhat a komponált rögzítési munkamenetek engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="89444-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="89444-109">Példák</span><span class="sxs-lookup"><span data-stu-id="89444-109">EXAMPLES</span></span>

### <span data-ttu-id="89444-110">---Példa 1: több szűrőből álló csomag létrehozása---</span><span class="sxs-lookup"><span data-stu-id="89444-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="89444-111">Ebben a példában a "PacketCaptureTest" nevű csomagot hozzuk létre több szűrővel és időkorlátozással.</span><span class="sxs-lookup"><span data-stu-id="89444-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="89444-112">A munkamenet befejezésekor a program a megadott tárterület-fiókba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="89444-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="89444-113">Megjegyzés: az Azure Network Watcher bővítménynek telepítve kell lennie a cél virtuális gépen a csomag rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="89444-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="89444-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89444-114">PARAMETERS</span></span>

### <span data-ttu-id="89444-115">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="89444-115">-LocalIPAddress</span></span>
<span data-ttu-id="89444-116">A szűrni kívánt helyi IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="89444-116">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="89444-117">Példa bemenetekre: "127.0.0.1" az egyetlen cím bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="89444-117">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="89444-118">"127.0.0.1-127.0.0.255" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="89444-118">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="89444-119">"127.0.0.1; 127.0.0.5;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="89444-119">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89444-120">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="89444-120">-LocalPort</span></span>
<span data-ttu-id="89444-121">A szűrni kívánt helyi IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="89444-121">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="89444-122">Példa bemenetekre: "127.0.0.1" az egyetlen cím bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="89444-122">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="89444-123">"127.0.0.1-127.0.0.255" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="89444-123">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="89444-124">"127.0.0.1; 127.0.0.5;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="89444-124">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89444-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="89444-125">-Protocol</span></span>
<span data-ttu-id="89444-126">A szűréshez használandó procotol adja meg.</span><span class="sxs-lookup"><span data-stu-id="89444-126">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="89444-127">Elfogadható értékek "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="89444-127">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89444-128">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="89444-128">-RemoteIPAddress</span></span>
<span data-ttu-id="89444-129">A szűrni kívánt távoli IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="89444-129">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="89444-130">Példa bemenetekre: "127.0.0.1" az egyetlen cím bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="89444-130">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="89444-131">"127.0.0.1-127.0.0.255" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="89444-131">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="89444-132">"127.0.0.1; 127.0.0.5;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="89444-132">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89444-133">-TávoliPORT</span><span class="sxs-lookup"><span data-stu-id="89444-133">-RemotePort</span></span>
<span data-ttu-id="89444-134">A szűrni kívánt távoli portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="89444-134">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="89444-135">Távoli port – például bemenetek: "80" egy portos bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="89444-135">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="89444-136">"80-85" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="89444-136">"80-85" for range.</span></span>
<span data-ttu-id="89444-137">"80; 443;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="89444-137">"80;443;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89444-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89444-138">-DefaultProfile</span></span>
<span data-ttu-id="89444-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89444-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89444-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89444-140">CommonParameters</span></span>
<span data-ttu-id="89444-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89444-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89444-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89444-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89444-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89444-143">INPUTS</span></span>

### <span data-ttu-id="89444-144">System. String</span><span class="sxs-lookup"><span data-stu-id="89444-144">System.String</span></span>

## <span data-ttu-id="89444-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89444-145">OUTPUTS</span></span>

### <span data-ttu-id="89444-146">Microsoft. Azure. commands. Network. models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="89444-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="89444-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89444-147">NOTES</span></span>
<span data-ttu-id="89444-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, csomag, rögzítés, forgalom, szűrő</span><span class="sxs-lookup"><span data-stu-id="89444-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="89444-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89444-149">RELATED LINKS</span></span>

[<span data-ttu-id="89444-150">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89444-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89444-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89444-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89444-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89444-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89444-153">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89444-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89444-154">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89444-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="89444-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89444-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="89444-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89444-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="89444-157">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="89444-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="89444-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="89444-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="89444-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="89444-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="89444-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="89444-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="89444-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="89444-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
