---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013630"
---
# <span data-ttu-id="e9fd7-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e9fd7-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="e9fd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="e9fd7-103">Új CosmosDB SQL-IndexingPolicy objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="e9fd7-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="e9fd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9fd7-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9fd7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="e9fd7-106">A **New-AzCosmosDBSqlIndexingPolicy** parancsmag új, PSSqlIndexingPolicy típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e9fd7-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="e9fd7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e9fd7-107">EXAMPLES</span></span>

### <span data-ttu-id="e9fd7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e9fd7-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $ipath2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $IncludedPath = New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>  $SpatialSpec = New-AzCosmosDBSqlSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\> $cp1 = New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending
PS C:\>  $cp2 = New-AzCosmosDBSqlCompositePath -Path "/aberc" -Order Descending
PS C:\> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\> New-AzCosmosDBSqlIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent

Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

## <span data-ttu-id="e9fd7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9fd7-109">PARAMETERS</span></span>

### <span data-ttu-id="e9fd7-110">-Automatikus</span><span class="sxs-lookup"><span data-stu-id="e9fd7-110">-Automatic</span></span>
<span data-ttu-id="e9fd7-111">Bool annak jelzése, hogy az indexelő házirend automatikus-e</span><span class="sxs-lookup"><span data-stu-id="e9fd7-111">Bool to indicate if the indexing policy is automatic</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd7-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="e9fd7-112">-CompositePath</span></span>
<span data-ttu-id="e9fd7-113">A Microsoft. Azure. commands. CosmosDB. PSCompositePath fájltípusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="e9fd7-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

```yaml
Type: PSCompositePath[][]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9fd7-114">-DefaultProfile</span></span>
<span data-ttu-id="e9fd7-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9fd7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9fd7-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="e9fd7-116">-ExcludedPath</span></span>
<span data-ttu-id="e9fd7-117">A excludedPath tartalmazó karakterláncok tömbje (az Azure Cosmos DB szolgáltatásban kizárt JSON-dokumentumon belül az elérési utat adja meg.)  elemek.</span><span class="sxs-lookup"><span data-stu-id="e9fd7-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd7-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="e9fd7-118">-IncludedPath</span></span>
<span data-ttu-id="e9fd7-119">A includedPath tartalmazó karakterláncok tömbje (az Azure Cosmos DB szolgáltatás részét képező JSON-dokumentumon belül az elérési utat adja meg.) elemek.</span><span class="sxs-lookup"><span data-stu-id="e9fd7-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd7-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="e9fd7-120">-IndexingMode</span></span>
<span data-ttu-id="e9fd7-121">az indexelési mód jelzése.</span><span class="sxs-lookup"><span data-stu-id="e9fd7-121">indicates the indexing mode.</span></span>
<span data-ttu-id="e9fd7-122">A lehetséges értékek a következők: "konzisztens", "lusta", "nincs"</span><span class="sxs-lookup"><span data-stu-id="e9fd7-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="e9fd7-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="e9fd7-123">-SpatialSpec</span></span>
<span data-ttu-id="e9fd7-124">A Microsoft. Azure. commands. CosmosDB. PSSpatialSpec fájltípusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="e9fd7-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9fd7-125">CommonParameters</span></span>
<span data-ttu-id="e9fd7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9fd7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9fd7-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e9fd7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9fd7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9fd7-128">INPUTS</span></span>

### <span data-ttu-id="e9fd7-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="e9fd7-129">None</span></span>

## <span data-ttu-id="e9fd7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9fd7-130">OUTPUTS</span></span>

### <span data-ttu-id="e9fd7-131">Microsoft. Azure. Command. CosmosDB. models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e9fd7-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="e9fd7-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9fd7-132">NOTES</span></span>

## <span data-ttu-id="e9fd7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9fd7-133">RELATED LINKS</span></span>
