---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480573"
---
# <span data-ttu-id="69d28-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="69d28-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="69d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69d28-102">SYNOPSIS</span></span>
<span data-ttu-id="69d28-103">Új PSSpatialSpec típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="69d28-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="69d28-104">Paraméterértékként a Set-AzCosmosDBGremlinIndexingPolicy paraméterértékeként is át lehetadva.</span><span class="sxs-lookup"><span data-stu-id="69d28-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="69d28-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="69d28-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69d28-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="69d28-106">DESCRIPTION</span></span>
<span data-ttu-id="69d28-107">A Gremlin API TérinektikaiSpecének megfelelő objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="69d28-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="69d28-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="69d28-108">EXAMPLES</span></span>

### <span data-ttu-id="69d28-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="69d28-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="69d28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69d28-110">PARAMETERS</span></span>

### <span data-ttu-id="69d28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69d28-111">-DefaultProfile</span></span>
<span data-ttu-id="69d28-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69d28-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69d28-113">-Path</span><span class="sxs-lookup"><span data-stu-id="69d28-113">-Path</span></span>
<span data-ttu-id="69d28-114">A JSON-dokumentum indexelési útvonala.</span><span class="sxs-lookup"><span data-stu-id="69d28-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="69d28-115">-Type</span><span class="sxs-lookup"><span data-stu-id="69d28-115">-Type</span></span>
<span data-ttu-id="69d28-116">Elfogadható értékeket tartalmazó karakterláncok tömbje: Pont, Sorkarakterlánc, Sokszög, TöbbPolygon.</span><span class="sxs-lookup"><span data-stu-id="69d28-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="69d28-117">Az útvonalak térbeli típusát ábrázolja.</span><span class="sxs-lookup"><span data-stu-id="69d28-117">Represent's paths spatial type.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69d28-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d28-118">CommonParameters</span></span>
<span data-ttu-id="69d28-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69d28-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d28-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69d28-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d28-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69d28-121">INPUTS</span></span>

### <span data-ttu-id="69d28-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="69d28-122">None</span></span>

## <span data-ttu-id="69d28-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69d28-123">OUTPUTS</span></span>

### <span data-ttu-id="69d28-124">Microsoft.Azure.Commands.CossDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="69d28-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="69d28-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="69d28-125">NOTES</span></span>

## <span data-ttu-id="69d28-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69d28-126">RELATED LINKS</span></span>
