---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 44bba48f1d066c4a9006595092bd84c68252bbd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499964"
---
# <span data-ttu-id="ce9f0-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ce9f0-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="ce9f0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce9f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9f0-103">Megtekintheti a virtuális gépre telepített, konfigurált és hatékony hálózatbiztonsági csoport szabályait.</span><span class="sxs-lookup"><span data-stu-id="ce9f0-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce9f0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce9f0-104">SYNTAX</span></span>

### <span data-ttu-id="ce9f0-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce9f0-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce9f0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ce9f0-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce9f0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce9f0-107">DESCRIPTION</span></span>
<span data-ttu-id="ce9f0-108">A Get-AzureRmNetworkWatcherSecurityGroupView lehetővé teszi, hogy megtekintse a VM-re konfigurált, konfigurált és hatékony hálózati biztonsági csoportok szabályait.</span><span class="sxs-lookup"><span data-stu-id="ce9f0-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="ce9f0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ce9f0-109">EXAMPLES</span></span>

### <span data-ttu-id="ce9f0-110">---Példa 1: biztonsági csoport nézetbe Hívás kezdeményezése VM----</span><span class="sxs-lookup"><span data-stu-id="ce9f0-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="ce9f0-111">A fenti példában először a regionális hálózati figyelőt, majd egy VM-et kaptunk a régióban.</span><span class="sxs-lookup"><span data-stu-id="ce9f0-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="ce9f0-112">Ezután egy biztonsági csoport nézetet készítünk a megadott VM-ről.</span><span class="sxs-lookup"><span data-stu-id="ce9f0-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="ce9f0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce9f0-113">PARAMETERS</span></span>

### <span data-ttu-id="ce9f0-114">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce9f0-114">-NetworkWatcher</span></span>
<span data-ttu-id="ce9f0-115">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ce9f0-115">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9f0-116">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ce9f0-116">-NetworkWatcherName</span></span>
<span data-ttu-id="ce9f0-117">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="ce9f0-117">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9f0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce9f0-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce9f0-119">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ce9f0-119">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9f0-120">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ce9f0-120">-TargetVirtualMachineId</span></span>
<span data-ttu-id="ce9f0-121">A cél VM-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ce9f0-121">The target VM Id</span></span>

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

### <span data-ttu-id="ce9f0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce9f0-122">-DefaultProfile</span></span>
<span data-ttu-id="ce9f0-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce9f0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce9f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9f0-124">CommonParameters</span></span>
<span data-ttu-id="ce9f0-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce9f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9f0-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce9f0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9f0-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce9f0-127">INPUTS</span></span>

### <span data-ttu-id="ce9f0-128">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce9f0-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ce9f0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ce9f0-129">System.String</span></span>

## <span data-ttu-id="ce9f0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce9f0-130">OUTPUTS</span></span>

### <span data-ttu-id="ce9f0-131">Microsoft. Azure. commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="ce9f0-131">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="ce9f0-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce9f0-132">NOTES</span></span>
<span data-ttu-id="ce9f0-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, adatfolyam, IP</span><span class="sxs-lookup"><span data-stu-id="ce9f0-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="ce9f0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce9f0-134">RELATED LINKS</span></span>

[<span data-ttu-id="ce9f0-135">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce9f0-135">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ce9f0-136">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce9f0-136">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ce9f0-137">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce9f0-137">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ce9f0-138">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ce9f0-138">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ce9f0-139">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ce9f0-139">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ce9f0-140">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ce9f0-140">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ce9f0-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ce9f0-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ce9f0-142">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ce9f0-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ce9f0-143">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ce9f0-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ce9f0-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ce9f0-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ce9f0-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ce9f0-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ce9f0-146">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ce9f0-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

