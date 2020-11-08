---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025447"
---
# <span data-ttu-id="01729-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="01729-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="01729-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01729-102">SYNOPSIS</span></span>
<span data-ttu-id="01729-103">Új CosmosDB-IndexingPolicy objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="01729-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="01729-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01729-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01729-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01729-105">DESCRIPTION</span></span>
<span data-ttu-id="01729-106">A **New-AzCosmosDBGremlinIndexingPolicy** parancsmag új, PSIndexingPolicy típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="01729-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="01729-107">Példák</span><span class="sxs-lookup"><span data-stu-id="01729-107">EXAMPLES</span></span>

### <span data-ttu-id="01729-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="01729-108">Example 1</span></span>
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

<span data-ttu-id="01729-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="01729-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="01729-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01729-110">PARAMETERS</span></span>

### <span data-ttu-id="01729-111">-Automatikus</span><span class="sxs-lookup"><span data-stu-id="01729-111">-Automatic</span></span>
<span data-ttu-id="01729-112">Bool annak jelzése, hogy az indexelő házirend automatikus-e</span><span class="sxs-lookup"><span data-stu-id="01729-112">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="01729-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="01729-113">-CompositePath</span></span>
<span data-ttu-id="01729-114">A Microsoft. Azure. commands. CosmosDB. PSCompositePath fájltípusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="01729-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="01729-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01729-115">-DefaultProfile</span></span>
<span data-ttu-id="01729-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01729-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01729-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="01729-117">-ExcludedPath</span></span>
<span data-ttu-id="01729-118">A excludedPath tartalmazó karakterláncok tömbje (az Azure Cosmos DB szolgáltatásban kizárt JSON-dokumentumon belül az elérési utat adja meg.)  elemek.</span><span class="sxs-lookup"><span data-stu-id="01729-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="01729-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="01729-119">-IncludedPath</span></span>
<span data-ttu-id="01729-120">A includedPath tartalmazó karakterláncok tömbje (az Azure Cosmos DB szolgáltatás részét képező JSON-dokumentumon belül az elérési utat adja meg.) elemek.</span><span class="sxs-lookup"><span data-stu-id="01729-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="01729-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="01729-121">-IndexingMode</span></span>
<span data-ttu-id="01729-122">Az indexelési mód jelzése.</span><span class="sxs-lookup"><span data-stu-id="01729-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="01729-123">A lehetséges értékek a következők: "konzisztens", "lusta", "nincs"</span><span class="sxs-lookup"><span data-stu-id="01729-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="01729-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="01729-124">-SpatialSpec</span></span>
<span data-ttu-id="01729-125">A Microsoft. Azure. commands. CosmosDB. PSSpatialSpec fájltípusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="01729-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="01729-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01729-126">CommonParameters</span></span>
<span data-ttu-id="01729-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01729-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01729-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="01729-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01729-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01729-129">INPUTS</span></span>

### <span data-ttu-id="01729-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="01729-130">None</span></span>

## <span data-ttu-id="01729-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01729-131">OUTPUTS</span></span>

### <span data-ttu-id="01729-132">Microsoft. Azure. Command. CosmosDB. models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="01729-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="01729-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01729-133">NOTES</span></span>

## <span data-ttu-id="01729-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01729-134">RELATED LINKS</span></span>
