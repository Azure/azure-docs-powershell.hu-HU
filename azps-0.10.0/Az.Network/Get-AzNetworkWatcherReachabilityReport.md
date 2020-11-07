---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 6da0a36ee5e394008ea1d1de4a16f7982227ca06
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841561"
---
# <span data-ttu-id="f4fb4-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f4fb4-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="f4fb4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fb4-103">Az internetszolgáltató relatív késési pontszámát adja meg egy adott helyről az Azure-régiók számára.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="f4fb4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4fb4-104">SYNTAX</span></span>

### <span data-ttu-id="f4fb4-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4fb4-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4fb4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f4fb4-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4fb4-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4fb4-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4fb4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4fb4-108">DESCRIPTION</span></span>
<span data-ttu-id="f4fb4-109">A Get-AzNetworkWatcherReachabilityReport az Azure-régiók meghatározott helyéről szerzi be az internetszolgáltató relatív késési pontszámát.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-109">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="f4fb4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f4fb4-110">EXAMPLES</span></span>

### <span data-ttu-id="f4fb4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4fb4-111">Example 1</span></span>
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

<span data-ttu-id="f4fb4-112">A 2017-10-10-től az 2017-10-12-ig, az Amerikai Egyesült ÁLLAMOKban.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="f4fb4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4fb4-113">PARAMETERS</span></span>

### <span data-ttu-id="f4fb4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4fb4-114">-AsJob</span></span>
<span data-ttu-id="f4fb4-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f4fb4-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-116">-Város</span><span class="sxs-lookup"><span data-stu-id="f4fb4-116">-City</span></span>
<span data-ttu-id="f4fb4-117">A város neve.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-118">-Ország</span><span class="sxs-lookup"><span data-stu-id="f4fb4-118">-Country</span></span>
<span data-ttu-id="f4fb4-119">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fb4-120">-DefaultProfile</span></span>
<span data-ttu-id="f4fb4-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-122">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="f4fb4-122">-EndTime</span></span>
<span data-ttu-id="f4fb4-123">Az Azure REACH-jelentés befejezési időpontja.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-123">The end time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="f4fb4-124">-Location</span></span>
<span data-ttu-id="f4fb4-125">Választható Azure-régiók: a lekérdezés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="f4fb4-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f4fb4-126">-NetworkWatcher</span></span>
<span data-ttu-id="f4fb4-127">A Hálózatfigyelő erőforrás</span><span class="sxs-lookup"><span data-stu-id="f4fb4-127">The network watcher resource</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f4fb4-128">-NetworkWatcherName</span></span>
<span data-ttu-id="f4fb4-129">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-130">-Szolgáltató</span><span class="sxs-lookup"><span data-stu-id="f4fb4-130">-Provider</span></span>
<span data-ttu-id="f4fb4-131">Az internetszolgáltatók listája.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="f4fb4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4fb4-132">-ResourceGroupName</span></span>
<span data-ttu-id="f4fb4-133">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-133">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4fb4-134">-ResourceId</span></span>
<span data-ttu-id="f4fb4-135">A Hálózatfigyelő-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-135">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-136">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="f4fb4-136">-StartTime</span></span>
<span data-ttu-id="f4fb4-137">Az Azure REACH-jelentés kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-137">The start time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-138">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="f4fb4-138">-State</span></span>
<span data-ttu-id="f4fb4-139">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="f4fb4-139">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fb4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fb4-140">CommonParameters</span></span>
<span data-ttu-id="f4fb4-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4fb4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fb4-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4fb4-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fb4-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4fb4-143">INPUTS</span></span>

### <span data-ttu-id="f4fb4-144">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f4fb4-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f4fb4-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f4fb4-145">System.String</span></span>

## <span data-ttu-id="f4fb4-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4fb4-146">OUTPUTS</span></span>

### <span data-ttu-id="f4fb4-147">Microsoft. Azure. commands. Network. models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f4fb4-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="f4fb4-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4fb4-148">NOTES</span></span>
<span data-ttu-id="f4fb4-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, elérhetőség, jelentés</span><span class="sxs-lookup"><span data-stu-id="f4fb4-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="f4fb4-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4fb4-150">RELATED LINKS</span></span>

[<span data-ttu-id="f4fb4-151">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f4fb4-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f4fb4-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f4fb4-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f4fb4-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f4fb4-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f4fb4-154">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f4fb4-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f4fb4-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f4fb4-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f4fb4-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f4fb4-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f4fb4-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f4fb4-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f4fb4-158">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f4fb4-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f4fb4-159">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f4fb4-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f4fb4-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f4fb4-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f4fb4-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f4fb4-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f4fb4-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f4fb4-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
