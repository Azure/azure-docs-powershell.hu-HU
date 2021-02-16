---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: dcdd4ef2fd6ca3481d9bb3f8333174307be7e3f6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404079"
---
# <span data-ttu-id="f2cfa-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f2cfa-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="f2cfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cfa-103">Az internetszolgáltatók relatív késési pontszámát kapja meg egy adott helyről az Azure-régiókba.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="f2cfa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2cfa-104">SYNTAX</span></span>

### <span data-ttu-id="f2cfa-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2cfa-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2cfa-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f2cfa-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2cfa-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2cfa-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2cfa-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f2cfa-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2cfa-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2cfa-109">DESCRIPTION</span></span>
<span data-ttu-id="f2cfa-110">A Get-AzNetworkWatcherReachabilityReport az internetszolgáltatók relatív késési pontszámát kapja meg egy adott helyről az Azure-régiókba.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="f2cfa-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2cfa-111">EXAMPLES</span></span>

### <span data-ttu-id="f2cfa-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="f2cfa-112">Example 1</span></span>
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

<span data-ttu-id="f2cfa-113">Relatív késéseket kap az Egyesült Államok nyugati részén található Azure Data Centerhez 2017-10-10 és 2017-10-12 között Az Egyesült Államokon belül.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="f2cfa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2cfa-114">PARAMETERS</span></span>

### <span data-ttu-id="f2cfa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2cfa-115">-AsJob</span></span>
<span data-ttu-id="f2cfa-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f2cfa-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2cfa-117">-City</span><span class="sxs-lookup"><span data-stu-id="f2cfa-117">-City</span></span>
<span data-ttu-id="f2cfa-118">A város neve.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-118">The name of the city.</span></span>

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

### <span data-ttu-id="f2cfa-119">-Country</span><span class="sxs-lookup"><span data-stu-id="f2cfa-119">-Country</span></span>
<span data-ttu-id="f2cfa-120">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-120">The name of the country.</span></span>

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

### <span data-ttu-id="f2cfa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2cfa-121">-DefaultProfile</span></span>
<span data-ttu-id="f2cfa-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2cfa-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f2cfa-123">-EndTime</span></span>
<span data-ttu-id="f2cfa-124">Az Azure-beli elérhetőség-jelentés záró ideje.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="f2cfa-125">-Location</span><span class="sxs-lookup"><span data-stu-id="f2cfa-125">-Location</span></span>
<span data-ttu-id="f2cfa-126">Választható Azure-régiók, amelyekre a lekérdezés hatókörét ki kell terjedni.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-126">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="f2cfa-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2cfa-127">-NetworkWatcher</span></span>
<span data-ttu-id="f2cfa-128">A hálózati figyelő erőforrás</span><span class="sxs-lookup"><span data-stu-id="f2cfa-128">The network watcher resource</span></span>

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

### <span data-ttu-id="f2cfa-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="f2cfa-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="f2cfa-130">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f2cfa-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f2cfa-131">-NetworkWatcherName</span></span>
<span data-ttu-id="f2cfa-132">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="f2cfa-133">-Provider</span><span class="sxs-lookup"><span data-stu-id="f2cfa-133">-Provider</span></span>
<span data-ttu-id="f2cfa-134">Az internetszolgáltatók listája.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-134">List of Internet service providers.</span></span>

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

### <span data-ttu-id="f2cfa-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2cfa-135">-ResourceGroupName</span></span>
<span data-ttu-id="f2cfa-136">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f2cfa-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2cfa-137">-ResourceId</span></span>
<span data-ttu-id="f2cfa-138">A hálózati figyelőerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="f2cfa-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f2cfa-139">-StartTime</span></span>
<span data-ttu-id="f2cfa-140">Az Azure-beli elérhetőség-jelentés kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="f2cfa-141">-State</span><span class="sxs-lookup"><span data-stu-id="f2cfa-141">-State</span></span>
<span data-ttu-id="f2cfa-142">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-142">The name of the state.</span></span>

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

### <span data-ttu-id="f2cfa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cfa-143">CommonParameters</span></span>
<span data-ttu-id="f2cfa-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2cfa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cfa-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2cfa-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cfa-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2cfa-146">INPUTS</span></span>

### <span data-ttu-id="f2cfa-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2cfa-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f2cfa-148">System.String</span><span class="sxs-lookup"><span data-stu-id="f2cfa-148">System.String</span></span>

## <span data-ttu-id="f2cfa-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2cfa-149">OUTPUTS</span></span>

### <span data-ttu-id="f2cfa-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f2cfa-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="f2cfa-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2cfa-151">NOTES</span></span>
<span data-ttu-id="f2cfa-152">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, elérhetőség, jelentés</span><span class="sxs-lookup"><span data-stu-id="f2cfa-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="f2cfa-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2cfa-153">RELATED LINKS</span></span>

[<span data-ttu-id="f2cfa-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2cfa-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f2cfa-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2cfa-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f2cfa-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f2cfa-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f2cfa-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f2cfa-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f2cfa-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f2cfa-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f2cfa-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f2cfa-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f2cfa-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f2cfa-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f2cfa-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2cfa-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2cfa-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f2cfa-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f2cfa-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2cfa-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2cfa-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2cfa-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2cfa-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2cfa-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f2cfa-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2cfa-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f2cfa-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f2cfa-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f2cfa-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f2cfa-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f2cfa-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2cfa-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f2cfa-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2cfa-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f2cfa-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2cfa-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f2cfa-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f2cfa-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f2cfa-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2cfa-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f2cfa-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2cfa-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f2cfa-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f2cfa-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f2cfa-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f2cfa-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f2cfa-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f2cfa-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f2cfa-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f2cfa-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f2cfa-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f2cfa-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f2cfa-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f2cfa-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
