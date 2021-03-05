---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 94a0764b61b32ce55ff4d9aca06a22d67b1edc96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008982"
---
# <span data-ttu-id="287b4-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="287b4-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="287b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="287b4-102">SYNOPSIS</span></span>
<span data-ttu-id="287b4-103">Adatkapcsolat frissítése.</span><span class="sxs-lookup"><span data-stu-id="287b4-103">Updates a data connection.</span></span>

## <span data-ttu-id="287b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="287b4-104">SYNTAX</span></span>

### <span data-ttu-id="287b4-105">UpdateExpandedEventHub (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="287b4-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="287b4-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="287b4-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="287b4-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="287b4-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="287b4-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="287b4-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="287b4-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="287b4-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="287b4-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="287b4-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="287b4-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="287b4-111">DESCRIPTION</span></span>
<span data-ttu-id="287b4-112">Adatkapcsolat frissítése.</span><span class="sxs-lookup"><span data-stu-id="287b4-112">Updates a data connection.</span></span>

## <span data-ttu-id="287b4-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="287b4-113">EXAMPLES</span></span>

### <span data-ttu-id="287b4-114">1. példa: Meglévő EventHub-adatkapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="287b4-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="287b4-115">A fenti parancs frissíti a "mykustodatabase" adatbázis "mykventhubdc" nevű meglévő EventHub-adatkapcsolatát a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="287b4-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="287b4-116">2. példa: Meglévő EventGrid-adatkapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="287b4-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="287b4-117">A fenti parancs frissíti a "mykustodatabase" nevű adatbázis "myeventgriddc" nevű EventGrid-adatkapcsolatát a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="287b4-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="287b4-118">3. példa: Meglévő IotHub-adatkapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="287b4-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="287b4-119">A fenti parancs frissíti a "mykustodatabase" adatbázis "mykustodatabase" nevű meglévő IotHub-adatkapcsolatát a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="287b4-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="287b4-120">4. példa: Meglévő EventHub-adatkapcsolat frissítése identitáson keresztül</span><span class="sxs-lookup"><span data-stu-id="287b4-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="287b4-121">A fenti parancs frissíti a "mykustodatabase" adatbázis "mykventhubdc" nevű meglévő EventHub-adatkapcsolatát a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="287b4-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="287b4-122">5. példa: Meglévő EventGrid-adatkapcsolat frissítése identitáson keresztül</span><span class="sxs-lookup"><span data-stu-id="287b4-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="287b4-123">A fenti parancs frissíti a "mykustodatabase" nevű adatbázis "myeventgriddc" nevű EventGrid-adatkapcsolatát a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="287b4-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="287b4-124">6. példa: Meglévő IotHub-adatkapcsolat frissítése identitáson keresztül</span><span class="sxs-lookup"><span data-stu-id="287b4-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="287b4-125">A fenti parancs frissíti a "mykustodatabase" adatbázis "mykustodatabase" nevű meglévő IotHub-adatkapcsolatát a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="287b4-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="287b4-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="287b4-126">PARAMETERS</span></span>

### <span data-ttu-id="287b4-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="287b4-127">-AsJob</span></span>
<span data-ttu-id="287b4-128">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="287b4-128">Run the command as a job</span></span>

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

### <span data-ttu-id="287b4-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="287b4-129">-BlobStorageEventType</span></span>
<span data-ttu-id="287b4-130">A feldolgozni használt blobtároló eseménytípus neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-130">The name of blob storage event type to process.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.BlobStorageEventType
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-131">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="287b4-131">-ClusterName</span></span>
<span data-ttu-id="287b4-132">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="287b4-133">-Compression</span></span>
<span data-ttu-id="287b4-134">Az eseményközpont üzenettömörítési típusa.</span><span class="sxs-lookup"><span data-stu-id="287b4-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: UpdateExpandedEventHub, UpdateViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="287b4-135">-ConsumerGroup</span></span>
<span data-ttu-id="287b4-136">Az esemény/iot hub fogyasztói csoportja.</span><span class="sxs-lookup"><span data-stu-id="287b4-136">The event/iot hub consumer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="287b4-137">-DatabaseName</span></span>
<span data-ttu-id="287b4-138">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="287b4-139">-DataFormat</span></span>
<span data-ttu-id="287b4-140">Az üzenet adatformátuma.</span><span class="sxs-lookup"><span data-stu-id="287b4-140">The data format of the message.</span></span>
<span data-ttu-id="287b4-141">Szükség esetén az adatformátum hozzáadható az egyes üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="287b4-141">Optionally the data format can be added to each message.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EventGridDataFormat
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287b4-142">-DefaultProfile</span></span>
<span data-ttu-id="287b4-143">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="287b4-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="287b4-144">-EventHubResourceId</span></span>
<span data-ttu-id="287b4-145">Az eseményközpontnak az adatkapcsolat/eseményrács létrehozásához használt erőforrás-azonosítója úgy van konfigurálva, hogy eseményeket küldjön.</span><span class="sxs-lookup"><span data-stu-id="287b4-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="287b4-146">-EventSystemProperty</span></span>
<span data-ttu-id="287b4-147">Az esemény/iot-központ rendszertulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="287b4-147">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpandedEventHub, UpdateExpandedIotHub, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="287b4-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="287b4-149">Ha igaz érték van beállítva, az azt jelenti, hogy a be nem figyelmének minden fájl első rekordját figyelmen kívül kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="287b4-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="287b4-150">-InputObject</span></span>
<span data-ttu-id="287b4-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="287b4-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpandedEventGrid, UpdateViaIdentityExpandedEventHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="287b4-152">-IotHubResourceId</span></span>
<span data-ttu-id="287b4-153">Az Iot-központ adatkapcsolat létrehozásához használt erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="287b4-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-154">-Kind</span><span class="sxs-lookup"><span data-stu-id="287b4-154">-Kind</span></span>
<span data-ttu-id="287b4-155">Az adatkapcsolat végpontjának fajtája</span><span class="sxs-lookup"><span data-stu-id="287b4-155">Kind of the endpoint for the data connection</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-156">-Location</span><span class="sxs-lookup"><span data-stu-id="287b4-156">-Location</span></span>
<span data-ttu-id="287b4-157">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="287b4-157">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="287b4-158">-MappingRuleName</span></span>
<span data-ttu-id="287b4-159">Az adatok kiosztására használt megfeleltetési szabály.</span><span class="sxs-lookup"><span data-stu-id="287b4-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="287b4-160">Szükség esetén a megfeleltetési adatok hozzáadhatóak az egyes üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="287b4-160">Optionally the mapping information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-161">-Name</span><span class="sxs-lookup"><span data-stu-id="287b4-161">-Name</span></span>
<span data-ttu-id="287b4-162">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-162">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-163">-NoWait</span><span class="sxs-lookup"><span data-stu-id="287b4-163">-NoWait</span></span>
<span data-ttu-id="287b4-164">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="287b4-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="287b4-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="287b4-165">-ResourceGroupName</span></span>
<span data-ttu-id="287b4-166">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-166">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="287b4-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="287b4-168">A megosztási hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-168">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedIotHub, UpdateViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="287b4-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="287b4-170">Annak a tárfióknak az erőforrás-azonosítója, amelyben az adatok találhatók.</span><span class="sxs-lookup"><span data-stu-id="287b4-170">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="287b4-171">-SubscriptionId</span></span>
<span data-ttu-id="287b4-172">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="287b4-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="287b4-173">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="287b4-173">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpandedEventGrid, UpdateExpandedEventHub, UpdateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-174">-TableName</span><span class="sxs-lookup"><span data-stu-id="287b4-174">-TableName</span></span>
<span data-ttu-id="287b4-175">Az a tábla, amelyben az adatokat meg kell ennünk.</span><span class="sxs-lookup"><span data-stu-id="287b4-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="287b4-176">Szükség esetén a táblázat adatai hozzáadhatóak az egyes üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="287b4-176">Optionally the table information can be added to each message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287b4-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="287b4-177">-Confirm</span></span>
<span data-ttu-id="287b4-178">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="287b4-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="287b4-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="287b4-179">-WhatIf</span></span>
<span data-ttu-id="287b4-180">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="287b4-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="287b4-181">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="287b4-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="287b4-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287b4-182">CommonParameters</span></span>
<span data-ttu-id="287b4-183">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="287b4-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287b4-184">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="287b4-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287b4-185">INPUTS</span><span class="sxs-lookup"><span data-stu-id="287b4-185">INPUTS</span></span>

### <span data-ttu-id="287b4-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="287b4-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="287b4-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="287b4-187">OUTPUTS</span></span>

### <span data-ttu-id="287b4-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="287b4-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="287b4-189">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="287b4-189">NOTES</span></span>

<span data-ttu-id="287b4-190">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="287b4-190">ALIASES</span></span>

<span data-ttu-id="287b4-191">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="287b4-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="287b4-192">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="287b4-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="287b4-193">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="287b4-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="287b4-194">INPUTOBJECT: <IKustoIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="287b4-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="287b4-195">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="287b4-196">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="287b4-197">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="287b4-198">`[DatabaseName <String>]`: A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="287b4-199">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="287b4-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="287b4-200">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="287b4-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="287b4-201">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="287b4-202">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="287b4-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="287b4-203">`[SubscriptionId <String>]`: Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="287b4-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="287b4-204">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="287b4-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="287b4-205">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="287b4-205">RELATED LINKS</span></span>

