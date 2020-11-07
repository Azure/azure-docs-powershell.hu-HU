---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 71227c2e351e12381a857dcf9cd66767f00265cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670518"
---
# <span data-ttu-id="c1d75-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c1d75-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="c1d75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1d75-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d75-103">Az internetszolgáltató relatív késési pontszámát adja meg egy adott helyről az Azure-régiók számára.</span><span class="sxs-lookup"><span data-stu-id="c1d75-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="c1d75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1d75-104">SYNTAX</span></span>

### <span data-ttu-id="c1d75-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1d75-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1d75-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c1d75-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1d75-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d75-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1d75-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c1d75-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1d75-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1d75-109">DESCRIPTION</span></span>
<span data-ttu-id="c1d75-110">A Get-AzNetworkWatcherReachabilityReport az Azure-régiók meghatározott helyéről szerzi be az internetszolgáltató relatív késési pontszámát.</span><span class="sxs-lookup"><span data-stu-id="c1d75-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="c1d75-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c1d75-111">EXAMPLES</span></span>

### <span data-ttu-id="c1d75-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c1d75-112">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="c1d75-113">A 2017-10-10-től az 2017-10-12-ig, az Amerikai Egyesült ÁLLAMOKban.</span><span class="sxs-lookup"><span data-stu-id="c1d75-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="c1d75-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1d75-114">PARAMETERS</span></span>

### <span data-ttu-id="c1d75-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1d75-115">-AsJob</span></span>
<span data-ttu-id="c1d75-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c1d75-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1d75-117">-Város</span><span class="sxs-lookup"><span data-stu-id="c1d75-117">-City</span></span>
<span data-ttu-id="c1d75-118">A város neve.</span><span class="sxs-lookup"><span data-stu-id="c1d75-118">The name of the city.</span></span>

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

### <span data-ttu-id="c1d75-119">-Ország</span><span class="sxs-lookup"><span data-stu-id="c1d75-119">-Country</span></span>
<span data-ttu-id="c1d75-120">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="c1d75-120">The name of the country.</span></span>

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

### <span data-ttu-id="c1d75-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d75-121">-DefaultProfile</span></span>
<span data-ttu-id="c1d75-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1d75-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1d75-123">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="c1d75-123">-EndTime</span></span>
<span data-ttu-id="c1d75-124">Az Azure REACH-jelentés befejezési időpontja.</span><span class="sxs-lookup"><span data-stu-id="c1d75-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="c1d75-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="c1d75-125">-Location</span></span>
<span data-ttu-id="c1d75-126">Választható Azure-régiók: a lekérdezés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="c1d75-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1d75-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c1d75-127">-NetworkWatcher</span></span>
<span data-ttu-id="c1d75-128">A Hálózatfigyelő erőforrás</span><span class="sxs-lookup"><span data-stu-id="c1d75-128">The network watcher resource</span></span>

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

### <span data-ttu-id="c1d75-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="c1d75-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="c1d75-130">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="c1d75-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c1d75-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c1d75-131">-NetworkWatcherName</span></span>
<span data-ttu-id="c1d75-132">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="c1d75-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="c1d75-133">-Szolgáltató</span><span class="sxs-lookup"><span data-stu-id="c1d75-133">-Provider</span></span>
<span data-ttu-id="c1d75-134">Az internetszolgáltatók listája.</span><span class="sxs-lookup"><span data-stu-id="c1d75-134">List of Internet service providers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1d75-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1d75-135">-ResourceGroupName</span></span>
<span data-ttu-id="c1d75-136">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c1d75-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c1d75-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1d75-137">-ResourceId</span></span>
<span data-ttu-id="c1d75-138">A Hálózatfigyelő-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c1d75-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="c1d75-139">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="c1d75-139">-StartTime</span></span>
<span data-ttu-id="c1d75-140">Az Azure REACH-jelentés kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="c1d75-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="c1d75-141">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="c1d75-141">-State</span></span>
<span data-ttu-id="c1d75-142">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="c1d75-142">The name of the state.</span></span>

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

### <span data-ttu-id="c1d75-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d75-143">CommonParameters</span></span>
<span data-ttu-id="c1d75-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1d75-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d75-145">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c1d75-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d75-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1d75-146">INPUTS</span></span>

### <span data-ttu-id="c1d75-147">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c1d75-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c1d75-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c1d75-148">System.String</span></span>

## <span data-ttu-id="c1d75-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1d75-149">OUTPUTS</span></span>

### <span data-ttu-id="c1d75-150">Microsoft. Azure. commands. Network. models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c1d75-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="c1d75-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1d75-151">NOTES</span></span>
<span data-ttu-id="c1d75-152">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, elérhetőség, jelentés</span><span class="sxs-lookup"><span data-stu-id="c1d75-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="c1d75-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1d75-153">RELATED LINKS</span></span>

[<span data-ttu-id="c1d75-154">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c1d75-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c1d75-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c1d75-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c1d75-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c1d75-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c1d75-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c1d75-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c1d75-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c1d75-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c1d75-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c1d75-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c1d75-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c1d75-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c1d75-161">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c1d75-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c1d75-162">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c1d75-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c1d75-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c1d75-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c1d75-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c1d75-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c1d75-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c1d75-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c1d75-166">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1d75-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c1d75-167">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c1d75-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c1d75-168">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c1d75-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c1d75-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1d75-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c1d75-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1d75-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c1d75-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1d75-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c1d75-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c1d75-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c1d75-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1d75-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c1d75-174">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1d75-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c1d75-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c1d75-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c1d75-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c1d75-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c1d75-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c1d75-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c1d75-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c1d75-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c1d75-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c1d75-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c1d75-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c1d75-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)