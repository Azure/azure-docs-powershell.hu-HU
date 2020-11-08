---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 2914284849fa9a00e3cb2d0b1c96c1efd905e9e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010551"
---
# <span data-ttu-id="a2357-101">Set-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="a2357-101">Set-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="a2357-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2357-102">SYNOPSIS</span></span>
<span data-ttu-id="a2357-103">Új CosmosDB hoz létre, vagy frissít egy meglévő SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="a2357-103">Creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="a2357-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2357-104">SYNTAX</span></span>

### <span data-ttu-id="a2357-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2357-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2357-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2357-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2357-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2357-107">DESCRIPTION</span></span>
<span data-ttu-id="a2357-108">A **set-AzCosmosDBSqlStoredProcedure** parancsmag új SQL-StoredProcedure hoz létre, vagy frissít egy meglévő CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a2357-108">The **Set-AzCosmosDBSqlStoredProcedure** cmdlet creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="a2357-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a2357-109">EXAMPLES</span></span>

### <span data-ttu-id="a2357-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2357-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName} -Body {sampleBody}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
SqlStoredProcedureGetResultsId :
Body                           :
_rid                           :
_ts                            :
_etag                          :
```

## <span data-ttu-id="a2357-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2357-111">PARAMETERS</span></span>

### <span data-ttu-id="a2357-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a2357-112">-AccountName</span></span>
<span data-ttu-id="a2357-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a2357-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a2357-114">-Body</span><span class="sxs-lookup"><span data-stu-id="a2357-114">-Body</span></span>
<span data-ttu-id="a2357-115">A tárolt eljárás törzse</span><span class="sxs-lookup"><span data-stu-id="a2357-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="a2357-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2357-116">-Confirm</span></span>
<span data-ttu-id="a2357-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2357-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2357-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a2357-118">-ContainerName</span></span>
<span data-ttu-id="a2357-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="a2357-119">Container name.</span></span>

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

### <span data-ttu-id="a2357-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2357-120">-DatabaseName</span></span>
<span data-ttu-id="a2357-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a2357-121">Database name.</span></span>

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

### <span data-ttu-id="a2357-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2357-122">-DefaultProfile</span></span>
<span data-ttu-id="a2357-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2357-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2357-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2357-124">-InputObject</span></span>
<span data-ttu-id="a2357-125">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="a2357-125">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2357-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2357-126">-Name</span></span>
<span data-ttu-id="a2357-127">A Prcodecure tárolt név.</span><span class="sxs-lookup"><span data-stu-id="a2357-127">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="a2357-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2357-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2357-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2357-129">Name of resource group.</span></span>

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

### <span data-ttu-id="a2357-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2357-130">-WhatIf</span></span>
<span data-ttu-id="a2357-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2357-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2357-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2357-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2357-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2357-133">CommonParameters</span></span>
<span data-ttu-id="a2357-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2357-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2357-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a2357-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2357-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2357-136">INPUTS</span></span>

### <span data-ttu-id="a2357-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="a2357-137">None</span></span>

## <span data-ttu-id="a2357-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2357-138">OUTPUTS</span></span>

### <span data-ttu-id="a2357-139">Microsoft. Azure. Command. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="a2357-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="a2357-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2357-140">NOTES</span></span>

## <span data-ttu-id="a2357-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2357-141">RELATED LINKS</span></span>
