---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299426"
---
# <span data-ttu-id="adaf8-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="adaf8-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="adaf8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="adaf8-102">SYNOPSIS</span></span>
<span data-ttu-id="adaf8-103">Ezzel a beállítással áttelepítheti az automatikus méretezést a manuális átviteli sebességre, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="adaf8-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="adaf8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="adaf8-104">SYNTAX</span></span>

### <span data-ttu-id="adaf8-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="adaf8-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adaf8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adaf8-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adaf8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adaf8-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adaf8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="adaf8-108">DESCRIPTION</span></span>
<span data-ttu-id="adaf8-109">A ThroughpyteType paraméter határozza meg, hogy milyen átviteli sebességet szeretne áttelepíteni.</span><span class="sxs-lookup"><span data-stu-id="adaf8-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="adaf8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="adaf8-110">EXAMPLES</span></span>

### <span data-ttu-id="adaf8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="adaf8-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="adaf8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="adaf8-112">PARAMETERS</span></span>

### <span data-ttu-id="adaf8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="adaf8-113">-AccountName</span></span>
<span data-ttu-id="adaf8-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="adaf8-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="adaf8-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="adaf8-115">-Confirm</span></span>
<span data-ttu-id="adaf8-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="adaf8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adaf8-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="adaf8-117">-DatabaseName</span></span>
<span data-ttu-id="adaf8-118">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="adaf8-118">Database name.</span></span>

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

### <span data-ttu-id="adaf8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adaf8-119">-DefaultProfile</span></span>
<span data-ttu-id="adaf8-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adaf8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adaf8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adaf8-121">-InputObject</span></span>
<span data-ttu-id="adaf8-122">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="adaf8-122">Sql Container object.</span></span>

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

### <span data-ttu-id="adaf8-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="adaf8-123">-Name</span></span>
<span data-ttu-id="adaf8-124">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="adaf8-124">Container name.</span></span>

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

### <span data-ttu-id="adaf8-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="adaf8-125">-ParentObject</span></span>
<span data-ttu-id="adaf8-126">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="adaf8-126">Sql Database object.</span></span>

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

### <span data-ttu-id="adaf8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adaf8-127">-ResourceGroupName</span></span>
<span data-ttu-id="adaf8-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="adaf8-128">Name of resource group.</span></span>

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

### <span data-ttu-id="adaf8-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="adaf8-129">-ThroughputType</span></span>
<span data-ttu-id="adaf8-130">Az áttelepítéshez használandó átviteli típus.</span><span class="sxs-lookup"><span data-stu-id="adaf8-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="adaf8-131">Lehetséges értékek: automatikus méretezés, kézi.</span><span class="sxs-lookup"><span data-stu-id="adaf8-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="adaf8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adaf8-132">-WhatIf</span></span>
<span data-ttu-id="adaf8-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="adaf8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adaf8-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="adaf8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adaf8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adaf8-135">CommonParameters</span></span>
<span data-ttu-id="adaf8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="adaf8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adaf8-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="adaf8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adaf8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="adaf8-138">INPUTS</span></span>

### <span data-ttu-id="adaf8-139">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="adaf8-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="adaf8-140">Microsoft. Azure. Command. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="adaf8-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="adaf8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adaf8-141">OUTPUTS</span></span>

### <span data-ttu-id="adaf8-142">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="adaf8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="adaf8-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="adaf8-143">NOTES</span></span>

## <span data-ttu-id="adaf8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adaf8-144">RELATED LINKS</span></span>
