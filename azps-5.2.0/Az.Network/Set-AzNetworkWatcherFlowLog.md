---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 04a9b4c0ca8b613ce4d4c590572d80a729a65147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344189"
---
# <span data-ttu-id="4e58f-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e58f-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="4e58f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e58f-102">SYNOPSIS</span></span>
<span data-ttu-id="4e58f-103">Frissíti a folyamatnapló-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="4e58f-103">Updates flow log resource.</span></span>

## <span data-ttu-id="4e58f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4e58f-104">SYNTAX</span></span>

### <span data-ttu-id="4e58f-105">SetByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e58f-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e58f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4e58f-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e58f-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="4e58f-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e58f-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="4e58f-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e58f-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4e58f-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e58f-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="4e58f-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e58f-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e58f-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e58f-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="4e58f-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e58f-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4e58f-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e58f-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4e58f-114">DESCRIPTION</span></span>
<span data-ttu-id="4e58f-115">Frissíti a folyamatnapló-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="4e58f-115">Updates flow log resource.</span></span>

## <span data-ttu-id="4e58f-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4e58f-116">EXAMPLES</span></span>

### <span data-ttu-id="4e58f-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="4e58f-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="4e58f-118">Név: pstest Id: /subscriptions/bbbbbbbb-bbbb-bb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState: Sikeres hely: eastus TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbb-bb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId: /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled: True RetentionPolicy: { "Days": 0, "Enabled": false } Format : { "Type": "JSON", "Verzió": 2 } FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="4e58f-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="4e58f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e58f-119">PARAMETERS</span></span>

### <span data-ttu-id="4e58f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e58f-120">-DefaultProfile</span></span>
<span data-ttu-id="4e58f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e58f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e58f-122">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="4e58f-122">-Enabled</span></span>
<span data-ttu-id="4e58f-123">Jelölő a folyamatnaplózás engedélyezéséhez/letiltásához.</span><span class="sxs-lookup"><span data-stu-id="4e58f-123">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="4e58f-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="4e58f-124">-EnableRetention</span></span>
<span data-ttu-id="4e58f-125">Jelölő a megőrzés engedélyezéséhez/letiltásához.</span><span class="sxs-lookup"><span data-stu-id="4e58f-125">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="4e58f-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="4e58f-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="4e58f-127">Flag to enable/disable TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="4e58f-127">Flag to enable/disable TrafficAnalytics</span></span>

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

### <span data-ttu-id="4e58f-128">-Force</span><span class="sxs-lookup"><span data-stu-id="4e58f-128">-Force</span></span>
<span data-ttu-id="4e58f-129">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="4e58f-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4e58f-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="4e58f-130">-FormatType</span></span>
<span data-ttu-id="4e58f-131">A folyamatnapló fájltípusa.</span><span class="sxs-lookup"><span data-stu-id="4e58f-131">The file type of flow log.</span></span>
<span data-ttu-id="4e58f-132">Az egyetlen támogatott érték most a "JSON".</span><span class="sxs-lookup"><span data-stu-id="4e58f-132">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="4e58f-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="4e58f-133">-FormatVersion</span></span>
<span data-ttu-id="4e58f-134">A folyamatnapló verziója (változata).</span><span class="sxs-lookup"><span data-stu-id="4e58f-134">The version (revision) of the flow log.</span></span>

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

### <span data-ttu-id="4e58f-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e58f-135">-InputObject</span></span>
<span data-ttu-id="4e58f-136">Flow lof objektum.</span><span class="sxs-lookup"><span data-stu-id="4e58f-136">Flow lof object.</span></span>

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

### <span data-ttu-id="4e58f-137">-Location</span><span class="sxs-lookup"><span data-stu-id="4e58f-137">-Location</span></span>
<span data-ttu-id="4e58f-138">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="4e58f-138">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4e58f-139">-Name</span><span class="sxs-lookup"><span data-stu-id="4e58f-139">-Name</span></span>
<span data-ttu-id="4e58f-140">A folyamatnapló neve.</span><span class="sxs-lookup"><span data-stu-id="4e58f-140">The flow log name.</span></span>

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

### <span data-ttu-id="4e58f-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e58f-141">-NetworkWatcher</span></span>
<span data-ttu-id="4e58f-142">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="4e58f-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="4e58f-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4e58f-143">-NetworkWatcherName</span></span>
<span data-ttu-id="4e58f-144">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="4e58f-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="4e58f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e58f-145">-ResourceGroupName</span></span>
<span data-ttu-id="4e58f-146">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4e58f-146">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4e58f-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e58f-147">-ResourceId</span></span>
<span data-ttu-id="4e58f-148">FlowLog erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="4e58f-148">FlowLog resource ID.</span></span>

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

### <span data-ttu-id="4e58f-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="4e58f-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="4e58f-150">A folyamatnaplórekordok megőrzésének napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="4e58f-150">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="4e58f-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="4e58f-151">-StorageId</span></span>
<span data-ttu-id="4e58f-152">A folyamatnapló tárolásához használt tárfiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4e58f-152">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="4e58f-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e58f-153">-Tag</span></span>
<span data-ttu-id="4e58f-154">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="4e58f-154">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4e58f-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4e58f-155">-TargetResourceId</span></span>
<span data-ttu-id="4e58f-156">Annak a hálózati biztonsági csoportnak az azonosítója, amelyre a folyamatnaplót alkalmazni fogja.</span><span class="sxs-lookup"><span data-stu-id="4e58f-156">ID of network security group to which flow log will be applied.</span></span>

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

### <span data-ttu-id="4e58f-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="4e58f-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="4e58f-158">Az az intervallum percben, amely azt határozza meg, hogy a TA szolgáltatásnak milyen gyakran kell folyamatelemzést folyatni.</span><span class="sxs-lookup"><span data-stu-id="4e58f-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="4e58f-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="4e58f-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="4e58f-160">A csatolt munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4e58f-160">Resource Id of the attached workspace.</span></span>

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

### <span data-ttu-id="4e58f-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e58f-161">-Confirm</span></span>
<span data-ttu-id="4e58f-162">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4e58f-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e58f-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e58f-163">-WhatIf</span></span>
<span data-ttu-id="4e58f-164">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4e58f-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e58f-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e58f-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e58f-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e58f-166">CommonParameters</span></span>
<span data-ttu-id="4e58f-167">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e58f-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e58f-168">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e58f-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e58f-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e58f-169">INPUTS</span></span>

### <span data-ttu-id="4e58f-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e58f-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4e58f-171">System.String</span><span class="sxs-lookup"><span data-stu-id="4e58f-171">System.String</span></span>

### <span data-ttu-id="4e58f-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="4e58f-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="4e58f-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e58f-173">OUTPUTS</span></span>

### <span data-ttu-id="4e58f-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="4e58f-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="4e58f-175">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4e58f-175">NOTES</span></span>

## <span data-ttu-id="4e58f-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e58f-176">RELATED LINKS</span></span>

[<span data-ttu-id="4e58f-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e58f-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4e58f-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e58f-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4e58f-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e58f-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4e58f-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4e58f-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4e58f-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4e58f-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4e58f-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4e58f-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4e58f-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4e58f-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4e58f-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e58f-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e58f-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4e58f-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4e58f-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e58f-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e58f-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e58f-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e58f-188">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e58f-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e58f-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e58f-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4e58f-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4e58f-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4e58f-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4e58f-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4e58f-192">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e58f-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e58f-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e58f-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e58f-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e58f-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e58f-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e58f-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4e58f-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e58f-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e58f-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e58f-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e58f-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4e58f-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4e58f-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4e58f-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4e58f-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4e58f-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4e58f-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4e58f-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4e58f-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4e58f-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="4e58f-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e58f-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="4e58f-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e58f-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="4e58f-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e58f-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="4e58f-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e58f-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
