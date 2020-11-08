---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: 8e1215adc9b6f6ab72d752fd58771f5155a8bc25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014852"
---
# <span data-ttu-id="4d158-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4d158-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="4d158-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d158-102">SYNOPSIS</span></span>
<span data-ttu-id="4d158-103">Hálózati konfigurációs diagnosztikai munkamenet meghívása a meghatározott hálózati profilokhoz a cél erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="4d158-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="4d158-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d158-104">SYNTAX</span></span>

### <span data-ttu-id="4d158-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d158-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d158-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4d158-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d158-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4d158-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d158-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d158-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d158-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d158-109">DESCRIPTION</span></span>
<span data-ttu-id="4d158-110">A Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic parancsmag hálózati konfigurációs diagnosztikai munkamenetet kezdeményez a meghatározott hálózati profilokhoz a cél erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="4d158-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="4d158-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4d158-111">EXAMPLES</span></span>

### <span data-ttu-id="4d158-112">1. példa: hálózati konfigurációs diagnosztikai munkamenet meghívása VM-hez és a megadott hálózati profilhoz</span><span class="sxs-lookup"><span data-stu-id="4d158-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="4d158-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d158-113">PARAMETERS</span></span>

### <span data-ttu-id="4d158-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d158-114">-AsJob</span></span>
<span data-ttu-id="4d158-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4d158-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d158-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d158-116">-DefaultProfile</span></span>
<span data-ttu-id="4d158-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d158-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d158-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="4d158-118">-Location</span></span>
<span data-ttu-id="4d158-119">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="4d158-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4d158-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d158-120">-NetworkWatcher</span></span>
<span data-ttu-id="4d158-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="4d158-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="4d158-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4d158-122">-NetworkWatcherName</span></span>
<span data-ttu-id="4d158-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="4d158-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="4d158-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="4d158-124">-Profile</span></span>
<span data-ttu-id="4d158-125">A hálózati konfiguráció diagnosztikai profiljainak listája.</span><span class="sxs-lookup"><span data-stu-id="4d158-125">List of network configuration diagnostic profiles.</span></span>

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

### <span data-ttu-id="4d158-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d158-126">-ResourceGroupName</span></span>
<span data-ttu-id="4d158-127">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d158-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4d158-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d158-128">-ResourceId</span></span>
<span data-ttu-id="4d158-129">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4d158-129">Resource ID.</span></span>

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

### <span data-ttu-id="4d158-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4d158-130">-TargetResourceId</span></span>
<span data-ttu-id="4d158-131">A cél-erőforrás azonosítója a hálózati konfigurációs diagnosztikai művelet végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="4d158-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="4d158-132">Az érvényes beállítások a VM, a NetworkInterface, a VMSS/NetworkInterface és az Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4d158-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="4d158-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="4d158-133">-VerbosityLevel</span></span>
<span data-ttu-id="4d158-134">Részletességi szint</span><span class="sxs-lookup"><span data-stu-id="4d158-134">Verbosity level.</span></span>
<span data-ttu-id="4d158-135">Az elfogadott értékek "normál", "minimum", "teljes".</span><span class="sxs-lookup"><span data-stu-id="4d158-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

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

### <span data-ttu-id="4d158-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d158-136">CommonParameters</span></span>
<span data-ttu-id="4d158-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d158-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d158-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d158-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d158-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d158-139">INPUTS</span></span>

### <span data-ttu-id="4d158-140">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d158-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4d158-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4d158-141">System.String</span></span>

## <span data-ttu-id="4d158-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d158-142">OUTPUTS</span></span>

### <span data-ttu-id="4d158-143">Microsoft. Azure. commands. Network. models. PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="4d158-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="4d158-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d158-144">NOTES</span></span>
<span data-ttu-id="4d158-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, diagnosztikai, profil</span><span class="sxs-lookup"><span data-stu-id="4d158-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="4d158-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d158-146">RELATED LINKS</span></span>

[<span data-ttu-id="4d158-147">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d158-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4d158-148">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d158-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4d158-149">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4d158-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4d158-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4d158-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4d158-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4d158-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4d158-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4d158-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4d158-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4d158-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4d158-154">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d158-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d158-155">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4d158-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4d158-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d158-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d158-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d158-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d158-158">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d158-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d158-159">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d158-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4d158-160">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4d158-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4d158-161">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4d158-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4d158-162">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d158-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4d158-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d158-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4d158-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d158-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4d158-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4d158-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4d158-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d158-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4d158-167">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d158-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4d158-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4d158-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4d158-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4d158-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4d158-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4d158-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4d158-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4d158-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4d158-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4d158-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4d158-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d158-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
