---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151418"
---
# <span data-ttu-id="f9e33-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f9e33-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="f9e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9e33-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e33-103">Frissíti a kapcsolatfigyelő erőforrást.</span><span class="sxs-lookup"><span data-stu-id="f9e33-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="f9e33-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9e33-104">SYNTAX</span></span>

### <span data-ttu-id="f9e33-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9e33-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9e33-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f9e33-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9e33-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="f9e33-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9e33-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="f9e33-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9e33-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f9e33-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9e33-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="f9e33-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9e33-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e33-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9e33-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="f9e33-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9e33-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="f9e33-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9e33-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9e33-114">DESCRIPTION</span></span>
<span data-ttu-id="f9e33-115">A Set-AzNetworkWatcherConnectionMonitor parancsmag frissíti a kapcsolatfigyelő erőforrást.</span><span class="sxs-lookup"><span data-stu-id="f9e33-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="f9e33-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9e33-116">EXAMPLES</span></span>

### <span data-ttu-id="f9e33-117">1. példa: Kapcsolatfigyelő frissítése</span><span class="sxs-lookup"><span data-stu-id="f9e33-117">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="f9e33-118">Ebben a példában frissítjük a meglévő kapcsolatfigyelőt a célCím módosításával és címkék hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="f9e33-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="f9e33-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9e33-119">PARAMETERS</span></span>

### <span data-ttu-id="f9e33-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9e33-120">-AsJob</span></span>
<span data-ttu-id="f9e33-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f9e33-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9e33-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="f9e33-122">-ConfigureOnly</span></span>
<span data-ttu-id="f9e33-123">A kapcsolatfigyelő beállítása, de nem indul el</span><span class="sxs-lookup"><span data-stu-id="f9e33-123">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e33-124">-DefaultProfile</span></span>
<span data-ttu-id="f9e33-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9e33-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9e33-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f9e33-126">-DestinationAddress</span></span>
<span data-ttu-id="f9e33-127">A kapcsolatfigyelő célhelyének címe (IP vagy tartománynév).</span><span class="sxs-lookup"><span data-stu-id="f9e33-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f9e33-128">-DestinationPort</span></span>
<span data-ttu-id="f9e33-129">A kapcsolatfigyelő által használt célport.</span><span class="sxs-lookup"><span data-stu-id="f9e33-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e33-130">-DestinationResourceId</span></span>
<span data-ttu-id="f9e33-131">A kapcsolatfigyelő által célként használt erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f9e33-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f9e33-132">-Force</span></span>
<span data-ttu-id="f9e33-133">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="f9e33-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f9e33-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9e33-134">-InputObject</span></span>
<span data-ttu-id="f9e33-135">Kapcsolatfigyelő objektum.</span><span class="sxs-lookup"><span data-stu-id="f9e33-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="f9e33-136">-Location</span><span class="sxs-lookup"><span data-stu-id="f9e33-136">-Location</span></span>
<span data-ttu-id="f9e33-137">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="f9e33-137">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f9e33-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="f9e33-139">Figyelési időköz másodpercben.</span><span class="sxs-lookup"><span data-stu-id="f9e33-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="f9e33-140">Az alapértelmezett érték 60 másodperc.</span><span class="sxs-lookup"><span data-stu-id="f9e33-140">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-141">-Name</span><span class="sxs-lookup"><span data-stu-id="f9e33-141">-Name</span></span>
<span data-ttu-id="f9e33-142">A kapcsolatfigyelő neve.</span><span class="sxs-lookup"><span data-stu-id="f9e33-142">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f9e33-143">-NetworkWatcher</span></span>
<span data-ttu-id="f9e33-144">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="f9e33-144">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f9e33-145">-NetworkWatcherName</span></span>
<span data-ttu-id="f9e33-146">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="f9e33-146">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-147">-Note</span><span class="sxs-lookup"><span data-stu-id="f9e33-147">-Note</span></span>
<span data-ttu-id="f9e33-148">A kapcsolatfigyelővel társított jegyzetek.</span><span class="sxs-lookup"><span data-stu-id="f9e33-148">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-149">-Kimenet</span><span class="sxs-lookup"><span data-stu-id="f9e33-149">-Output</span></span>
<span data-ttu-id="f9e33-150">A kapcsolatfigyelő kimeneti célhelyét ismerteti.</span><span class="sxs-lookup"><span data-stu-id="f9e33-150">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e33-151">-ResourceGroupName</span></span>
<span data-ttu-id="f9e33-152">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f9e33-152">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e33-153">-ResourceId</span></span>
<span data-ttu-id="f9e33-154">ConnectionMonitor erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="f9e33-154">ConnectionMonitor resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="f9e33-155">-SourcePort</span></span>
<span data-ttu-id="f9e33-156">A kapcsolatfigyelő által használt forrásport.</span><span class="sxs-lookup"><span data-stu-id="f9e33-156">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="f9e33-157">-SourceResourceId</span></span>
<span data-ttu-id="f9e33-158">A kapcsolatfigyelő által forrásként használt erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f9e33-158">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9e33-159">-Tag</span></span>
<span data-ttu-id="f9e33-160">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="f9e33-160">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="f9e33-161">-TestGroup</span></span>
<span data-ttu-id="f9e33-162">A tesztcsoportok listája.</span><span class="sxs-lookup"><span data-stu-id="f9e33-162">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9e33-163">-Confirm</span></span>
<span data-ttu-id="f9e33-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f9e33-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9e33-165">-WhatIf</span></span>
<span data-ttu-id="f9e33-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f9e33-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9e33-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9e33-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e33-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e33-168">CommonParameters</span></span>
<span data-ttu-id="f9e33-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9e33-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e33-170">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9e33-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e33-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9e33-171">INPUTS</span></span>

### <span data-ttu-id="f9e33-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f9e33-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f9e33-173">System.String</span><span class="sxs-lookup"><span data-stu-id="f9e33-173">System.String</span></span>

### <span data-ttu-id="f9e33-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="f9e33-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="f9e33-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9e33-175">OUTPUTS</span></span>

### <span data-ttu-id="f9e33-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="f9e33-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="f9e33-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="f9e33-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="f9e33-178">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9e33-178">NOTES</span></span>

## <span data-ttu-id="f9e33-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9e33-179">RELATED LINKS</span></span>
