---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a2c66f9e93a26c433c245f87c8506b71ad01c5e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845910"
---
# <span data-ttu-id="24f48-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="24f48-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="24f48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24f48-102">SYNOPSIS</span></span>
<span data-ttu-id="24f48-103">Az összes elérhető internetszolgáltató felsorolása egy megadott Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="24f48-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="24f48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24f48-104">SYNTAX</span></span>

### <span data-ttu-id="24f48-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24f48-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24f48-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="24f48-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24f48-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="24f48-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24f48-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="24f48-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24f48-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="24f48-109">DESCRIPTION</span></span>
<span data-ttu-id="24f48-110">A Get-AzNetworkWatcherReachabilityProvidersList felsorolja az összes elérhető internetszolgáltatót egy megadott Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="24f48-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="24f48-111">Példák</span><span class="sxs-lookup"><span data-stu-id="24f48-111">EXAMPLES</span></span>

### <span data-ttu-id="24f48-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24f48-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="24f48-113">Felsorolja az összes elérhető szolgáltatót a Seattle-i, az Azure Data Center in West US-ben.</span><span class="sxs-lookup"><span data-stu-id="24f48-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="24f48-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24f48-114">PARAMETERS</span></span>

### <span data-ttu-id="24f48-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24f48-115">-AsJob</span></span>
<span data-ttu-id="24f48-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="24f48-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24f48-117">-Város</span><span class="sxs-lookup"><span data-stu-id="24f48-117">-City</span></span>
<span data-ttu-id="24f48-118">A város neve.</span><span class="sxs-lookup"><span data-stu-id="24f48-118">The name of the city.</span></span>

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

### <span data-ttu-id="24f48-119">-Ország</span><span class="sxs-lookup"><span data-stu-id="24f48-119">-Country</span></span>
<span data-ttu-id="24f48-120">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="24f48-120">The name of the country.</span></span>

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

### <span data-ttu-id="24f48-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f48-121">-DefaultProfile</span></span>
<span data-ttu-id="24f48-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24f48-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24f48-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="24f48-123">-Location</span></span>
<span data-ttu-id="24f48-124">Választható Azure-régiók: a lekérdezés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="24f48-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="24f48-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="24f48-125">-NetworkWatcher</span></span>
<span data-ttu-id="24f48-126">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="24f48-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="24f48-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="24f48-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="24f48-128">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="24f48-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="24f48-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="24f48-129">-NetworkWatcherName</span></span>
<span data-ttu-id="24f48-130">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="24f48-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="24f48-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f48-131">-ResourceGroupName</span></span>
<span data-ttu-id="24f48-132">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="24f48-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="24f48-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24f48-133">-ResourceId</span></span>
<span data-ttu-id="24f48-134">A Hálózatfigyelő-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="24f48-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="24f48-135">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="24f48-135">-State</span></span>
<span data-ttu-id="24f48-136">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="24f48-136">The name of the state.</span></span>

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

### <span data-ttu-id="24f48-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f48-137">CommonParameters</span></span>
<span data-ttu-id="24f48-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24f48-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f48-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="24f48-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f48-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24f48-140">INPUTS</span></span>

### <span data-ttu-id="24f48-141">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="24f48-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="24f48-142">System. String</span><span class="sxs-lookup"><span data-stu-id="24f48-142">System.String</span></span>

## <span data-ttu-id="24f48-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24f48-143">OUTPUTS</span></span>

### <span data-ttu-id="24f48-144">Microsoft. Azure. commands. Network. models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="24f48-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="24f48-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24f48-145">NOTES</span></span>
<span data-ttu-id="24f48-146">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, következő, ugrás</span><span class="sxs-lookup"><span data-stu-id="24f48-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="24f48-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24f48-147">RELATED LINKS</span></span>

[<span data-ttu-id="24f48-148">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="24f48-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="24f48-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="24f48-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="24f48-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="24f48-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="24f48-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="24f48-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="24f48-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="24f48-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="24f48-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="24f48-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="24f48-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="24f48-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="24f48-155">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24f48-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24f48-156">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="24f48-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="24f48-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24f48-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24f48-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24f48-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24f48-159">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24f48-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24f48-160">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="24f48-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="24f48-161">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="24f48-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="24f48-162">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="24f48-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="24f48-163">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="24f48-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="24f48-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="24f48-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="24f48-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="24f48-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="24f48-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="24f48-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="24f48-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="24f48-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="24f48-168">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="24f48-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="24f48-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="24f48-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="24f48-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="24f48-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="24f48-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="24f48-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="24f48-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="24f48-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="24f48-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="24f48-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="24f48-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="24f48-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
