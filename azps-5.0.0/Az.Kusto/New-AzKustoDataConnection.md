---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: 4fadb8a48b9886fe1c5a7c916d8f810abd8de6cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194703"
---
# <span data-ttu-id="7e3a6-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="7e3a6-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="7e3a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3a6-103">Adatkapcsolatot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="7e3a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e3a6-104">SYNTAX</span></span>

### <span data-ttu-id="7e3a6-105">CreateExpandedEventHub (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e3a6-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7e3a6-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="7e3a6-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7e3a6-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="7e3a6-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7e3a6-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="7e3a6-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7e3a6-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="7e3a6-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7e3a6-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e3a6-110">DESCRIPTION</span></span>
<span data-ttu-id="7e3a6-111">Adatkapcsolatot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="7e3a6-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7e3a6-112">EXAMPLES</span></span>

### <span data-ttu-id="7e3a6-113">Példa 1: új EventHub-adatkapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="7e3a6-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="7e3a6-114">A fenti parancs új EventHub-adatkapcsolatot hoz létre a "myeventhubdc" nevű adatbázis "mykustodatabase" nevű adatbázisában "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="7e3a6-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="7e3a6-115">2. példa: új EventGrid-adatkapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="7e3a6-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="7e3a6-116">A fenti parancs új EventGrid-adatkapcsolatot hoz létre a "myeventgriddc" nevű adatbázis "mykustodatabase" nevű adatbázisában "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="7e3a6-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="7e3a6-117">3. példa: új IotHub-adatkapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="7e3a6-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="7e3a6-118">A fenti parancs új IotHub-adatkapcsolatot hoz létre a "myiothubdc" nevű adatbázis "mykustodatabase" nevű adatbázisában "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="7e3a6-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="7e3a6-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e3a6-119">PARAMETERS</span></span>

### <span data-ttu-id="7e3a6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e3a6-120">-AsJob</span></span>
<span data-ttu-id="7e3a6-121">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="7e3a6-121">Run the command as a job</span></span>

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

### <span data-ttu-id="7e3a6-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="7e3a6-122">-BlobStorageEventType</span></span>
<span data-ttu-id="7e3a6-123">A feldolgozni kívánt blob-tárolási esemény neve.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-123">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="7e3a6-124">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="7e3a6-124">-ClusterName</span></span>
<span data-ttu-id="7e3a6-125">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7e3a6-126">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="7e3a6-126">-Compression</span></span>
<span data-ttu-id="7e3a6-127">Az esemény hub-üzenetek tömörítési típusa.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-127">The event hub messages compression type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Compression
Parameter Sets: CreateExpandedEventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e3a6-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7e3a6-128">-ConsumerGroup</span></span>
<span data-ttu-id="7e3a6-129">Az esemény/IOT hub fogyasztói csoport.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="7e3a6-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e3a6-130">-DatabaseName</span></span>
<span data-ttu-id="7e3a6-131">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="7e3a6-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="7e3a6-132">-DataFormat</span></span>
<span data-ttu-id="7e3a6-133">Az üzenet adatformátuma.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-133">The data format of the message.</span></span>
<span data-ttu-id="7e3a6-134">Tetszés szerint minden üzenethez hozzáadhat adatformátumot.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-134">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="7e3a6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3a6-135">-DefaultProfile</span></span>
<span data-ttu-id="7e3a6-136">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e3a6-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="7e3a6-137">-EventHubResourceId</span></span>
<span data-ttu-id="7e3a6-138">Az adatkapcsolat/esemény rácsának létrehozásához használt esemény hub erőforrás-azonosítója az események küldésére van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid, CreateExpandedEventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e3a6-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="7e3a6-139">-EventSystemProperty</span></span>
<span data-ttu-id="7e3a6-140">Az esemény/IOT hub rendszertulajdonságai.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-140">System properties of the event/iot hub.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpandedEventHub, CreateExpandedIotHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e3a6-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="7e3a6-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="7e3a6-142">Ha a True értékre van állítva, akkor az azt jelzi, hogy a lenyelési érték minden fájl első rekordját figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="7e3a6-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="7e3a6-143">-IotHubResourceId</span></span>
<span data-ttu-id="7e3a6-144">Az IOT-központ erőforrás-azonosítója, amellyel adatkapcsolat hozható létre.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e3a6-145">-Kind</span><span class="sxs-lookup"><span data-stu-id="7e3a6-145">-Kind</span></span>
<span data-ttu-id="7e3a6-146">Az adatkapcsolat végpontjának típusa</span><span class="sxs-lookup"><span data-stu-id="7e3a6-146">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="7e3a6-147">-Hely</span><span class="sxs-lookup"><span data-stu-id="7e3a6-147">-Location</span></span>
<span data-ttu-id="7e3a6-148">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-148">Resource location.</span></span>

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

### <span data-ttu-id="7e3a6-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="7e3a6-149">-MappingRuleName</span></span>
<span data-ttu-id="7e3a6-150">Az adatvesztéshez használandó megfeleltetési szabály.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="7e3a6-151">Tetszés szerint a megfeleltetési adatok mindegyik üzenethez hozzáadhatók.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="7e3a6-152">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e3a6-152">-Name</span></span>
<span data-ttu-id="7e3a6-153">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-153">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e3a6-154">-Várva</span><span class="sxs-lookup"><span data-stu-id="7e3a6-154">-NoWait</span></span>
<span data-ttu-id="7e3a6-155">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="7e3a6-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7e3a6-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e3a6-156">-ResourceGroupName</span></span>
<span data-ttu-id="7e3a6-157">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7e3a6-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="7e3a6-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="7e3a6-159">A megosztási hozzáférés házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-159">The name of the share access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedIotHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e3a6-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="7e3a6-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="7e3a6-161">Annak a tárolási fióknak az erőforrás-azonosítója, amelyben az adatforgalom található.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-161">The resource ID of the storage account where the data resides.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpandedEventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e3a6-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e3a6-162">-SubscriptionId</span></span>
<span data-ttu-id="7e3a6-163">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7e3a6-164">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-164">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e3a6-165">-Táblanév</span><span class="sxs-lookup"><span data-stu-id="7e3a6-165">-TableName</span></span>
<span data-ttu-id="7e3a6-166">Az a táblázat, ahol az adatot el kell fogyasztani.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="7e3a6-167">Tetszés szerint a táblázat adatai hozzáadhatók az egyes üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="7e3a6-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e3a6-168">-Confirm</span></span>
<span data-ttu-id="7e3a6-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e3a6-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e3a6-170">-WhatIf</span></span>
<span data-ttu-id="7e3a6-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e3a6-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e3a6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3a6-173">CommonParameters</span></span>
<span data-ttu-id="7e3a6-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e3a6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3a6-175">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7e3a6-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3a6-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e3a6-176">INPUTS</span></span>

## <span data-ttu-id="7e3a6-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e3a6-177">OUTPUTS</span></span>

### <span data-ttu-id="7e3a6-178">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="7e3a6-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="7e3a6-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e3a6-179">NOTES</span></span>

<span data-ttu-id="7e3a6-180">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7e3a6-180">ALIASES</span></span>

## <span data-ttu-id="7e3a6-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e3a6-181">RELATED LINKS</span></span>

