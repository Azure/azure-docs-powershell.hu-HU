---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164035"
---
# <span data-ttu-id="ba454-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="ba454-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="ba454-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba454-102">SYNOPSIS</span></span>
<span data-ttu-id="ba454-103">Létrehoz egy új, AbDB indexelésiPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="ba454-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="ba454-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba454-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba454-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba454-105">DESCRIPTION</span></span>
<span data-ttu-id="ba454-106">A **New-AzCosmosDBGremlinIndexingPolicy** parancsmag létrehoz egy új, PSIndexingPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="ba454-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="ba454-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba454-107">EXAMPLES</span></span>

### <span data-ttu-id="ba454-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ba454-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

<span data-ttu-id="ba454-109">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="ba454-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ba454-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba454-110">PARAMETERS</span></span>

### <span data-ttu-id="ba454-111">-Automatic</span><span class="sxs-lookup"><span data-stu-id="ba454-111">-Automatic</span></span>
<span data-ttu-id="ba454-112">Bool to indicate if the indexing policy is automatic</span><span class="sxs-lookup"><span data-stu-id="ba454-112">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="ba454-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="ba454-113">-CompositePath</span></span>
<span data-ttu-id="ba454-114">A Microsoft.Azure.Commands.FogósDB.PSCompositePath típusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="ba454-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="ba454-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba454-115">-DefaultProfile</span></span>
<span data-ttu-id="ba454-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba454-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba454-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="ba454-117">-ExcludedPath</span></span>
<span data-ttu-id="ba454-118">Az excludedPath karakterláncok tömbje(Egy JSON-dokumentumon belüli elérési utat ad meg, amely nem lesz kizárva az Azure Tok DB szolgáltatásban.)  elemet.</span><span class="sxs-lookup"><span data-stu-id="ba454-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="ba454-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="ba454-119">-IncludedPath</span></span>
<span data-ttu-id="ba454-120">A mellékeltPath-fájlokat tartalmazó karakterláncok tömbje (Megadja az Azure Azure Karakterlánc-adatbázis szolgáltatásban szerepelni szükséges elérési utat egy JSON-dokumentumon belül.</span><span class="sxs-lookup"><span data-stu-id="ba454-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="ba454-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="ba454-121">-IndexingMode</span></span>
<span data-ttu-id="ba454-122">Az indexelési módot jelzi.</span><span class="sxs-lookup"><span data-stu-id="ba454-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="ba454-123">A lehetséges értékek a következők: "Konzisztens", "Lassú", "Nincs"</span><span class="sxs-lookup"><span data-stu-id="ba454-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="ba454-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="ba454-124">-SpatialSpec</span></span>
<span data-ttu-id="ba454-125">Microsoft.Azure.Commands.FogsDB.PSSpatialSpec típusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="ba454-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="ba454-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba454-126">CommonParameters</span></span>
<span data-ttu-id="ba454-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba454-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba454-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba454-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba454-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba454-129">INPUTS</span></span>

### <span data-ttu-id="ba454-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="ba454-130">None</span></span>

## <span data-ttu-id="ba454-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba454-131">OUTPUTS</span></span>

### <span data-ttu-id="ba454-132">Microsoft.Azure.Commands.CossDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="ba454-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="ba454-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba454-133">NOTES</span></span>

## <span data-ttu-id="ba454-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba454-134">RELATED LINKS</span></span>
