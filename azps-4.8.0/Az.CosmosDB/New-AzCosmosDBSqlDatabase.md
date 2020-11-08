---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 2953da3747404c0b6b98992cc8a8b80573da5129
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024081"
---
# <span data-ttu-id="7e175-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7e175-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="7e175-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e175-102">SYNOPSIS</span></span>
<span data-ttu-id="7e175-103">Új CosmosDB SQL-adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="7e175-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="7e175-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e175-104">SYNTAX</span></span>

### <span data-ttu-id="7e175-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e175-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e175-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e175-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e175-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e175-107">DESCRIPTION</span></span>
<span data-ttu-id="7e175-108">Új CosmosDB SQL-adatbázis létrehozása</span><span class="sxs-lookup"><span data-stu-id="7e175-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="7e175-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7e175-109">EXAMPLES</span></span>

### <span data-ttu-id="7e175-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7e175-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="7e175-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e175-111">PARAMETERS</span></span>

### <span data-ttu-id="7e175-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7e175-112">-AccountName</span></span>
<span data-ttu-id="7e175-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="7e175-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7e175-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7e175-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7e175-115">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="7e175-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7e175-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e175-116">-Confirm</span></span>
<span data-ttu-id="7e175-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e175-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e175-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e175-118">-DefaultProfile</span></span>
<span data-ttu-id="7e175-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e175-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e175-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e175-120">-Name</span></span>
<span data-ttu-id="7e175-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7e175-121">Database name.</span></span>

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

### <span data-ttu-id="7e175-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7e175-122">-ParentObject</span></span>
<span data-ttu-id="7e175-123">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="7e175-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7e175-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e175-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e175-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7e175-125">Name of resource group.</span></span>

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

### <span data-ttu-id="7e175-126">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="7e175-126">-Throughput</span></span>
<span data-ttu-id="7e175-127">Az SQL-adatbázis (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="7e175-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="7e175-128">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="7e175-128">Default value is 400.</span></span>

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

### <span data-ttu-id="7e175-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e175-129">-WhatIf</span></span>
<span data-ttu-id="7e175-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7e175-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e175-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e175-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e175-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e175-132">CommonParameters</span></span>
<span data-ttu-id="7e175-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e175-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e175-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7e175-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e175-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e175-135">INPUTS</span></span>

### <span data-ttu-id="7e175-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7e175-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7e175-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e175-137">OUTPUTS</span></span>

### <span data-ttu-id="7e175-138">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7e175-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="7e175-139">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="7e175-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="7e175-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e175-140">NOTES</span></span>

## <span data-ttu-id="7e175-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e175-141">RELATED LINKS</span></span>
