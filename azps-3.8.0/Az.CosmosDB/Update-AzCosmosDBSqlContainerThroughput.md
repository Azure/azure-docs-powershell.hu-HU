---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: e38e10765bc9a9768efaf1598a1865ec985b376c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012185"
---
# <span data-ttu-id="d5b3d-101">Update-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="d5b3d-101">Update-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="d5b3d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b3d-103">Frissíti a CosmosDB SQL-tároló átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-103">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="d5b3d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5b3d-104">SYNTAX</span></span>

### <span data-ttu-id="d5b3d-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5b3d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5b3d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5b3d-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5b3d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5b3d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5b3d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d5b3d-108">EXAMPLES</span></span>

### <span data-ttu-id="d5b3d-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d5b3d-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlContainerThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {myDatabaseName} -Name {myContainerName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/conatiners/{myContainerName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="d5b3d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5b3d-110">PARAMETERS</span></span>

### <span data-ttu-id="d5b3d-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d5b3d-111">-AccountName</span></span>
<span data-ttu-id="d5b3d-112">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d5b3d-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d5b3d-113">-Confirm</span></span>
<span data-ttu-id="d5b3d-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5b3d-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5b3d-115">-DatabaseName</span></span>
<span data-ttu-id="d5b3d-116">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-116">Database name.</span></span>

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

### <span data-ttu-id="d5b3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b3d-117">-DefaultProfile</span></span>
<span data-ttu-id="d5b3d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5b3d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5b3d-119">-InputObject</span></span>
<span data-ttu-id="d5b3d-120">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-120">Sql Database object.</span></span>

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

### <span data-ttu-id="d5b3d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5b3d-121">-Name</span></span>
<span data-ttu-id="d5b3d-122">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-122">Container name.</span></span>

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

### <span data-ttu-id="d5b3d-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d5b3d-123">-ParentObject</span></span>
<span data-ttu-id="d5b3d-124">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-124">Sql Database object.</span></span>

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

### <span data-ttu-id="d5b3d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5b3d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d5b3d-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-126">Name of resource group.</span></span>

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

### <span data-ttu-id="d5b3d-127">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="d5b3d-127">-Throughput</span></span>
<span data-ttu-id="d5b3d-128">Az SQL-tároló (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-128">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="d5b3d-129">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b3d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5b3d-130">-WhatIf</span></span>
<span data-ttu-id="d5b3d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5b3d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5b3d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b3d-133">CommonParameters</span></span>
<span data-ttu-id="d5b3d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5b3d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b3d-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d5b3d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b3d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5b3d-136">INPUTS</span></span>

### <span data-ttu-id="d5b3d-137">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d5b3d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="d5b3d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5b3d-138">OUTPUTS</span></span>

### <span data-ttu-id="d5b3d-139">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d5b3d-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d5b3d-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5b3d-140">NOTES</span></span>

## <span data-ttu-id="d5b3d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5b3d-141">RELATED LINKS</span></span>
