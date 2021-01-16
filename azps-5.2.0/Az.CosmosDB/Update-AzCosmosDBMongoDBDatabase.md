---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363157"
---
# <span data-ttu-id="c5597-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="c5597-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="c5597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5597-102">SYNOPSIS</span></span>
<span data-ttu-id="c5597-103">Frissíti aFrissítésekDB MongoDB adatbázist.</span><span class="sxs-lookup"><span data-stu-id="c5597-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="c5597-104">Ügyféloldali javítást hajt végre a meglévő adatbázis olvasásával.</span><span class="sxs-lookup"><span data-stu-id="c5597-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="c5597-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5597-105">SYNTAX</span></span>

### <span data-ttu-id="c5597-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5597-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5597-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5597-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5597-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5597-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5597-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5597-109">DESCRIPTION</span></span>
<span data-ttu-id="c5597-110">Frissíti aFrissítésekDB MongoDB adatbázist.</span><span class="sxs-lookup"><span data-stu-id="c5597-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="c5597-111">Ügyféloldali javítást hajt végre a meglévő adatbázis olvasásával.</span><span class="sxs-lookup"><span data-stu-id="c5597-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="c5597-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5597-112">EXAMPLES</span></span>

### <span data-ttu-id="c5597-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="c5597-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="c5597-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5597-114">PARAMETERS</span></span>

### <span data-ttu-id="c5597-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c5597-115">-AccountName</span></span>
<span data-ttu-id="c5597-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="c5597-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c5597-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c5597-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c5597-118">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="c5597-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c5597-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5597-119">-Confirm</span></span>
<span data-ttu-id="c5597-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c5597-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5597-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5597-121">-DefaultProfile</span></span>
<span data-ttu-id="c5597-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5597-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5597-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5597-123">-InputObject</span></span>
<span data-ttu-id="c5597-124">Mongo Adatbázis objektum.</span><span class="sxs-lookup"><span data-stu-id="c5597-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5597-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c5597-125">-Name</span></span>
<span data-ttu-id="c5597-126">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c5597-126">Database name.</span></span>

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

### <span data-ttu-id="c5597-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c5597-127">-ParentObject</span></span>
<span data-ttu-id="c5597-128">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="c5597-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c5597-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5597-129">-ResourceGroupName</span></span>
<span data-ttu-id="c5597-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c5597-130">Name of resource group.</span></span>

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

### <span data-ttu-id="c5597-131">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="c5597-131">-Throughput</span></span>
<span data-ttu-id="c5597-132">A Mongo-adatbázis (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="c5597-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="c5597-133">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="c5597-133">Default value is 400.</span></span>

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

### <span data-ttu-id="c5597-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5597-134">-WhatIf</span></span>
<span data-ttu-id="c5597-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c5597-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5597-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5597-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5597-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5597-137">CommonParameters</span></span>
<span data-ttu-id="c5597-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5597-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5597-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5597-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5597-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5597-140">INPUTS</span></span>

### <span data-ttu-id="c5597-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="c5597-141">None</span></span>

## <span data-ttu-id="c5597-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5597-142">OUTPUTS</span></span>

### <span data-ttu-id="c5597-143">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c5597-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="c5597-144">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c5597-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="c5597-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5597-145">NOTES</span></span>

## <span data-ttu-id="c5597-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5597-146">RELATED LINKS</span></span>
