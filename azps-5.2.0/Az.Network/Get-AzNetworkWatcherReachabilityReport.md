---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334613"
---
# <span data-ttu-id="d0bca-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d0bca-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="d0bca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0bca-102">SYNOPSIS</span></span>
<span data-ttu-id="d0bca-103">Az internetszolgáltatók relatív késési pontszámát kapja meg egy adott helyről az Azure-régiókba.</span><span class="sxs-lookup"><span data-stu-id="d0bca-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="d0bca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0bca-104">SYNTAX</span></span>

### <span data-ttu-id="d0bca-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0bca-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0bca-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d0bca-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0bca-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0bca-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0bca-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d0bca-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0bca-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0bca-109">DESCRIPTION</span></span>
<span data-ttu-id="d0bca-110">A Get-AzNetworkWatcherReachabilityReport az internetszolgáltatók relatív késési pontszámát kapja meg egy adott helyről az Azure-régiókba.</span><span class="sxs-lookup"><span data-stu-id="d0bca-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="d0bca-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0bca-111">EXAMPLES</span></span>

### <span data-ttu-id="d0bca-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="d0bca-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="d0bca-113">Relatív késéseket kap az Egyesült Államok nyugati részén található Azure Data Centerhez 2017-10-10 és 2017-10-12 között Az Egyesült Államokon belül.</span><span class="sxs-lookup"><span data-stu-id="d0bca-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="d0bca-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="d0bca-114">Example 2</span></span>

<span data-ttu-id="d0bca-115">Az internetszolgáltatók relatív késési pontszámát kapja meg egy adott helyről az Azure-régiókba.</span><span class="sxs-lookup"><span data-stu-id="d0bca-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="d0bca-116">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="d0bca-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="d0bca-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0bca-117">PARAMETERS</span></span>

### <span data-ttu-id="d0bca-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0bca-118">-AsJob</span></span>
<span data-ttu-id="d0bca-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d0bca-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0bca-120">-City</span><span class="sxs-lookup"><span data-stu-id="d0bca-120">-City</span></span>
<span data-ttu-id="d0bca-121">A város neve.</span><span class="sxs-lookup"><span data-stu-id="d0bca-121">The name of the city.</span></span>

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

### <span data-ttu-id="d0bca-122">-Country</span><span class="sxs-lookup"><span data-stu-id="d0bca-122">-Country</span></span>
<span data-ttu-id="d0bca-123">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="d0bca-123">The name of the country.</span></span>

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

### <span data-ttu-id="d0bca-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0bca-124">-DefaultProfile</span></span>
<span data-ttu-id="d0bca-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0bca-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0bca-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d0bca-126">-EndTime</span></span>
<span data-ttu-id="d0bca-127">Az Azure-beli elérhetőség-jelentés záró ideje.</span><span class="sxs-lookup"><span data-stu-id="d0bca-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="d0bca-128">-Location</span><span class="sxs-lookup"><span data-stu-id="d0bca-128">-Location</span></span>
<span data-ttu-id="d0bca-129">Választható Azure-régiók, amelyekre a lekérdezés hatókörét ki kell terjedni.</span><span class="sxs-lookup"><span data-stu-id="d0bca-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="d0bca-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0bca-130">-NetworkWatcher</span></span>
<span data-ttu-id="d0bca-131">A hálózati figyelő erőforrás</span><span class="sxs-lookup"><span data-stu-id="d0bca-131">The network watcher resource</span></span>

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

### <span data-ttu-id="d0bca-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="d0bca-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="d0bca-133">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="d0bca-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d0bca-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d0bca-134">-NetworkWatcherName</span></span>
<span data-ttu-id="d0bca-135">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="d0bca-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="d0bca-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="d0bca-136">-Provider</span></span>
<span data-ttu-id="d0bca-137">Az internetszolgáltatók listája.</span><span class="sxs-lookup"><span data-stu-id="d0bca-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="d0bca-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0bca-138">-ResourceGroupName</span></span>
<span data-ttu-id="d0bca-139">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d0bca-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d0bca-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0bca-140">-ResourceId</span></span>
<span data-ttu-id="d0bca-141">A hálózati figyelőerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d0bca-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="d0bca-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d0bca-142">-StartTime</span></span>
<span data-ttu-id="d0bca-143">Az Azure-beli elérhetőség-jelentés kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="d0bca-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="d0bca-144">-State</span><span class="sxs-lookup"><span data-stu-id="d0bca-144">-State</span></span>
<span data-ttu-id="d0bca-145">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="d0bca-145">The name of the state.</span></span>

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

### <span data-ttu-id="d0bca-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0bca-146">CommonParameters</span></span>
<span data-ttu-id="d0bca-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0bca-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0bca-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0bca-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0bca-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0bca-149">INPUTS</span></span>

### <span data-ttu-id="d0bca-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0bca-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d0bca-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d0bca-151">System.String</span></span>

## <span data-ttu-id="d0bca-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0bca-152">OUTPUTS</span></span>

### <span data-ttu-id="d0bca-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d0bca-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="d0bca-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0bca-154">NOTES</span></span>
<span data-ttu-id="d0bca-155">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span><span class="sxs-lookup"><span data-stu-id="d0bca-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="d0bca-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0bca-156">RELATED LINKS</span></span>

[<span data-ttu-id="d0bca-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0bca-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d0bca-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0bca-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d0bca-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0bca-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d0bca-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d0bca-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d0bca-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d0bca-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d0bca-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d0bca-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d0bca-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d0bca-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d0bca-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0bca-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0bca-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d0bca-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d0bca-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0bca-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0bca-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0bca-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0bca-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0bca-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0bca-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0bca-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d0bca-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d0bca-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d0bca-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d0bca-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d0bca-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0bca-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d0bca-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0bca-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d0bca-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0bca-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d0bca-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d0bca-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d0bca-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0bca-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d0bca-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0bca-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d0bca-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d0bca-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d0bca-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d0bca-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d0bca-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d0bca-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d0bca-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d0bca-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d0bca-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d0bca-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d0bca-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0bca-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
