---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: c559001c68126c42c3d4ae6eaead2beda3ded5f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185974"
---
# <span data-ttu-id="3d167-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="3d167-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="3d167-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d167-102">SYNOPSIS</span></span>
<span data-ttu-id="3d167-103">Új hálózati konfigurációs diagnosztikai profil objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="3d167-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="3d167-104">Ezzel az objektummal korlátozható a hálózati konfiguráció a megadott feltételeknek megfelelő diagnosztikai munkamenet során.</span><span class="sxs-lookup"><span data-stu-id="3d167-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="3d167-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d167-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d167-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d167-106">DESCRIPTION</span></span>
<span data-ttu-id="3d167-107">Az New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile parancsmag új diagnosztikai profil-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3d167-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="3d167-108">Ez az objektum a hálózati konfiguráció korlátozására szolgál a hálózati konfigurációs diagnosztikai munkamenet során a megadott feltételekkel.</span><span class="sxs-lookup"><span data-stu-id="3d167-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="3d167-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3d167-109">EXAMPLES</span></span>

### <span data-ttu-id="3d167-110">1. példa: hálózati konfigurációs diagnosztikai munkamenet meghívása VM-hez és a megadott hálózati profilhoz</span><span class="sxs-lookup"><span data-stu-id="3d167-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="3d167-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d167-111">PARAMETERS</span></span>

### <span data-ttu-id="3d167-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d167-112">-DefaultProfile</span></span>
<span data-ttu-id="3d167-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d167-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d167-114">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="3d167-114">-Destination</span></span>
<span data-ttu-id="3d167-115">Forgalmi cél.</span><span class="sxs-lookup"><span data-stu-id="3d167-115">Traffic destination.</span></span>
<span data-ttu-id="3d167-116">Az elfogadott értékek a következők: "\*", IP-cím/CIDR, szolgáltatás címke.</span><span class="sxs-lookup"><span data-stu-id="3d167-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="3d167-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3d167-117">-DestinationPort</span></span>
<span data-ttu-id="3d167-118">Forgalom szerinti célport</span><span class="sxs-lookup"><span data-stu-id="3d167-118">Traffic destination port.</span></span>
<span data-ttu-id="3d167-119">Az elfogadott értékek "\*", port (például 3389) és porttartomány (például 80-100).</span><span class="sxs-lookup"><span data-stu-id="3d167-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="3d167-120">-Irány</span><span class="sxs-lookup"><span data-stu-id="3d167-120">-Direction</span></span>
<span data-ttu-id="3d167-121">A forgalom iránya.</span><span class="sxs-lookup"><span data-stu-id="3d167-121">The direction of the traffic.</span></span>
<span data-ttu-id="3d167-122">Az elfogadott értékek "Beérkezők" és "kimenő"</span><span class="sxs-lookup"><span data-stu-id="3d167-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="3d167-123">-Protocol</span><span class="sxs-lookup"><span data-stu-id="3d167-123">-Protocol</span></span>
<span data-ttu-id="3d167-124">Ellenőrizendő protokoll.</span><span class="sxs-lookup"><span data-stu-id="3d167-124">Protocol to be verified on.</span></span>
<span data-ttu-id="3d167-125">Az elfogadott értékek "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="3d167-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="3d167-126">-Forrás</span><span class="sxs-lookup"><span data-stu-id="3d167-126">-Source</span></span>
<span data-ttu-id="3d167-127">Forgalom forrása.</span><span class="sxs-lookup"><span data-stu-id="3d167-127">Traffic source.</span></span>
<span data-ttu-id="3d167-128">Az elfogadott értékek: ' \* ', IP-cím/CIDR, szolgáltatás címke.</span><span class="sxs-lookup"><span data-stu-id="3d167-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="3d167-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d167-129">CommonParameters</span></span>
<span data-ttu-id="3d167-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d167-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d167-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d167-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d167-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d167-132">INPUTS</span></span>

### <span data-ttu-id="3d167-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3d167-133">System.String</span></span>

## <span data-ttu-id="3d167-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d167-134">OUTPUTS</span></span>

### <span data-ttu-id="3d167-135">Microsoft. Azure. commands. Network. models. PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="3d167-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="3d167-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d167-136">NOTES</span></span>
<span data-ttu-id="3d167-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, diagnosztikai, profil</span><span class="sxs-lookup"><span data-stu-id="3d167-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="3d167-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d167-138">RELATED LINKS</span></span>

[<span data-ttu-id="3d167-139">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d167-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3d167-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d167-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3d167-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d167-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3d167-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3d167-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3d167-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3d167-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3d167-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3d167-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3d167-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3d167-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3d167-146">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d167-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d167-147">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3d167-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3d167-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d167-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d167-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d167-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d167-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d167-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d167-151">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d167-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3d167-152">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3d167-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3d167-153">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3d167-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3d167-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d167-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d167-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d167-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d167-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d167-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d167-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3d167-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3d167-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d167-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d167-159">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d167-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d167-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3d167-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3d167-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3d167-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3d167-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3d167-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3d167-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3d167-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3d167-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3d167-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3d167-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d167-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
