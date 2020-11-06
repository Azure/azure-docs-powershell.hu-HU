---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 9fe23ea5fa9bef544feae6112879cb1be6eeae7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493642"
---
# <span data-ttu-id="9bfc0-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9bfc0-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="9bfc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bfc0-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfc0-103">Megtekintheti a virtuális gépre telepített, konfigurált és hatékony hálózatbiztonsági csoport szabályait.</span><span class="sxs-lookup"><span data-stu-id="9bfc0-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bfc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bfc0-104">SYNTAX</span></span>

### <span data-ttu-id="9bfc0-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9bfc0-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bfc0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9bfc0-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bfc0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9bfc0-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bfc0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bfc0-108">DESCRIPTION</span></span>
<span data-ttu-id="9bfc0-109">A Get-AzureRmNetworkWatcherSecurityGroupView lehetővé teszi, hogy megtekintse a VM-re konfigurált, konfigurált és hatékony hálózati biztonsági csoportok szabályait.</span><span class="sxs-lookup"><span data-stu-id="9bfc0-109">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="9bfc0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9bfc0-110">EXAMPLES</span></span>

### <span data-ttu-id="9bfc0-111">1. példa: biztonsági csoport nézetbe Hívás kezdeményezése VM-en</span><span class="sxs-lookup"><span data-stu-id="9bfc0-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="9bfc0-112">A fenti példában először a regionális hálózati figyelőt, majd egy VM-et kaptunk a régióban.</span><span class="sxs-lookup"><span data-stu-id="9bfc0-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="9bfc0-113">Ezután egy biztonsági csoport nézetet készítünk a megadott VM-ről.</span><span class="sxs-lookup"><span data-stu-id="9bfc0-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="9bfc0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bfc0-114">PARAMETERS</span></span>

### <span data-ttu-id="9bfc0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bfc0-115">-AsJob</span></span>
<span data-ttu-id="9bfc0-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9bfc0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bfc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfc0-117">-DefaultProfile</span></span>
<span data-ttu-id="9bfc0-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bfc0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bfc0-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="9bfc0-119">-Location</span></span>
<span data-ttu-id="9bfc0-120">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="9bfc0-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9bfc0-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9bfc0-121">-NetworkWatcher</span></span>
<span data-ttu-id="9bfc0-122">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="9bfc0-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="9bfc0-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9bfc0-123">-NetworkWatcherName</span></span>
<span data-ttu-id="9bfc0-124">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="9bfc0-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="9bfc0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bfc0-125">-ResourceGroupName</span></span>
<span data-ttu-id="9bfc0-126">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9bfc0-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9bfc0-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="9bfc0-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="9bfc0-128">A cél VM-azonosítója</span><span class="sxs-lookup"><span data-stu-id="9bfc0-128">The target VM Id</span></span>

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

### <span data-ttu-id="9bfc0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfc0-129">CommonParameters</span></span>
<span data-ttu-id="9bfc0-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bfc0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfc0-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bfc0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfc0-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bfc0-132">INPUTS</span></span>

### <span data-ttu-id="9bfc0-133">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9bfc0-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9bfc0-134">Paraméterek: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9bfc0-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="9bfc0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9bfc0-135">System.String</span></span>
<span data-ttu-id="9bfc0-136">Paraméterek: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9bfc0-136">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="9bfc0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bfc0-137">OUTPUTS</span></span>

### <span data-ttu-id="9bfc0-138">Microsoft. Azure. commands. Network. models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="9bfc0-138">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="9bfc0-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bfc0-139">NOTES</span></span>
<span data-ttu-id="9bfc0-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, adatfolyam, IP</span><span class="sxs-lookup"><span data-stu-id="9bfc0-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="9bfc0-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bfc0-141">RELATED LINKS</span></span>

[<span data-ttu-id="9bfc0-142">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9bfc0-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9bfc0-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9bfc0-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9bfc0-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9bfc0-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9bfc0-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9bfc0-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="9bfc0-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9bfc0-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9bfc0-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9bfc0-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="9bfc0-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9bfc0-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9bfc0-149">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9bfc0-149">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9bfc0-150">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9bfc0-150">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="9bfc0-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9bfc0-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9bfc0-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9bfc0-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9bfc0-153">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9bfc0-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9bfc0-154">Új – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bfc0-154">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9bfc0-155">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9bfc0-155">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="9bfc0-156">Teszt-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9bfc0-156">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="9bfc0-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bfc0-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9bfc0-158">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bfc0-158">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9bfc0-159">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bfc0-159">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9bfc0-160">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9bfc0-160">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9bfc0-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bfc0-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9bfc0-162">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bfc0-162">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9bfc0-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9bfc0-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9bfc0-164">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9bfc0-164">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9bfc0-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9bfc0-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9bfc0-166">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9bfc0-166">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9bfc0-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9bfc0-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="9bfc0-168">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9bfc0-168">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
