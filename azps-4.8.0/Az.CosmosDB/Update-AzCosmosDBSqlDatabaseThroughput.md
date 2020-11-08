---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 324350329b166ab3a41f7e2bd8b59af1b9efdcb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184607"
---
# <span data-ttu-id="64d53-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="64d53-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="64d53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64d53-102">SYNOPSIS</span></span>
<span data-ttu-id="64d53-103">Frissíti a CosmosDB SQL-adatbázisok átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="64d53-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="64d53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64d53-104">SYNTAX</span></span>

### <span data-ttu-id="64d53-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64d53-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64d53-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64d53-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64d53-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64d53-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64d53-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="64d53-108">DESCRIPTION</span></span>
<span data-ttu-id="64d53-109">Frissíti a CosmosDB SQL-adatbázisok átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="64d53-109">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="64d53-110">Példák</span><span class="sxs-lookup"><span data-stu-id="64d53-110">EXAMPLES</span></span>

### <span data-ttu-id="64d53-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="64d53-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="64d53-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64d53-112">PARAMETERS</span></span>

### <span data-ttu-id="64d53-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="64d53-113">-AccountName</span></span>
<span data-ttu-id="64d53-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="64d53-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="64d53-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="64d53-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="64d53-116">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="64d53-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="64d53-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64d53-117">-Confirm</span></span>
<span data-ttu-id="64d53-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64d53-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64d53-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d53-119">-DefaultProfile</span></span>
<span data-ttu-id="64d53-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64d53-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64d53-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64d53-121">-InputObject</span></span>
<span data-ttu-id="64d53-122">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="64d53-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="64d53-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64d53-123">-Name</span></span>
<span data-ttu-id="64d53-124">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="64d53-124">Database name.</span></span>

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

### <span data-ttu-id="64d53-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="64d53-125">-ParentObject</span></span>
<span data-ttu-id="64d53-126">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="64d53-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="64d53-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d53-127">-ResourceGroupName</span></span>
<span data-ttu-id="64d53-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="64d53-128">Name of resource group.</span></span>

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

### <span data-ttu-id="64d53-129">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="64d53-129">-Throughput</span></span>
<span data-ttu-id="64d53-130">Az SQL-adatbázis (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="64d53-130">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="64d53-131">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="64d53-131">Default value is 400.</span></span>

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

### <span data-ttu-id="64d53-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d53-132">-WhatIf</span></span>
<span data-ttu-id="64d53-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64d53-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64d53-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64d53-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64d53-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d53-135">CommonParameters</span></span>
<span data-ttu-id="64d53-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64d53-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d53-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="64d53-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d53-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64d53-138">INPUTS</span></span>

### <span data-ttu-id="64d53-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="64d53-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="64d53-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64d53-140">OUTPUTS</span></span>

### <span data-ttu-id="64d53-141">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="64d53-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="64d53-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64d53-142">NOTES</span></span>

## <span data-ttu-id="64d53-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64d53-143">RELATED LINKS</span></span>
