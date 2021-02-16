---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: 6b689a96a4f737b2f92b4146f71faff7a09d8d36
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402711"
---
# <span data-ttu-id="1b538-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1b538-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="1b538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b538-102">SYNOPSIS</span></span>
<span data-ttu-id="1b538-103">Visszaadja egy adott forrás virtuális gép és egy célhely csatlakozási adatait.</span><span class="sxs-lookup"><span data-stu-id="1b538-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="1b538-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b538-104">SYNTAX</span></span>

### <span data-ttu-id="1b538-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b538-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b538-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1b538-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b538-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1b538-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b538-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b538-108">DESCRIPTION</span></span>
<span data-ttu-id="1b538-109">A Test-AzNetworkWatcherConnectivity parancsmag kapcsolódási adatokat ad vissza egy adott forrás VM-hez és egy célhelyhez.</span><span class="sxs-lookup"><span data-stu-id="1b538-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="1b538-110">Ha nem lehet kapcsolatot létrehozni a forrás és a cél között, a parancsmag részletes információkat ad a problémáról.</span><span class="sxs-lookup"><span data-stu-id="1b538-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="1b538-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b538-111">EXAMPLES</span></span>

### <span data-ttu-id="1b538-112">1. példa: Hálózati figyelő csatlakoztatásának tesztelése virtuális gépről egy webhelyre</span><span class="sxs-lookup"><span data-stu-id="1b538-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="1b538-113">Ebben a példában teszteljük az Azure virtuális gép és a www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="1b538-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="1b538-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b538-114">PARAMETERS</span></span>

### <span data-ttu-id="1b538-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b538-115">-AsJob</span></span>
<span data-ttu-id="1b538-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1b538-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b538-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b538-117">-DefaultProfile</span></span>
<span data-ttu-id="1b538-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b538-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b538-119">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="1b538-119">-DestinationAddress</span></span>
<span data-ttu-id="1b538-120">Az az IP-cím vagy URI-cím, amelyhez csatlakozási kísérletet fog tenni.</span><span class="sxs-lookup"><span data-stu-id="1b538-120">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="1b538-121">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="1b538-121">-DestinationId</span></span>
<span data-ttu-id="1b538-122">Annak az erőforrásnak az azonosítója, amelyhez csatlakozási kísérlet készül.</span><span class="sxs-lookup"><span data-stu-id="1b538-122">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="1b538-123">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="1b538-123">-DestinationPort</span></span>
<span data-ttu-id="1b538-124">Port, amelyen a kapcsolat ellenőrzése történik.</span><span class="sxs-lookup"><span data-stu-id="1b538-124">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b538-125">-Location</span><span class="sxs-lookup"><span data-stu-id="1b538-125">-Location</span></span>
<span data-ttu-id="1b538-126">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="1b538-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1b538-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b538-127">-NetworkWatcher</span></span>
<span data-ttu-id="1b538-128">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="1b538-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="1b538-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1b538-129">-NetworkWatcherName</span></span>
<span data-ttu-id="1b538-130">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="1b538-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b538-131">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b538-131">-ProtocolConfiguration</span></span>
<span data-ttu-id="1b538-132">Protocal configuration on which check connectivity will be performed.</span><span class="sxs-lookup"><span data-stu-id="1b538-132">Protocal configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b538-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b538-133">-ResourceGroupName</span></span>
<span data-ttu-id="1b538-134">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1b538-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1b538-135">-SourceId</span><span class="sxs-lookup"><span data-stu-id="1b538-135">-SourceId</span></span>
<span data-ttu-id="1b538-136">Annak az erőforrásnak az azonosítója, amelyből a kapcsolatellenőrzést kezdeményezni fogja.</span><span class="sxs-lookup"><span data-stu-id="1b538-136">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="1b538-137">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="1b538-137">-SourcePort</span></span>
<span data-ttu-id="1b538-138">Az a forrásport, amelyről a kapcsolat ellenőrzése történik.</span><span class="sxs-lookup"><span data-stu-id="1b538-138">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b538-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b538-139">CommonParameters</span></span>
<span data-ttu-id="1b538-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b538-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b538-141">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b538-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b538-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b538-142">INPUTS</span></span>

### <span data-ttu-id="1b538-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b538-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1b538-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1b538-144">System.String</span></span>

### <span data-ttu-id="1b538-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1b538-145">System.Int32</span></span>

## <span data-ttu-id="1b538-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b538-146">OUTPUTS</span></span>

### <span data-ttu-id="1b538-147">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="1b538-147">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="1b538-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b538-148">NOTES</span></span>
<span data-ttu-id="1b538-149">Kulcsszavak: azure, azurerm, arm, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő</span><span class="sxs-lookup"><span data-stu-id="1b538-149">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="1b538-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b538-150">RELATED LINKS</span></span>

<span data-ttu-id="1b538-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="1b538-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="1b538-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="1b538-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="1b538-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="1b538-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="1b538-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="1b538-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span></span>
