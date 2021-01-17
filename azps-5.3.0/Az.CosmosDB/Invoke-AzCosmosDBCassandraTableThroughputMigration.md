---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480598"
---
# <span data-ttu-id="85726-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="85726-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="85726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85726-102">SYNOPSIS</span></span>
<span data-ttu-id="85726-103">Ezzel a funkcióval az automatikus skálás átviteli sebességet manuális átviteli sebességre, illetve fordítva.</span><span class="sxs-lookup"><span data-stu-id="85726-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="85726-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="85726-104">SYNTAX</span></span>

### <span data-ttu-id="85726-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85726-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85726-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85726-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85726-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85726-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85726-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="85726-108">DESCRIPTION</span></span>
<span data-ttu-id="85726-109">Az ThroughpyteType paraméter azt az átviteli sebességet határozza meg, amelybe át szeretne áttérni.</span><span class="sxs-lookup"><span data-stu-id="85726-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="85726-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="85726-110">EXAMPLES</span></span>

### <span data-ttu-id="85726-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="85726-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="85726-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85726-112">PARAMETERS</span></span>

### <span data-ttu-id="85726-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="85726-113">-AccountName</span></span>
<span data-ttu-id="85726-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="85726-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="85726-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85726-115">-Confirm</span></span>
<span data-ttu-id="85726-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="85726-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85726-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85726-117">-DefaultProfile</span></span>
<span data-ttu-id="85726-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85726-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85726-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85726-119">-InputObject</span></span>
<span data-ttu-id="85726-120">2010.01.012.01.</span><span class="sxs-lookup"><span data-stu-id="85726-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="85726-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="85726-121">-KeyspaceName</span></span>
<span data-ttu-id="85726-122">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="85726-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="85726-123">-Name</span><span class="sxs-lookup"><span data-stu-id="85726-123">-Name</span></span>
<span data-ttu-id="85726-124">Kéttáblás tábla neve.</span><span class="sxs-lookup"><span data-stu-id="85726-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="85726-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="85726-125">-ParentObject</span></span>
<span data-ttu-id="85726-126">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="85726-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="85726-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85726-127">-ResourceGroupName</span></span>
<span data-ttu-id="85726-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="85726-128">Name of resource group.</span></span>

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

### <span data-ttu-id="85726-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="85726-129">-ThroughputType</span></span>
<span data-ttu-id="85726-130">Az áttűnni megfelelő átviteli sebesség típusa.</span><span class="sxs-lookup"><span data-stu-id="85726-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="85726-131">Lehetséges értékek: Automatikus méretezés, Kézi.</span><span class="sxs-lookup"><span data-stu-id="85726-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="85726-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85726-132">-WhatIf</span></span>
<span data-ttu-id="85726-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="85726-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85726-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="85726-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85726-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85726-135">CommonParameters</span></span>
<span data-ttu-id="85726-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85726-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85726-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85726-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85726-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85726-138">INPUTS</span></span>

### <span data-ttu-id="85726-139">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="85726-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="85726-140">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="85726-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="85726-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85726-141">OUTPUTS</span></span>

### <span data-ttu-id="85726-142">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="85726-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="85726-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="85726-143">NOTES</span></span>

## <span data-ttu-id="85726-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85726-144">RELATED LINKS</span></span>
