---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148466"
---
# <span data-ttu-id="a144f-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a144f-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="a144f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a144f-102">SYNOPSIS</span></span>
<span data-ttu-id="a144f-103">Frissíti a 2010-es sqladatbázist.</span><span class="sxs-lookup"><span data-stu-id="a144f-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="a144f-104">Ügyféloldali javítást hajt végre a meglévő adatbázis olvasásával.</span><span class="sxs-lookup"><span data-stu-id="a144f-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="a144f-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a144f-105">SYNTAX</span></span>

### <span data-ttu-id="a144f-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a144f-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a144f-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a144f-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a144f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a144f-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a144f-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a144f-109">DESCRIPTION</span></span>
<span data-ttu-id="a144f-110">Frissíti a 2010-es sqladatbázist.</span><span class="sxs-lookup"><span data-stu-id="a144f-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="a144f-111">Ügyféloldali javítást hajt végre a meglévő adatbázis olvasásával.</span><span class="sxs-lookup"><span data-stu-id="a144f-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="a144f-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a144f-112">EXAMPLES</span></span>

### <span data-ttu-id="a144f-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="a144f-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="a144f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a144f-114">PARAMETERS</span></span>

### <span data-ttu-id="a144f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a144f-115">-AccountName</span></span>
<span data-ttu-id="a144f-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="a144f-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a144f-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="a144f-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="a144f-118">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="a144f-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="a144f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a144f-119">-Confirm</span></span>
<span data-ttu-id="a144f-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a144f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a144f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a144f-121">-DefaultProfile</span></span>
<span data-ttu-id="a144f-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a144f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a144f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a144f-123">-InputObject</span></span>
<span data-ttu-id="a144f-124">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="a144f-124">Sql Database object.</span></span>

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

### <span data-ttu-id="a144f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a144f-125">-Name</span></span>
<span data-ttu-id="a144f-126">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a144f-126">Database name.</span></span>

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

### <span data-ttu-id="a144f-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a144f-127">-ParentObject</span></span>
<span data-ttu-id="a144f-128">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="a144f-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a144f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a144f-129">-ResourceGroupName</span></span>
<span data-ttu-id="a144f-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a144f-130">Name of resource group.</span></span>

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

### <span data-ttu-id="a144f-131">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="a144f-131">-Throughput</span></span>
<span data-ttu-id="a144f-132">Az SQL-adatbázis (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="a144f-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="a144f-133">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="a144f-133">Default value is 400.</span></span>

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

### <span data-ttu-id="a144f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a144f-134">-WhatIf</span></span>
<span data-ttu-id="a144f-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a144f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a144f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a144f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a144f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a144f-137">CommonParameters</span></span>
<span data-ttu-id="a144f-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a144f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a144f-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a144f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a144f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a144f-140">INPUTS</span></span>

### <span data-ttu-id="a144f-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a144f-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="a144f-142">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a144f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="a144f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a144f-143">OUTPUTS</span></span>

### <span data-ttu-id="a144f-144">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a144f-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="a144f-145">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="a144f-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="a144f-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a144f-146">NOTES</span></span>

## <span data-ttu-id="a144f-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a144f-147">RELATED LINKS</span></span>
