---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 7ec4ebbe9e1224e47605a35f7f21feb2dfbcf045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499783"
---
# <span data-ttu-id="9746d-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9746d-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="9746d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9746d-102">SYNOPSIS</span></span>
<span data-ttu-id="9746d-103">Az internetszolgáltató relatív késési pontszámát adja meg egy adott helyről az Azure-régiók számára.</span><span class="sxs-lookup"><span data-stu-id="9746d-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9746d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9746d-104">SYNTAX</span></span>

### <span data-ttu-id="9746d-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9746d-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9746d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9746d-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9746d-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9746d-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9746d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9746d-108">DESCRIPTION</span></span>
<span data-ttu-id="9746d-109">A Get-AzureRmNetworkWatcherReachabilityReport az Azure-régiók meghatározott helyéről szerzi be az internetszolgáltató relatív késési pontszámát.</span><span class="sxs-lookup"><span data-stu-id="9746d-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="9746d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9746d-110">EXAMPLES</span></span>

### <span data-ttu-id="9746d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9746d-111">Example 1</span></span>
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

<span data-ttu-id="9746d-112">A 2017-10-10-től az 2017-10-12-ig, az Amerikai Egyesült ÁLLAMOKban.</span><span class="sxs-lookup"><span data-stu-id="9746d-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="9746d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9746d-113">PARAMETERS</span></span>

### <span data-ttu-id="9746d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9746d-114">-AsJob</span></span>
<span data-ttu-id="9746d-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9746d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9746d-116">-Város</span><span class="sxs-lookup"><span data-stu-id="9746d-116">-City</span></span>
<span data-ttu-id="9746d-117">A város neve.</span><span class="sxs-lookup"><span data-stu-id="9746d-117">The name of the city.</span></span>

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

### <span data-ttu-id="9746d-118">-Ország</span><span class="sxs-lookup"><span data-stu-id="9746d-118">-Country</span></span>
<span data-ttu-id="9746d-119">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="9746d-119">The name of the country.</span></span>

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

### <span data-ttu-id="9746d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9746d-120">-DefaultProfile</span></span>
<span data-ttu-id="9746d-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9746d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9746d-122">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="9746d-122">-EndTime</span></span>
<span data-ttu-id="9746d-123">Az Azure REACH-jelentés befejezési időpontja.</span><span class="sxs-lookup"><span data-stu-id="9746d-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="9746d-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="9746d-124">-Location</span></span>
<span data-ttu-id="9746d-125">Választható Azure-régiók: a lekérdezés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="9746d-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="9746d-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9746d-126">-NetworkWatcher</span></span>
<span data-ttu-id="9746d-127">A Hálózatfigyelő erőforrás</span><span class="sxs-lookup"><span data-stu-id="9746d-127">The network watcher resource</span></span>

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

### <span data-ttu-id="9746d-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9746d-128">-NetworkWatcherName</span></span>
<span data-ttu-id="9746d-129">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="9746d-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="9746d-130">-Szolgáltató</span><span class="sxs-lookup"><span data-stu-id="9746d-130">-Provider</span></span>
<span data-ttu-id="9746d-131">Az internetszolgáltatók listája.</span><span class="sxs-lookup"><span data-stu-id="9746d-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="9746d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9746d-132">-ResourceGroupName</span></span>
<span data-ttu-id="9746d-133">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9746d-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9746d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9746d-134">-ResourceId</span></span>
<span data-ttu-id="9746d-135">A Hálózatfigyelő-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9746d-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="9746d-136">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="9746d-136">-StartTime</span></span>
<span data-ttu-id="9746d-137">Az Azure REACH-jelentés kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="9746d-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="9746d-138">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="9746d-138">-State</span></span>
<span data-ttu-id="9746d-139">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="9746d-139">The name of the state.</span></span>

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

### <span data-ttu-id="9746d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9746d-140">CommonParameters</span></span>
<span data-ttu-id="9746d-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9746d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9746d-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9746d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9746d-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9746d-143">INPUTS</span></span>

### <span data-ttu-id="9746d-144">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9746d-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9746d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9746d-145">System.String</span></span>

## <span data-ttu-id="9746d-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9746d-146">OUTPUTS</span></span>

### <span data-ttu-id="9746d-147">Microsoft. Azure. commands. Network. models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9746d-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="9746d-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9746d-148">NOTES</span></span>
<span data-ttu-id="9746d-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, elérhetőség, jelentés</span><span class="sxs-lookup"><span data-stu-id="9746d-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="9746d-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9746d-150">RELATED LINKS</span></span>

[<span data-ttu-id="9746d-151">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9746d-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9746d-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9746d-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9746d-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9746d-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9746d-154">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9746d-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="9746d-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9746d-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9746d-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9746d-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="9746d-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9746d-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9746d-158">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9746d-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9746d-159">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9746d-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="9746d-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9746d-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9746d-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9746d-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9746d-162">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9746d-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
