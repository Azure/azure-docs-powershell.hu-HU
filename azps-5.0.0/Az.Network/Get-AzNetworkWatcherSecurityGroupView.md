---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 37da72dd26df32dddee0ea28d2378418e9e4922e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195669"
---
# <span data-ttu-id="1b7cd-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1b7cd-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="1b7cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="1b7cd-103">Megtekintheti a virtuális gépre telepített, konfigurált és hatékony hálózatbiztonsági csoport szabályait.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="1b7cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b7cd-104">SYNTAX</span></span>

### <span data-ttu-id="1b7cd-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b7cd-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b7cd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1b7cd-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b7cd-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1b7cd-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b7cd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b7cd-108">DESCRIPTION</span></span>
<span data-ttu-id="1b7cd-109">A Get-AzNetworkWatcherSecurityGroupView lehetővé teszi, hogy megtekintse a VM-re konfigurált, konfigurált és hatékony hálózati biztonsági csoportok szabályait.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="1b7cd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1b7cd-110">EXAMPLES</span></span>

### <span data-ttu-id="1b7cd-111">1. példa: biztonsági csoport nézetbe Hívás kezdeményezése VM-en</span><span class="sxs-lookup"><span data-stu-id="1b7cd-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="1b7cd-112">A fenti példában először a regionális hálózati figyelőt, majd egy VM-et kaptunk a régióban.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="1b7cd-113">Ezután egy biztonsági csoport nézetet készítünk a megadott VM-ről.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="1b7cd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b7cd-114">PARAMETERS</span></span>

### <span data-ttu-id="1b7cd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b7cd-115">-AsJob</span></span>
<span data-ttu-id="1b7cd-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1b7cd-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b7cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b7cd-117">-DefaultProfile</span></span>
<span data-ttu-id="1b7cd-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b7cd-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="1b7cd-119">-Location</span></span>
<span data-ttu-id="1b7cd-120">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-120">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b7cd-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b7cd-121">-NetworkWatcher</span></span>
<span data-ttu-id="1b7cd-122">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="1b7cd-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1b7cd-123">-NetworkWatcherName</span></span>
<span data-ttu-id="1b7cd-124">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="1b7cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b7cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="1b7cd-126">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1b7cd-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="1b7cd-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="1b7cd-128">A cél VM-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1b7cd-128">The target VM Id</span></span>

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

### <span data-ttu-id="1b7cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b7cd-129">CommonParameters</span></span>
<span data-ttu-id="1b7cd-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b7cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b7cd-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b7cd-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b7cd-132">INPUTS</span></span>

### <span data-ttu-id="1b7cd-133">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b7cd-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1b7cd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1b7cd-134">System.String</span></span>

## <span data-ttu-id="1b7cd-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b7cd-135">OUTPUTS</span></span>

### <span data-ttu-id="1b7cd-136">Microsoft. Azure. commands. Network. models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="1b7cd-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="1b7cd-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b7cd-137">NOTES</span></span>
<span data-ttu-id="1b7cd-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, adatfolyam, IP</span><span class="sxs-lookup"><span data-stu-id="1b7cd-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="1b7cd-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b7cd-139">RELATED LINKS</span></span>

[<span data-ttu-id="1b7cd-140">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b7cd-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1b7cd-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b7cd-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1b7cd-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b7cd-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1b7cd-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1b7cd-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1b7cd-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1b7cd-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1b7cd-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1b7cd-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1b7cd-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1b7cd-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1b7cd-147">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b7cd-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b7cd-148">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1b7cd-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1b7cd-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b7cd-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b7cd-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b7cd-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b7cd-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b7cd-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b7cd-152">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b7cd-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1b7cd-153">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1b7cd-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1b7cd-154">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1b7cd-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1b7cd-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b7cd-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b7cd-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b7cd-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b7cd-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b7cd-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b7cd-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1b7cd-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1b7cd-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b7cd-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b7cd-160">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b7cd-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b7cd-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1b7cd-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1b7cd-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1b7cd-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1b7cd-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1b7cd-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1b7cd-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1b7cd-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1b7cd-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1b7cd-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1b7cd-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b7cd-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
