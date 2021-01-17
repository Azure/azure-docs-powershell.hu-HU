---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480583"
---
# <span data-ttu-id="24d78-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="24d78-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="24d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24d78-102">SYNOPSIS</span></span>
<span data-ttu-id="24d78-103">Létrehoz egy új MellőDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="24d78-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="24d78-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="24d78-104">SYNTAX</span></span>

### <span data-ttu-id="24d78-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24d78-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d78-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24d78-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24d78-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="24d78-107">DESCRIPTION</span></span>
<span data-ttu-id="24d78-108">Létrehoz egy új MellőDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="24d78-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="24d78-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="24d78-109">EXAMPLES</span></span>

### <span data-ttu-id="24d78-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="24d78-110">Example 1</span></span>
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

## <span data-ttu-id="24d78-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24d78-111">PARAMETERS</span></span>

### <span data-ttu-id="24d78-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24d78-112">-AccountName</span></span>
<span data-ttu-id="24d78-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="24d78-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24d78-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="24d78-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="24d78-115">Analitikus tárolási TTL.</span><span class="sxs-lookup"><span data-stu-id="24d78-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="24d78-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="24d78-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="24d78-117">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="24d78-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="24d78-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24d78-118">-Confirm</span></span>
<span data-ttu-id="24d78-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="24d78-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d78-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d78-120">-DefaultProfile</span></span>
<span data-ttu-id="24d78-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24d78-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d78-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="24d78-122">-KeyspaceName</span></span>
<span data-ttu-id="24d78-123">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="24d78-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="24d78-124">-Name</span><span class="sxs-lookup"><span data-stu-id="24d78-124">-Name</span></span>
<span data-ttu-id="24d78-125">Kéttáblás tábla neve.</span><span class="sxs-lookup"><span data-stu-id="24d78-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="24d78-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="24d78-126">-ParentObject</span></span>
<span data-ttu-id="24d78-127">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="24d78-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="24d78-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d78-128">-ResourceGroupName</span></span>
<span data-ttu-id="24d78-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="24d78-129">Name of resource group.</span></span>

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

### <span data-ttu-id="24d78-130">-Séma</span><span class="sxs-lookup"><span data-stu-id="24d78-130">-Schema</span></span>
<span data-ttu-id="24d78-131">PSCassandraSchema objektum.</span><span class="sxs-lookup"><span data-stu-id="24d78-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="24d78-132">Az New-AzCosmosDBCassandraSchema objektum létrehozásához használja a New-AzCosmosDBCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="24d78-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="24d78-133">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="24d78-133">-Throughput</span></span>
<span data-ttu-id="24d78-134">A Siandra Keyspace (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="24d78-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="24d78-135">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="24d78-135">Default value is 400.</span></span>

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

### <span data-ttu-id="24d78-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="24d78-136">-TtlInSeconds</span></span>
<span data-ttu-id="24d78-137">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="24d78-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="24d78-138">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="24d78-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="24d78-139">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="24d78-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="24d78-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d78-140">-WhatIf</span></span>
<span data-ttu-id="24d78-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="24d78-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d78-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24d78-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d78-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d78-143">CommonParameters</span></span>
<span data-ttu-id="24d78-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d78-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d78-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24d78-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d78-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24d78-146">INPUTS</span></span>

### <span data-ttu-id="24d78-147">Microsoft.Azure.Commands.IssDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="24d78-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="24d78-148">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="24d78-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="24d78-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24d78-149">OUTPUTS</span></span>

### <span data-ttu-id="24d78-150">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="24d78-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="24d78-151">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="24d78-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="24d78-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="24d78-152">NOTES</span></span>

## <span data-ttu-id="24d78-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24d78-153">RELATED LINKS</span></span>
