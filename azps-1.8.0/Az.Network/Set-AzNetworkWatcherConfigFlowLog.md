---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: bd921f855d95e729ebc2ff0fed32ef56bfe52110
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400093"
---
# <span data-ttu-id="c47b0-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c47b0-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="c47b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c47b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c47b0-103">Folyamatnaplózás beállítása célerőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="c47b0-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="c47b0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c47b0-104">SYNTAX</span></span>

### <span data-ttu-id="c47b0-105">SetFlowlogByResourceWithoutTA (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c47b0-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c47b0-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="c47b0-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c47b0-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="c47b0-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c47b0-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="c47b0-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c47b0-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="c47b0-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c47b0-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="c47b0-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c47b0-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="c47b0-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c47b0-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="c47b0-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c47b0-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="c47b0-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c47b0-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c47b0-114">DESCRIPTION</span></span>
<span data-ttu-id="c47b0-115">A Set-AzNetworkWatcherConfigFlowLog konfigurálja a folyamatnaplózást egy célerőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="c47b0-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="c47b0-116">Konfigurálható tulajdonságok: engedélyezve van-e a folyamatnaplózás az erőforráshoz, a konfigurált tárfiók naplók küldésekor, a folyamatnaplózási formátum és a naplók adatmegőrzési házirende.</span><span class="sxs-lookup"><span data-stu-id="c47b0-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="c47b0-117">A hálózati biztonsági csoportok jelenleg a folyamatnaplózásban támogatottak.</span><span class="sxs-lookup"><span data-stu-id="c47b0-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="c47b0-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c47b0-118">EXAMPLES</span></span>

### <span data-ttu-id="c47b0-119">1. példa: Folyamatnaplózás konfigurálása egy megadott NSG-hez</span><span class="sxs-lookup"><span data-stu-id="c47b0-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="c47b0-120">Ebben a példában egy hálózati biztonsági csoport folyamatnaplózási állapotát konfiguráljuk.</span><span class="sxs-lookup"><span data-stu-id="c47b0-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="c47b0-121">A válaszban azt látjuk, hogy a megadott NSG-hez engedélyezve van a folyamatnaplózás, az alapértelmezett formátum, és nincs beállítva adatmegőrzési házirend.</span><span class="sxs-lookup"><span data-stu-id="c47b0-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="c47b0-122">2. példa: A folyamatnaplózás konfigurálása egy megadott NSG-hez, és a folyamatnaplózás verziójának beállítása 2-re.</span><span class="sxs-lookup"><span data-stu-id="c47b0-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="c47b0-123">Ebben a példában egy 2-es verziójú naplók beállításával konfiguráljuk egy hálózati biztonsági csoport (NSG) folyamatnaplózását.</span><span class="sxs-lookup"><span data-stu-id="c47b0-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="c47b0-124">A válaszban azt látjuk, hogy a megadott NSG-nek engedélyezve van a folyamatnaplózása, be van állítva a formátum, és nincs konfigurálva adatmegőrzési házirend.</span><span class="sxs-lookup"><span data-stu-id="c47b0-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="c47b0-125">Ha a régió nem támogatja az Ön által megadott verziót, a Hálózati figyelő megírja az alapértelmezett támogatott verziót a régióban.</span><span class="sxs-lookup"><span data-stu-id="c47b0-125">If the region does not support version you specificed, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="c47b0-126">3. példa: Folyamatnaplózás és forgalomelemzés konfigurálása egy megadott NSG-hez</span><span class="sxs-lookup"><span data-stu-id="c47b0-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="c47b0-127">Ebben a példában egy hálózati biztonsági csoport folyamatnaplózási állapotát és forgalomelemzését konfiguráljuk.</span><span class="sxs-lookup"><span data-stu-id="c47b0-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="c47b0-128">A válaszban azt látjuk, hogy a megadott NSG-nek engedélyezve van a folyamatnaplózása, engedélyezve van a Forgalomelemzés, az alapértelmezett formátum, és nincs beállítva adatmegőrzési házirend.</span><span class="sxs-lookup"><span data-stu-id="c47b0-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

## <span data-ttu-id="c47b0-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c47b0-129">PARAMETERS</span></span>

### <span data-ttu-id="c47b0-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c47b0-130">-AsJob</span></span>
<span data-ttu-id="c47b0-131">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c47b0-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c47b0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c47b0-132">-DefaultProfile</span></span>
<span data-ttu-id="c47b0-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c47b0-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c47b0-134">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="c47b0-134">-EnableFlowLog</span></span>
<span data-ttu-id="c47b0-135">Jelölő a folyamatnaplózás engedélyezéséhez/letiltásához.</span><span class="sxs-lookup"><span data-stu-id="c47b0-135">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="c47b0-136">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="c47b0-136">-EnableRetention</span></span>
<span data-ttu-id="c47b0-137">Jelölő a megőrzés engedélyezéséhez/letiltásához.</span><span class="sxs-lookup"><span data-stu-id="c47b0-137">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="c47b0-138">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="c47b0-138">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="c47b0-139">Jelölő a megőrzés engedélyezéséhez/letiltásához.</span><span class="sxs-lookup"><span data-stu-id="c47b0-139">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="c47b0-140">-FormatType</span><span class="sxs-lookup"><span data-stu-id="c47b0-140">-FormatType</span></span>
<span data-ttu-id="c47b0-141">A folyamatnapló formátumának típusa.</span><span class="sxs-lookup"><span data-stu-id="c47b0-141">Type of flow log format.</span></span>

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

### <span data-ttu-id="c47b0-142">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="c47b0-142">-FormatVersion</span></span>
<span data-ttu-id="c47b0-143">A folyamatnapló formátumának verziója.</span><span class="sxs-lookup"><span data-stu-id="c47b0-143">Version of flow log format.</span></span>

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

### <span data-ttu-id="c47b0-144">-Location</span><span class="sxs-lookup"><span data-stu-id="c47b0-144">-Location</span></span>
<span data-ttu-id="c47b0-145">A hálózati figyelő helye.</span><span class="sxs-lookup"><span data-stu-id="c47b0-145">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c47b0-146">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c47b0-146">-NetworkWatcher</span></span>
<span data-ttu-id="c47b0-147">A hálózati figyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="c47b0-147">The network watcher resource.</span></span>

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

### <span data-ttu-id="c47b0-148">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c47b0-148">-NetworkWatcherName</span></span>
<span data-ttu-id="c47b0-149">A hálózati figyelő neve.</span><span class="sxs-lookup"><span data-stu-id="c47b0-149">The name of network watcher.</span></span>

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

### <span data-ttu-id="c47b0-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c47b0-150">-ResourceGroupName</span></span>
<span data-ttu-id="c47b0-151">A hálózatfigyelő erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c47b0-151">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c47b0-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c47b0-152">-RetentionInDays</span></span>
<span data-ttu-id="c47b0-153">A folyamatnaplórekordok megőrzésének napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="c47b0-153">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="c47b0-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c47b0-154">-StorageAccountId</span></span>
<span data-ttu-id="c47b0-155">A folyamatnapló tárolásához használt tárfiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c47b0-155">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="c47b0-156">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c47b0-156">-TargetResourceId</span></span>
<span data-ttu-id="c47b0-157">A célerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c47b0-157">The target resource ID.</span></span>

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

### <span data-ttu-id="c47b0-158">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="c47b0-158">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="c47b0-159">Beállítja vagy beállítja az intervallumot (percben), amely meghatározza, hogy a TA-szolgáltatás milyen gyakran használja a folyamatelemzést.</span><span class="sxs-lookup"><span data-stu-id="c47b0-159">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="c47b0-160">-Workspace</span><span class="sxs-lookup"><span data-stu-id="c47b0-160">-Workspace</span></span>
<span data-ttu-id="c47b0-161">A forgalomelemzési adatok tárolására használt WS-objektum.</span><span class="sxs-lookup"><span data-stu-id="c47b0-161">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="c47b0-162">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="c47b0-162">-WorkspaceGUID</span></span>
<span data-ttu-id="c47b0-163">A forgalomelemzési adatok tárolására használt WS GUID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c47b0-163">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="c47b0-164">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="c47b0-164">-WorkspaceLocation</span></span>
<span data-ttu-id="c47b0-165">A WS Azure-régiója, amely a forgalomelemzési adatok tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="c47b0-165">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="c47b0-166">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="c47b0-166">-WorkspaceResourceId</span></span>
<span data-ttu-id="c47b0-167">A forgalomelemzési adatok tárolására használt WS előfizetése.</span><span class="sxs-lookup"><span data-stu-id="c47b0-167">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="c47b0-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c47b0-168">-Confirm</span></span>
<span data-ttu-id="c47b0-169">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c47b0-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c47b0-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c47b0-170">-WhatIf</span></span>
<span data-ttu-id="c47b0-171">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c47b0-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c47b0-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c47b0-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c47b0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c47b0-173">CommonParameters</span></span>
<span data-ttu-id="c47b0-174">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c47b0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c47b0-175">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c47b0-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c47b0-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c47b0-176">INPUTS</span></span>

### <span data-ttu-id="c47b0-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c47b0-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c47b0-178">System.String</span><span class="sxs-lookup"><span data-stu-id="c47b0-178">System.String</span></span>

### <span data-ttu-id="c47b0-179">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c47b0-179">System.Boolean</span></span>

### <span data-ttu-id="c47b0-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c47b0-180">System.Int32</span></span>

### <span data-ttu-id="c47b0-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c47b0-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c47b0-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="c47b0-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="c47b0-183">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c47b0-183">OUTPUTS</span></span>

### <span data-ttu-id="c47b0-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="c47b0-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="c47b0-185">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c47b0-185">NOTES</span></span>
<span data-ttu-id="c47b0-186">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, hálózat, hálózatkezelés, figyelő, folyamat, naplók, folyamatábra, naplózás</span><span class="sxs-lookup"><span data-stu-id="c47b0-186">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="c47b0-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c47b0-187">RELATED LINKS</span></span>

[<span data-ttu-id="c47b0-188">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c47b0-188">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c47b0-189">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c47b0-189">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c47b0-190">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c47b0-190">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c47b0-191">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c47b0-191">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c47b0-192">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c47b0-192">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c47b0-193">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c47b0-193">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c47b0-194">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c47b0-194">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c47b0-195">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c47b0-195">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c47b0-196">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c47b0-196">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c47b0-197">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c47b0-197">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c47b0-198">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c47b0-198">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c47b0-199">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c47b0-199">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c47b0-200">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c47b0-200">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c47b0-201">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c47b0-201">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c47b0-202">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c47b0-202">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c47b0-203">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c47b0-203">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c47b0-204">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c47b0-204">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c47b0-205">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c47b0-205">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c47b0-206">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c47b0-206">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c47b0-207">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c47b0-207">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c47b0-208">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c47b0-208">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c47b0-209">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c47b0-209">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c47b0-210">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c47b0-210">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c47b0-211">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c47b0-211">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c47b0-212">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c47b0-212">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c47b0-213">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c47b0-213">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c47b0-214">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c47b0-214">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
