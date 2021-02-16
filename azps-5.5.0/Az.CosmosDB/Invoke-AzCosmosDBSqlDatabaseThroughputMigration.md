---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 15ee57c32d8eeeca996994900113360adac1c407
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144539"
---
# <span data-ttu-id="c0116-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="c0116-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="c0116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0116-102">SYNOPSIS</span></span>
<span data-ttu-id="c0116-103">Ezzel a funkcióval az automatikus skálás átviteli sebességet manuális átviteli sebességre, illetve fordítva.</span><span class="sxs-lookup"><span data-stu-id="c0116-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="c0116-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0116-104">SYNTAX</span></span>

### <span data-ttu-id="c0116-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0116-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0116-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0116-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0116-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0116-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0116-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0116-108">DESCRIPTION</span></span>
<span data-ttu-id="c0116-109">Az ThroughpyteType paraméter azt az átviteli sebességet határozza meg, amelybe át szeretne áttérni.</span><span class="sxs-lookup"><span data-stu-id="c0116-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="c0116-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0116-110">EXAMPLES</span></span>

### <span data-ttu-id="c0116-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c0116-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="c0116-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0116-112">PARAMETERS</span></span>

### <span data-ttu-id="c0116-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0116-113">-AccountName</span></span>
<span data-ttu-id="c0116-114">A Külön db-adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="c0116-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c0116-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0116-115">-Confirm</span></span>
<span data-ttu-id="c0116-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c0116-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0116-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0116-117">-DefaultProfile</span></span>
<span data-ttu-id="c0116-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0116-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0116-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0116-119">-InputObject</span></span>
<span data-ttu-id="c0116-120">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="c0116-120">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0116-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c0116-121">-Name</span></span>
<span data-ttu-id="c0116-122">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c0116-122">Database name.</span></span>

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

### <span data-ttu-id="c0116-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c0116-123">-ParentObject</span></span>
<span data-ttu-id="c0116-124">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="c0116-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0116-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0116-125">-ResourceGroupName</span></span>
<span data-ttu-id="c0116-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c0116-126">Name of resource group.</span></span>

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

### <span data-ttu-id="c0116-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="c0116-127">-ThroughputType</span></span>
<span data-ttu-id="c0116-128">Az áttűnni megfelelő átviteli sebesség típusa.</span><span class="sxs-lookup"><span data-stu-id="c0116-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="c0116-129">Lehetséges értékek: Automatikus méretezés, Kézi.</span><span class="sxs-lookup"><span data-stu-id="c0116-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="c0116-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0116-130">-WhatIf</span></span>
<span data-ttu-id="c0116-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c0116-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0116-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0116-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0116-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0116-133">CommonParameters</span></span>
<span data-ttu-id="c0116-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0116-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0116-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0116-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0116-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0116-136">INPUTS</span></span>

### <span data-ttu-id="c0116-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="c0116-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="c0116-138">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c0116-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="c0116-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0116-139">OUTPUTS</span></span>

### <span data-ttu-id="c0116-140">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c0116-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c0116-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0116-141">NOTES</span></span>

## <span data-ttu-id="c0116-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0116-142">RELATED LINKS</span></span>
