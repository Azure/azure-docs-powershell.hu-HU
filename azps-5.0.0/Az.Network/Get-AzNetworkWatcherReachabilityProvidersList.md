---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a4e9c9a928d3a6c3ddeb7afa754cc957089a2283
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186413"
---
# <span data-ttu-id="c9020-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c9020-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="c9020-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9020-102">SYNOPSIS</span></span>
<span data-ttu-id="c9020-103">Az összes elérhető internetszolgáltató felsorolása egy megadott Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="c9020-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="c9020-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9020-104">SYNTAX</span></span>

### <span data-ttu-id="c9020-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9020-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9020-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c9020-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9020-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c9020-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9020-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c9020-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9020-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9020-109">DESCRIPTION</span></span>
<span data-ttu-id="c9020-110">A Get-AzNetworkWatcherReachabilityProvidersList felsorolja az összes elérhető internetszolgáltatót egy megadott Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="c9020-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="c9020-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c9020-111">EXAMPLES</span></span>

### <span data-ttu-id="c9020-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c9020-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="c9020-113">Felsorolja az összes elérhető szolgáltatót a Seattle-i, az Azure Data Center in West US-ben.</span><span class="sxs-lookup"><span data-stu-id="c9020-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="c9020-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c9020-114">Example 2</span></span>

<span data-ttu-id="c9020-115">Az összes elérhető internetszolgáltató felsorolása egy megadott Azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="c9020-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="c9020-116">autogenerated</span><span class="sxs-lookup"><span data-stu-id="c9020-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="c9020-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9020-117">PARAMETERS</span></span>

### <span data-ttu-id="c9020-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9020-118">-AsJob</span></span>
<span data-ttu-id="c9020-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c9020-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9020-120">-Város</span><span class="sxs-lookup"><span data-stu-id="c9020-120">-City</span></span>
<span data-ttu-id="c9020-121">A város neve.</span><span class="sxs-lookup"><span data-stu-id="c9020-121">The name of the city.</span></span>

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

### <span data-ttu-id="c9020-122">-Ország</span><span class="sxs-lookup"><span data-stu-id="c9020-122">-Country</span></span>
<span data-ttu-id="c9020-123">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="c9020-123">The name of the country.</span></span>

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

### <span data-ttu-id="c9020-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9020-124">-DefaultProfile</span></span>
<span data-ttu-id="c9020-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9020-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9020-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="c9020-126">-Location</span></span>
<span data-ttu-id="c9020-127">Választható Azure-régiók: a lekérdezés hatóköre.</span><span class="sxs-lookup"><span data-stu-id="c9020-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="c9020-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c9020-128">-NetworkWatcher</span></span>
<span data-ttu-id="c9020-129">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="c9020-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="c9020-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="c9020-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="c9020-131">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="c9020-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c9020-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c9020-132">-NetworkWatcherName</span></span>
<span data-ttu-id="c9020-133">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="c9020-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="c9020-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9020-134">-ResourceGroupName</span></span>
<span data-ttu-id="c9020-135">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9020-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c9020-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9020-136">-ResourceId</span></span>
<span data-ttu-id="c9020-137">A Hálózatfigyelő-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c9020-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="c9020-138">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="c9020-138">-State</span></span>
<span data-ttu-id="c9020-139">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="c9020-139">The name of the state.</span></span>

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

### <span data-ttu-id="c9020-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9020-140">CommonParameters</span></span>
<span data-ttu-id="c9020-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9020-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9020-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c9020-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9020-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9020-143">INPUTS</span></span>

### <span data-ttu-id="c9020-144">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c9020-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c9020-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c9020-145">System.String</span></span>

## <span data-ttu-id="c9020-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9020-146">OUTPUTS</span></span>

### <span data-ttu-id="c9020-147">Microsoft. Azure. commands. Network. models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="c9020-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="c9020-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9020-148">NOTES</span></span>
<span data-ttu-id="c9020-149">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, Hálózatfigyelő, következő, ugrás</span><span class="sxs-lookup"><span data-stu-id="c9020-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="c9020-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9020-150">RELATED LINKS</span></span>

[<span data-ttu-id="c9020-151">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c9020-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c9020-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c9020-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c9020-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c9020-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c9020-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c9020-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c9020-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c9020-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c9020-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c9020-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c9020-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c9020-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c9020-158">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c9020-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c9020-159">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c9020-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c9020-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c9020-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c9020-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c9020-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c9020-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c9020-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c9020-163">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9020-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c9020-164">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c9020-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c9020-165">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c9020-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c9020-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c9020-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c9020-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c9020-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c9020-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c9020-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c9020-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c9020-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c9020-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c9020-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c9020-171">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c9020-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c9020-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c9020-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c9020-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c9020-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c9020-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c9020-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c9020-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c9020-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c9020-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c9020-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c9020-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c9020-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
