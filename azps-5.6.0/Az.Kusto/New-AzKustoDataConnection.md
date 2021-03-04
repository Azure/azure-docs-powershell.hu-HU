---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDataConnection.md
ms.openlocfilehash: e9f221563f3d4d689e075f47a281620bc87d9011
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922378"
---
# <span data-ttu-id="d2a30-101">New-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="d2a30-101">New-AzKustoDataConnection</span></span>

## <span data-ttu-id="d2a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a30-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a30-103">Adatkapcsolat létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="d2a30-103">Creates or updates a data connection.</span></span>

## <span data-ttu-id="d2a30-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2a30-104">SYNTAX</span></span>

### <span data-ttu-id="d2a30-105">CreateExpandedEventHub (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2a30-105">CreateExpandedEventHub (Default)</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-Compression <Compression>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d2a30-106">CreateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="d2a30-106">CreateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -EventHubResourceId <String> -Kind <Kind>
 -Location <String> -StorageAccountResourceId <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-MappingRuleName <String>] [-TableName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2a30-107">CreateExpandedIotHub</span><span class="sxs-lookup"><span data-stu-id="d2a30-107">CreateExpandedIotHub</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -IotHubResourceId <String> -Kind <Kind>
 -Location <String> -SharedAccessPolicyName <String> [-SubscriptionId <String>]
 [-DataFormat <EventGridDataFormat>] [-EventSystemProperty <String[]>] [-MappingRuleName <String>]
 [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d2a30-108">UpdateExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="d2a30-108">UpdateExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2a30-109">UpdateViaIdentityExpandedEventGrid</span><span class="sxs-lookup"><span data-stu-id="d2a30-109">UpdateViaIdentityExpandedEventGrid</span></span>
```
New-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> -ConsumerGroup <String> -Kind <Kind> -Location <String>
 [-SubscriptionId <String>] [-BlobStorageEventType <BlobStorageEventType>] [-DataFormat <EventGridDataFormat>]
 [-IgnoreFirstRecord] [-MappingRuleName <String>] [-TableName <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2a30-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2a30-110">DESCRIPTION</span></span>
<span data-ttu-id="d2a30-111">Adatkapcsolat létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="d2a30-111">Creates or updates a data connection.</span></span>

## <span data-ttu-id="d2a30-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2a30-112">EXAMPLES</span></span>

### <span data-ttu-id="d2a30-113">1. példa: Új EventHub-adatkapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="d2a30-113">Example 1: Create a new EventHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventhubdc" -Location="East US" -Kind "EventHub" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -DataFormat "JSON" -ConsumerGroup '$Default' -Compression "None" -TableName "Events" -MappingRuleName "EventsMapping"

Kind     Location Name                                             Type
----     -------- ----                                             ----
EventHub East US  testnewkustocluster/mykustodatabase/myeventhubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="d2a30-114">A fenti parancs létrehoz egy új EventHub adatkapcsolatot "myeventhubdc" névvel a "mykustodatabase" adatbázishoz a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="d2a30-114">The above command creates a new EventHub data connection named "myeventhubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d2a30-115">2. példa: Új EventGrid-adatkapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="d2a30-115">Example 2: Create a new EventGrid data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myeventgriddc" -Location="East US" -Kind "EventGrid" -EventHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.EventHub/namespaces/myeventhubns/eventhubs/myeventhub" -StorageAccountResourceId $storageAccountResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Storage/storageAccounts/mystorage" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping" -IgnoreFirstRecord "false" -BlobStorageEventType "Microsoft.Storage.BlobRenamed"

Kind      Location Name                                              Type
----      -------- ----                                              ----
EventGrid East US  testnewkustocluster/mykustodatabase/myeventgriddc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="d2a30-116">A fenti parancs létrehoz egy új EventGrid-adatkapcsolatot "myeventgriddc" névvel a "mykustodatabase" adatbázishoz a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="d2a30-116">The above command creates a new EventGrid data connection named "myeventgriddc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="d2a30-117">3. példa: Új IotHub-adatkapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="d2a30-117">Example 3: Create a new IotHub data connection</span></span>
```powershell
PS C:\> New-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "myiothubdc" -Location="East US" -Kind "IotHub" -IotHubResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Devices/IotHubs/myiothub" -SharedAccessPolicyName "myiothubpolicy" -DataFormat "JSON" -ConsumerGroup '$Default' -TableName "Events" -MappingRuleName "EventsMapping"

Kind      Location Name                                        Type
----      -------- ----                                        ----
IotHub East US  testnewkustocluster/mykustodatabase/myiothubdc Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="d2a30-118">A fenti parancs létrehoz egy új IotHub adatkapcsolatot "myiothubdc" névvel a "mykustodatabase" adatbázishoz a "testnewkustocluster" fürtben.</span><span class="sxs-lookup"><span data-stu-id="d2a30-118">The above command creates a new IotHub data connection named "myiothubdc" for the database "mykustodatabase" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="d2a30-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2a30-119">PARAMETERS</span></span>

### <span data-ttu-id="d2a30-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2a30-120">-AsJob</span></span>
<span data-ttu-id="d2a30-121">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="d2a30-121">Run the command as a job</span></span>

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

### <span data-ttu-id="d2a30-122">-BlobStorageEventType</span><span class="sxs-lookup"><span data-stu-id="d2a30-122">-BlobStorageEventType</span></span>
<span data-ttu-id="d2a30-123">A feldolgozni használt blobtároló eseménytípus neve.</span><span class="sxs-lookup"><span data-stu-id="d2a30-123">The name of blob storage event type to process.</span></span>

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

### <span data-ttu-id="d2a30-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d2a30-124">-ClusterName</span></span>
<span data-ttu-id="d2a30-125">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d2a30-125">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d2a30-126">-Compression</span><span class="sxs-lookup"><span data-stu-id="d2a30-126">-Compression</span></span>
<span data-ttu-id="d2a30-127">Az eseményközpont üzenettömörítési típusa.</span><span class="sxs-lookup"><span data-stu-id="d2a30-127">The event hub messages compression type.</span></span>

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

### <span data-ttu-id="d2a30-128">-ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d2a30-128">-ConsumerGroup</span></span>
<span data-ttu-id="d2a30-129">Az esemény/iot hub fogyasztói csoportja.</span><span class="sxs-lookup"><span data-stu-id="d2a30-129">The event/iot hub consumer group.</span></span>

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

### <span data-ttu-id="d2a30-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d2a30-130">-DatabaseName</span></span>
<span data-ttu-id="d2a30-131">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d2a30-131">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d2a30-132">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="d2a30-132">-DataFormat</span></span>
<span data-ttu-id="d2a30-133">Az üzenet adatformátuma.</span><span class="sxs-lookup"><span data-stu-id="d2a30-133">The data format of the message.</span></span>
<span data-ttu-id="d2a30-134">Szükség esetén az adatformátum hozzáadható az egyes üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="d2a30-134">Optionally the data format can be added to each message.</span></span>

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

### <span data-ttu-id="d2a30-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a30-135">-DefaultProfile</span></span>
<span data-ttu-id="d2a30-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2a30-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2a30-137">-EventHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a30-137">-EventHubResourceId</span></span>
<span data-ttu-id="d2a30-138">Az eseményközpontnak az adatkapcsolat/eseményrács létrehozásához használt erőforrás-azonosítója úgy van konfigurálva, hogy eseményeket küldjön.</span><span class="sxs-lookup"><span data-stu-id="d2a30-138">The resource ID of the event hub to be used to create a data connection / event grid is configured to send events.</span></span>

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

### <span data-ttu-id="d2a30-139">-EventSystemProperty</span><span class="sxs-lookup"><span data-stu-id="d2a30-139">-EventSystemProperty</span></span>
<span data-ttu-id="d2a30-140">Az esemény/iot-központ rendszertulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d2a30-140">System properties of the event/iot hub.</span></span>

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

### <span data-ttu-id="d2a30-141">-IgnoreFirstRecord</span><span class="sxs-lookup"><span data-stu-id="d2a30-141">-IgnoreFirstRecord</span></span>
<span data-ttu-id="d2a30-142">Ha igaz érték van beállítva, az azt jelenti, hogy a be nem figyelmének minden fájl első rekordját figyelmen kívül kell hagynia.</span><span class="sxs-lookup"><span data-stu-id="d2a30-142">If set to true, indicates that ingestion should ignore the first record of every file.</span></span>

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

### <span data-ttu-id="d2a30-143">-IotHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a30-143">-IotHubResourceId</span></span>
<span data-ttu-id="d2a30-144">Az Iot-központ adatkapcsolat létrehozásához használt erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d2a30-144">The resource ID of the Iot hub to be used to create a data connection.</span></span>

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

### <span data-ttu-id="d2a30-145">-Kind</span><span class="sxs-lookup"><span data-stu-id="d2a30-145">-Kind</span></span>
<span data-ttu-id="d2a30-146">Az adatkapcsolat végpontjának fajtája</span><span class="sxs-lookup"><span data-stu-id="d2a30-146">Kind of the endpoint for the data connection</span></span>

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

### <span data-ttu-id="d2a30-147">-Location</span><span class="sxs-lookup"><span data-stu-id="d2a30-147">-Location</span></span>
<span data-ttu-id="d2a30-148">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d2a30-148">Resource location.</span></span>

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

### <span data-ttu-id="d2a30-149">-MappingRuleName</span><span class="sxs-lookup"><span data-stu-id="d2a30-149">-MappingRuleName</span></span>
<span data-ttu-id="d2a30-150">Az adatok kiosztására használt megfeleltetési szabály.</span><span class="sxs-lookup"><span data-stu-id="d2a30-150">The mapping rule to be used to ingest the data.</span></span>
<span data-ttu-id="d2a30-151">Szükség esetén a megfeleltetési adatok hozzáadhatóak az egyes üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="d2a30-151">Optionally the mapping information can be added to each message.</span></span>

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

### <span data-ttu-id="d2a30-152">-Name</span><span class="sxs-lookup"><span data-stu-id="d2a30-152">-Name</span></span>
<span data-ttu-id="d2a30-153">Az adatkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="d2a30-153">The name of the data connection.</span></span>

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

### <span data-ttu-id="d2a30-154">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d2a30-154">-NoWait</span></span>
<span data-ttu-id="d2a30-155">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="d2a30-155">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2a30-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a30-156">-ResourceGroupName</span></span>
<span data-ttu-id="d2a30-157">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d2a30-157">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d2a30-158">-SharedAccessPolicyName</span><span class="sxs-lookup"><span data-stu-id="d2a30-158">-SharedAccessPolicyName</span></span>
<span data-ttu-id="d2a30-159">A megosztási hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="d2a30-159">The name of the share access policy.</span></span>

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

### <span data-ttu-id="d2a30-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a30-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="d2a30-161">Annak a tárfióknak az erőforrás-azonosítója, amelyben az adatok találhatók.</span><span class="sxs-lookup"><span data-stu-id="d2a30-161">The resource ID of the storage account where the data resides.</span></span>

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

### <span data-ttu-id="d2a30-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2a30-162">-SubscriptionId</span></span>
<span data-ttu-id="d2a30-163">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d2a30-163">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d2a30-164">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d2a30-164">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d2a30-165">-TableName</span><span class="sxs-lookup"><span data-stu-id="d2a30-165">-TableName</span></span>
<span data-ttu-id="d2a30-166">Az a tábla, amelyben az adatokat meg kell ennünk.</span><span class="sxs-lookup"><span data-stu-id="d2a30-166">The table where the data should be ingested.</span></span>
<span data-ttu-id="d2a30-167">Szükség esetén a táblázat adatai hozzáadhatóak az egyes üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="d2a30-167">Optionally the table information can be added to each message.</span></span>

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

### <span data-ttu-id="d2a30-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2a30-168">-Confirm</span></span>
<span data-ttu-id="d2a30-169">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d2a30-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2a30-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a30-170">-WhatIf</span></span>
<span data-ttu-id="d2a30-171">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d2a30-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2a30-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2a30-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2a30-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a30-173">CommonParameters</span></span>
<span data-ttu-id="d2a30-174">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a30-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a30-175">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2a30-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a30-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2a30-176">INPUTS</span></span>

## <span data-ttu-id="d2a30-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2a30-177">OUTPUTS</span></span>

### <span data-ttu-id="d2a30-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="d2a30-178">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="d2a30-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2a30-179">NOTES</span></span>

<span data-ttu-id="d2a30-180">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d2a30-180">ALIASES</span></span>

## <span data-ttu-id="d2a30-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2a30-181">RELATED LINKS</span></span>

