---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: 3593b9742da7c4ad8975e662033a394e0aee73b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941745"
---
# <span data-ttu-id="922ff-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="922ff-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="922ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="922ff-102">SYNOPSIS</span></span>
<span data-ttu-id="922ff-103">Meghívhatja a hálózatkonfigurációs diagnosztikai munkamenetet a célerőforrás meghatározott hálózati profiljaihoz.</span><span class="sxs-lookup"><span data-stu-id="922ff-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="922ff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="922ff-104">SYNTAX</span></span>

### <span data-ttu-id="922ff-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="922ff-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="922ff-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="922ff-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="922ff-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="922ff-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="922ff-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="922ff-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="922ff-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="922ff-109">DESCRIPTION</span></span>
<span data-ttu-id="922ff-110">A Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic parancsmag meghívja a hálózati konfigurációs diagnosztikai munkamenetet a célerőforrás megadott hálózati profiljaihoz.</span><span class="sxs-lookup"><span data-stu-id="922ff-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="922ff-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="922ff-111">EXAMPLES</span></span>

### <span data-ttu-id="922ff-112">1. példa: A virtuális géphez és a megadott hálózati profilhoz szükséges hálózati konfigurációs diagnosztikai munkamenet meghívása</span><span class="sxs-lookup"><span data-stu-id="922ff-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="922ff-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="922ff-113">PARAMETERS</span></span>

### <span data-ttu-id="922ff-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="922ff-114">-AsJob</span></span>
<span data-ttu-id="922ff-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="922ff-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="922ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922ff-116">-DefaultProfile</span></span>
<span data-ttu-id="922ff-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="922ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="922ff-118">-Location</span><span class="sxs-lookup"><span data-stu-id="922ff-118">-Location</span></span>
<span data-ttu-id="922ff-119">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="922ff-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="922ff-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="922ff-120">-NetworkWatcher</span></span>
<span data-ttu-id="922ff-121">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="922ff-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="922ff-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="922ff-122">-NetworkWatcherName</span></span>
<span data-ttu-id="922ff-123">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="922ff-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="922ff-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="922ff-124">-Profile</span></span>
<span data-ttu-id="922ff-125">Hálózati konfigurációs diagnosztikai profilok listája.</span><span class="sxs-lookup"><span data-stu-id="922ff-125">List of network configuration diagnostic profiles.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="922ff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="922ff-126">-ResourceGroupName</span></span>
<span data-ttu-id="922ff-127">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="922ff-127">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="922ff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="922ff-128">-ResourceId</span></span>
<span data-ttu-id="922ff-129">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="922ff-129">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="922ff-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="922ff-130">-TargetResourceId</span></span>
<span data-ttu-id="922ff-131">A hálózati konfigurációs diagnosztikai célerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="922ff-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="922ff-132">Érvényes beállítások: VM, NetworkInterface, VMSS/NetworkInterface és Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="922ff-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="922ff-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="922ff-133">-VerbosityLevel</span></span>
<span data-ttu-id="922ff-134">Részletességi szint.</span><span class="sxs-lookup"><span data-stu-id="922ff-134">Verbosity level.</span></span>
<span data-ttu-id="922ff-135">Az elfogadott értékek: "Normál", "Minimum", "Teljes".</span><span class="sxs-lookup"><span data-stu-id="922ff-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="922ff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922ff-136">CommonParameters</span></span>
<span data-ttu-id="922ff-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922ff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922ff-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922ff-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922ff-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="922ff-139">INPUTS</span></span>

### <span data-ttu-id="922ff-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="922ff-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="922ff-141">System.String</span><span class="sxs-lookup"><span data-stu-id="922ff-141">System.String</span></span>

## <span data-ttu-id="922ff-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="922ff-142">OUTPUTS</span></span>

### <span data-ttu-id="922ff-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="922ff-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="922ff-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="922ff-144">NOTES</span></span>
<span data-ttu-id="922ff-145">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, figyelő, diagnosztikai, profil</span><span class="sxs-lookup"><span data-stu-id="922ff-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="922ff-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="922ff-146">RELATED LINKS</span></span>

[<span data-ttu-id="922ff-147">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="922ff-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="922ff-148">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="922ff-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="922ff-149">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="922ff-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="922ff-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="922ff-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="922ff-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="922ff-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="922ff-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="922ff-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="922ff-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="922ff-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="922ff-154">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="922ff-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="922ff-155">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="922ff-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="922ff-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="922ff-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="922ff-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="922ff-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="922ff-158">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="922ff-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="922ff-159">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="922ff-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="922ff-160">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="922ff-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="922ff-161">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="922ff-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="922ff-162">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="922ff-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="922ff-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="922ff-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="922ff-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="922ff-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="922ff-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="922ff-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="922ff-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="922ff-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="922ff-167">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="922ff-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="922ff-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="922ff-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="922ff-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="922ff-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="922ff-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="922ff-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="922ff-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="922ff-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="922ff-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="922ff-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="922ff-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="922ff-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
