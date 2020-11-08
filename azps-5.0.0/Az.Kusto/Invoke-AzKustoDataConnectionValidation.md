---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodataconnectionvalidation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDataConnectionValidation.md
ms.openlocfilehash: 9eb3ff31873b23fc97f53fffecdbbb38367ac2b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194715"
---
# <span data-ttu-id="70f9f-101">Invoke-AzKustoDataConnectionValidation</span><span class="sxs-lookup"><span data-stu-id="70f9f-101">Invoke-AzKustoDataConnectionValidation</span></span>

## <span data-ttu-id="70f9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="70f9f-103">Ellenőrzi, hogy az adatkapcsolati paraméterek érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="70f9f-103">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="70f9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70f9f-104">SYNTAX</span></span>

### <span data-ttu-id="70f9f-105">DataExpandedEventHub (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70f9f-105">DataExpandedEventHub (Default)</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70f9f-106">DataExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="70f9f-106">DataExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -EventHubResourceId <String>
 -Kind <Kind> -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70f9f-107">DataExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="70f9f-107">DataExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -DataConnectionName <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70f9f-108">DataViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="70f9f-108">DataViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 -StorageAccountResourceId <String> [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70f9f-109">DataViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="70f9f-109">DataViaIdentityExpandedEventHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -EventHubResourceId <String> -Kind <Kind> -Location <String>
 [-Compression <Compression>] [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="70f9f-110">DataViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="70f9f-110">DataViaIdentityExpandedIotHub</span></span>
```
Invoke-AzKustoDataConnectionValidation -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -DataConnectionName <String> -IotHubResourceId <String> -Kind <Kind> -Location <String>
 -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="70f9f-111">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="70f9f-111">UpdateExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70f9f-112">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="70f9f-112">UpdateViaIdentityExpandedEventGrid</span></span>
```
Invoke-AzKustoDataConnectionValidation -ConsumerGroup <String> -DataConnectionName <String> -Kind <Kind>
 -Location <String> [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="70f9f-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="70f9f-113">DESCRIPTION</span></span>
<span data-ttu-id="70f9f-114">Ellenőrzi, hogy az adatkapcsolati paraméterek érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="70f9f-114">Checks that the data connection parameters are valid.</span></span>

## <span data-ttu-id="70f9f-115">Példák</span><span class="sxs-lookup"><span data-stu-id="70f9f-115">EXAMPLES</span></span>

### <span data-ttu-id="70f9f-116">Példa 1: a EventHub-adatkapcsolat paramétereinek érvényesítése</span><span class="sxs-lookup"><span data-stu-id="70f9f-116">Example 1: Validate EventHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="70f9f-117">A fenti parancs ellenőrzi a "myeventhubdc" nevű EventHub-adatkapcsolatot az "mykustodatabase" nevű adatbázis "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="70f9f-117">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="70f9f-118">2. példa: az EventGrid-adatkapcsolat paramétereinek érvényesítése</span><span class="sxs-lookup"><span data-stu-id="70f9f-118">Example 2: Validate EventGrid data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="70f9f-119">A fenti parancs ellenőrzi a "myeventgriddc" nevű EventGrid-adatkapcsolatot az "mykustodatabase" nevű adatbázis "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="70f9f-119">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="70f9f-120">3. példa: az IotHub-adatkapcsolat paramétereinek érvényesítése</span><span class="sxs-lookup"><span data-stu-id="70f9f-120">Example 3: Validate IotHub data connection parameters</span></span>
```powershell
PS C:\> Invoke-AzKustoDataConnectionValidation -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="70f9f-121">A fenti parancs ellenőrzi a "myiothubdc" nevű IotHub-adatkapcsolatot az "mykustodatabase" nevű adatbázis "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="70f9f-121">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="70f9f-122">4. példa: EventHub-adatkapcsolat paramétereinek érvényesítése identitás útján</span><span class="sxs-lookup"><span data-stu-id="70f9f-122">Example 4: Validate EventHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventhubdc" -Location "East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="70f9f-123">A fenti parancs ellenőrzi a "myeventhubdc" nevű EventHub-adatkapcsolatot az "mykustodatabase" nevű adatbázis "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="70f9f-123">The above command validates EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="70f9f-124">Példa 5: az EventGrid-adatkapcsolat paramétereinek érvényesítése identitás útján</span><span class="sxs-lookup"><span data-stu-id="70f9f-124">Example 5: Validate EventGrid data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myeventgriddc" -Location "East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="70f9f-125">A fenti parancs ellenőrzi a "myeventgriddc" nevű EventGrid-adatkapcsolatot az "mykustodatabase" nevű adatbázis "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="70f9f-125">The above command validates EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="70f9f-126">6. példa: IotHub-adatkapcsolat paramétereinek érvényesítése identitás útján</span><span class="sxs-lookup"><span data-stu-id="70f9f-126">Example 6: Validate IotHub data connection parameters via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" 
PS C:\> Invoke-AzKustoDataConnectionValidation -InputObject $database -DataConnectionName "myiothubdc" -Location "East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

ErrorMessage
------------
event hub resource id and consumer group tuple provided are already used
```

<span data-ttu-id="70f9f-127">A fenti parancs ellenőrzi a "myiothubdc" nevű IotHub-adatkapcsolatot az "mykustodatabase" nevű adatbázis "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="70f9f-127">The above command validates IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="70f9f-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70f9f-128">PARAMETERS</span></span>

### <span data-ttu-id="70f9f-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="70f9f-129">-BlobStorageEventType</span></span>
<span data-ttu-id="70f9f-130">A feldolgozni kívánt blob-tárolási esemény neve.</span><span class="sxs-lookup"><span data-stu-id="70f9f-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="70f9f-131">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="70f9f-131">-ClusterName</span></span>
<span data-ttu-id="70f9f-132">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="70f9f-132">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-133">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="70f9f-133">-Compression</span></span>
<span data-ttu-id="70f9f-134">Az esemény hub-üzenetek tömörítési típusa.</span><span class="sxs-lookup"><span data-stu-id="70f9f-134">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: DataExpandedEventHub, DataViaIdentityExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="70f9f-135">-ConsumerGroup</span></span>
<span data-ttu-id="70f9f-136">Az esemény/IOT hub fogyasztói csoport.</span><span class="sxs-lookup"><span data-stu-id="70f9f-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="70f9f-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70f9f-137">-DatabaseName</span></span>
<span data-ttu-id="70f9f-138">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="70f9f-138">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-139">-DataConnectionName</span><span class="sxs-lookup"><span data-stu-id="70f9f-139">-DataConnectionName</span></span>
<span data-ttu-id="70f9f-140">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="70f9f-140">The name of the data connection.</span></span>

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

### <span data-ttu-id="70f9f-141">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="70f9f-141">-DataFormat</span></span>
<span data-ttu-id="70f9f-142">Az üzenet adatformátuma.</span><span class="sxs-lookup"><span data-stu-id="70f9f-142">The data format of the message.</span></span>
<span data-ttu-id="70f9f-143">Tetszés szerint minden üzenethez hozzáadhat adatformátumot.</span><span class="sxs-lookup"><span data-stu-id="70f9f-143">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="70f9f-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f9f-144">-DefaultProfile</span></span>
<span data-ttu-id="70f9f-145">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70f9f-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70f9f-146">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="70f9f-146">-EventHubResourceId</span></span>
<span data-ttu-id="70f9f-147">Az adatkapcsolat/esemény rácsának létrehozásához használt esemény hub erőforrás-azonosítója az események küldésére van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="70f9f-147">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-148">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="70f9f-148">-EventSystemProperty</span></span>
<span data-ttu-id="70f9f-149">Az esemény/IOT hub rendszertulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="70f9f-149">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DataExpandedEventHub, DataExpandedIotHub, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-150">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="70f9f-150">-IgnoreFirstRecord</span></span>
<span data-ttu-id="70f9f-151">Ha a True értékre van állítva, akkor az azt jelzi, hogy a lenyelési érték minden fájl első rekordját figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="70f9f-151">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="70f9f-152">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70f9f-152">-InputObject</span></span>
<span data-ttu-id="70f9f-153">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70f9f-153">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DataViaIdentityExpandedEventGrid, DataViaIdentityExpandedEventHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-154">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="70f9f-154">-IotHubResourceId</span></span>
<span data-ttu-id="70f9f-155">Az IOT-központ erőforrás-azonosítója, amellyel adatkapcsolat hozható létre.</span><span class="sxs-lookup"><span data-stu-id="70f9f-155">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-156">-Kind</span><span class="sxs-lookup"><span data-stu-id="70f9f-156">-Kind</span></span>
<span data-ttu-id="70f9f-157">Az adatkapcsolat végpontjának típusa</span><span class="sxs-lookup"><span data-stu-id="70f9f-157">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="70f9f-158">-Hely</span><span class="sxs-lookup"><span data-stu-id="70f9f-158">-Location</span></span>
<span data-ttu-id="70f9f-159">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="70f9f-159">Resource location.</span></span>

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

### <span data-ttu-id="70f9f-160">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="70f9f-160">-MappingRuleName</span></span>
<span data-ttu-id="70f9f-161">Az adatvesztéshez használandó megfeleltetési szabály.</span><span class="sxs-lookup"><span data-stu-id="70f9f-161">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="70f9f-162">Tetszés szerint a megfeleltetési adatok mindegyik üzenethez hozzáadhatók.</span><span class="sxs-lookup"><span data-stu-id="70f9f-162">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="70f9f-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f9f-163">-ResourceGroupName</span></span>
<span data-ttu-id="70f9f-164">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="70f9f-164">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-165">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="70f9f-165">-SharedAccessPolicyName</span></span>
<span data-ttu-id="70f9f-166">A megosztási hozzáférés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="70f9f-166">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedIotHub, DataViaIdentityExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-167">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="70f9f-167">-StorageAccountResourceId</span></span>
<span data-ttu-id="70f9f-168">Annak a tárolási fióknak az erőforrás-azonosítója, amelyben az adatforgalom található.</span><span class="sxs-lookup"><span data-stu-id="70f9f-168">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataViaIdentityExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-169">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70f9f-169">-SubscriptionId</span></span>
<span data-ttu-id="70f9f-170">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="70f9f-170">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="70f9f-171">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="70f9f-171">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DataExpandedEventGrid, DataExpandedEventHub, DataExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9f-172">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="70f9f-172">-TableName</span></span>
<span data-ttu-id="70f9f-173">Az a táblázat, ahol az adatot el kell fogyasztani.</span><span class="sxs-lookup"><span data-stu-id="70f9f-173">The table where the data should be ingested.</span></span>
<span data-ttu-id="70f9f-174">Tetszés szerint a táblázat adatai hozzáadhatók az egyes üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="70f9f-174">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="70f9f-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70f9f-175">-Confirm</span></span>
<span data-ttu-id="70f9f-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70f9f-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f9f-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f9f-177">-WhatIf</span></span>
<span data-ttu-id="70f9f-178">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70f9f-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70f9f-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70f9f-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70f9f-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f9f-180">CommonParameters</span></span>
<span data-ttu-id="70f9f-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70f9f-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f9f-182">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70f9f-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f9f-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70f9f-183">INPUTS</span></span>

### <span data-ttu-id="70f9f-184">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="70f9f-184">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="70f9f-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70f9f-185">OUTPUTS</span></span>

### <span data-ttu-id="70f9f-186">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDataConnectionValidationResult</span><span class="sxs-lookup"><span data-stu-id="70f9f-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnectionValidationResult</span></span>

## <span data-ttu-id="70f9f-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70f9f-187">NOTES</span></span>

<span data-ttu-id="70f9f-188">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="70f9f-188">ALIASES</span></span>

<span data-ttu-id="70f9f-189">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="70f9f-189">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="70f9f-190">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="70f9f-190">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70f9f-191">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="70f9f-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="70f9f-192">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="70f9f-192">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="70f9f-193">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="70f9f-193">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="70f9f-194">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="70f9f-194">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="70f9f-195">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="70f9f-195">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="70f9f-196">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="70f9f-196">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="70f9f-197">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="70f9f-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="70f9f-198">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="70f9f-198">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="70f9f-199">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="70f9f-199">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="70f9f-200">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="70f9f-200">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="70f9f-201">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="70f9f-201">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="70f9f-202">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="70f9f-202">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="70f9f-203">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70f9f-203">RELATED LINKS</span></span>

