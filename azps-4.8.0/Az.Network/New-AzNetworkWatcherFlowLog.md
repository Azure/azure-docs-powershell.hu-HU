---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 1fe3cb8227751553ac748fb99cf08baa044a6f0d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184366"
---
# <span data-ttu-id="ed9bd-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ed9bd-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="ed9bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9bd-103">Folyamatábra-erőforrás létrehozása vagy frissítése a megadott hálózati biztonsági csoport számára.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="ed9bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed9bd-104">SYNTAX</span></span>

### <span data-ttu-id="ed9bd-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed9bd-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed9bd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ed9bd-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed9bd-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="ed9bd-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed9bd-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="ed9bd-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed9bd-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ed9bd-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed9bd-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="ed9bd-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed9bd-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed9bd-111">DESCRIPTION</span></span>
<span data-ttu-id="ed9bd-112">New-AzNetworkWatcherFlowLog parancs a megadott hálózati biztonsági csoporthoz hoz létre vagy frissít egy folyamatábra-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="ed9bd-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ed9bd-113">EXAMPLES</span></span>

### <span data-ttu-id="ed9bd-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ed9bd-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="ed9bd-115">Név: pstest-azonosító:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid. hálózat/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETAG: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: sikerült hely: eastus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MySTorage: true RetentionPolicy: {"Days": 5, "enabled": true} formátum: {"type": "JSON", "version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb"; "workspaceRegion": "eastus", "workspaceResourceId": "/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr": "oups FlowLogsV2Demo/OperationalInsights/Providers/Microsoft. MyWorkspace 60</span><span class="sxs-lookup"><span data-stu-id="ed9bd-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="ed9bd-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="ed9bd-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="ed9bd-117">Ha le szeretné tiltani a flowLog-erőforrást, amelyre a TrafficAnalytics konfigurálva van, le kell tiltania a TrafficAnalytics is.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="ed9bd-118">Ezt úgy teheti meg, mint a 2.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="ed9bd-119">Név: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETAG: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: sikerült hely: eastus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. hálózat/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MySTorage enabled: false RetentionPolicy: {"Days": 0, "enabled": false} formátum: {"type": "JSON", "version": 1} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"TrafficAnalyticsInterval": {"enabled": false, "": 60}}</span><span class="sxs-lookup"><span data-stu-id="ed9bd-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="ed9bd-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed9bd-120">PARAMETERS</span></span>

### <span data-ttu-id="ed9bd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9bd-121">-DefaultProfile</span></span>
<span data-ttu-id="ed9bd-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-123">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="ed9bd-123">-Enabled</span></span>
<span data-ttu-id="ed9bd-124">A forgalom naplózásának engedélyezésére/letiltására szolgáló jelölő</span><span class="sxs-lookup"><span data-stu-id="ed9bd-124">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="ed9bd-125">-EnableRetention</span></span>
<span data-ttu-id="ed9bd-126">Jelölő az adatmegőrzés engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-126">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="ed9bd-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="ed9bd-128">Megjelölés a TrafficAnalytics engedélyezésére/letiltására</span><span class="sxs-lookup"><span data-stu-id="ed9bd-128">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-129">-Force</span><span class="sxs-lookup"><span data-stu-id="ed9bd-129">-Force</span></span>
<span data-ttu-id="ed9bd-130">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ed9bd-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="ed9bd-131">-FormatType</span></span>
<span data-ttu-id="ed9bd-132">A folyamatábra fájltípusa.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-132">The file type of flow log.</span></span>
<span data-ttu-id="ed9bd-133">Az egyetlen támogatott érték most a "JSON".</span><span class="sxs-lookup"><span data-stu-id="ed9bd-133">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="ed9bd-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="ed9bd-134">-FormatVersion</span></span>
<span data-ttu-id="ed9bd-135">A folyamatábra (átdolgozás) verziója.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-135">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-136">-Hely</span><span class="sxs-lookup"><span data-stu-id="ed9bd-136">-Location</span></span>
<span data-ttu-id="ed9bd-137">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-137">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed9bd-138">-Name</span></span>
<span data-ttu-id="ed9bd-139">A folyamatábra neve.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-139">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed9bd-140">-NetworkWatcher</span></span>
<span data-ttu-id="ed9bd-141">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-141">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ed9bd-142">-NetworkWatcherName</span></span>
<span data-ttu-id="ed9bd-143">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-143">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed9bd-144">-ResourceGroupName</span></span>
<span data-ttu-id="ed9bd-145">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-145">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="ed9bd-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="ed9bd-147">A átfolyási napló rekordjainak megtartására szolgáló napok száma.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-147">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-148">-StorageId</span><span class="sxs-lookup"><span data-stu-id="ed9bd-148">-StorageId</span></span>
<span data-ttu-id="ed9bd-149">Annak a tárolási fióknak az azonosítója, amely a folyamatábra tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-149">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-150">-Címke</span><span class="sxs-lookup"><span data-stu-id="ed9bd-150">-Tag</span></span>
<span data-ttu-id="ed9bd-151">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-151">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ed9bd-152">-TargetResourceId</span></span>
<span data-ttu-id="ed9bd-153">Annak a hálózati biztonsági csoportnak az azonosítója, amelyre a program a folyamatábrát alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-153">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="ed9bd-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="ed9bd-155">Az intervallum percben, amely azt határozza meg, hogy milyen gyakran kell a TA-t átáramlni a szolgáltató?</span><span class="sxs-lookup"><span data-stu-id="ed9bd-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="ed9bd-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="ed9bd-157">A csatolt munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-157">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed9bd-158">-Confirm</span></span>
<span data-ttu-id="ed9bd-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed9bd-160">-WhatIf</span></span>
<span data-ttu-id="ed9bd-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed9bd-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9bd-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9bd-163">CommonParameters</span></span>
<span data-ttu-id="ed9bd-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed9bd-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9bd-165">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9bd-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed9bd-166">INPUTS</span></span>

### <span data-ttu-id="ed9bd-167">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed9bd-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="ed9bd-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed9bd-168">OUTPUTS</span></span>

### <span data-ttu-id="ed9bd-169">Microsoft. Azure. commands. Network. models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="ed9bd-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="ed9bd-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed9bd-170">NOTES</span></span>

## <span data-ttu-id="ed9bd-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed9bd-171">RELATED LINKS</span></span>

[<span data-ttu-id="ed9bd-172">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed9bd-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ed9bd-173">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed9bd-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ed9bd-174">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed9bd-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ed9bd-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ed9bd-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ed9bd-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ed9bd-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ed9bd-177">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ed9bd-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ed9bd-178">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ed9bd-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ed9bd-179">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed9bd-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed9bd-180">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ed9bd-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ed9bd-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed9bd-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed9bd-182">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed9bd-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed9bd-183">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ed9bd-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ed9bd-184">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed9bd-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ed9bd-185">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ed9bd-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ed9bd-186">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ed9bd-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ed9bd-187">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed9bd-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed9bd-188">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed9bd-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed9bd-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed9bd-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed9bd-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ed9bd-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ed9bd-191">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed9bd-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed9bd-192">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed9bd-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ed9bd-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ed9bd-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ed9bd-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ed9bd-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ed9bd-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ed9bd-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ed9bd-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ed9bd-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ed9bd-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ed9bd-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="ed9bd-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed9bd-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="ed9bd-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ed9bd-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="ed9bd-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ed9bd-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="ed9bd-201">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ed9bd-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
