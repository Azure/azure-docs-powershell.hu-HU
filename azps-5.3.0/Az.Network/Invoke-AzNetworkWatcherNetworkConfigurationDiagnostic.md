---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: 5a1500554c1026b591faea63074ca9c12fef1b10
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379594"
---
# <span data-ttu-id="3c399-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3c399-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="3c399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c399-102">SYNOPSIS</span></span>
<span data-ttu-id="3c399-103">Meghívhatja a hálózatkonfigurációs diagnosztikai munkamenetet a célerőforrás meghatározott hálózati profiljaihoz.</span><span class="sxs-lookup"><span data-stu-id="3c399-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="3c399-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c399-104">SYNTAX</span></span>

### <span data-ttu-id="3c399-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c399-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c399-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3c399-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c399-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3c399-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c399-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c399-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c399-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c399-109">DESCRIPTION</span></span>
<span data-ttu-id="3c399-110">A Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic parancsmag meghívja a hálózati konfigurációs diagnosztikai munkamenetet a célerőforrás megadott hálózati profiljaihoz.</span><span class="sxs-lookup"><span data-stu-id="3c399-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="3c399-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c399-111">EXAMPLES</span></span>

### <span data-ttu-id="3c399-112">1. példa: A virtuális géphez és a megadott hálózati profilhoz szükséges hálózati konfigurációs diagnosztikai munkamenet meghívása</span><span class="sxs-lookup"><span data-stu-id="3c399-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="3c399-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c399-113">PARAMETERS</span></span>

### <span data-ttu-id="3c399-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c399-114">-AsJob</span></span>
<span data-ttu-id="3c399-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3c399-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c399-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c399-116">-DefaultProfile</span></span>
<span data-ttu-id="3c399-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c399-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c399-118">-Location</span><span class="sxs-lookup"><span data-stu-id="3c399-118">-Location</span></span>
<span data-ttu-id="3c399-119">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="3c399-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3c399-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c399-120">-NetworkWatcher</span></span>
<span data-ttu-id="3c399-121">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="3c399-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="3c399-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3c399-122">-NetworkWatcherName</span></span>
<span data-ttu-id="3c399-123">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="3c399-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="3c399-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c399-124">-Profile</span></span>
<span data-ttu-id="3c399-125">Hálózati konfigurációs diagnosztikai profilok listája.</span><span class="sxs-lookup"><span data-stu-id="3c399-125">List of network configuration diagnostic profiles.</span></span>

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

### <span data-ttu-id="3c399-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c399-126">-ResourceGroupName</span></span>
<span data-ttu-id="3c399-127">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3c399-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3c399-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c399-128">-ResourceId</span></span>
<span data-ttu-id="3c399-129">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3c399-129">Resource ID.</span></span>

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

### <span data-ttu-id="3c399-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3c399-130">-TargetResourceId</span></span>
<span data-ttu-id="3c399-131">A hálózati konfigurációs diagnosztikai célerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c399-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="3c399-132">Érvényes beállítások: VM, NetworkInterface, VMSS/NetworkInterface és Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3c399-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="3c399-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="3c399-133">-VerbosityLevel</span></span>
<span data-ttu-id="3c399-134">Részletességi szint.</span><span class="sxs-lookup"><span data-stu-id="3c399-134">Verbosity level.</span></span>
<span data-ttu-id="3c399-135">Az elfogadott értékek: "Normál", "Minimum", "Teljes".</span><span class="sxs-lookup"><span data-stu-id="3c399-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

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

### <span data-ttu-id="3c399-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c399-136">CommonParameters</span></span>
<span data-ttu-id="3c399-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c399-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c399-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c399-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c399-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c399-139">INPUTS</span></span>

### <span data-ttu-id="3c399-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c399-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3c399-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3c399-141">System.String</span></span>

## <span data-ttu-id="3c399-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c399-142">OUTPUTS</span></span>

### <span data-ttu-id="3c399-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="3c399-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="3c399-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c399-144">NOTES</span></span>
<span data-ttu-id="3c399-145">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, figyelő, diagnosztikai, profil</span><span class="sxs-lookup"><span data-stu-id="3c399-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="3c399-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c399-146">RELATED LINKS</span></span>

[<span data-ttu-id="3c399-147">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c399-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3c399-148">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c399-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3c399-149">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3c399-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3c399-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3c399-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3c399-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3c399-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3c399-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3c399-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3c399-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3c399-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3c399-154">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3c399-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3c399-155">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3c399-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3c399-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3c399-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3c399-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3c399-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3c399-158">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3c399-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3c399-159">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c399-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3c399-160">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3c399-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3c399-161">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3c399-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3c399-162">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c399-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3c399-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c399-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3c399-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c399-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3c399-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3c399-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3c399-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c399-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3c399-167">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c399-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3c399-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3c399-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3c399-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3c399-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3c399-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3c399-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3c399-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3c399-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3c399-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3c399-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3c399-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3c399-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
