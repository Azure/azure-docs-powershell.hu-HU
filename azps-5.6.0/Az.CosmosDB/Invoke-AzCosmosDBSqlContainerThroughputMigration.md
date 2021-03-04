---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: c502040c2d4b11302c158cffb66bf6fd01e148ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941937"
---
# <span data-ttu-id="bc348-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="bc348-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="bc348-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc348-102">SYNOPSIS</span></span>
<span data-ttu-id="bc348-103">Ezzel a funkcióval az automatikus skálás átviteli sebességet manuális átviteli sebességre, illetve fordítva.</span><span class="sxs-lookup"><span data-stu-id="bc348-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="bc348-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bc348-104">SYNTAX</span></span>

### <span data-ttu-id="bc348-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc348-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc348-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc348-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc348-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc348-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc348-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bc348-108">DESCRIPTION</span></span>
<span data-ttu-id="bc348-109">Az ThroughpyteType paraméter azt az átviteli sebességet határozza meg, amelybe át szeretne áttérni.</span><span class="sxs-lookup"><span data-stu-id="bc348-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="bc348-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bc348-110">EXAMPLES</span></span>

### <span data-ttu-id="bc348-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bc348-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```

## <span data-ttu-id="bc348-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc348-112">PARAMETERS</span></span>

### <span data-ttu-id="bc348-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bc348-113">-AccountName</span></span>
<span data-ttu-id="bc348-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="bc348-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bc348-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc348-115">-Confirm</span></span>
<span data-ttu-id="bc348-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bc348-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc348-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bc348-117">-DatabaseName</span></span>
<span data-ttu-id="bc348-118">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="bc348-118">Database name.</span></span>

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

### <span data-ttu-id="bc348-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc348-119">-DefaultProfile</span></span>
<span data-ttu-id="bc348-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc348-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc348-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc348-121">-InputObject</span></span>
<span data-ttu-id="bc348-122">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="bc348-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc348-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bc348-123">-Name</span></span>
<span data-ttu-id="bc348-124">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="bc348-124">Container name.</span></span>

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

### <span data-ttu-id="bc348-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bc348-125">-ParentObject</span></span>
<span data-ttu-id="bc348-126">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="bc348-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc348-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc348-127">-ResourceGroupName</span></span>
<span data-ttu-id="bc348-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bc348-128">Name of resource group.</span></span>

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

### <span data-ttu-id="bc348-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="bc348-129">-ThroughputType</span></span>
<span data-ttu-id="bc348-130">Az áttűnni megfelelő átviteli sebesség típusa.</span><span class="sxs-lookup"><span data-stu-id="bc348-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="bc348-131">Lehetséges értékek: Automatikus méretezés, Kézi.</span><span class="sxs-lookup"><span data-stu-id="bc348-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="bc348-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc348-132">-WhatIf</span></span>
<span data-ttu-id="bc348-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bc348-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc348-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc348-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc348-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc348-135">CommonParameters</span></span>
<span data-ttu-id="bc348-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc348-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc348-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc348-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc348-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc348-138">INPUTS</span></span>

### <span data-ttu-id="bc348-139">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bc348-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="bc348-140">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="bc348-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="bc348-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc348-141">OUTPUTS</span></span>

### <span data-ttu-id="bc348-142">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bc348-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bc348-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bc348-143">NOTES</span></span>

## <span data-ttu-id="bc348-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc348-144">RELATED LINKS</span></span>
