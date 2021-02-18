---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: 79dcea6f66d01e9bfa2dd53b990a8f38ec5b0f2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204639"
---
# <span data-ttu-id="09ba1-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="09ba1-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="09ba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="09ba1-103">Ezzel a funkcióval az automatikus skálás átviteli sebességet manuális átviteli sebességre, illetve fordítva.</span><span class="sxs-lookup"><span data-stu-id="09ba1-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="09ba1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09ba1-104">SYNTAX</span></span>

### <span data-ttu-id="09ba1-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09ba1-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09ba1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09ba1-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09ba1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09ba1-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09ba1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09ba1-108">DESCRIPTION</span></span>
<span data-ttu-id="09ba1-109">Az ThroughpyteType paraméter azt az átviteli sebességet határozza meg, amelybe át szeretne áttérni.</span><span class="sxs-lookup"><span data-stu-id="09ba1-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="09ba1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09ba1-110">EXAMPLES</span></span>

### <span data-ttu-id="09ba1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="09ba1-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```

## <span data-ttu-id="09ba1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09ba1-112">PARAMETERS</span></span>

### <span data-ttu-id="09ba1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09ba1-113">-AccountName</span></span>
<span data-ttu-id="09ba1-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="09ba1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="09ba1-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09ba1-115">-Confirm</span></span>
<span data-ttu-id="09ba1-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="09ba1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09ba1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09ba1-117">-DatabaseName</span></span>
<span data-ttu-id="09ba1-118">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="09ba1-118">Database name.</span></span>

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

### <span data-ttu-id="09ba1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ba1-119">-DefaultProfile</span></span>
<span data-ttu-id="09ba1-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09ba1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09ba1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09ba1-121">-InputObject</span></span>
<span data-ttu-id="09ba1-122">Mongo Collection objektum.</span><span class="sxs-lookup"><span data-stu-id="09ba1-122">Mongo Collection object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09ba1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="09ba1-123">-Name</span></span>
<span data-ttu-id="09ba1-124">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="09ba1-124">Collection name.</span></span>

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

### <span data-ttu-id="09ba1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="09ba1-125">-ParentObject</span></span>
<span data-ttu-id="09ba1-126">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="09ba1-126">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09ba1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ba1-127">-ResourceGroupName</span></span>
<span data-ttu-id="09ba1-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="09ba1-128">Name of resource group.</span></span>

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

### <span data-ttu-id="09ba1-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="09ba1-129">-ThroughputType</span></span>
<span data-ttu-id="09ba1-130">Az áttűnni megfelelő átviteli sebesség típusa.</span><span class="sxs-lookup"><span data-stu-id="09ba1-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="09ba1-131">Lehetséges értékek: Automatikus méretezés, Kézi.</span><span class="sxs-lookup"><span data-stu-id="09ba1-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="09ba1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09ba1-132">-WhatIf</span></span>
<span data-ttu-id="09ba1-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="09ba1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09ba1-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09ba1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09ba1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ba1-135">CommonParameters</span></span>
<span data-ttu-id="09ba1-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ba1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ba1-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09ba1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ba1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09ba1-138">INPUTS</span></span>

### <span data-ttu-id="09ba1-139">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="09ba1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="09ba1-140">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="09ba1-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="09ba1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09ba1-141">OUTPUTS</span></span>

### <span data-ttu-id="09ba1-142">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="09ba1-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="09ba1-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09ba1-143">NOTES</span></span>

## <span data-ttu-id="09ba1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09ba1-144">RELATED LINKS</span></span>
