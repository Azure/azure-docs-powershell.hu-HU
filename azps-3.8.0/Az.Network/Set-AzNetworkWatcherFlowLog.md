---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: c59034dcd587c9fee3ce6a4a7699670c77ea372f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401579"
---
# <span data-ttu-id="7a4dd-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7a4dd-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="7a4dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7a4dd-103">Frissíti a folyamatnapló-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-103">Updates flow log resource.</span></span>

## <span data-ttu-id="7a4dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a4dd-104">SYNTAX</span></span>

### <span data-ttu-id="7a4dd-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a4dd-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a4dd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7a4dd-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a4dd-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="7a4dd-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a4dd-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="7a4dd-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a4dd-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7a4dd-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a4dd-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="7a4dd-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a4dd-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a4dd-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a4dd-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="7a4dd-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a4dd-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="7a4dd-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a4dd-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a4dd-114">DESCRIPTION</span></span>
<span data-ttu-id="7a4dd-115">Frissíti a folyamatnapló-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-115">Updates flow log resource.</span></span>

## <span data-ttu-id="7a4dd-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a4dd-116">EXAMPLES</span></span>

### <span data-ttu-id="7a4dd-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="7a4dd-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="7a4dd-118">Név: pstest Id: /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState: Sikeres hely: eastus TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId: /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled: True RetentionPolicy: { "Days": 0, "Enabled": false } Format : { "Type": "JSON", "Verzió": 2 } FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="7a4dd-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="7a4dd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a4dd-119">PARAMETERS</span></span>

### <span data-ttu-id="7a4dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a4dd-120">-DefaultProfile</span></span>
<span data-ttu-id="7a4dd-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a4dd-122">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="7a4dd-122">-Enabled</span></span>
<span data-ttu-id="7a4dd-123">Jelölő a folyamatnaplózás engedélyezéséhez/letiltásához.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-123">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="7a4dd-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="7a4dd-124">-EnableRetention</span></span>
<span data-ttu-id="7a4dd-125">Jelölő a megőrzés engedélyezéséhez/letiltásához.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-125">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="7a4dd-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="7a4dd-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="7a4dd-127">Flag to enable/disable TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="7a4dd-127">Flag to enable/disable TrafficAnalytics</span></span>

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

### <span data-ttu-id="7a4dd-128">-Force</span><span class="sxs-lookup"><span data-stu-id="7a4dd-128">-Force</span></span>
<span data-ttu-id="7a4dd-129">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="7a4dd-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7a4dd-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="7a4dd-130">-FormatType</span></span>
<span data-ttu-id="7a4dd-131">A folyamatnapló fájltípusa.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-131">The file type of flow log.</span></span>
<span data-ttu-id="7a4dd-132">Az egyetlen támogatott érték most a "JSON".</span><span class="sxs-lookup"><span data-stu-id="7a4dd-132">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="7a4dd-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="7a4dd-133">-FormatVersion</span></span>
<span data-ttu-id="7a4dd-134">A folyamatnapló verziója (változata).</span><span class="sxs-lookup"><span data-stu-id="7a4dd-134">The version (revision) of the flow log.</span></span>

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

### <span data-ttu-id="7a4dd-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a4dd-135">-InputObject</span></span>
<span data-ttu-id="7a4dd-136">Flow lof objektum.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-136">Flow lof object.</span></span>

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

### <span data-ttu-id="7a4dd-137">-Location</span><span class="sxs-lookup"><span data-stu-id="7a4dd-137">-Location</span></span>
<span data-ttu-id="7a4dd-138">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-138">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7a4dd-139">-Name</span><span class="sxs-lookup"><span data-stu-id="7a4dd-139">-Name</span></span>
<span data-ttu-id="7a4dd-140">A folyamatnapló neve.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-140">The flow log name.</span></span>

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

### <span data-ttu-id="7a4dd-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a4dd-141">-NetworkWatcher</span></span>
<span data-ttu-id="7a4dd-142">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="7a4dd-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7a4dd-143">-NetworkWatcherName</span></span>
<span data-ttu-id="7a4dd-144">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="7a4dd-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a4dd-145">-ResourceGroupName</span></span>
<span data-ttu-id="7a4dd-146">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-146">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7a4dd-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a4dd-147">-ResourceId</span></span>
<span data-ttu-id="7a4dd-148">FlowLog erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-148">FlowLog resource ID.</span></span>

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

### <span data-ttu-id="7a4dd-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="7a4dd-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="7a4dd-150">A folyamatnaplórekordok megőrzésének napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-150">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="7a4dd-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="7a4dd-151">-StorageId</span></span>
<span data-ttu-id="7a4dd-152">A folyamatnapló tárolásához használt tárfiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-152">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="7a4dd-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a4dd-153">-Tag</span></span>
<span data-ttu-id="7a4dd-154">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-154">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7a4dd-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7a4dd-155">-TargetResourceId</span></span>
<span data-ttu-id="7a4dd-156">Annak a hálózati biztonsági csoportnak az azonosítója, amelyre a folyamatnaplót alkalmazni fogja.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-156">ID of network security group to which flow log will be applied.</span></span>

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

### <span data-ttu-id="7a4dd-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="7a4dd-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="7a4dd-158">Az az intervallum percben, amely azt határozza meg, hogy a TA szolgáltatásnak milyen gyakran kell folyamatelemzést folyatni.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="7a4dd-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7a4dd-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="7a4dd-160">A csatolt munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-160">Resource Id of the attached workspace.</span></span>

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

### <span data-ttu-id="7a4dd-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a4dd-161">-Confirm</span></span>
<span data-ttu-id="7a4dd-162">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a4dd-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a4dd-163">-WhatIf</span></span>
<span data-ttu-id="7a4dd-164">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a4dd-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a4dd-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a4dd-166">CommonParameters</span></span>
<span data-ttu-id="7a4dd-167">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a4dd-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a4dd-168">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a4dd-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a4dd-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a4dd-169">INPUTS</span></span>

### <span data-ttu-id="7a4dd-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a4dd-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7a4dd-171">System.String</span><span class="sxs-lookup"><span data-stu-id="7a4dd-171">System.String</span></span>

### <span data-ttu-id="7a4dd-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="7a4dd-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="7a4dd-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a4dd-173">OUTPUTS</span></span>

### <span data-ttu-id="7a4dd-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="7a4dd-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="7a4dd-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a4dd-175">NOTES</span></span>

## <span data-ttu-id="7a4dd-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a4dd-176">RELATED LINKS</span></span>

[<span data-ttu-id="7a4dd-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a4dd-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7a4dd-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a4dd-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7a4dd-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7a4dd-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7a4dd-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7a4dd-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7a4dd-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7a4dd-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7a4dd-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7a4dd-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7a4dd-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7a4dd-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7a4dd-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a4dd-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a4dd-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7a4dd-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7a4dd-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a4dd-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a4dd-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a4dd-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a4dd-188">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7a4dd-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7a4dd-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a4dd-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7a4dd-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7a4dd-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7a4dd-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7a4dd-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7a4dd-192">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7a4dd-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7a4dd-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7a4dd-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7a4dd-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7a4dd-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7a4dd-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7a4dd-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7a4dd-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7a4dd-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7a4dd-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7a4dd-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7a4dd-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7a4dd-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7a4dd-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7a4dd-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7a4dd-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7a4dd-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7a4dd-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7a4dd-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7a4dd-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7a4dd-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7a4dd-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7a4dd-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7a4dd-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7a4dd-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="7a4dd-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7a4dd-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="7a4dd-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="7a4dd-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
