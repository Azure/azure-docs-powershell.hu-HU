---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 5b48cbabfe91b16924a1296a73354db659ec8f3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680694"
---
# <span data-ttu-id="f14e4-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f14e4-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="f14e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f14e4-102">SYNOPSIS</span></span>
<span data-ttu-id="f14e4-103">Megtekintheti a virtuális gépre telepített, konfigurált és hatékony hálózatbiztonsági csoport szabályait.</span><span class="sxs-lookup"><span data-stu-id="f14e4-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f14e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f14e4-104">SYNTAX</span></span>

### <span data-ttu-id="f14e4-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f14e4-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f14e4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f14e4-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f14e4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f14e4-107">DESCRIPTION</span></span>
<span data-ttu-id="f14e4-108">A Get-AzureRmNetworkWatcherSecurityGroupView lehetővé teszi, hogy megtekintse a VM-re konfigurált, konfigurált és hatékony hálózati biztonsági csoportok szabályait.</span><span class="sxs-lookup"><span data-stu-id="f14e4-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="f14e4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f14e4-109">EXAMPLES</span></span>

### <span data-ttu-id="f14e4-110">---Példa 1: biztonsági csoport nézetbe Hívás kezdeményezése VM----</span><span class="sxs-lookup"><span data-stu-id="f14e4-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="f14e4-111">A fenti példában először a regionális hálózati figyelőt, majd egy VM-et kaptunk a régióban.</span><span class="sxs-lookup"><span data-stu-id="f14e4-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="f14e4-112">Ezután egy biztonsági csoport nézetet készítünk a megadott VM-ről.</span><span class="sxs-lookup"><span data-stu-id="f14e4-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="f14e4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f14e4-113">PARAMETERS</span></span>

### <span data-ttu-id="f14e4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f14e4-114">-AsJob</span></span>
<span data-ttu-id="f14e4-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f14e4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f14e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14e4-116">-DefaultProfile</span></span>
<span data-ttu-id="f14e4-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f14e4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f14e4-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f14e4-118">-NetworkWatcher</span></span>
<span data-ttu-id="f14e4-119">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="f14e4-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="f14e4-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f14e4-120">-NetworkWatcherName</span></span>
<span data-ttu-id="f14e4-121">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="f14e4-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="f14e4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f14e4-122">-ResourceGroupName</span></span>
<span data-ttu-id="f14e4-123">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f14e4-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f14e4-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f14e4-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f14e4-125">A cél VM-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f14e4-125">The target VM Id</span></span>

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

### <span data-ttu-id="f14e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14e4-126">CommonParameters</span></span>
<span data-ttu-id="f14e4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f14e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14e4-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f14e4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14e4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f14e4-129">INPUTS</span></span>

### <span data-ttu-id="f14e4-130">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f14e4-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f14e4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f14e4-131">System.String</span></span>

## <span data-ttu-id="f14e4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f14e4-132">OUTPUTS</span></span>

### <span data-ttu-id="f14e4-133">Microsoft. Azure. commands. Network. models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="f14e4-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="f14e4-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f14e4-134">NOTES</span></span>
<span data-ttu-id="f14e4-135">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, adatfolyam, IP</span><span class="sxs-lookup"><span data-stu-id="f14e4-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="f14e4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f14e4-136">RELATED LINKS</span></span>

[<span data-ttu-id="f14e4-137">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f14e4-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f14e4-138">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f14e4-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f14e4-139">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f14e4-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f14e4-140">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f14e4-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f14e4-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f14e4-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f14e4-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f14e4-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f14e4-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f14e4-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f14e4-144">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f14e4-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f14e4-145">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f14e4-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f14e4-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f14e4-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f14e4-147">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f14e4-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f14e4-148">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f14e4-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

