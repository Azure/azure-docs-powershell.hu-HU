---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 27363873996505a15e8eccd3dcb3620a2f88c1a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845145"
---
# <span data-ttu-id="d885e-101">Set-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="d885e-101">Set-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="d885e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d885e-102">SYNOPSIS</span></span>
<span data-ttu-id="d885e-103">Új CosmosDB hoz létre, vagy frissít egy meglévő SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="d885e-103">Creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="d885e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d885e-104">SYNTAX</span></span>

### <span data-ttu-id="d885e-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d885e-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d885e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d885e-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d885e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d885e-107">DESCRIPTION</span></span>
<span data-ttu-id="d885e-108">A **set-AzCosmosDBSqlUserDefinedFunction** parancsmag új SQL-UserDefinedFunction hoz létre, vagy frissít egy meglévő CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d885e-108">The **Set-AzCosmosDBSqlUserDefinedFunction** cmdlet creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="d885e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d885e-109">EXAMPLES</span></span>

### <span data-ttu-id="d885e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d885e-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {udfName} -ContainerName {containerName} -Body {sampleBody}

Name                               : {udfName}
Id                                 : {udfId}
SqlUserDefinedFunctionGetResultsId :
Body                               :
_rid                               :
_ts                                :
_etag                              :
```

## <span data-ttu-id="d885e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d885e-111">PARAMETERS</span></span>

### <span data-ttu-id="d885e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d885e-112">-AccountName</span></span>
<span data-ttu-id="d885e-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d885e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d885e-114">-Body</span><span class="sxs-lookup"><span data-stu-id="d885e-114">-Body</span></span>
<span data-ttu-id="d885e-115">A felhasználó által definiált függvény törzse.</span><span class="sxs-lookup"><span data-stu-id="d885e-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="d885e-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d885e-116">-Confirm</span></span>
<span data-ttu-id="d885e-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d885e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d885e-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d885e-118">-ContainerName</span></span>
<span data-ttu-id="d885e-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="d885e-119">Container name.</span></span>

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

### <span data-ttu-id="d885e-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d885e-120">-DatabaseName</span></span>
<span data-ttu-id="d885e-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d885e-121">Database name.</span></span>

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

### <span data-ttu-id="d885e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d885e-122">-DefaultProfile</span></span>
<span data-ttu-id="d885e-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d885e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d885e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d885e-124">-InputObject</span></span>
<span data-ttu-id="d885e-125">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="d885e-125">Sql Container object.</span></span>

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

### <span data-ttu-id="d885e-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d885e-126">-Name</span></span>
<span data-ttu-id="d885e-127">Felhasználó által definiált függvény neve.</span><span class="sxs-lookup"><span data-stu-id="d885e-127">User Defined Function Name.</span></span>

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

### <span data-ttu-id="d885e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d885e-128">-ResourceGroupName</span></span>
<span data-ttu-id="d885e-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d885e-129">Name of resource group.</span></span>

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

### <span data-ttu-id="d885e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d885e-130">-WhatIf</span></span>
<span data-ttu-id="d885e-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d885e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d885e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d885e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d885e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d885e-133">CommonParameters</span></span>
<span data-ttu-id="d885e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d885e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d885e-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d885e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d885e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d885e-136">INPUTS</span></span>

### <span data-ttu-id="d885e-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="d885e-137">None</span></span>

## <span data-ttu-id="d885e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d885e-138">OUTPUTS</span></span>

### <span data-ttu-id="d885e-139">Microsoft. Azure. Command. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="d885e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="d885e-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d885e-140">NOTES</span></span>

## <span data-ttu-id="d885e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d885e-141">RELATED LINKS</span></span>
