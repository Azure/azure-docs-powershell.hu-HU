---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 028af170e73397178dfe3b81ff216b7fdb0ecfe6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402507"
---
# <span data-ttu-id="00eb6-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="00eb6-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="00eb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="00eb6-103">Egy adott Azure-régió összes elérhető internetszolgáltatóját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="00eb6-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="00eb6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00eb6-104">SYNTAX</span></span>

### <span data-ttu-id="00eb6-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00eb6-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00eb6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="00eb6-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00eb6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="00eb6-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00eb6-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="00eb6-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00eb6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00eb6-109">DESCRIPTION</span></span>
<span data-ttu-id="00eb6-110">A Get-AzNetworkWatcherReachabilityProvidersList egy adott Azure-régió összes elérhető internetszolgáltatóját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="00eb6-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="00eb6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00eb6-111">EXAMPLES</span></span>

### <span data-ttu-id="00eb6-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="00eb6-112">Example 1</span></span>
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

<span data-ttu-id="00eb6-113">Az összes elérhető szolgáltató a nyugat-egyesült államokbeli Azure Data Center szolgáltatáshoz Seattle-ben és Wa-ban.</span><span class="sxs-lookup"><span data-stu-id="00eb6-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="00eb6-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="00eb6-114">Example 2</span></span>

<span data-ttu-id="00eb6-115">Egy adott Azure-régió összes elérhető internetszolgáltatóját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="00eb6-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="00eb6-116">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="00eb6-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="00eb6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00eb6-117">PARAMETERS</span></span>

### <span data-ttu-id="00eb6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00eb6-118">-AsJob</span></span>
<span data-ttu-id="00eb6-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="00eb6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00eb6-120">-City</span><span class="sxs-lookup"><span data-stu-id="00eb6-120">-City</span></span>
<span data-ttu-id="00eb6-121">A város neve.</span><span class="sxs-lookup"><span data-stu-id="00eb6-121">The name of the city.</span></span>

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

### <span data-ttu-id="00eb6-122">-Country</span><span class="sxs-lookup"><span data-stu-id="00eb6-122">-Country</span></span>
<span data-ttu-id="00eb6-123">Az ország neve.</span><span class="sxs-lookup"><span data-stu-id="00eb6-123">The name of the country.</span></span>

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

### <span data-ttu-id="00eb6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00eb6-124">-DefaultProfile</span></span>
<span data-ttu-id="00eb6-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00eb6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00eb6-126">-Location</span><span class="sxs-lookup"><span data-stu-id="00eb6-126">-Location</span></span>
<span data-ttu-id="00eb6-127">Választható Azure-régiók, amelyekre a lekérdezés hatókörét ki kell terjedni.</span><span class="sxs-lookup"><span data-stu-id="00eb6-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="00eb6-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="00eb6-128">-NetworkWatcher</span></span>
<span data-ttu-id="00eb6-129">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="00eb6-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="00eb6-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="00eb6-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="00eb6-131">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="00eb6-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="00eb6-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="00eb6-132">-NetworkWatcherName</span></span>
<span data-ttu-id="00eb6-133">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="00eb6-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="00eb6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00eb6-134">-ResourceGroupName</span></span>
<span data-ttu-id="00eb6-135">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="00eb6-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="00eb6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00eb6-136">-ResourceId</span></span>
<span data-ttu-id="00eb6-137">A hálózati figyelőerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00eb6-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="00eb6-138">-State</span><span class="sxs-lookup"><span data-stu-id="00eb6-138">-State</span></span>
<span data-ttu-id="00eb6-139">Az állam neve.</span><span class="sxs-lookup"><span data-stu-id="00eb6-139">The name of the state.</span></span>

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

### <span data-ttu-id="00eb6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00eb6-140">CommonParameters</span></span>
<span data-ttu-id="00eb6-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00eb6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00eb6-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00eb6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00eb6-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00eb6-143">INPUTS</span></span>

### <span data-ttu-id="00eb6-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="00eb6-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="00eb6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="00eb6-145">System.String</span></span>

## <span data-ttu-id="00eb6-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00eb6-146">OUTPUTS</span></span>

### <span data-ttu-id="00eb6-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="00eb6-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="00eb6-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00eb6-148">NOTES</span></span>
<span data-ttu-id="00eb6-149">Kulcsszavak: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="00eb6-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="00eb6-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00eb6-150">RELATED LINKS</span></span>

[<span data-ttu-id="00eb6-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="00eb6-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="00eb6-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="00eb6-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="00eb6-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="00eb6-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="00eb6-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="00eb6-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="00eb6-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="00eb6-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="00eb6-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="00eb6-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="00eb6-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="00eb6-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="00eb6-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="00eb6-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="00eb6-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="00eb6-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="00eb6-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="00eb6-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="00eb6-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="00eb6-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="00eb6-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="00eb6-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="00eb6-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="00eb6-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="00eb6-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="00eb6-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="00eb6-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="00eb6-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="00eb6-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="00eb6-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="00eb6-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="00eb6-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="00eb6-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="00eb6-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="00eb6-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="00eb6-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="00eb6-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="00eb6-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="00eb6-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="00eb6-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="00eb6-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="00eb6-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="00eb6-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="00eb6-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="00eb6-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="00eb6-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="00eb6-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="00eb6-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="00eb6-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="00eb6-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="00eb6-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="00eb6-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
