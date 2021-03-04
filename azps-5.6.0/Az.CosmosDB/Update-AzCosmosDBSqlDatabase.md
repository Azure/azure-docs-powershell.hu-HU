---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1bfb0ec8392c0ddcce20db839f1817688e8feb7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931217"
---
# <span data-ttu-id="ff2ff-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff2ff-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="ff2ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ff2ff-103">Frissíti a 2010-es sqladatbázist.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="ff2ff-104">Ügyféloldali javítást hajt végre a meglévő adatbázis olvasásával.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="ff2ff-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ff2ff-105">SYNTAX</span></span>

### <span data-ttu-id="ff2ff-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff2ff-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff2ff-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff2ff-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff2ff-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff2ff-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff2ff-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ff2ff-109">DESCRIPTION</span></span>
<span data-ttu-id="ff2ff-110">Frissíti a 2010-es sqladatbázist.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="ff2ff-111">Ügyféloldali javítást hajt végre a meglévő adatbázis olvasásával.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="ff2ff-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ff2ff-112">EXAMPLES</span></span>

### <span data-ttu-id="ff2ff-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="ff2ff-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="ff2ff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff2ff-114">PARAMETERS</span></span>

### <span data-ttu-id="ff2ff-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff2ff-115">-AccountName</span></span>
<span data-ttu-id="ff2ff-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ff2ff-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ff2ff-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ff2ff-118">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ff2ff-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff2ff-119">-Confirm</span></span>
<span data-ttu-id="ff2ff-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff2ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2ff-121">-DefaultProfile</span></span>
<span data-ttu-id="ff2ff-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff2ff-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff2ff-123">-InputObject</span></span>
<span data-ttu-id="ff2ff-124">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-124">Sql Database object.</span></span>

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

### <span data-ttu-id="ff2ff-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ff2ff-125">-Name</span></span>
<span data-ttu-id="ff2ff-126">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-126">Database name.</span></span>

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

### <span data-ttu-id="ff2ff-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ff2ff-127">-ParentObject</span></span>
<span data-ttu-id="ff2ff-128">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="ff2ff-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ff2ff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff2ff-129">-ResourceGroupName</span></span>
<span data-ttu-id="ff2ff-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-130">Name of resource group.</span></span>

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

### <span data-ttu-id="ff2ff-131">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="ff2ff-131">-Throughput</span></span>
<span data-ttu-id="ff2ff-132">Az SQL-adatbázis (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="ff2ff-133">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-133">Default value is 400.</span></span>

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

### <span data-ttu-id="ff2ff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff2ff-134">-WhatIf</span></span>
<span data-ttu-id="ff2ff-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff2ff-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff2ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2ff-137">CommonParameters</span></span>
<span data-ttu-id="ff2ff-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff2ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff2ff-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff2ff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2ff-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff2ff-140">INPUTS</span></span>

### <span data-ttu-id="ff2ff-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ff2ff-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="ff2ff-142">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ff2ff-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="ff2ff-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff2ff-143">OUTPUTS</span></span>

### <span data-ttu-id="ff2ff-144">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ff2ff-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="ff2ff-145">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ff2ff-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="ff2ff-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ff2ff-146">NOTES</span></span>

## <span data-ttu-id="ff2ff-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff2ff-147">RELATED LINKS</span></span>
