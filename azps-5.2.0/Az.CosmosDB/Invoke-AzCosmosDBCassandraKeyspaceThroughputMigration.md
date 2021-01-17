---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346026"
---
# <span data-ttu-id="ab239-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="ab239-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="ab239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab239-102">SYNOPSIS</span></span>
<span data-ttu-id="ab239-103">Ezzel a funkcióval az automatikus skálás átviteli sebességet manuális átviteli sebességre, illetve fordítva.</span><span class="sxs-lookup"><span data-stu-id="ab239-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="ab239-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab239-104">SYNTAX</span></span>

### <span data-ttu-id="ab239-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab239-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab239-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab239-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab239-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab239-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab239-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab239-108">DESCRIPTION</span></span>
<span data-ttu-id="ab239-109">Az ThroughpyteType paraméter azt az átviteli sebességet határozza meg, amelybe át szeretne áttérni.</span><span class="sxs-lookup"><span data-stu-id="ab239-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="ab239-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab239-110">EXAMPLES</span></span>

### <span data-ttu-id="ab239-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ab239-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="ab239-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab239-112">PARAMETERS</span></span>

### <span data-ttu-id="ab239-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ab239-113">-AccountName</span></span>
<span data-ttu-id="ab239-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="ab239-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ab239-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab239-115">-Confirm</span></span>
<span data-ttu-id="ab239-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ab239-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab239-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab239-117">-DefaultProfile</span></span>
<span data-ttu-id="ab239-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab239-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab239-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab239-119">-InputObject</span></span>
<span data-ttu-id="ab239-120">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="ab239-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab239-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ab239-121">-Name</span></span>
<span data-ttu-id="ab239-122">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="ab239-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="ab239-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ab239-123">-ParentObject</span></span>
<span data-ttu-id="ab239-124">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="ab239-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ab239-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab239-125">-ResourceGroupName</span></span>
<span data-ttu-id="ab239-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ab239-126">Name of resource group.</span></span>

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

### <span data-ttu-id="ab239-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="ab239-127">-ThroughputType</span></span>
<span data-ttu-id="ab239-128">Az áttűnni megfelelő átviteli sebesség típusa.</span><span class="sxs-lookup"><span data-stu-id="ab239-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="ab239-129">Lehetséges értékek: Automatikus méretezés, Kézi.</span><span class="sxs-lookup"><span data-stu-id="ab239-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="ab239-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab239-130">-WhatIf</span></span>
<span data-ttu-id="ab239-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ab239-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab239-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ab239-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab239-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab239-133">CommonParameters</span></span>
<span data-ttu-id="ab239-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab239-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab239-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab239-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab239-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab239-136">INPUTS</span></span>

### <span data-ttu-id="ab239-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="ab239-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="ab239-138">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="ab239-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="ab239-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab239-139">OUTPUTS</span></span>

### <span data-ttu-id="ab239-140">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ab239-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ab239-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab239-141">NOTES</span></span>

## <span data-ttu-id="ab239-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab239-142">RELATED LINKS</span></span>
