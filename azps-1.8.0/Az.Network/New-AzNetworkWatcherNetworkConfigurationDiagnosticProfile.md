---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: b05f62559670bdbdb0c018dff8febd8c5c8dfb20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670300"
---
# <span data-ttu-id="56ad2-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="56ad2-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="56ad2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="56ad2-103">Új hálózati konfigurációs diagnosztikai profil objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="56ad2-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="56ad2-104">Ezzel az objektummal korlátozhatja a hálózati Confiuration a megadott feltételeknek megfelelő diagnosztikai munkamenet során.</span><span class="sxs-lookup"><span data-stu-id="56ad2-104">This object is used to restrict the network confiuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="56ad2-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56ad2-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56ad2-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="56ad2-106">DESCRIPTION</span></span>
<span data-ttu-id="56ad2-107">Az New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile parancsmag új diagnosztikai profil-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="56ad2-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="56ad2-108">Ezzel az objektummal korlátozhatja a hálózati Confiuration egy hálózati konfigurációs diagnosztikai munkamenet során a megadott feltételekkel.</span><span class="sxs-lookup"><span data-stu-id="56ad2-108">This object is used to restrict the network confiuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="56ad2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="56ad2-109">EXAMPLES</span></span>

### <span data-ttu-id="56ad2-110">1. példa: hálózati konfigurációs diagnosztikai munkamenet meghívása VM-hez és a megadott hálózati profilhoz</span><span class="sxs-lookup"><span data-stu-id="56ad2-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="56ad2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56ad2-111">PARAMETERS</span></span>

### <span data-ttu-id="56ad2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ad2-112">-DefaultProfile</span></span>
<span data-ttu-id="56ad2-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56ad2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56ad2-114">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="56ad2-114">-Destination</span></span>
<span data-ttu-id="56ad2-115">Forgalmi cél.</span><span class="sxs-lookup"><span data-stu-id="56ad2-115">Traffic destination.</span></span>
<span data-ttu-id="56ad2-116">Az elfogadott értékek a következők: "\*", IP-cím/CIDR, szolgáltatás címke.</span><span class="sxs-lookup"><span data-stu-id="56ad2-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="56ad2-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="56ad2-117">-DestinationPort</span></span>
<span data-ttu-id="56ad2-118">Forgalom szerinti célport</span><span class="sxs-lookup"><span data-stu-id="56ad2-118">Traffic destination port.</span></span>
<span data-ttu-id="56ad2-119">Az elfogadott értékek "\*", port (például 3389) és porttartomány (például 80-100).</span><span class="sxs-lookup"><span data-stu-id="56ad2-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="56ad2-120">-Irány</span><span class="sxs-lookup"><span data-stu-id="56ad2-120">-Direction</span></span>
<span data-ttu-id="56ad2-121">A forgalom iránya.</span><span class="sxs-lookup"><span data-stu-id="56ad2-121">The direction of the traffic.</span></span>
<span data-ttu-id="56ad2-122">Az elfogadott értékek "Beérkezők" és "kimenő"</span><span class="sxs-lookup"><span data-stu-id="56ad2-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="56ad2-123">-Protocol</span><span class="sxs-lookup"><span data-stu-id="56ad2-123">-Protocol</span></span>
<span data-ttu-id="56ad2-124">Ellenőrizendő protokoll.</span><span class="sxs-lookup"><span data-stu-id="56ad2-124">Protocol to be verified on.</span></span>
<span data-ttu-id="56ad2-125">Az elfogadott értékek "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="56ad2-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="56ad2-126">-Forrás</span><span class="sxs-lookup"><span data-stu-id="56ad2-126">-Source</span></span>
<span data-ttu-id="56ad2-127">Forgalom forrása.</span><span class="sxs-lookup"><span data-stu-id="56ad2-127">Traffic source.</span></span>
<span data-ttu-id="56ad2-128">Az elfogadott értékek: ' \* ', IP-cím/CIDR, szolgáltatás címke.</span><span class="sxs-lookup"><span data-stu-id="56ad2-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="56ad2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ad2-129">CommonParameters</span></span>
<span data-ttu-id="56ad2-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56ad2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ad2-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56ad2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ad2-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56ad2-132">INPUTS</span></span>

### <span data-ttu-id="56ad2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="56ad2-133">System.String</span></span>

## <span data-ttu-id="56ad2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56ad2-134">OUTPUTS</span></span>

### <span data-ttu-id="56ad2-135">Microsoft. Azure. commands. Network. models. PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="56ad2-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="56ad2-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56ad2-136">NOTES</span></span>
<span data-ttu-id="56ad2-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, diagnosztikai, profil</span><span class="sxs-lookup"><span data-stu-id="56ad2-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="56ad2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56ad2-138">RELATED LINKS</span></span>

[<span data-ttu-id="56ad2-139">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56ad2-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="56ad2-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56ad2-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="56ad2-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56ad2-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="56ad2-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="56ad2-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="56ad2-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="56ad2-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="56ad2-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="56ad2-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="56ad2-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="56ad2-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="56ad2-146">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56ad2-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56ad2-147">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="56ad2-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="56ad2-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56ad2-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56ad2-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56ad2-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56ad2-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56ad2-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56ad2-151">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="56ad2-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="56ad2-152">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="56ad2-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="56ad2-153">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="56ad2-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="56ad2-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="56ad2-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="56ad2-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="56ad2-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="56ad2-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="56ad2-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="56ad2-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="56ad2-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="56ad2-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="56ad2-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="56ad2-159">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="56ad2-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="56ad2-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="56ad2-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="56ad2-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="56ad2-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="56ad2-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="56ad2-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="56ad2-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="56ad2-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="56ad2-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="56ad2-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="56ad2-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="56ad2-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
