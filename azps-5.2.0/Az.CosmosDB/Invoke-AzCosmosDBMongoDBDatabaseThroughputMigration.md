---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343445"
---
# <span data-ttu-id="efa7d-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="efa7d-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="efa7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="efa7d-103">Ezzel a funkcióval az automatikus skálás átviteli sebességet manuális átviteli sebességre, illetve fordítva.</span><span class="sxs-lookup"><span data-stu-id="efa7d-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="efa7d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efa7d-104">SYNTAX</span></span>

### <span data-ttu-id="efa7d-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efa7d-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efa7d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efa7d-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa7d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efa7d-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efa7d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efa7d-108">DESCRIPTION</span></span>
<span data-ttu-id="efa7d-109">Az ThroughpyteType paraméter azt az átviteli sebességet határozza meg, amelybe át szeretne áttérni.</span><span class="sxs-lookup"><span data-stu-id="efa7d-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="efa7d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efa7d-110">EXAMPLES</span></span>

### <span data-ttu-id="efa7d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="efa7d-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="efa7d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efa7d-112">PARAMETERS</span></span>

### <span data-ttu-id="efa7d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="efa7d-113">-AccountName</span></span>
<span data-ttu-id="efa7d-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="efa7d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="efa7d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efa7d-115">-Confirm</span></span>
<span data-ttu-id="efa7d-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="efa7d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa7d-117">-DefaultProfile</span></span>
<span data-ttu-id="efa7d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efa7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efa7d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efa7d-119">-InputObject</span></span>
<span data-ttu-id="efa7d-120">Mongo Adatbázis objektum.</span><span class="sxs-lookup"><span data-stu-id="efa7d-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="efa7d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="efa7d-121">-Name</span></span>
<span data-ttu-id="efa7d-122">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="efa7d-122">Database name.</span></span>

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

### <span data-ttu-id="efa7d-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="efa7d-123">-ParentObject</span></span>
<span data-ttu-id="efa7d-124">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="efa7d-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="efa7d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa7d-125">-ResourceGroupName</span></span>
<span data-ttu-id="efa7d-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="efa7d-126">Name of resource group.</span></span>

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

### <span data-ttu-id="efa7d-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="efa7d-127">-ThroughputType</span></span>
<span data-ttu-id="efa7d-128">Az áttűnni megfelelő átviteli sebesség típusa.</span><span class="sxs-lookup"><span data-stu-id="efa7d-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="efa7d-129">Lehetséges értékek: Automatikus méretezés, Kézi.</span><span class="sxs-lookup"><span data-stu-id="efa7d-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="efa7d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa7d-130">-WhatIf</span></span>
<span data-ttu-id="efa7d-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="efa7d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efa7d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="efa7d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa7d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa7d-133">CommonParameters</span></span>
<span data-ttu-id="efa7d-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa7d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa7d-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efa7d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa7d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efa7d-136">INPUTS</span></span>

### <span data-ttu-id="efa7d-137">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="efa7d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="efa7d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efa7d-138">OUTPUTS</span></span>

### <span data-ttu-id="efa7d-139">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="efa7d-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="efa7d-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efa7d-140">NOTES</span></span>

## <span data-ttu-id="efa7d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efa7d-141">RELATED LINKS</span></span>
