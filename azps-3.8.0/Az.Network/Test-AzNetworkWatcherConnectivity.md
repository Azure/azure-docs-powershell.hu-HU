---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: b6c33809c1b738db47407ec65352adfcfb001957
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011096"
---
# <span data-ttu-id="11f28-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="11f28-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="11f28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11f28-102">SYNOPSIS</span></span>
<span data-ttu-id="11f28-103">A megadott forrású VM és rendeltetési hely kapcsolati adatait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="11f28-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="11f28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11f28-104">SYNTAX</span></span>

### <span data-ttu-id="11f28-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11f28-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11f28-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="11f28-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11f28-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="11f28-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11f28-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="11f28-108">DESCRIPTION</span></span>
<span data-ttu-id="11f28-109">A Test-AzNetworkWatcherConnectivity parancsmag a megadott forrású VM és a célhely kapcsolati adatait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="11f28-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="11f28-110">Ha a forrás és a cél közötti kapcsolat nem hozható létre, a parancsmag részleteket ad meg a problémáról.</span><span class="sxs-lookup"><span data-stu-id="11f28-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="11f28-111">Példák</span><span class="sxs-lookup"><span data-stu-id="11f28-111">EXAMPLES</span></span>

### <span data-ttu-id="11f28-112">1. példa: a Hálózatfigyelő-kapcsolat tesztelése VM-ről egy webhelyre</span><span class="sxs-lookup"><span data-stu-id="11f28-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
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

<span data-ttu-id="11f28-113">Ebben a példában a VM-től az Azure-www.bing.com való kapcsolatot teszteljük.</span><span class="sxs-lookup"><span data-stu-id="11f28-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="11f28-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11f28-114">PARAMETERS</span></span>

### <span data-ttu-id="11f28-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11f28-115">-AsJob</span></span>
<span data-ttu-id="11f28-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="11f28-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11f28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f28-117">-DefaultProfile</span></span>
<span data-ttu-id="11f28-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11f28-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11f28-119">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="11f28-119">-DestinationAddress</span></span>
<span data-ttu-id="11f28-120">Annak az erőforrásnak az IP-címe vagy URI-azonosítója, amelyhez csatlakozási kísérletet tesz.</span><span class="sxs-lookup"><span data-stu-id="11f28-120">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="11f28-121">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="11f28-121">-DestinationId</span></span>
<span data-ttu-id="11f28-122">Annak az erőforrásnak az azonosítója, amelyhez csatlakozási kísérletet fog tenni.</span><span class="sxs-lookup"><span data-stu-id="11f28-122">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="11f28-123">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="11f28-123">-DestinationPort</span></span>
<span data-ttu-id="11f28-124">Annak a portnak a végrehajtása, amelyen ellenőrizni fogja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="11f28-124">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="11f28-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="11f28-125">-Location</span></span>
<span data-ttu-id="11f28-126">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="11f28-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="11f28-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11f28-127">-NetworkWatcher</span></span>
<span data-ttu-id="11f28-128">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="11f28-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="11f28-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="11f28-129">-NetworkWatcherName</span></span>
<span data-ttu-id="11f28-130">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="11f28-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="11f28-131">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="11f28-131">-ProtocolConfiguration</span></span>
<span data-ttu-id="11f28-132">Annak a protokollnak a konfigurációja, amelyen a kapcsolat ellenőrzése történik.</span><span class="sxs-lookup"><span data-stu-id="11f28-132">Protocol configuration on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="11f28-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11f28-133">-ResourceGroupName</span></span>
<span data-ttu-id="11f28-134">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="11f28-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="11f28-135">-SourceId forrásazonosító</span><span class="sxs-lookup"><span data-stu-id="11f28-135">-SourceId</span></span>
<span data-ttu-id="11f28-136">Annak az erőforrásnak az azonosítója, amelyből a kapcsolódási ellenőrzést kezdeményezni kívánja.</span><span class="sxs-lookup"><span data-stu-id="11f28-136">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="11f28-137">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="11f28-137">-SourcePort</span></span>
<span data-ttu-id="11f28-138">Annak a forrásnak a portja, amelyből a kapcsolódási ellenőrzést végrehajtja.</span><span class="sxs-lookup"><span data-stu-id="11f28-138">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="11f28-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f28-139">CommonParameters</span></span>
<span data-ttu-id="11f28-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11f28-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f28-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f28-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f28-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11f28-142">INPUTS</span></span>

### <span data-ttu-id="11f28-143">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11f28-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="11f28-144">System. String</span><span class="sxs-lookup"><span data-stu-id="11f28-144">System.String</span></span>

### <span data-ttu-id="11f28-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="11f28-145">System.Int32</span></span>

## <span data-ttu-id="11f28-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11f28-146">OUTPUTS</span></span>

### <span data-ttu-id="11f28-147">Microsoft. Azure. commands. Network. models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="11f28-147">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="11f28-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11f28-148">NOTES</span></span>
<span data-ttu-id="11f28-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózat, hálózati figyelő</span><span class="sxs-lookup"><span data-stu-id="11f28-149">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="11f28-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11f28-150">RELATED LINKS</span></span>

<span data-ttu-id="11f28-151">[Új – AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="11f28-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="11f28-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="11f28-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="11f28-153">[Új – AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Új – AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="11f28-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="11f28-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [Új – AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [Teszt-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [Teszt-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Új – AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="11f28-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
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
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span></span>