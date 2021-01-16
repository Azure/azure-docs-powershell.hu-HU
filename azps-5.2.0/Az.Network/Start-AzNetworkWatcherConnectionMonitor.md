---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 83d7da65ad8c525d4c37ab1b5f78eb72bf1d9f49
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352349"
---
# <span data-ttu-id="2fc37-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fc37-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="2fc37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fc37-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc37-103">Kapcsolatfigyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fc37-103">Start a connection monitor</span></span>

## <span data-ttu-id="2fc37-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2fc37-104">SYNTAX</span></span>

### <span data-ttu-id="2fc37-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2fc37-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc37-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2fc37-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc37-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2fc37-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc37-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc37-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc37-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2fc37-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc37-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2fc37-110">DESCRIPTION</span></span>
<span data-ttu-id="2fc37-111">A Start-AzNetworkWatcherConnectionMonitor parancsmag elindítja a megadott kapcsolatfigyelőt.</span><span class="sxs-lookup"><span data-stu-id="2fc37-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="2fc37-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2fc37-112">EXAMPLES</span></span>

### <span data-ttu-id="2fc37-113">1. példa: Kapcsolatfigyelő létrehozása</span><span class="sxs-lookup"><span data-stu-id="2fc37-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="2fc37-114">Ebben a példában elindítjuk a név és a hálózati figyelő által megadott kapcsolatfigyelőt</span><span class="sxs-lookup"><span data-stu-id="2fc37-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="2fc37-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fc37-115">PARAMETERS</span></span>

### <span data-ttu-id="2fc37-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fc37-116">-AsJob</span></span>
<span data-ttu-id="2fc37-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2fc37-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc37-118">-DefaultProfile</span></span>
<span data-ttu-id="2fc37-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2fc37-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fc37-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fc37-120">-InputObject</span></span>
<span data-ttu-id="2fc37-121">Kapcsolatfigyelő objektum.</span><span class="sxs-lookup"><span data-stu-id="2fc37-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc37-122">-Location</span><span class="sxs-lookup"><span data-stu-id="2fc37-122">-Location</span></span>
<span data-ttu-id="2fc37-123">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="2fc37-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2fc37-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2fc37-124">-Name</span></span>
<span data-ttu-id="2fc37-125">A kapcsolatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="2fc37-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc37-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fc37-126">-NetworkWatcher</span></span>
<span data-ttu-id="2fc37-127">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="2fc37-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="2fc37-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2fc37-128">-NetworkWatcherName</span></span>
<span data-ttu-id="2fc37-129">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="2fc37-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="2fc37-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fc37-130">-PassThru</span></span>
<span data-ttu-id="2fc37-131">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="2fc37-131">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc37-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc37-132">-ResourceGroupName</span></span>
<span data-ttu-id="2fc37-133">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2fc37-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2fc37-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc37-134">-ResourceId</span></span>
<span data-ttu-id="2fc37-135">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2fc37-135">Resource ID.</span></span>

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

### <span data-ttu-id="2fc37-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fc37-136">-Confirm</span></span>
<span data-ttu-id="2fc37-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2fc37-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc37-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc37-138">-WhatIf</span></span>
<span data-ttu-id="2fc37-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2fc37-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fc37-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2fc37-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc37-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc37-141">CommonParameters</span></span>
<span data-ttu-id="2fc37-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc37-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc37-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc37-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc37-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2fc37-144">INPUTS</span></span>

### <span data-ttu-id="2fc37-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fc37-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2fc37-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2fc37-146">System.String</span></span>

### <span data-ttu-id="2fc37-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="2fc37-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="2fc37-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fc37-148">OUTPUTS</span></span>

### <span data-ttu-id="2fc37-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2fc37-149">System.Boolean</span></span>

## <span data-ttu-id="2fc37-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2fc37-150">NOTES</span></span>
<span data-ttu-id="2fc37-151">Kulcsszavak: azure, azurerm, arm, erőforrás, kapcsolat, kezelés, vezető, hálózat, hálózatkezelés, hálózati figyelő, kapcsolatfigyelő</span><span class="sxs-lookup"><span data-stu-id="2fc37-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="2fc37-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fc37-152">RELATED LINKS</span></span>

[<span data-ttu-id="2fc37-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fc37-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2fc37-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fc37-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2fc37-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fc37-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2fc37-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2fc37-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2fc37-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2fc37-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2fc37-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2fc37-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2fc37-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2fc37-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2fc37-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fc37-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fc37-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2fc37-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2fc37-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fc37-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fc37-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fc37-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fc37-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fc37-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fc37-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fc37-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fc37-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2fc37-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2fc37-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fc37-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fc37-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fc37-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fc37-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fc37-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fc37-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fc37-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fc37-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fc37-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2fc37-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2fc37-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2fc37-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2fc37-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2fc37-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2fc37-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2fc37-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fc37-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fc37-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2fc37-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2fc37-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2fc37-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2fc37-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2fc37-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2fc37-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2fc37-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
