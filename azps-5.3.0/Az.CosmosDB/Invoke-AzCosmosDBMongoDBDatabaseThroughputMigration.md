---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480591"
---
# <span data-ttu-id="e77f0-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="e77f0-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="e77f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e77f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e77f0-103">Ezzel a funkcióval az automatikus skálás átviteli sebességet manuális átviteli sebességre, illetve fordítva.</span><span class="sxs-lookup"><span data-stu-id="e77f0-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="e77f0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e77f0-104">SYNTAX</span></span>

### <span data-ttu-id="e77f0-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e77f0-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e77f0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e77f0-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77f0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e77f0-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e77f0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e77f0-108">DESCRIPTION</span></span>
<span data-ttu-id="e77f0-109">Az ThroughpyteType paraméter azt az átviteli sebességet határozza meg, amelybe át szeretne áttérni.</span><span class="sxs-lookup"><span data-stu-id="e77f0-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="e77f0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e77f0-110">EXAMPLES</span></span>

### <span data-ttu-id="e77f0-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e77f0-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="e77f0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e77f0-112">PARAMETERS</span></span>

### <span data-ttu-id="e77f0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e77f0-113">-AccountName</span></span>
<span data-ttu-id="e77f0-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="e77f0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e77f0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e77f0-115">-Confirm</span></span>
<span data-ttu-id="e77f0-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e77f0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e77f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e77f0-117">-DefaultProfile</span></span>
<span data-ttu-id="e77f0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e77f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e77f0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e77f0-119">-InputObject</span></span>
<span data-ttu-id="e77f0-120">Mongo Adatbázis objektum.</span><span class="sxs-lookup"><span data-stu-id="e77f0-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e77f0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e77f0-121">-Name</span></span>
<span data-ttu-id="e77f0-122">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e77f0-122">Database name.</span></span>

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

### <span data-ttu-id="e77f0-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e77f0-123">-ParentObject</span></span>
<span data-ttu-id="e77f0-124">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="e77f0-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e77f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="e77f0-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e77f0-126">Name of resource group.</span></span>

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

### <span data-ttu-id="e77f0-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="e77f0-127">-ThroughputType</span></span>
<span data-ttu-id="e77f0-128">Az áttűnni megfelelő átviteli sebesség típusa.</span><span class="sxs-lookup"><span data-stu-id="e77f0-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="e77f0-129">Lehetséges értékek: Automatikus méretezés, Kézi.</span><span class="sxs-lookup"><span data-stu-id="e77f0-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="e77f0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e77f0-130">-WhatIf</span></span>
<span data-ttu-id="e77f0-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e77f0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e77f0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e77f0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e77f0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e77f0-133">CommonParameters</span></span>
<span data-ttu-id="e77f0-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e77f0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e77f0-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e77f0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e77f0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e77f0-136">INPUTS</span></span>

### <span data-ttu-id="e77f0-137">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e77f0-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="e77f0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e77f0-138">OUTPUTS</span></span>

### <span data-ttu-id="e77f0-139">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e77f0-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e77f0-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e77f0-140">NOTES</span></span>

## <span data-ttu-id="e77f0-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e77f0-141">RELATED LINKS</span></span>
