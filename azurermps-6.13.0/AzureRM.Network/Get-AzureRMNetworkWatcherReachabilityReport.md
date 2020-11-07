---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 09d75e73cc6139bfa2c3d0d6293b07060a709f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680055"
---
# <span data-ttu-id="c277c-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c277c-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="c277c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c277c-102">SYNOPSIS</span></span>
<span data-ttu-id="c277c-103">Az internetszolgáltató relatív késési pontszámát adja meg egy adott helyről az Azure-régiók számára.</span><span class="sxs-lookup"><span data-stu-id="c277c-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c277c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c277c-104">SYNTAX</span></span>

### <span data-ttu-id="c277c-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c277c-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c277c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c277c-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c277c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c277c-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c277c-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c277c-108">SetByLocation</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherLocation <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c277c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c277c-109">DESCRIPTION</span></span>
<span data-ttu-id="c277c-110">A Get-AzureRmNetworkWatcherReachabilityReport az Azure-régiók meghatározott helyéről szerzi be az internetszolgáltató relatív késési pontszámát.</span><span class="sxs-lookup"><span data-stu-id="c277c-110">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="c277c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c277c-111">EXAMPLES</span></span>

### <span data-ttu-id="c277c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c277c-112">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="c277c-113">A 2017-10-10-től az 2017-10-12-ig, az Amerikai Egyesült ÁLLAMOKban.</span><span class="sxs-lookup"><span data-stu-id="c277c-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="c277c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c277c-114">PARAMETERS</span></span>

### <span data-ttu-id="c277c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c277c-115">-AsJob</span></span>
<span data-ttu-id="c277c-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c277c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c277c-117">-Város</span><span class="sxs-lookup"><span data-stu-id="c277c-117">-City</span></span>
<span data-ttu-id="c277c-118">A város neve.</span><span class="sxs-lookup"><span data-stu-id="c277c-118">The name of the city.</span></span>

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

### <span data-ttu-id="c277c-119">-Ország</span><span class="sxs-lookup"><span data-stu-id="c277c-119">-Country</span></span>
<span data-ttu-id="c277c-120">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="c277c-120">The name of the country.</span></span>

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

### <span data-ttu-id="c277c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c277c-121">-DefaultProfile</span></span>
<span data-ttu-id="c277c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c277c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c277c-123">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="c277c-123">-EndTime</span></span>
<span data-ttu-id="c277c-124">Az Azure REACH-jelentés befejezési időpontja.</span><span class="sxs-lookup"><span data-stu-id="c277c-124">The end time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c277c-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="c277c-125">-Location</span></span>
<span data-ttu-id="c277c-126">Választható Azure-régiók: a lekérdezés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="c277c-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c277c-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c277c-127">-NetworkWatcher</span></span>
<span data-ttu-id="c277c-128">A Hálózatfigyelő erőforrás</span><span class="sxs-lookup"><span data-stu-id="c277c-128">The network watcher resource</span></span>

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

### <span data-ttu-id="c277c-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="c277c-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="c277c-130">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="c277c-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c277c-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c277c-131">-NetworkWatcherName</span></span>
<span data-ttu-id="c277c-132">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="c277c-132">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c277c-133">-Szolgáltató</span><span class="sxs-lookup"><span data-stu-id="c277c-133">-Provider</span></span>
<span data-ttu-id="c277c-134">Az internetszolgáltatók listája.</span><span class="sxs-lookup"><span data-stu-id="c277c-134">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c277c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c277c-135">-ResourceGroupName</span></span>
<span data-ttu-id="c277c-136">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c277c-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c277c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c277c-137">-ResourceId</span></span>
<span data-ttu-id="c277c-138">A Hálózatfigyelő-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c277c-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="c277c-139">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="c277c-139">-StartTime</span></span>
<span data-ttu-id="c277c-140">Az Azure REACH-jelentés kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="c277c-140">The start time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c277c-141">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="c277c-141">-State</span></span>
<span data-ttu-id="c277c-142">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="c277c-142">The name of the state.</span></span>

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

### <span data-ttu-id="c277c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c277c-143">CommonParameters</span></span>
<span data-ttu-id="c277c-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c277c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c277c-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c277c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c277c-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c277c-146">INPUTS</span></span>

### <span data-ttu-id="c277c-147">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c277c-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c277c-148">Paraméterek: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c277c-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="c277c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c277c-149">System.String</span></span>

## <span data-ttu-id="c277c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c277c-150">OUTPUTS</span></span>

### <span data-ttu-id="c277c-151">Microsoft. Azure. commands. Network. models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c277c-151">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="c277c-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c277c-152">NOTES</span></span>
<span data-ttu-id="c277c-153">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, elérhetőség, jelentés</span><span class="sxs-lookup"><span data-stu-id="c277c-153">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="c277c-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c277c-154">RELATED LINKS</span></span>

[<span data-ttu-id="c277c-155">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c277c-155">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c277c-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c277c-156">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c277c-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c277c-157">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c277c-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c277c-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c277c-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c277c-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c277c-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c277c-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c277c-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c277c-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c277c-162">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c277c-162">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c277c-163">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c277c-163">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c277c-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c277c-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c277c-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c277c-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c277c-166">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c277c-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c277c-167">Új – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c277c-167">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c277c-168">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c277c-168">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c277c-169">Teszt-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c277c-169">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="c277c-170">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c277c-170">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c277c-171">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c277c-171">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c277c-172">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c277c-172">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c277c-173">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c277c-173">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c277c-174">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c277c-174">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c277c-175">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c277c-175">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c277c-176">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c277c-176">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c277c-177">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c277c-177">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c277c-178">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c277c-178">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c277c-179">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c277c-179">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c277c-180">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c277c-180">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c277c-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c277c-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
