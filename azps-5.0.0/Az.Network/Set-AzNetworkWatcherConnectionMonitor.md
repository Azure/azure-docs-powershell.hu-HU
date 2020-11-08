---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194900"
---
# <span data-ttu-id="926f7-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="926f7-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="926f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="926f7-102">SYNOPSIS</span></span>
<span data-ttu-id="926f7-103">A kapcsolat figyelése erőforrás frissítése</span><span class="sxs-lookup"><span data-stu-id="926f7-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="926f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="926f7-104">SYNTAX</span></span>

### <span data-ttu-id="926f7-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="926f7-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="926f7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="926f7-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="926f7-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="926f7-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="926f7-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="926f7-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="926f7-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="926f7-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="926f7-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="926f7-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="926f7-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="926f7-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="926f7-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="926f7-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="926f7-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="926f7-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="926f7-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="926f7-114">DESCRIPTION</span></span>
<span data-ttu-id="926f7-115">A Set-AzNetworkWatcherConnectionMonitor parancsmag frissíti a kapcsolat figyelése erőforrást.</span><span class="sxs-lookup"><span data-stu-id="926f7-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="926f7-116">Példák</span><span class="sxs-lookup"><span data-stu-id="926f7-116">EXAMPLES</span></span>

### <span data-ttu-id="926f7-117">1. példa: a kapcsolat monitorának frissítése</span><span class="sxs-lookup"><span data-stu-id="926f7-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="926f7-118">Ebben a példában frissítjük a meglévő kapcsolati monitort a destinationAddress módosításával és a címkék hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="926f7-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="926f7-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="926f7-119">PARAMETERS</span></span>

### <span data-ttu-id="926f7-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="926f7-120">-AsJob</span></span>
<span data-ttu-id="926f7-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="926f7-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="926f7-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="926f7-122">-ConfigureOnly</span></span>
<span data-ttu-id="926f7-123">A kapcsolati monitor beállítása, de nem indul el</span><span class="sxs-lookup"><span data-stu-id="926f7-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="926f7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926f7-124">-DefaultProfile</span></span>
<span data-ttu-id="926f7-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="926f7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="926f7-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="926f7-126">-DestinationAddress</span></span>
<span data-ttu-id="926f7-127">A kapcsolat figyelési célhelyének címe (IP vagy tartománynév).</span><span class="sxs-lookup"><span data-stu-id="926f7-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="926f7-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="926f7-128">-DestinationPort</span></span>
<span data-ttu-id="926f7-129">A kapcsolat figyelője által használt célport.</span><span class="sxs-lookup"><span data-stu-id="926f7-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="926f7-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="926f7-130">-DestinationResourceId</span></span>
<span data-ttu-id="926f7-131">A kapcsolat figyelője által célként használt erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="926f7-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="926f7-132">-Force</span><span class="sxs-lookup"><span data-stu-id="926f7-132">-Force</span></span>
<span data-ttu-id="926f7-133">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="926f7-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="926f7-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="926f7-134">-InputObject</span></span>
<span data-ttu-id="926f7-135">A kapcsolat figyelése objektum</span><span class="sxs-lookup"><span data-stu-id="926f7-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="926f7-136">-Hely</span><span class="sxs-lookup"><span data-stu-id="926f7-136">-Location</span></span>
<span data-ttu-id="926f7-137">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="926f7-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="926f7-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="926f7-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="926f7-139">A figyelés intervalluma másodpercben</span><span class="sxs-lookup"><span data-stu-id="926f7-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="926f7-140">Az alapértelmezett érték 60 másodperc.</span><span class="sxs-lookup"><span data-stu-id="926f7-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="926f7-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="926f7-141">-Name</span></span>
<span data-ttu-id="926f7-142">A kapcsolat figyelésének neve.</span><span class="sxs-lookup"><span data-stu-id="926f7-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="926f7-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="926f7-143">-NetworkWatcher</span></span>
<span data-ttu-id="926f7-144">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="926f7-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="926f7-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="926f7-145">-NetworkWatcherName</span></span>
<span data-ttu-id="926f7-146">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="926f7-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="926f7-147">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="926f7-147">-Note</span></span>
<span data-ttu-id="926f7-148">A kapcsolati monitorral társított megjegyzések.</span><span class="sxs-lookup"><span data-stu-id="926f7-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="926f7-149">-Output (kimenet)</span><span class="sxs-lookup"><span data-stu-id="926f7-149">-Output</span></span>
<span data-ttu-id="926f7-150">A képernyőn megjelenő kimeneti célhelyek ismertetése.</span><span class="sxs-lookup"><span data-stu-id="926f7-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="926f7-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="926f7-151">-ResourceGroupName</span></span>
<span data-ttu-id="926f7-152">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="926f7-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="926f7-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="926f7-153">-ResourceId</span></span>
<span data-ttu-id="926f7-154">ConnectionMonitor erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="926f7-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="926f7-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="926f7-155">-SourcePort</span></span>
<span data-ttu-id="926f7-156">A Csatlakozáskezelő által használt forrás-port.</span><span class="sxs-lookup"><span data-stu-id="926f7-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="926f7-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="926f7-157">-SourceResourceId</span></span>
<span data-ttu-id="926f7-158">A forrásként használt erőforrás azonosítója a kapcsolat figyelője szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="926f7-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="926f7-159">-Címke</span><span class="sxs-lookup"><span data-stu-id="926f7-159">-Tag</span></span>
<span data-ttu-id="926f7-160">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="926f7-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="926f7-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="926f7-161">-TestGroup</span></span>
<span data-ttu-id="926f7-162">A vizsgálati csoportok listája.</span><span class="sxs-lookup"><span data-stu-id="926f7-162">The list of test groups.</span></span>

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

### <span data-ttu-id="926f7-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="926f7-163">-Confirm</span></span>
<span data-ttu-id="926f7-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="926f7-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="926f7-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="926f7-165">-WhatIf</span></span>
<span data-ttu-id="926f7-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="926f7-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="926f7-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="926f7-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="926f7-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926f7-168">CommonParameters</span></span>
<span data-ttu-id="926f7-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="926f7-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926f7-170">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="926f7-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926f7-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="926f7-171">INPUTS</span></span>

### <span data-ttu-id="926f7-172">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="926f7-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="926f7-173">System. String</span><span class="sxs-lookup"><span data-stu-id="926f7-173">System.String</span></span>

### <span data-ttu-id="926f7-174">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="926f7-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="926f7-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="926f7-175">OUTPUTS</span></span>

### <span data-ttu-id="926f7-176">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="926f7-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="926f7-177">Microsoft. Azure. commands. Network. models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="926f7-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="926f7-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="926f7-178">NOTES</span></span>

## <span data-ttu-id="926f7-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="926f7-179">RELATED LINKS</span></span>