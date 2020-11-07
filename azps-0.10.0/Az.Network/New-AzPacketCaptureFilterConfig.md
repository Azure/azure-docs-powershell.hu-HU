---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 77a760fd78b06d4f04d5a805b689139977433f26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841289"
---
# <span data-ttu-id="d6e3c-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d6e3c-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="d6e3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e3c-103">Új csomagkapcsolt rögzítési szűrő objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="d6e3c-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="d6e3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6e3c-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6e3c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6e3c-105">DESCRIPTION</span></span>
<span data-ttu-id="d6e3c-106">Az New-AzPacketCaptureFilterConfig parancsmag létrehoz egy új csomagkapcsolt rögzítési szűrő objektumot.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="d6e3c-107">Ezzel az objektummal korlátozható, hogy milyen típusú csomagokat rögzít a program a csomag rögzítésekor a megadott feltételekkel.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="d6e3c-108">A New-AzNetworkWatcherPacketCapture parancsmag több szűrő objektumot is elfogadhat a komponált rögzítési munkamenetek engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="d6e3c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d6e3c-109">EXAMPLES</span></span>

### <span data-ttu-id="d6e3c-110">---Példa 1: több szűrőből álló csomag létrehozása---</span><span class="sxs-lookup"><span data-stu-id="d6e3c-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="d6e3c-111">Ebben a példában a "PacketCaptureTest" nevű csomagot hozzuk létre több szűrővel és időkorlátozással.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="d6e3c-112">A munkamenet befejezésekor a program a megadott tárterület-fiókba menti a fájlt.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="d6e3c-113">Megjegyzés: az Azure Network Watcher bővítménynek telepítve kell lennie a cél virtuális gépen a csomag rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="d6e3c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6e3c-114">PARAMETERS</span></span>

### <span data-ttu-id="d6e3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e3c-115">-DefaultProfile</span></span>
<span data-ttu-id="d6e3c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6e3c-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="d6e3c-117">-LocalIPAddress</span></span>
<span data-ttu-id="d6e3c-118">A szűrni kívánt helyi IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="d6e3c-119">Példa bemenetekre: "127.0.0.1" az egyetlen cím bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d6e3c-120">"127.0.0.1-127.0.0.255" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d6e3c-121">"127.0.0.1; 127.0.0.5;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e3c-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="d6e3c-122">-LocalPort</span></span>
<span data-ttu-id="d6e3c-123">A szűrni kívánt helyi IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="d6e3c-124">Példa bemenetekre: "127.0.0.1" az egyetlen cím bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d6e3c-125">"127.0.0.1-127.0.0.255" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d6e3c-126">"127.0.0.1; 127.0.0.5;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e3c-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d6e3c-127">-Protocol</span></span>
<span data-ttu-id="d6e3c-128">A szűréshez használandó procotol adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="d6e3c-129">Elfogadható értékek "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="d6e3c-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e3c-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="d6e3c-130">-RemoteIPAddress</span></span>
<span data-ttu-id="d6e3c-131">A szűrni kívánt távoli IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="d6e3c-132">Példa bemenetekre: "127.0.0.1" az egyetlen cím bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d6e3c-133">"127.0.0.1-127.0.0.255" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d6e3c-134">"127.0.0.1; 127.0.0.5;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e3c-135">-TávoliPORT</span><span class="sxs-lookup"><span data-stu-id="d6e3c-135">-RemotePort</span></span>
<span data-ttu-id="d6e3c-136">A szűrni kívánt távoli portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="d6e3c-137">Távoli port – például bemenetek: "80" egy portos bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="d6e3c-138">"80-85" a tartománnyal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-138">"80-85" for range.</span></span>
<span data-ttu-id="d6e3c-139">"80; 443;" több bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="d6e3c-139">"80;443;" for multiple entries.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e3c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e3c-140">CommonParameters</span></span>
<span data-ttu-id="d6e3c-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6e3c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e3c-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6e3c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e3c-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6e3c-143">INPUTS</span></span>

### <span data-ttu-id="d6e3c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d6e3c-144">System.String</span></span>

## <span data-ttu-id="d6e3c-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6e3c-145">OUTPUTS</span></span>

### <span data-ttu-id="d6e3c-146">Microsoft. Azure. commands. Network. models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="d6e3c-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="d6e3c-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6e3c-147">NOTES</span></span>
<span data-ttu-id="d6e3c-148">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, csomag, rögzítés, forgalom, szűrő</span><span class="sxs-lookup"><span data-stu-id="d6e3c-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="d6e3c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6e3c-149">RELATED LINKS</span></span>

[<span data-ttu-id="d6e3c-150">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6e3c-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6e3c-151">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6e3c-151">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6e3c-152">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6e3c-152">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6e3c-153">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6e3c-153">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6e3c-154">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6e3c-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d6e3c-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6e3c-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d6e3c-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6e3c-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d6e3c-157">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d6e3c-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d6e3c-158">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d6e3c-158">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d6e3c-159">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d6e3c-159">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d6e3c-160">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d6e3c-160">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d6e3c-161">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d6e3c-161">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
