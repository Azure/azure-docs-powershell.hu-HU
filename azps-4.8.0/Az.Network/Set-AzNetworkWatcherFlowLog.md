---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 04a9b4c0ca8b613ce4d4c590572d80a729a65147
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182968"
---
# <span data-ttu-id="6bccc-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="6bccc-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="6bccc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6bccc-102">SYNOPSIS</span></span>
<span data-ttu-id="6bccc-103">Frissíti a folyamatábra erőforrását.</span><span class="sxs-lookup"><span data-stu-id="6bccc-103">Updates flow log resource.</span></span>

## <span data-ttu-id="6bccc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6bccc-104">SYNTAX</span></span>

### <span data-ttu-id="6bccc-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6bccc-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bccc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6bccc-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bccc-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="6bccc-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bccc-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="6bccc-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bccc-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6bccc-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bccc-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="6bccc-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bccc-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bccc-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bccc-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="6bccc-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bccc-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="6bccc-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bccc-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="6bccc-114">DESCRIPTION</span></span>
<span data-ttu-id="6bccc-115">Frissíti a folyamatábra erőforrását.</span><span class="sxs-lookup"><span data-stu-id="6bccc-115">Updates flow log resource.</span></span>

## <span data-ttu-id="6bccc-116">Példák</span><span class="sxs-lookup"><span data-stu-id="6bccc-116">EXAMPLES</span></span>

### <span data-ttu-id="6bccc-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6bccc-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="6bccc-118">Név: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. hálózat/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETAG: W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState: a sikeres hely: eastus TargetResourceId:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MyStorage enabled: true RetentionPolicy: {"Days": 0, "enabled": false} Format: {"type": "JSON", "version": 2} FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="6bccc-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="6bccc-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6bccc-119">PARAMETERS</span></span>

### <span data-ttu-id="6bccc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bccc-120">-DefaultProfile</span></span>
<span data-ttu-id="6bccc-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bccc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bccc-122">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="6bccc-122">-Enabled</span></span>
<span data-ttu-id="6bccc-123">A forgalom naplózásának engedélyezésére/letiltására szolgáló jelölő</span><span class="sxs-lookup"><span data-stu-id="6bccc-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="6bccc-124">-EnableRetention</span></span>
<span data-ttu-id="6bccc-125">Jelölő az adatmegőrzés engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="6bccc-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="6bccc-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="6bccc-127">Megjelölés a TrafficAnalytics engedélyezésére/letiltására</span><span class="sxs-lookup"><span data-stu-id="6bccc-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-128">-Force</span><span class="sxs-lookup"><span data-stu-id="6bccc-128">-Force</span></span>
<span data-ttu-id="6bccc-129">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6bccc-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6bccc-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="6bccc-130">-FormatType</span></span>
<span data-ttu-id="6bccc-131">A folyamatábra fájltípusa.</span><span class="sxs-lookup"><span data-stu-id="6bccc-131">The file type of flow log.</span></span>
<span data-ttu-id="6bccc-132">Az egyetlen támogatott érték most a "JSON".</span><span class="sxs-lookup"><span data-stu-id="6bccc-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="6bccc-133">-FormatVersion</span></span>
<span data-ttu-id="6bccc-134">A folyamatábra (átdolgozás) verziója.</span><span class="sxs-lookup"><span data-stu-id="6bccc-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bccc-135">-InputObject</span></span>
<span data-ttu-id="6bccc-136">Folyamatábra LOF objektum</span><span class="sxs-lookup"><span data-stu-id="6bccc-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="6bccc-137">-Location</span></span>
<span data-ttu-id="6bccc-138">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="6bccc-138">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6bccc-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6bccc-139">-Name</span></span>
<span data-ttu-id="6bccc-140">A folyamatábra neve.</span><span class="sxs-lookup"><span data-stu-id="6bccc-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6bccc-141">-NetworkWatcher</span></span>
<span data-ttu-id="6bccc-142">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6bccc-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="6bccc-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6bccc-143">-NetworkWatcherName</span></span>
<span data-ttu-id="6bccc-144">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="6bccc-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="6bccc-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bccc-145">-ResourceGroupName</span></span>
<span data-ttu-id="6bccc-146">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6bccc-146">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6bccc-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bccc-147">-ResourceId</span></span>
<span data-ttu-id="6bccc-148">FlowLog erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6bccc-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="6bccc-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="6bccc-150">A átfolyási napló rekordjainak megtartására szolgáló napok száma.</span><span class="sxs-lookup"><span data-stu-id="6bccc-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="6bccc-151">-StorageId</span></span>
<span data-ttu-id="6bccc-152">Annak a tárolási fióknak az azonosítója, amely a folyamatábra tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="6bccc-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-153">-Címke</span><span class="sxs-lookup"><span data-stu-id="6bccc-153">-Tag</span></span>
<span data-ttu-id="6bccc-154">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6bccc-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6bccc-155">-TargetResourceId</span></span>
<span data-ttu-id="6bccc-156">Annak a hálózati biztonsági csoportnak az azonosítója, amelyre a program a folyamatábrát alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="6bccc-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="6bccc-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="6bccc-158">Az intervallum percben, amely azt határozza meg, hogy milyen gyakran kell a TA-t átáramlni a szolgáltató?</span><span class="sxs-lookup"><span data-stu-id="6bccc-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="6bccc-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="6bccc-160">A csatolt munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6bccc-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bccc-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6bccc-161">-Confirm</span></span>
<span data-ttu-id="6bccc-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6bccc-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bccc-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bccc-163">-WhatIf</span></span>
<span data-ttu-id="6bccc-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6bccc-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bccc-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6bccc-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bccc-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bccc-166">CommonParameters</span></span>
<span data-ttu-id="6bccc-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6bccc-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bccc-168">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6bccc-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bccc-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bccc-169">INPUTS</span></span>

### <span data-ttu-id="6bccc-170">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6bccc-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="6bccc-171">System. String</span><span class="sxs-lookup"><span data-stu-id="6bccc-171">System.String</span></span>

### <span data-ttu-id="6bccc-172">Microsoft. Azure. commands. Network. models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="6bccc-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="6bccc-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bccc-173">OUTPUTS</span></span>

### <span data-ttu-id="6bccc-174">Microsoft. Azure. commands. Network. models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="6bccc-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="6bccc-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6bccc-175">NOTES</span></span>

## <span data-ttu-id="6bccc-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bccc-176">RELATED LINKS</span></span>

[<span data-ttu-id="6bccc-177">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6bccc-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6bccc-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6bccc-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6bccc-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6bccc-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6bccc-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6bccc-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6bccc-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6bccc-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6bccc-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6bccc-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6bccc-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6bccc-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6bccc-184">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6bccc-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6bccc-185">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6bccc-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6bccc-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6bccc-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6bccc-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6bccc-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6bccc-188">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6bccc-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6bccc-189">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bccc-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6bccc-190">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6bccc-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6bccc-191">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6bccc-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6bccc-192">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bccc-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6bccc-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bccc-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6bccc-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bccc-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6bccc-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6bccc-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6bccc-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bccc-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6bccc-197">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bccc-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6bccc-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6bccc-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6bccc-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6bccc-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6bccc-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6bccc-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6bccc-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6bccc-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6bccc-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6bccc-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="6bccc-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6bccc-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="6bccc-204">Új – AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="6bccc-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="6bccc-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="6bccc-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="6bccc-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="6bccc-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
