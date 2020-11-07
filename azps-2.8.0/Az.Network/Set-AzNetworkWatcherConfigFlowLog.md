---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f2e063e6870ebfe41034441b7b3134694d9a85a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838229"
---
# <span data-ttu-id="0e89f-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0e89f-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="0e89f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e89f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e89f-103">Beállítja a folyamatábra erőforrás-naplózását.</span><span class="sxs-lookup"><span data-stu-id="0e89f-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="0e89f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e89f-104">SYNTAX</span></span>

### <span data-ttu-id="0e89f-105">SetFlowlogByResourceWithoutTA (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e89f-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e89f-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="0e89f-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e89f-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="0e89f-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e89f-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="0e89f-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e89f-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="0e89f-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e89f-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="0e89f-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e89f-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="0e89f-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e89f-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="0e89f-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e89f-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="0e89f-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e89f-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e89f-114">DESCRIPTION</span></span>
<span data-ttu-id="0e89f-115">A Set-AzNetworkWatcherConfigFlowLog beállítja a cél erőforráshoz tartozó folyamatábra naplózását.</span><span class="sxs-lookup"><span data-stu-id="0e89f-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="0e89f-116">A megadható tulajdonságok: az adott erőforrásra vonatkozóan engedélyezve van-e a forgalom naplózása, a konfigurált tárterület-fiók a naplók küldéséhez, a forgalom naplózásához és a naplók adatmegőrzési házirendjéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="0e89f-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="0e89f-117">Jelenleg hálózati biztonsági csoportok támogatottak a forgalom naplózásához.</span><span class="sxs-lookup"><span data-stu-id="0e89f-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="0e89f-118">Példák</span><span class="sxs-lookup"><span data-stu-id="0e89f-118">EXAMPLES</span></span>

### <span data-ttu-id="0e89f-119">Példa 1: a forgalom naplózásának beállítása megadott NSG</span><span class="sxs-lookup"><span data-stu-id="0e89f-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
```

<span data-ttu-id="0e89f-120">Ebben a példában a naplózási állapotot egy hálózati biztonsági csoporthoz konfiguráltuk.</span><span class="sxs-lookup"><span data-stu-id="0e89f-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="0e89f-121">A válaszban láthatja, hogy a megadott NSG van forgalom naplózás engedélyezve, alapértelmezett formátum és nincs adatmegőrzési házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="0e89f-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="0e89f-122">2. példa: a forgalom naplózásának beállítása egy megadott NSG, és a forgalom naplózási verziójának beállítása a 2 értékre.</span><span class="sxs-lookup"><span data-stu-id="0e89f-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -FormatVersion 2

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 2
                   }
```

<span data-ttu-id="0e89f-123">Ebben a példában a flow naplózást egy hálózati biztonsági csoportban (NSG) konfiguráltuk, amelyen a 2-es verziójú naplók van megadva.</span><span class="sxs-lookup"><span data-stu-id="0e89f-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="0e89f-124">A válaszban láthatja, hogy a megadott NSG engedélyezve van a forgalom naplózása, a formátum be van állítva, és nincs beállítva adatmegőrzési szabály.</span><span class="sxs-lookup"><span data-stu-id="0e89f-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="0e89f-125">Ha a régió nem támogatja a megadott verziót, a Hálózatfigyelő az alapértelmezett támogatott verziót fogja írni a régióban.</span><span class="sxs-lookup"><span data-stu-id="0e89f-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="0e89f-126">3. példa: a forgalmi naplózás és a forgalmi elemzés beállítása egy megadott NSG</span><span class="sxs-lookup"><span data-stu-id="0e89f-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="0e89f-127">Ebben a példában a folyamat naplózási állapotát és a forgalmi elemzést egy hálózati biztonsági csoporthoz konfiguráltuk.</span><span class="sxs-lookup"><span data-stu-id="0e89f-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="0e89f-128">A válaszban láthatja, hogy a megadott NSG folyik a naplózás és a forgalmi statisztika, az alapértelmezett formátum és a nincs adatmegőrzési házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="0e89f-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

## <span data-ttu-id="0e89f-129">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e89f-129">PARAMETERS</span></span>

### <span data-ttu-id="0e89f-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e89f-130">-AsJob</span></span>
<span data-ttu-id="0e89f-131">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0e89f-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e89f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e89f-132">-DefaultProfile</span></span>
<span data-ttu-id="0e89f-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e89f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e89f-134">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="0e89f-134">-EnableFlowLog</span></span>
<span data-ttu-id="0e89f-135">A forgalom naplózásának engedélyezésére/letiltására szolgáló jelölő</span><span class="sxs-lookup"><span data-stu-id="0e89f-135">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-136">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="0e89f-136">-EnableRetention</span></span>
<span data-ttu-id="0e89f-137">Jelölő az adatmegőrzés engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="0e89f-137">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-138">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="0e89f-138">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="0e89f-139">Jelölő az adatmegőrzés engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="0e89f-139">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases: EnableTA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-140">-FormatType</span><span class="sxs-lookup"><span data-stu-id="0e89f-140">-FormatType</span></span>
<span data-ttu-id="0e89f-141">A flow log formátum típusa.</span><span class="sxs-lookup"><span data-stu-id="0e89f-141">Type of flow log format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-142">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="0e89f-142">-FormatVersion</span></span>
<span data-ttu-id="0e89f-143">A flow log formátum verziója.</span><span class="sxs-lookup"><span data-stu-id="0e89f-143">Version of flow log format.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-144">-Hely</span><span class="sxs-lookup"><span data-stu-id="0e89f-144">-Location</span></span>
<span data-ttu-id="0e89f-145">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="0e89f-145">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails, SetFlowlogByLocationWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-146">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e89f-146">-NetworkWatcher</span></span>
<span data-ttu-id="0e89f-147">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="0e89f-147">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetFlowlogByResourceWithoutTA, SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-148">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0e89f-148">-NetworkWatcherName</span></span>
<span data-ttu-id="0e89f-149">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="0e89f-149">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e89f-150">-ResourceGroupName</span></span>
<span data-ttu-id="0e89f-151">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0e89f-151">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0e89f-152">-RetentionInDays</span></span>
<span data-ttu-id="0e89f-153">A átfolyási napló rekordjainak megtartására szolgáló napok száma.</span><span class="sxs-lookup"><span data-stu-id="0e89f-153">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0e89f-154">-StorageAccountId</span></span>
<span data-ttu-id="0e89f-155">Annak a tárolási fióknak az azonosítója, amely a folyamatábra tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="0e89f-155">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-156">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0e89f-156">-TargetResourceId</span></span>
<span data-ttu-id="0e89f-157">A cél erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0e89f-157">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-158">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="0e89f-158">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="0e89f-159">Beadja vagy beállítja azt az intervallumot (percben), amelynek alapján a TA-s szolgáltatásnak a forgalom-elemzést meg kell tennie.</span><span class="sxs-lookup"><span data-stu-id="0e89f-159">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-160">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="0e89f-160">-Workspace</span></span>
<span data-ttu-id="0e89f-161">Az a WS objektum, amely a forgalmi statisztika adatainak tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="0e89f-161">The WS object which is used to store the traffic analytics data.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByResourceWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByLocationWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-162">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="0e89f-162">-WorkspaceGUID</span></span>
<span data-ttu-id="0e89f-163">Annak a WS-nek a GUID-azonosítója, amely a forgalmi statisztika adatainak tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="0e89f-163">GUID of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-164">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="0e89f-164">-WorkspaceLocation</span></span>
<span data-ttu-id="0e89f-165">A WS Azure-területe, amely a forgalmi statisztika adatainak tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="0e89f-165">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-166">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="0e89f-166">-WorkspaceResourceId</span></span>
<span data-ttu-id="0e89f-167">A forgalom-elemzési adatokat tároló WS előfizetése.</span><span class="sxs-lookup"><span data-stu-id="0e89f-167">Subscription of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e89f-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e89f-168">-Confirm</span></span>
<span data-ttu-id="0e89f-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e89f-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e89f-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e89f-170">-WhatIf</span></span>
<span data-ttu-id="0e89f-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e89f-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e89f-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e89f-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e89f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e89f-173">CommonParameters</span></span>
<span data-ttu-id="0e89f-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e89f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e89f-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e89f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e89f-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e89f-176">INPUTS</span></span>

### <span data-ttu-id="0e89f-177">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e89f-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0e89f-178">System. String</span><span class="sxs-lookup"><span data-stu-id="0e89f-178">System.String</span></span>

### <span data-ttu-id="0e89f-179">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e89f-179">System.Boolean</span></span>

### <span data-ttu-id="0e89f-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0e89f-180">System.Int32</span></span>

### <span data-ttu-id="0e89f-181">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0e89f-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0e89f-182">Microsoft. Azure. Management. internal. Network. Common. IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e89f-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="0e89f-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e89f-183">OUTPUTS</span></span>

### <span data-ttu-id="0e89f-184">Microsoft. Azure. commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="0e89f-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="0e89f-185">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e89f-185">NOTES</span></span>
<span data-ttu-id="0e89f-186">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, flow, naplók, flowlog, naplózás</span><span class="sxs-lookup"><span data-stu-id="0e89f-186">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="0e89f-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e89f-187">RELATED LINKS</span></span>

[<span data-ttu-id="0e89f-188">Új – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e89f-188">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0e89f-189">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e89f-189">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0e89f-190">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e89f-190">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0e89f-191">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0e89f-191">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0e89f-192">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0e89f-192">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0e89f-193">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0e89f-193">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0e89f-194">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0e89f-194">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0e89f-195">Új – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e89f-195">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e89f-196">Új – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0e89f-196">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0e89f-197">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e89f-197">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e89f-198">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e89f-198">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e89f-199">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e89f-199">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e89f-200">Új – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e89f-200">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0e89f-201">Teszt-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0e89f-201">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0e89f-202">Teszt-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0e89f-202">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0e89f-203">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e89f-203">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e89f-204">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e89f-204">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e89f-205">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e89f-205">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e89f-206">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0e89f-206">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0e89f-207">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e89f-207">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e89f-208">Új – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e89f-208">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0e89f-209">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0e89f-209">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0e89f-210">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0e89f-210">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0e89f-211">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0e89f-211">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0e89f-212">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0e89f-212">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0e89f-213">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0e89f-213">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="0e89f-214">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0e89f-214">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
