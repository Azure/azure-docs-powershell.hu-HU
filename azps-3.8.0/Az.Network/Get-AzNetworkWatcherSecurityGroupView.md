---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 01334e8a94ad4f73ec5f347748468bada119c070
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845902"
---
# <span data-ttu-id="0f74f-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0f74f-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="0f74f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f74f-102">SYNOPSIS</span></span>
<span data-ttu-id="0f74f-103">Megtekintheti a virtuális gépre telepített, konfigurált és hatékony hálózatbiztonsági csoport szabályait.</span><span class="sxs-lookup"><span data-stu-id="0f74f-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="0f74f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f74f-104">SYNTAX</span></span>

### <span data-ttu-id="0f74f-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0f74f-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f74f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0f74f-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f74f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0f74f-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f74f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f74f-108">DESCRIPTION</span></span>
<span data-ttu-id="0f74f-109">A Get-AzNetworkWatcherSecurityGroupView lehetővé teszi, hogy megtekintse a VM-re konfigurált, konfigurált és hatékony hálózati biztonsági csoportok szabályait.</span><span class="sxs-lookup"><span data-stu-id="0f74f-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="0f74f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0f74f-110">EXAMPLES</span></span>

### <span data-ttu-id="0f74f-111">1. példa: biztonsági csoport nézetbe Hívás kezdeményezése VM-en</span><span class="sxs-lookup"><span data-stu-id="0f74f-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="0f74f-112">A fenti példában először a regionális hálózati figyelőt, majd egy VM-et kaptunk a régióban.</span><span class="sxs-lookup"><span data-stu-id="0f74f-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="0f74f-113">Ezután egy biztonsági csoport nézetet készítünk a megadott VM-ről.</span><span class="sxs-lookup"><span data-stu-id="0f74f-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="0f74f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f74f-114">PARAMETERS</span></span>

### <span data-ttu-id="0f74f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f74f-115">-AsJob</span></span>
<span data-ttu-id="0f74f-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0f74f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f74f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f74f-117">-DefaultProfile</span></span>
<span data-ttu-id="0f74f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f74f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f74f-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="0f74f-119">-Location</span></span>
<span data-ttu-id="0f74f-120">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="0f74f-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0f74f-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f74f-121">-NetworkWatcher</span></span>
<span data-ttu-id="0f74f-122">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="0f74f-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="0f74f-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0f74f-123">-NetworkWatcherName</span></span>
<span data-ttu-id="0f74f-124">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="0f74f-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="0f74f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f74f-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f74f-126">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0f74f-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0f74f-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0f74f-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="0f74f-128">A cél VM-azonosítója</span><span class="sxs-lookup"><span data-stu-id="0f74f-128">The target VM Id</span></span>

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

### <span data-ttu-id="0f74f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f74f-129">CommonParameters</span></span>
<span data-ttu-id="0f74f-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f74f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f74f-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0f74f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f74f-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f74f-132">INPUTS</span></span>

### <span data-ttu-id="0f74f-133">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f74f-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0f74f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0f74f-134">System.String</span></span>

## <span data-ttu-id="0f74f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f74f-135">OUTPUTS</span></span>

### <span data-ttu-id="0f74f-136">Microsoft. Azure. commands. Network. models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="0f74f-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="0f74f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f74f-137">NOTES</span></span>
<span data-ttu-id="0f74f-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, adatfolyam, IP</span><span class="sxs-lookup"><span data-stu-id="0f74f-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="0f74f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f74f-139">RELATED LINKS</span></span>

[<span data-ttu-id="0f74f-140">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f74f-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0f74f-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f74f-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0f74f-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f74f-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0f74f-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0f74f-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0f74f-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0f74f-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0f74f-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0f74f-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0f74f-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0f74f-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0f74f-147">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f74f-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f74f-148">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0f74f-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0f74f-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f74f-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f74f-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f74f-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f74f-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f74f-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f74f-152">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f74f-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0f74f-153">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0f74f-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0f74f-154">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0f74f-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0f74f-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f74f-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0f74f-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f74f-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0f74f-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f74f-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0f74f-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0f74f-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0f74f-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f74f-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0f74f-160">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f74f-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0f74f-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0f74f-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0f74f-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0f74f-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0f74f-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0f74f-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0f74f-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0f74f-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0f74f-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0f74f-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="0f74f-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f74f-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
