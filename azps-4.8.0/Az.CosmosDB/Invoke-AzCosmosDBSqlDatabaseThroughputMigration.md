---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 927cdbd6c599b090a66120e95a1ac1a024360271
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025470"
---
# <span data-ttu-id="4eb1f-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="4eb1f-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="4eb1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4eb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb1f-103">Ezzel a beállítással áttelepítheti az automatikus méretezést a manuális átviteli sebességre, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="4eb1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4eb1f-104">SYNTAX</span></span>

### <span data-ttu-id="4eb1f-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4eb1f-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4eb1f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb1f-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb1f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb1f-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb1f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4eb1f-108">DESCRIPTION</span></span>
<span data-ttu-id="4eb1f-109">A ThroughpyteType paraméter határozza meg, hogy milyen átviteli sebességet szeretne áttelepíteni.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="4eb1f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4eb1f-110">EXAMPLES</span></span>

### <span data-ttu-id="4eb1f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4eb1f-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="4eb1f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4eb1f-112">PARAMETERS</span></span>

### <span data-ttu-id="4eb1f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4eb1f-113">-AccountName</span></span>
<span data-ttu-id="4eb1f-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4eb1f-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4eb1f-115">-Confirm</span></span>
<span data-ttu-id="4eb1f-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb1f-117">-DefaultProfile</span></span>
<span data-ttu-id="4eb1f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb1f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eb1f-119">-InputObject</span></span>
<span data-ttu-id="4eb1f-120">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-120">Sql Database object.</span></span>

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

### <span data-ttu-id="4eb1f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4eb1f-121">-Name</span></span>
<span data-ttu-id="4eb1f-122">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-122">Database name.</span></span>

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

### <span data-ttu-id="4eb1f-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4eb1f-123">-ParentObject</span></span>
<span data-ttu-id="4eb1f-124">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="4eb1f-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="4eb1f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb1f-125">-ResourceGroupName</span></span>
<span data-ttu-id="4eb1f-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-126">Name of resource group.</span></span>

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

### <span data-ttu-id="4eb1f-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="4eb1f-127">-ThroughputType</span></span>
<span data-ttu-id="4eb1f-128">Az áttelepítéshez használandó átviteli típus.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="4eb1f-129">Lehetséges értékek: automatikus méretezés, kézi.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="4eb1f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb1f-130">-WhatIf</span></span>
<span data-ttu-id="4eb1f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb1f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb1f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb1f-133">CommonParameters</span></span>
<span data-ttu-id="4eb1f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4eb1f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb1f-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb1f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eb1f-136">INPUTS</span></span>

### <span data-ttu-id="4eb1f-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="4eb1f-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="4eb1f-138">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4eb1f-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="4eb1f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eb1f-139">OUTPUTS</span></span>

### <span data-ttu-id="4eb1f-140">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4eb1f-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4eb1f-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4eb1f-141">NOTES</span></span>

## <span data-ttu-id="4eb1f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4eb1f-142">RELATED LINKS</span></span>
