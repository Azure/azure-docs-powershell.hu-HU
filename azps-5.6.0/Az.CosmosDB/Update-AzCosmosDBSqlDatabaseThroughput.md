---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 23e4ed96f464d29e95bacd04b93326cb5ce8e3da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931202"
---
# <span data-ttu-id="9f051-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="9f051-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="9f051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f051-102">SYNOPSIS</span></span>
<span data-ttu-id="9f051-103">Frissíti a NaplósDB Sql-adatbázis átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="9f051-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9f051-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f051-104">SYNTAX</span></span>

### <span data-ttu-id="9f051-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f051-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f051-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f051-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f051-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f051-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f051-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f051-108">DESCRIPTION</span></span>
<span data-ttu-id="9f051-109">Frissíti a NaplósDB Sql-adatbázis átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="9f051-109">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9f051-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f051-110">EXAMPLES</span></span>

### <span data-ttu-id="9f051-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9f051-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="9f051-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f051-112">PARAMETERS</span></span>

### <span data-ttu-id="9f051-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9f051-113">-AccountName</span></span>
<span data-ttu-id="9f051-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="9f051-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9f051-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="9f051-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="9f051-116">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="9f051-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="9f051-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f051-117">-Confirm</span></span>
<span data-ttu-id="9f051-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9f051-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f051-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f051-119">-DefaultProfile</span></span>
<span data-ttu-id="9f051-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f051-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f051-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f051-121">-InputObject</span></span>
<span data-ttu-id="9f051-122">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="9f051-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9f051-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9f051-123">-Name</span></span>
<span data-ttu-id="9f051-124">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9f051-124">Database name.</span></span>

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

### <span data-ttu-id="9f051-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9f051-125">-ParentObject</span></span>
<span data-ttu-id="9f051-126">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="9f051-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9f051-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f051-127">-ResourceGroupName</span></span>
<span data-ttu-id="9f051-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9f051-128">Name of resource group.</span></span>

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

### <span data-ttu-id="9f051-129">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="9f051-129">-Throughput</span></span>
<span data-ttu-id="9f051-130">Az SQL-adatbázis (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="9f051-130">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="9f051-131">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="9f051-131">Default value is 400.</span></span>

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

### <span data-ttu-id="9f051-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f051-132">-WhatIf</span></span>
<span data-ttu-id="9f051-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9f051-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f051-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f051-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f051-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f051-135">CommonParameters</span></span>
<span data-ttu-id="9f051-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f051-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f051-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f051-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f051-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f051-138">INPUTS</span></span>

### <span data-ttu-id="9f051-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9f051-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9f051-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f051-140">OUTPUTS</span></span>

### <span data-ttu-id="9f051-141">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9f051-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9f051-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f051-142">NOTES</span></span>

## <span data-ttu-id="9f051-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f051-143">RELATED LINKS</span></span>
