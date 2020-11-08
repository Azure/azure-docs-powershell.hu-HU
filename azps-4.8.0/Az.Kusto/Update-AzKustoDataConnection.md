---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDataConnection.md
ms.openlocfilehash: 70862dee30fd03430d93de88e1e63f0f5acf5e6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184493"
---
# <span data-ttu-id="eca49-101">Update-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="eca49-101">Update-AzKustoDataConnection</span></span>

## <span data-ttu-id="eca49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eca49-102">SYNOPSIS</span></span>
<span data-ttu-id="eca49-103">Frissíti az adatkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="eca49-103">Updates a data connection.</span></span>

## <span data-ttu-id="eca49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eca49-104">SYNTAX</span></span>

### <span data-ttu-id="eca49-105">UpdateExpandedEventHub (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eca49-105">UpdateExpandedEventHub (Default)</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="eca49-106">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="eca49-106">UpdateExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eca49-107">UpdateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="eca49-107">UpdateExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="eca49-108">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="eca49-108">UpdateViaIdentityExpandedEventGrid</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> -StorageAccountResourceId <String>
 [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>] [-IgnoreFirstRecord]
 [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eca49-109">UpdateViaIdentityExpandedEventHub</span><span class="sxs-lookup"><span data-stu-id="eca49-109">UpdateViaIdentityExpandedEventHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String>
 -EventHubResourceId <String> -Kind <Kind> -Location <String> [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="eca49-110">UpdateViaIdentityExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="eca49-110">UpdateViaIdentityExpandedIotHub</span></span>
```
Update-AzKustoDataConnection -InputObject <IKustoIdentity> -ConsumerGroup <String> -IotHubResourceId <String>
 -Kind <Kind> -Location <String> -SharedAccessPolicyName <String> [-DataFormat <EventGridDataFormat>]
 [-EventSystemProperty <String[]>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eca49-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="eca49-111">DESCRIPTION</span></span>
<span data-ttu-id="eca49-112">Frissíti az adatkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="eca49-112">Updates a data connection.</span></span>

## <span data-ttu-id="eca49-113">Példák</span><span class="sxs-lookup"><span data-stu-id="eca49-113">EXAMPLES</span></span>

### <span data-ttu-id="eca49-114">Példa 1: meglévő EventHub-adatkapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="eca49-114">Example 1: Update an existing EventHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eca49-115">A fenti parancs frissíti a "myeventhubdc" nevű "mykustodatabase" nevű adatbázis "" nevű "" nevű adatbázis "testnewkustocluster" nevű "EventHub" nevű adatkapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="eca49-115">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="eca49-116">2. példa: meglévő EventGrid-adatkapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="eca49-116">Example 2: Update an existing EventGrid data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eca49-117">A fenti parancs frissíti a "myeventgriddc" nevű "mykustodatabase" nevű adatbázis "" nevű "" nevű adatbázis "testnewkustocluster" nevű "EventGrid" nevű adatkapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="eca49-117">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="eca49-118">3. példa: meglévő IotHub-adatkapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="eca49-118">Example 3: Update an existing IotHub data connection</span></span>
```powershell
PS C:\> Update-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eca49-119">A fenti parancs frissíti a "myiothubdc" nevű "mykustodatabase" nevű adatbázis "" nevű "" nevű adatbázis "testnewkustocluster" nevű "IotHub" nevű adatkapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="eca49-119">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="eca49-120">Példa 4: meglévő EventHub-adatkapcsolat frissítése identitás útján</span><span class="sxs-lookup"><span data-stu-id="eca49-120">Example 4: Update an existing EventHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eca49-121">A fenti parancs frissíti a "myeventhubdc" nevű "mykustodatabase" nevű adatbázis "" nevű "" nevű adatbázis "testnewkustocluster" nevű "EventHub" nevű adatkapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="eca49-121">The above command updates the existing EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="eca49-122">Példa 5: meglévő EventGrid-adatkapcsolat frissítése identitás útján</span><span class="sxs-lookup"><span data-stu-id="eca49-122">Example 5: Update an existing EventGrid data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eca49-123">A fenti parancs frissíti a "myeventgriddc" nevű "mykustodatabase" nevű adatbázis "" nevű "" nevű adatbázis "testnewkustocluster" nevű "EventGrid" nevű adatkapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="eca49-123">The above command updates the existing EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="eca49-124">Példa 6: meglévő IotHub-adatkapcsolat frissítése identitás útján</span><span class="sxs-lookup"><span data-stu-id="eca49-124">Example 6: Update an existing IotHub data connection via identity</span></span>
```powershell
PS C:\> $dataConnection = Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" 
PS C:\> Update-AzKustoDataConnection -InputObject $dataConnection -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "NewEventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="eca49-125">A fenti parancs frissíti a "myiothubdc" nevű "mykustodatabase" nevű adatbázis "" nevű "" nevű adatbázis "testnewkustocluster" nevű "IotHub" nevű adatkapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="eca49-125">The above command updates the existing IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="eca49-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eca49-126">PARAMETERS</span></span>

### <span data-ttu-id="eca49-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eca49-127">-AsJob</span></span>
<span data-ttu-id="eca49-128">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="eca49-128">Run the command as a job</span></span>

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

### <span data-ttu-id="eca49-129">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="eca49-129">-BlobStorageEventType</span></span>
<span data-ttu-id="eca49-130">A feldolgozni kívánt blob-tárolási esemény neve.</span><span class="sxs-lookup"><span data-stu-id="eca49-130">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="eca49-131">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="eca49-131">-ClusterName</span></span>
<span data-ttu-id="eca49-132">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="eca49-132">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="eca49-133">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="eca49-133">-Compression</span></span>
<span data-ttu-id="eca49-134">Az esemény hub-üzenetek tömörítési típusa.</span><span class="sxs-lookup"><span data-stu-id="eca49-134">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="eca49-135">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="eca49-135">-ConsumerGroup</span></span>
<span data-ttu-id="eca49-136">Az esemény/IOT hub fogyasztói csoport.</span><span class="sxs-lookup"><span data-stu-id="eca49-136">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="eca49-137">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eca49-137">-DatabaseName</span></span>
<span data-ttu-id="eca49-138">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="eca49-138">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="eca49-139">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="eca49-139">-DataFormat</span></span>
<span data-ttu-id="eca49-140">Az üzenet adatformátuma.</span><span class="sxs-lookup"><span data-stu-id="eca49-140">The data format of the message.</span></span>
<span data-ttu-id="eca49-141">Tetszés szerint minden üzenethez hozzáadhat adatformátumot.</span><span class="sxs-lookup"><span data-stu-id="eca49-141">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="eca49-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca49-142">-DefaultProfile</span></span>
<span data-ttu-id="eca49-143">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eca49-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eca49-144">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="eca49-144">-EventHubResourceId</span></span>
<span data-ttu-id="eca49-145">Az adatkapcsolat/esemény rácsának létrehozásához használt esemény hub erőforrás-azonosítója az események küldésére van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="eca49-145">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="eca49-146">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="eca49-146">-EventSystemProperty</span></span>
<span data-ttu-id="eca49-147">Az esemény/IOT hub rendszertulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="eca49-147">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="eca49-148">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="eca49-148">-IgnoreFirstRecord</span></span>
<span data-ttu-id="eca49-149">Ha a True értékre van állítva, akkor az azt jelzi, hogy a lenyelési érték minden fájl első rekordját figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="eca49-149">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="eca49-150">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eca49-150">-InputObject</span></span>
<span data-ttu-id="eca49-151">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eca49-151">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eca49-152">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="eca49-152">-IotHubResourceId</span></span>
<span data-ttu-id="eca49-153">Az IOT-központ erőforrás-azonosítója, amellyel adatkapcsolat hozható létre.</span><span class="sxs-lookup"><span data-stu-id="eca49-153">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="eca49-154">-Kind</span><span class="sxs-lookup"><span data-stu-id="eca49-154">-Kind</span></span>
<span data-ttu-id="eca49-155">Az adatkapcsolat végpontjának típusa</span><span class="sxs-lookup"><span data-stu-id="eca49-155">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="eca49-156">-Hely</span><span class="sxs-lookup"><span data-stu-id="eca49-156">-Location</span></span>
<span data-ttu-id="eca49-157">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="eca49-157">Resource location.</span></span>

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

### <span data-ttu-id="eca49-158">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="eca49-158">-MappingRuleName</span></span>
<span data-ttu-id="eca49-159">Az adatvesztéshez használandó megfeleltetési szabály.</span><span class="sxs-lookup"><span data-stu-id="eca49-159">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="eca49-160">Tetszés szerint a megfeleltetési adatok mindegyik üzenethez hozzáadhatók.</span><span class="sxs-lookup"><span data-stu-id="eca49-160">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="eca49-161">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eca49-161">-Name</span></span>
<span data-ttu-id="eca49-162">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="eca49-162">The name of the data connection.</span></span>

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

### <span data-ttu-id="eca49-163">-Várva</span><span class="sxs-lookup"><span data-stu-id="eca49-163">-NoWait</span></span>
<span data-ttu-id="eca49-164">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="eca49-164">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eca49-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca49-165">-ResourceGroupName</span></span>
<span data-ttu-id="eca49-166">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eca49-166">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="eca49-167">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="eca49-167">-SharedAccessPolicyName</span></span>
<span data-ttu-id="eca49-168">A megosztási hozzáférés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="eca49-168">The name of the share access policy.</span></span>

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

### <span data-ttu-id="eca49-169">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="eca49-169">-StorageAccountResourceId</span></span>
<span data-ttu-id="eca49-170">Annak a tárolási fióknak az erőforrás-azonosítója, amelyben az adatforgalom található.</span><span class="sxs-lookup"><span data-stu-id="eca49-170">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="eca49-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eca49-171">-SubscriptionId</span></span>
<span data-ttu-id="eca49-172">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eca49-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eca49-173">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="eca49-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eca49-174">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="eca49-174">-TableName</span></span>
<span data-ttu-id="eca49-175">Az a táblázat, ahol az adatot el kell fogyasztani.</span><span class="sxs-lookup"><span data-stu-id="eca49-175">The table where the data should be ingested.</span></span>
<span data-ttu-id="eca49-176">Tetszés szerint a táblázat adatai hozzáadhatók az egyes üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="eca49-176">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="eca49-177">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eca49-177">-Confirm</span></span>
<span data-ttu-id="eca49-178">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eca49-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca49-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca49-179">-WhatIf</span></span>
<span data-ttu-id="eca49-180">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eca49-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eca49-181">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eca49-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca49-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca49-182">CommonParameters</span></span>
<span data-ttu-id="eca49-183">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eca49-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca49-184">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eca49-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca49-185">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eca49-185">INPUTS</span></span>

### <span data-ttu-id="eca49-186">Microsoft. Azure. PowerShell. parancsmagok. Kusto. models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="eca49-186">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="eca49-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eca49-187">OUTPUTS</span></span>

### <span data-ttu-id="eca49-188">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="eca49-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="eca49-189">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eca49-189">NOTES</span></span>

<span data-ttu-id="eca49-190">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="eca49-190">ALIASES</span></span>

<span data-ttu-id="eca49-191">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="eca49-191">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eca49-192">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="eca49-192">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eca49-193">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="eca49-193">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eca49-194">INPUTOBJECT <IKustoIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="eca49-194">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eca49-195">`[AttachedDatabaseConfigurationName <String>]`: A csatolt adatbázis-konfiguráció neve.</span><span class="sxs-lookup"><span data-stu-id="eca49-195">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="eca49-196">`[ClusterName <String>]`: A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="eca49-196">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="eca49-197">`[DataConnectionName <String>]`: Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="eca49-197">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="eca49-198">`[DatabaseName <String>]`: Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="eca49-198">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="eca49-199">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="eca49-199">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eca49-200">`[Location <String>]`: Azure-hely.</span><span class="sxs-lookup"><span data-stu-id="eca49-200">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="eca49-201">`[PrincipalAssignmentName <String>]`: A Kusto principalAssignment neve.</span><span class="sxs-lookup"><span data-stu-id="eca49-201">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="eca49-202">`[ResourceGroupName <String>]`: A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eca49-202">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="eca49-203">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eca49-203">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eca49-204">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="eca49-204">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="eca49-205">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eca49-205">RELATED LINKS</span></span>

