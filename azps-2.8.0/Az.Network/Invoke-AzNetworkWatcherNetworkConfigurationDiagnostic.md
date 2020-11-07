---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: a79de3beadefefd3de65b830f42e4728ca6b6b82
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837530"
---
# <span data-ttu-id="488fe-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="488fe-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="488fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="488fe-102">SYNOPSIS</span></span>
<span data-ttu-id="488fe-103">Hálózati konfigurációs diagnosztikai munkamenet meghívása a meghatározott hálózati profilokhoz a cél erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="488fe-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="488fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="488fe-104">SYNTAX</span></span>

### <span data-ttu-id="488fe-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="488fe-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="488fe-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="488fe-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="488fe-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="488fe-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="488fe-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="488fe-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="488fe-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="488fe-109">DESCRIPTION</span></span>
<span data-ttu-id="488fe-110">A Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic parancsmag hálózati konfigurációs diagnosztikai munkamenetet kezdeményez a meghatározott hálózati profilokhoz a cél erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="488fe-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="488fe-111">Példák</span><span class="sxs-lookup"><span data-stu-id="488fe-111">EXAMPLES</span></span>

### <span data-ttu-id="488fe-112">1. példa: hálózati konfigurációs diagnosztikai munkamenet meghívása VM-hez és a megadott hálózati profilhoz</span><span class="sxs-lookup"><span data-stu-id="488fe-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="488fe-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="488fe-113">PARAMETERS</span></span>

### <span data-ttu-id="488fe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="488fe-114">-AsJob</span></span>
<span data-ttu-id="488fe-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="488fe-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="488fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="488fe-116">-DefaultProfile</span></span>
<span data-ttu-id="488fe-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="488fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="488fe-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="488fe-118">-Location</span></span>
<span data-ttu-id="488fe-119">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="488fe-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="488fe-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="488fe-120">-NetworkWatcher</span></span>
<span data-ttu-id="488fe-121">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="488fe-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="488fe-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="488fe-122">-NetworkWatcherName</span></span>
<span data-ttu-id="488fe-123">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="488fe-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="488fe-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="488fe-124">-Profile</span></span>
<span data-ttu-id="488fe-125">A hálózati konfiguráció diagnosztikai profiljainak listája.</span><span class="sxs-lookup"><span data-stu-id="488fe-125">List of network configuration diagnostic profiles.</span></span>

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

### <span data-ttu-id="488fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="488fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="488fe-127">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="488fe-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="488fe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="488fe-128">-ResourceId</span></span>
<span data-ttu-id="488fe-129">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="488fe-129">Resource ID.</span></span>

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

### <span data-ttu-id="488fe-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="488fe-130">-TargetResourceId</span></span>
<span data-ttu-id="488fe-131">A cél-erőforrás azonosítója a hálózati konfigurációs diagnosztikai művelet végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="488fe-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="488fe-132">Az érvényes beállítások a VM, a NetworkInterface, a VMSS/NetworkInterface és az Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="488fe-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="488fe-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="488fe-133">-VerbosityLevel</span></span>
<span data-ttu-id="488fe-134">Részletességi szint</span><span class="sxs-lookup"><span data-stu-id="488fe-134">Verbosity level.</span></span>
<span data-ttu-id="488fe-135">Az elfogadott értékek "normál", "minimum", "teljes".</span><span class="sxs-lookup"><span data-stu-id="488fe-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

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

### <span data-ttu-id="488fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="488fe-136">CommonParameters</span></span>
<span data-ttu-id="488fe-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="488fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="488fe-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="488fe-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="488fe-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="488fe-139">INPUTS</span></span>

### <span data-ttu-id="488fe-140">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="488fe-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="488fe-141">System. String</span><span class="sxs-lookup"><span data-stu-id="488fe-141">System.String</span></span>

## <span data-ttu-id="488fe-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="488fe-142">OUTPUTS</span></span>

### <span data-ttu-id="488fe-143">Microsoft. Azure. commands. Network. models. PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="488fe-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="488fe-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="488fe-144">NOTES</span></span>
<span data-ttu-id="488fe-145">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, diagnosztikai, profil</span><span class="sxs-lookup"><span data-stu-id="488fe-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="488fe-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="488fe-146">RELATED LINKS</span></span>

[<span data-ttu-id="488fe-147">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="488fe-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="488fe-148">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="488fe-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="488fe-149">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="488fe-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="488fe-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="488fe-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="488fe-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="488fe-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="488fe-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="488fe-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="488fe-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="488fe-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="488fe-154">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="488fe-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="488fe-155">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="488fe-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="488fe-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="488fe-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="488fe-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="488fe-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="488fe-158">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="488fe-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="488fe-159">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="488fe-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="488fe-160">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="488fe-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="488fe-161">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="488fe-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="488fe-162">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="488fe-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="488fe-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="488fe-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="488fe-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="488fe-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="488fe-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="488fe-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="488fe-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="488fe-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="488fe-167">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="488fe-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="488fe-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="488fe-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="488fe-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="488fe-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="488fe-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="488fe-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="488fe-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="488fe-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="488fe-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="488fe-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="488fe-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="488fe-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
