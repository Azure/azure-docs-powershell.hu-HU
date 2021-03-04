---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 3f41c44c6abffaf5147ffba17fe3ec84561315b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931329"
---
# <span data-ttu-id="ff9b6-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="ff9b6-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="ff9b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff9b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9b6-103">Frissíti a 2016.01.02.012.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="ff9b6-104">Ügyféloldali javítást hajt végre a meglévő táblázat elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="ff9b6-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ff9b6-105">SYNTAX</span></span>

### <span data-ttu-id="ff9b6-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff9b6-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff9b6-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff9b6-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff9b6-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff9b6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ff9b6-109">DESCRIPTION</span></span>
<span data-ttu-id="ff9b6-110">Frissíti a 2016.01.02.012.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="ff9b6-111">Ügyféloldali javítást hajt végre a meglévő táblázat elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="ff9b6-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ff9b6-112">EXAMPLES</span></span>

### <span data-ttu-id="ff9b6-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="ff9b6-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="ff9b6-114">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="ff9b6-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="ff9b6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff9b6-115">PARAMETERS</span></span>

### <span data-ttu-id="ff9b6-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff9b6-116">-AccountName</span></span>
<span data-ttu-id="ff9b6-117">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ff9b6-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="ff9b6-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="ff9b6-119">Analitikus tárolási TTL.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="ff9b6-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ff9b6-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ff9b6-121">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ff9b6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff9b6-122">-Confirm</span></span>
<span data-ttu-id="ff9b6-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff9b6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9b6-124">-DefaultProfile</span></span>
<span data-ttu-id="ff9b6-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff9b6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff9b6-126">-InputObject</span></span>
<span data-ttu-id="ff9b6-127">2010.01.012.01.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-127">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9b6-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="ff9b6-128">-KeyspaceName</span></span>
<span data-ttu-id="ff9b6-129">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="ff9b6-130">-Name</span><span class="sxs-lookup"><span data-stu-id="ff9b6-130">-Name</span></span>
<span data-ttu-id="ff9b6-131">Kéttáblás tábla neve.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-131">Cassandra Table Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9b6-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ff9b6-132">-ParentObject</span></span>
<span data-ttu-id="ff9b6-133">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="ff9b6-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="ff9b6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff9b6-134">-ResourceGroupName</span></span>
<span data-ttu-id="ff9b6-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-135">Name of resource group.</span></span>

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

### <span data-ttu-id="ff9b6-136">-Séma</span><span class="sxs-lookup"><span data-stu-id="ff9b6-136">-Schema</span></span>
<span data-ttu-id="ff9b6-137">PSCassandraSchema objektum.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="ff9b6-138">Az New-AzCosmosDBCassandraSchema objektum létrehozásához használja a New-AzCosmosDBCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9b6-139">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="ff9b6-139">-Throughput</span></span>
<span data-ttu-id="ff9b6-140">A Siandra Keyspace (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="ff9b6-141">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-141">Default value is 400.</span></span>

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

### <span data-ttu-id="ff9b6-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="ff9b6-142">-TtlInSeconds</span></span>
<span data-ttu-id="ff9b6-143">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="ff9b6-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="ff9b6-144">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="ff9b6-145">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="ff9b6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff9b6-146">-WhatIf</span></span>
<span data-ttu-id="ff9b6-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff9b6-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff9b6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9b6-149">CommonParameters</span></span>
<span data-ttu-id="ff9b6-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff9b6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9b6-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff9b6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9b6-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff9b6-152">INPUTS</span></span>

### <span data-ttu-id="ff9b6-153">Microsoft.Azure.Commands.IssDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="ff9b6-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="ff9b6-154">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="ff9b6-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="ff9b6-155">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="ff9b6-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="ff9b6-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff9b6-156">OUTPUTS</span></span>

### <span data-ttu-id="ff9b6-157">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="ff9b6-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="ff9b6-158">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ff9b6-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="ff9b6-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ff9b6-159">NOTES</span></span>

## <span data-ttu-id="ff9b6-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff9b6-160">RELATED LINKS</span></span>
