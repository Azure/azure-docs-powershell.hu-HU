---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: f406ddbf3e975e6caa3d9e9164673ec95a311e76
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400178"
---
# <span data-ttu-id="2b74f-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="2b74f-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="2b74f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b74f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b74f-103">Létrehoz egy új hálózati konfigurációs diagnosztikai profilobjektumot.</span><span class="sxs-lookup"><span data-stu-id="2b74f-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="2b74f-104">Ez az objektum egy diagnosztikai munkamenet során a megadott feltételekkel korlátozza a hálózati konfekurációt.</span><span class="sxs-lookup"><span data-stu-id="2b74f-104">This object is used to restrict the network confiuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="2b74f-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b74f-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b74f-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b74f-106">DESCRIPTION</span></span>
<span data-ttu-id="2b74f-107">A New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile parancsmag létrehoz egy új diagnosztikai profilobjektumot.</span><span class="sxs-lookup"><span data-stu-id="2b74f-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="2b74f-108">Ezzel az objektummal korlátozható a hálózati konfiguráció beállítása egy hálózati konfigurációs diagnosztikai munkamenetben a megadott feltételekkel.</span><span class="sxs-lookup"><span data-stu-id="2b74f-108">This object is used to restrict the network confiuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="2b74f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b74f-109">EXAMPLES</span></span>

### <span data-ttu-id="2b74f-110">1. példa: A virtuális géphez és a megadott hálózati profilhoz szükséges hálózati konfigurációs diagnosztikai munkamenet meghívása</span><span class="sxs-lookup"><span data-stu-id="2b74f-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="2b74f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b74f-111">PARAMETERS</span></span>

### <span data-ttu-id="2b74f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b74f-112">-DefaultProfile</span></span>
<span data-ttu-id="2b74f-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b74f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b74f-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="2b74f-114">-Destination</span></span>
<span data-ttu-id="2b74f-115">Forgalom célhelye.</span><span class="sxs-lookup"><span data-stu-id="2b74f-115">Traffic destination.</span></span>
<span data-ttu-id="2b74f-116">Az elfogadott értékek: '\*', IP Address/CIDR, Service Tag.</span><span class="sxs-lookup"><span data-stu-id="2b74f-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="2b74f-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2b74f-117">-DestinationPort</span></span>
<span data-ttu-id="2b74f-118">Forgalom célportja.</span><span class="sxs-lookup"><span data-stu-id="2b74f-118">Traffic destination port.</span></span>
<span data-ttu-id="2b74f-119">Az elfogadott értékek a "\*", a port (például 3389) és a porttartomány (például 80–100).</span><span class="sxs-lookup"><span data-stu-id="2b74f-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="2b74f-120">-Irány</span><span class="sxs-lookup"><span data-stu-id="2b74f-120">-Direction</span></span>
<span data-ttu-id="2b74f-121">A forgalom iránya.</span><span class="sxs-lookup"><span data-stu-id="2b74f-121">The direction of the traffic.</span></span>
<span data-ttu-id="2b74f-122">Az elfogadott értékek a "Bejövő" és a "Kimenő" érték.</span><span class="sxs-lookup"><span data-stu-id="2b74f-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b74f-123">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2b74f-123">-Protocol</span></span>
<span data-ttu-id="2b74f-124">A igazolható protokoll.</span><span class="sxs-lookup"><span data-stu-id="2b74f-124">Protocol to be verified on.</span></span>
<span data-ttu-id="2b74f-125">Az elfogadott értékek: '\*', TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="2b74f-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="2b74f-126">-Source</span><span class="sxs-lookup"><span data-stu-id="2b74f-126">-Source</span></span>
<span data-ttu-id="2b74f-127">Forgalomforrás.</span><span class="sxs-lookup"><span data-stu-id="2b74f-127">Traffic source.</span></span>
<span data-ttu-id="2b74f-128">Az elfogadott értékek: '\*', IP Address/CIDR, Service Tag.</span><span class="sxs-lookup"><span data-stu-id="2b74f-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="2b74f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b74f-129">CommonParameters</span></span>
<span data-ttu-id="2b74f-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b74f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b74f-131">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b74f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b74f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b74f-132">INPUTS</span></span>

### <span data-ttu-id="2b74f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2b74f-133">System.String</span></span>

## <span data-ttu-id="2b74f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b74f-134">OUTPUTS</span></span>

### <span data-ttu-id="2b74f-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="2b74f-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="2b74f-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b74f-136">NOTES</span></span>
<span data-ttu-id="2b74f-137">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, figyelő, diagnosztikai, profil</span><span class="sxs-lookup"><span data-stu-id="2b74f-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="2b74f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b74f-138">RELATED LINKS</span></span>

[<span data-ttu-id="2b74f-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b74f-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2b74f-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b74f-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2b74f-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b74f-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2b74f-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2b74f-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2b74f-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2b74f-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2b74f-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2b74f-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2b74f-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2b74f-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2b74f-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b74f-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b74f-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2b74f-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2b74f-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b74f-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b74f-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b74f-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b74f-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b74f-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b74f-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b74f-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2b74f-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2b74f-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2b74f-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2b74f-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2b74f-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b74f-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2b74f-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b74f-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2b74f-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b74f-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2b74f-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2b74f-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2b74f-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b74f-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2b74f-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b74f-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2b74f-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2b74f-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2b74f-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2b74f-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2b74f-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2b74f-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2b74f-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2b74f-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2b74f-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2b74f-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2b74f-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b74f-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
