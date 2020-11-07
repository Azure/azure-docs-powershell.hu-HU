---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: fe315ac4b6c29b8ffd1c82c8045ba9b7a7aab4a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841558"
---
# <span data-ttu-id="00891-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="00891-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="00891-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00891-102">SYNOPSIS</span></span>
<span data-ttu-id="00891-103">Megtekintheti a virtuális gépre telepített, konfigurált és hatékony hálózatbiztonsági csoport szabályait.</span><span class="sxs-lookup"><span data-stu-id="00891-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="00891-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00891-104">SYNTAX</span></span>

### <span data-ttu-id="00891-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00891-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00891-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="00891-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00891-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="00891-107">DESCRIPTION</span></span>
<span data-ttu-id="00891-108">A Get-AzNetworkWatcherSecurityGroupView lehetővé teszi, hogy megtekintse a VM-re konfigurált, konfigurált és hatékony hálózati biztonsági csoportok szabályait.</span><span class="sxs-lookup"><span data-stu-id="00891-108">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="00891-109">Példák</span><span class="sxs-lookup"><span data-stu-id="00891-109">EXAMPLES</span></span>

### <span data-ttu-id="00891-110">---Példa 1: biztonsági csoport nézetbe Hívás kezdeményezése VM----</span><span class="sxs-lookup"><span data-stu-id="00891-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="00891-111">A fenti példában először a regionális hálózati figyelőt, majd egy VM-et kaptunk a régióban.</span><span class="sxs-lookup"><span data-stu-id="00891-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="00891-112">Ezután egy biztonsági csoport nézetet készítünk a megadott VM-ről.</span><span class="sxs-lookup"><span data-stu-id="00891-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="00891-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00891-113">PARAMETERS</span></span>

### <span data-ttu-id="00891-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00891-114">-AsJob</span></span>
<span data-ttu-id="00891-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="00891-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00891-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00891-116">-DefaultProfile</span></span>
<span data-ttu-id="00891-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00891-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00891-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="00891-118">-NetworkWatcher</span></span>
<span data-ttu-id="00891-119">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="00891-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="00891-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="00891-120">-NetworkWatcherName</span></span>
<span data-ttu-id="00891-121">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="00891-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="00891-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00891-122">-ResourceGroupName</span></span>
<span data-ttu-id="00891-123">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="00891-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="00891-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="00891-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="00891-125">A cél VM-azonosítója</span><span class="sxs-lookup"><span data-stu-id="00891-125">The target VM Id</span></span>

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

### <span data-ttu-id="00891-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00891-126">CommonParameters</span></span>
<span data-ttu-id="00891-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00891-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00891-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00891-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00891-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00891-129">INPUTS</span></span>

### <span data-ttu-id="00891-130">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="00891-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="00891-131">System. String</span><span class="sxs-lookup"><span data-stu-id="00891-131">System.String</span></span>

## <span data-ttu-id="00891-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00891-132">OUTPUTS</span></span>

### <span data-ttu-id="00891-133">Microsoft. Azure. commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="00891-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="00891-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00891-134">NOTES</span></span>
<span data-ttu-id="00891-135">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, adatfolyam, IP</span><span class="sxs-lookup"><span data-stu-id="00891-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="00891-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00891-136">RELATED LINKS</span></span>

[<span data-ttu-id="00891-137">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="00891-137">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="00891-138">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="00891-138">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="00891-139">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="00891-139">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="00891-140">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="00891-140">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="00891-141">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="00891-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="00891-142">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="00891-142">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="00891-143">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="00891-143">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="00891-144">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="00891-144">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="00891-145">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="00891-145">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="00891-146">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="00891-146">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="00891-147">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="00891-147">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="00891-148">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="00891-148">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

