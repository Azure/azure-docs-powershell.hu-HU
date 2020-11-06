---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 20d59fb2a112b32c95b380c114ebc1b365569235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494028"
---
# <span data-ttu-id="6e350-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6e350-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="6e350-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e350-102">SYNOPSIS</span></span>
<span data-ttu-id="6e350-103">Beállítja a folyamatábra erőforrás-naplózását.</span><span class="sxs-lookup"><span data-stu-id="6e350-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e350-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e350-104">SYNTAX</span></span>

### <span data-ttu-id="6e350-105">SetFlowlogByResourceWithoutTA (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e350-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e350-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="6e350-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e350-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="6e350-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String> -WorkspaceGUID <String>
 -WorkspaceLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e350-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="6e350-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e350-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="6e350-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e350-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="6e350-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e350-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="6e350-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e350-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="6e350-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-EnableTrafficAnalytics] -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e350-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="6e350-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e350-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e350-114">DESCRIPTION</span></span>
<span data-ttu-id="6e350-115">A Set-AzureRmNetworkWatcherConfigFlowLog beállítja a cél erőforráshoz tartozó folyamatábra naplózását.</span><span class="sxs-lookup"><span data-stu-id="6e350-115">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="6e350-116">A megadható tulajdonságok: az adott erőforrásra vonatkozóan engedélyezve van-e a forgalom naplózása, a konfigurált tárterület-fiók a naplók küldéséhez és a naplók adatmegőrzési házirendjéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="6e350-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="6e350-117">Jelenleg hálózati biztonsági csoportok támogatottak a forgalom naplózásához.</span><span class="sxs-lookup"><span data-stu-id="6e350-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="6e350-118">Példák</span><span class="sxs-lookup"><span data-stu-id="6e350-118">EXAMPLES</span></span>

### <span data-ttu-id="6e350-119">Példa 1: a forgalom naplózásának beállítása megadott NSG</span><span class="sxs-lookup"><span data-stu-id="6e350-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="6e350-120">Ebben a példában a naplózási állapotot egy hálózati biztonsági csoporthoz konfiguráltuk.</span><span class="sxs-lookup"><span data-stu-id="6e350-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="6e350-121">A válaszban láthatja, hogy a megadott NSG engedélyezve van a forgalom naplózása, és nincs adatmegőrzési házirend beállítva.</span><span class="sxs-lookup"><span data-stu-id="6e350-121">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

### <span data-ttu-id="6e350-122">2. példa: a forgalmi naplózás és a forgalmi elemzés beállítása egy megadott NSG</span><span class="sxs-lookup"><span data-stu-id="6e350-122">Example 2: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzureRmOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName"
            }
          }
```

<span data-ttu-id="6e350-123">Ebben a példában a folyamat naplózási állapotát és a forgalmi elemzést egy hálózati biztonsági csoporthoz konfiguráltuk.</span><span class="sxs-lookup"><span data-stu-id="6e350-123">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="6e350-124">A válaszban láthatja, hogy a megadott NSG a forgalom naplózása és a forgalmi statisztika engedélyezve van, és nincs adatmegőrzési házirend beállítva.</span><span class="sxs-lookup"><span data-stu-id="6e350-124">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, and no retention policy set.</span></span>

## <span data-ttu-id="6e350-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e350-125">PARAMETERS</span></span>

### <span data-ttu-id="6e350-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e350-126">-AsJob</span></span>
<span data-ttu-id="6e350-127">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6e350-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e350-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e350-128">-DefaultProfile</span></span>
<span data-ttu-id="6e350-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e350-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e350-130">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="6e350-130">-EnableFlowLog</span></span>
<span data-ttu-id="6e350-131">A forgalom naplózásának engedélyezésére/letiltására szolgáló jelölő</span><span class="sxs-lookup"><span data-stu-id="6e350-131">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="6e350-132">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="6e350-132">-EnableRetention</span></span>
<span data-ttu-id="6e350-133">Jelölő az adatmegőrzés engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="6e350-133">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="6e350-134">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="6e350-134">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="6e350-135">Jelölő az adatmegőrzés engedélyezéséhez vagy letiltásához.</span><span class="sxs-lookup"><span data-stu-id="6e350-135">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="6e350-136">-Hely</span><span class="sxs-lookup"><span data-stu-id="6e350-136">-Location</span></span>
<span data-ttu-id="6e350-137">A Hálózatfigyelő helye.</span><span class="sxs-lookup"><span data-stu-id="6e350-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6e350-138">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e350-138">-NetworkWatcher</span></span>
<span data-ttu-id="6e350-139">A Hálózatfigyelő erőforrás.</span><span class="sxs-lookup"><span data-stu-id="6e350-139">The network watcher resource.</span></span>

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

### <span data-ttu-id="6e350-140">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6e350-140">-NetworkWatcherName</span></span>
<span data-ttu-id="6e350-141">A Network Watcher neve.</span><span class="sxs-lookup"><span data-stu-id="6e350-141">The name of network watcher.</span></span>

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

### <span data-ttu-id="6e350-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e350-142">-ResourceGroupName</span></span>
<span data-ttu-id="6e350-143">A Network Watcher erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6e350-143">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6e350-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6e350-144">-RetentionInDays</span></span>
<span data-ttu-id="6e350-145">A átfolyási napló rekordjainak megtartására szolgáló napok száma.</span><span class="sxs-lookup"><span data-stu-id="6e350-145">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="6e350-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6e350-146">-StorageAccountId</span></span>
<span data-ttu-id="6e350-147">Annak a tárolási fióknak az azonosítója, amely a folyamatábra tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="6e350-147">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="6e350-148">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6e350-148">-TargetResourceId</span></span>
<span data-ttu-id="6e350-149">A cél erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6e350-149">The target resource ID.</span></span>

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

### <span data-ttu-id="6e350-150">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="6e350-150">-Workspace</span></span>
<span data-ttu-id="6e350-151">Az a WS objektum, amely a forgalmi statisztika adatainak tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="6e350-151">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="6e350-152">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="6e350-152">-WorkspaceGUID</span></span>
<span data-ttu-id="6e350-153">Annak a WS-nek a GUID-azonosítója, amely a forgalmi statisztika adatainak tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="6e350-153">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="6e350-154">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="6e350-154">-WorkspaceLocation</span></span>
<span data-ttu-id="6e350-155">A WS Azure-területe, amely a forgalmi statisztika adatainak tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="6e350-155">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="6e350-156">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="6e350-156">-WorkspaceResourceId</span></span>
<span data-ttu-id="6e350-157">A forgalom-elemzési adatokat tároló WS előfizetése.</span><span class="sxs-lookup"><span data-stu-id="6e350-157">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="6e350-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e350-158">-Confirm</span></span>
<span data-ttu-id="6e350-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e350-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e350-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e350-160">-WhatIf</span></span>
<span data-ttu-id="6e350-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6e350-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e350-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e350-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e350-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e350-163">CommonParameters</span></span>
<span data-ttu-id="6e350-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e350-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e350-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e350-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e350-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e350-166">INPUTS</span></span>

### <span data-ttu-id="6e350-167">Microsoft. Azure. commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e350-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6e350-168">Paraméterek: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e350-168">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="6e350-169">System. String</span><span class="sxs-lookup"><span data-stu-id="6e350-169">System.String</span></span>
<span data-ttu-id="6e350-170">Paraméterek: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e350-170">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="6e350-171">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e350-171">System.Boolean</span></span>

### <span data-ttu-id="6e350-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6e350-172">System.Int32</span></span>

### <span data-ttu-id="6e350-173">Microsoft. Azure. Management. internal. Network. Common. IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="6e350-173">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="6e350-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e350-174">OUTPUTS</span></span>

### <span data-ttu-id="6e350-175">Microsoft. Azure. commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="6e350-175">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="6e350-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e350-176">NOTES</span></span>
<span data-ttu-id="6e350-177">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat, figyelő, flow, naplók, flowlog, naplózás</span><span class="sxs-lookup"><span data-stu-id="6e350-177">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="6e350-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e350-178">RELATED LINKS</span></span>

[<span data-ttu-id="6e350-179">Új – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e350-179">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6e350-180">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e350-180">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6e350-181">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6e350-181">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6e350-182">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6e350-182">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6e350-183">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6e350-183">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6e350-184">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6e350-184">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6e350-185">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6e350-185">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6e350-186">Új – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e350-186">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6e350-187">Új – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6e350-187">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="6e350-188">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e350-188">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6e350-189">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e350-189">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6e350-190">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e350-190">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6e350-191">Új – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e350-191">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6e350-192">Teszt-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6e350-192">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6e350-193">Teszt-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6e350-193">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="6e350-194">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6e350-194">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6e350-195">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6e350-195">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6e350-196">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6e350-196">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6e350-197">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6e350-197">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6e350-198">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6e350-198">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6e350-199">Új – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6e350-199">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6e350-200">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6e350-200">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6e350-201">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6e350-201">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6e350-202">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6e350-202">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6e350-203">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6e350-203">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6e350-204">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6e350-204">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="6e350-205">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6e350-205">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
