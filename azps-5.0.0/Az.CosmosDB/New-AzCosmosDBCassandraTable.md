---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299369"
---
# <span data-ttu-id="ff39f-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="ff39f-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="ff39f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff39f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff39f-103">Új CosmosDB-Cassandra táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ff39f-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="ff39f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff39f-104">SYNTAX</span></span>

### <span data-ttu-id="ff39f-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff39f-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff39f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff39f-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff39f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff39f-107">DESCRIPTION</span></span>
<span data-ttu-id="ff39f-108">Új CosmosDB-Cassandra táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ff39f-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="ff39f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ff39f-109">EXAMPLES</span></span>

### <span data-ttu-id="ff39f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ff39f-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="ff39f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff39f-111">PARAMETERS</span></span>

### <span data-ttu-id="ff39f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff39f-112">-AccountName</span></span>
<span data-ttu-id="ff39f-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ff39f-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39f-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="ff39f-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="ff39f-115">Analitikai tárterület ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="ff39f-115">Analytical Storage TTL.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39f-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ff39f-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ff39f-117">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ff39f-117">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39f-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff39f-118">-Confirm</span></span>
<span data-ttu-id="ff39f-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff39f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff39f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff39f-120">-DefaultProfile</span></span>
<span data-ttu-id="ff39f-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff39f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff39f-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="ff39f-122">-KeyspaceName</span></span>
<span data-ttu-id="ff39f-123">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="ff39f-123">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff39f-124">-Name</span></span>
<span data-ttu-id="ff39f-125">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ff39f-125">Cassandra Table Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39f-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ff39f-126">-ParentObject</span></span>
<span data-ttu-id="ff39f-127">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="ff39f-127">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff39f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff39f-128">-ResourceGroupName</span></span>
<span data-ttu-id="ff39f-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ff39f-129">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39f-130">-Schema (séma)</span><span class="sxs-lookup"><span data-stu-id="ff39f-130">-Schema</span></span>
<span data-ttu-id="ff39f-131">PSCassandraSchema objektum</span><span class="sxs-lookup"><span data-stu-id="ff39f-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="ff39f-132">Az objektum létrehozásához használja a New-AzCosmosDBCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="ff39f-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff39f-133">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="ff39f-133">-Throughput</span></span>
<span data-ttu-id="ff39f-134">A szóköz (RU/s) méretének átvitele.</span><span class="sxs-lookup"><span data-stu-id="ff39f-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="ff39f-135">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="ff39f-135">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39f-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="ff39f-136">-TtlInSeconds</span></span>
<span data-ttu-id="ff39f-137">Az alapértelmezett élettartam másodpercben</span><span class="sxs-lookup"><span data-stu-id="ff39f-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="ff39f-138">Ha az érték hiányzik vagy a-1 érték van megadva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="ff39f-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="ff39f-139">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítási idő után lejárnak.</span><span class="sxs-lookup"><span data-stu-id="ff39f-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff39f-140">-WhatIf</span></span>
<span data-ttu-id="ff39f-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff39f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff39f-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff39f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff39f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff39f-143">CommonParameters</span></span>
<span data-ttu-id="ff39f-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff39f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff39f-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ff39f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff39f-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff39f-146">INPUTS</span></span>

### <span data-ttu-id="ff39f-147">Microsoft. Azure. Command. CosmosDB. models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="ff39f-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="ff39f-148">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="ff39f-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="ff39f-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff39f-149">OUTPUTS</span></span>

### <span data-ttu-id="ff39f-150">Microsoft. Azure. Command. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="ff39f-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="ff39f-151">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="ff39f-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="ff39f-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff39f-152">NOTES</span></span>

## <span data-ttu-id="ff39f-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff39f-153">RELATED LINKS</span></span>
