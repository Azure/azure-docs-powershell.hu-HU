---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: b3d7591bf5dd83967230f6c96c3ca5b02232e316
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930570"
---
# <span data-ttu-id="cebea-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="cebea-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="cebea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cebea-102">SYNOPSIS</span></span>
<span data-ttu-id="cebea-103">Létrehoz egy új TárolóDB Sql IndexingPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="cebea-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="cebea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cebea-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cebea-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cebea-105">DESCRIPTION</span></span>
<span data-ttu-id="cebea-106">A **New-AzCosmosDBSqlIndexingPolicy** parancsmag létrehoz egy új, PSSqlIndexingPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="cebea-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="cebea-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cebea-107">EXAMPLES</span></span>

### <span data-ttu-id="cebea-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="cebea-108">Example 1</span></span>
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

## <span data-ttu-id="cebea-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cebea-109">PARAMETERS</span></span>

### <span data-ttu-id="cebea-110">-Automatic</span><span class="sxs-lookup"><span data-stu-id="cebea-110">-Automatic</span></span>
<span data-ttu-id="cebea-111">Bool to indicate if the indexing policy is automatic</span><span class="sxs-lookup"><span data-stu-id="cebea-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="cebea-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="cebea-112">-CompositePath</span></span>
<span data-ttu-id="cebea-113">A Microsoft.Azure.Commands.FogósDB.PSCompositePath típusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="cebea-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="cebea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cebea-114">-DefaultProfile</span></span>
<span data-ttu-id="cebea-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cebea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cebea-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="cebea-116">-ExcludedPath</span></span>
<span data-ttu-id="cebea-117">Az excludedPath karakterláncok tömbje(Egy JSON-dokumentumon belüli elérési utat ad meg, amely nem lesz kizárva az Azure Tok DB szolgáltatásban.)  elemet.</span><span class="sxs-lookup"><span data-stu-id="cebea-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="cebea-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="cebea-118">-IncludedPath</span></span>
<span data-ttu-id="cebea-119">A mellékeltPath-fájlokat tartalmazó karakterláncok tömbje (Megadja az Azure Azure Karakterlánc-adatbázis szolgáltatásban szerepelni szükséges elérési utat egy JSON-dokumentumon belül.</span><span class="sxs-lookup"><span data-stu-id="cebea-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="cebea-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="cebea-120">-IndexingMode</span></span>
<span data-ttu-id="cebea-121">az indexelési módot jelzi.</span><span class="sxs-lookup"><span data-stu-id="cebea-121">indicates the indexing mode.</span></span>
<span data-ttu-id="cebea-122">A lehetséges értékek a következők: "Konzisztens", "Lassú", "Nincs"</span><span class="sxs-lookup"><span data-stu-id="cebea-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="cebea-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="cebea-123">-SpatialSpec</span></span>
<span data-ttu-id="cebea-124">Microsoft.Azure.Commands.FogsDB.PSSpatialSpec típusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="cebea-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="cebea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebea-125">CommonParameters</span></span>
<span data-ttu-id="cebea-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cebea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebea-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cebea-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebea-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cebea-128">INPUTS</span></span>

### <span data-ttu-id="cebea-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="cebea-129">None</span></span>

## <span data-ttu-id="cebea-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cebea-130">OUTPUTS</span></span>

### <span data-ttu-id="cebea-131">Microsoft.Azure.Commands.EzresDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="cebea-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="cebea-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cebea-132">NOTES</span></span>

## <span data-ttu-id="cebea-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cebea-133">RELATED LINKS</span></span>
