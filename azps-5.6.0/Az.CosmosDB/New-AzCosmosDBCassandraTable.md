---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7251b4b928bb0adc94bc42da9d5bcef063c86259
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008005"
---
# <span data-ttu-id="592a0-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="592a0-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="592a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="592a0-102">SYNOPSIS</span></span>
<span data-ttu-id="592a0-103">Létrehoz egy új MellőDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="592a0-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="592a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="592a0-104">SYNTAX</span></span>

### <span data-ttu-id="592a0-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="592a0-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="592a0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="592a0-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="592a0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="592a0-107">DESCRIPTION</span></span>
<span data-ttu-id="592a0-108">Létrehoz egy új MellőDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="592a0-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="592a0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="592a0-109">EXAMPLES</span></span>

### <span data-ttu-id="592a0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="592a0-110">Example 1</span></span>
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

## <span data-ttu-id="592a0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="592a0-111">PARAMETERS</span></span>

### <span data-ttu-id="592a0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="592a0-112">-AccountName</span></span>
<span data-ttu-id="592a0-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="592a0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="592a0-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="592a0-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="592a0-115">Analitikus tárolási TTL.</span><span class="sxs-lookup"><span data-stu-id="592a0-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="592a0-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="592a0-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="592a0-117">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="592a0-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="592a0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="592a0-118">-Confirm</span></span>
<span data-ttu-id="592a0-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="592a0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="592a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592a0-120">-DefaultProfile</span></span>
<span data-ttu-id="592a0-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="592a0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="592a0-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="592a0-122">-KeyspaceName</span></span>
<span data-ttu-id="592a0-123">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="592a0-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="592a0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="592a0-124">-Name</span></span>
<span data-ttu-id="592a0-125">Kéttáblás tábla neve.</span><span class="sxs-lookup"><span data-stu-id="592a0-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="592a0-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="592a0-126">-ParentObject</span></span>
<span data-ttu-id="592a0-127">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="592a0-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="592a0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592a0-128">-ResourceGroupName</span></span>
<span data-ttu-id="592a0-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="592a0-129">Name of resource group.</span></span>

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

### <span data-ttu-id="592a0-130">-Séma</span><span class="sxs-lookup"><span data-stu-id="592a0-130">-Schema</span></span>
<span data-ttu-id="592a0-131">PSCassandraSchema objektum.</span><span class="sxs-lookup"><span data-stu-id="592a0-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="592a0-132">Az New-AzCosmosDBCassandraSchema objektum létrehozásához használja a New-AzCosmosDBCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="592a0-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="592a0-133">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="592a0-133">-Throughput</span></span>
<span data-ttu-id="592a0-134">A Siandra Keyspace (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="592a0-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="592a0-135">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="592a0-135">Default value is 400.</span></span>

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

### <span data-ttu-id="592a0-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="592a0-136">-TtlInSeconds</span></span>
<span data-ttu-id="592a0-137">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="592a0-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="592a0-138">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="592a0-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="592a0-139">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="592a0-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="592a0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="592a0-140">-WhatIf</span></span>
<span data-ttu-id="592a0-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="592a0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="592a0-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="592a0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="592a0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592a0-143">CommonParameters</span></span>
<span data-ttu-id="592a0-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592a0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592a0-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="592a0-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592a0-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="592a0-146">INPUTS</span></span>

### <span data-ttu-id="592a0-147">Microsoft.Azure.Commands.IssDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="592a0-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="592a0-148">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="592a0-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="592a0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="592a0-149">OUTPUTS</span></span>

### <span data-ttu-id="592a0-150">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="592a0-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="592a0-151">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="592a0-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="592a0-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="592a0-152">NOTES</span></span>

## <span data-ttu-id="592a0-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="592a0-153">RELATED LINKS</span></span>
