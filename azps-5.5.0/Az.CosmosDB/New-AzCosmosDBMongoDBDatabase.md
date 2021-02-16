---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: d4724976d5b4c702999fdd64c0811aa975c258d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144482"
---
# <span data-ttu-id="22b6d-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="22b6d-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="22b6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="22b6d-103">Létrehoz egy új TárolóDB MongoDB adatbázist.</span><span class="sxs-lookup"><span data-stu-id="22b6d-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="22b6d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22b6d-104">SYNTAX</span></span>

### <span data-ttu-id="22b6d-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22b6d-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b6d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22b6d-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22b6d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22b6d-107">DESCRIPTION</span></span>
<span data-ttu-id="22b6d-108">Létrehoz egy új TárolóDB MongoDB adatbázist.</span><span class="sxs-lookup"><span data-stu-id="22b6d-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="22b6d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22b6d-109">EXAMPLES</span></span>

### <span data-ttu-id="22b6d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="22b6d-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="22b6d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22b6d-111">PARAMETERS</span></span>

### <span data-ttu-id="22b6d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22b6d-112">-AccountName</span></span>
<span data-ttu-id="22b6d-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="22b6d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="22b6d-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="22b6d-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="22b6d-115">Maximális átviteli sebesség, ha engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="22b6d-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="22b6d-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22b6d-116">-Confirm</span></span>
<span data-ttu-id="22b6d-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22b6d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22b6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b6d-118">-DefaultProfile</span></span>
<span data-ttu-id="22b6d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22b6d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b6d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="22b6d-120">-Name</span></span>
<span data-ttu-id="22b6d-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="22b6d-121">Database name.</span></span>

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

### <span data-ttu-id="22b6d-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="22b6d-122">-ParentObject</span></span>
<span data-ttu-id="22b6d-123">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="22b6d-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="22b6d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22b6d-124">-ResourceGroupName</span></span>
<span data-ttu-id="22b6d-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="22b6d-125">Name of resource group.</span></span>

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

### <span data-ttu-id="22b6d-126">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="22b6d-126">-Throughput</span></span>
<span data-ttu-id="22b6d-127">A Mongo-adatbázis (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="22b6d-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="22b6d-128">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="22b6d-128">Default value is 400.</span></span>

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

### <span data-ttu-id="22b6d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b6d-129">-WhatIf</span></span>
<span data-ttu-id="22b6d-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22b6d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b6d-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22b6d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22b6d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b6d-132">CommonParameters</span></span>
<span data-ttu-id="22b6d-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b6d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b6d-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22b6d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b6d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22b6d-135">INPUTS</span></span>

### <span data-ttu-id="22b6d-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="22b6d-136">None</span></span>

## <span data-ttu-id="22b6d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22b6d-137">OUTPUTS</span></span>

### <span data-ttu-id="22b6d-138">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="22b6d-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="22b6d-139">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="22b6d-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="22b6d-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22b6d-140">NOTES</span></span>

## <span data-ttu-id="22b6d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22b6d-141">RELATED LINKS</span></span>
