---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 4cb80bec513459797790ae04c3e26a2f25fe95db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499491"
---
# <span data-ttu-id="43feb-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="43feb-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="43feb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43feb-102">SYNOPSIS</span></span>
<span data-ttu-id="43feb-103">Az összes elérhető internetszolgáltató felsorolása egy megadott Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="43feb-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43feb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43feb-104">SYNTAX</span></span>

### <span data-ttu-id="43feb-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43feb-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43feb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="43feb-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43feb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="43feb-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43feb-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="43feb-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43feb-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="43feb-109">DESCRIPTION</span></span>
<span data-ttu-id="43feb-110">A Get-AzureRmNetworkWatcherReachabilityProvidersList felsorolja az összes elérhető internetszolgáltatót egy megadott Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="43feb-110">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="43feb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="43feb-111">EXAMPLES</span></span>

### <span data-ttu-id="43feb-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="43feb-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="43feb-113">Felsorolja az összes elérhető szolgáltatót a Seattle-i, az Azure Data Center in West US-ben.</span><span class="sxs-lookup"><span data-stu-id="43feb-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="43feb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43feb-114">PARAMETERS</span></span>

### <span data-ttu-id="43feb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43feb-115">-AsJob</span></span>
<span data-ttu-id="43feb-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43feb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43feb-117">-Város</span><span class="sxs-lookup"><span data-stu-id="43feb-117">-City</span></span>
<span data-ttu-id="43feb-118">A város neve.</span><span class="sxs-lookup"><span data-stu-id="43feb-118">The name of the city.</span></span>

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

### <span data-ttu-id="43feb-119">-Ország</span><span class="sxs-lookup"><span data-stu-id="43feb-119">-Country</span></span>
<span data-ttu-id="43feb-120">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="43feb-120">The name of the country.</span></span>

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

### <span data-ttu-id="43feb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43feb-121">-DefaultProfile</span></span>
<span data-ttu-id="43feb-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43feb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43feb-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="43feb-123">-Location</span></span>
<span data-ttu-id="43feb-124">Választható Azure-régiók: a lekérdezés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="43feb-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="43feb-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43feb-125">-NetworkWatcher</span></span>
<span data-ttu-id="43feb-126">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="43feb-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="43feb-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="43feb-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="43feb-128">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="43feb-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="43feb-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="43feb-129">-NetworkWatcherName</span></span>
<span data-ttu-id="43feb-130">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="43feb-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="43feb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43feb-131">-ResourceGroupName</span></span>
<span data-ttu-id="43feb-132">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="43feb-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="43feb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43feb-133">-ResourceId</span></span>
<span data-ttu-id="43feb-134">A Hálózatfigyelő-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="43feb-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="43feb-135">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="43feb-135">-State</span></span>
<span data-ttu-id="43feb-136">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="43feb-136">The name of the state.</span></span>

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

### <span data-ttu-id="43feb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43feb-137">CommonParameters</span></span>
<span data-ttu-id="43feb-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43feb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43feb-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43feb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43feb-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43feb-140">INPUTS</span></span>

### <span data-ttu-id="43feb-141">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43feb-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="43feb-142">Paraméterek: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43feb-142">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="43feb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="43feb-143">System.String</span></span>

## <span data-ttu-id="43feb-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43feb-144">OUTPUTS</span></span>

### <span data-ttu-id="43feb-145">Microsoft. Azure. commands. Network. models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="43feb-145">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="43feb-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43feb-146">NOTES</span></span>
<span data-ttu-id="43feb-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, következő, ugrás</span><span class="sxs-lookup"><span data-stu-id="43feb-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="43feb-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43feb-148">RELATED LINKS</span></span>

[<span data-ttu-id="43feb-149">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43feb-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="43feb-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43feb-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="43feb-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43feb-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="43feb-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="43feb-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="43feb-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="43feb-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="43feb-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="43feb-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="43feb-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="43feb-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="43feb-156">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43feb-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="43feb-157">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="43feb-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="43feb-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43feb-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="43feb-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43feb-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="43feb-160">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="43feb-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="43feb-161">Új – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="43feb-161">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="43feb-162">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="43feb-162">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="43feb-163">Teszt-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="43feb-163">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="43feb-164">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43feb-164">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="43feb-165">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43feb-165">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="43feb-166">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43feb-166">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="43feb-167">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="43feb-167">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="43feb-168">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43feb-168">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="43feb-169">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43feb-169">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="43feb-170">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="43feb-170">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="43feb-171">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="43feb-171">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="43feb-172">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="43feb-172">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="43feb-173">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="43feb-173">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="43feb-174">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="43feb-174">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="43feb-175">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="43feb-175">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
