---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204630"
---
# <span data-ttu-id="ba22b-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="ba22b-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="ba22b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba22b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba22b-103">Létrehoz egy új TárolóDB Sql IndexingPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="ba22b-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="ba22b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba22b-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba22b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba22b-105">DESCRIPTION</span></span>
<span data-ttu-id="ba22b-106">A **New-AzCosmosDBSqlIndexingPolicy** parancsmag létrehoz egy új, PSSqlIndexingPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="ba22b-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="ba22b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba22b-107">EXAMPLES</span></span>

### <span data-ttu-id="ba22b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ba22b-108">Example 1</span></span>
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

## <span data-ttu-id="ba22b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba22b-109">PARAMETERS</span></span>

### <span data-ttu-id="ba22b-110">-Automatic</span><span class="sxs-lookup"><span data-stu-id="ba22b-110">-Automatic</span></span>
<span data-ttu-id="ba22b-111">Bool to indicate if the indexing policy is automatic</span><span class="sxs-lookup"><span data-stu-id="ba22b-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="ba22b-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="ba22b-112">-CompositePath</span></span>
<span data-ttu-id="ba22b-113">A Microsoft.Azure.Commands.FogósDB.PSCompositePath típusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="ba22b-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="ba22b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba22b-114">-DefaultProfile</span></span>
<span data-ttu-id="ba22b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba22b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba22b-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="ba22b-116">-ExcludedPath</span></span>
<span data-ttu-id="ba22b-117">Az excludedPath karakterláncok tömbje(Egy JSON-dokumentumon belüli elérési utat ad meg, amely nem lesz kizárva az Azure Azure Tok DB szolgáltatásban.)  elemet.</span><span class="sxs-lookup"><span data-stu-id="ba22b-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="ba22b-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="ba22b-118">-IncludedPath</span></span>
<span data-ttu-id="ba22b-119">A mellékeltPath-fájlokat tartalmazó karakterláncok tömbje (Megadja az Azure Azure Karakterlánc-adatbázis szolgáltatásban szerepelni szükséges elérési utat egy JSON-dokumentumon belül.</span><span class="sxs-lookup"><span data-stu-id="ba22b-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="ba22b-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="ba22b-120">-IndexingMode</span></span>
<span data-ttu-id="ba22b-121">az indexelési módot jelzi.</span><span class="sxs-lookup"><span data-stu-id="ba22b-121">indicates the indexing mode.</span></span>
<span data-ttu-id="ba22b-122">Lehetséges értékek: "Konzisztens", "Tetszető", "Nincs"</span><span class="sxs-lookup"><span data-stu-id="ba22b-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="ba22b-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="ba22b-123">-SpatialSpec</span></span>
<span data-ttu-id="ba22b-124">Microsoft.Azure.Commands.FogsDB.PSSpatialSpec típusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="ba22b-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="ba22b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba22b-125">CommonParameters</span></span>
<span data-ttu-id="ba22b-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba22b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba22b-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba22b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba22b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba22b-128">INPUTS</span></span>

### <span data-ttu-id="ba22b-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="ba22b-129">None</span></span>

## <span data-ttu-id="ba22b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba22b-130">OUTPUTS</span></span>

### <span data-ttu-id="ba22b-131">Microsoft.Azure.Commands.EzresDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="ba22b-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="ba22b-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba22b-132">NOTES</span></span>

## <span data-ttu-id="ba22b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba22b-133">RELATED LINKS</span></span>
