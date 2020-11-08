---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184620"
---
# <span data-ttu-id="944d7-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="944d7-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="944d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="944d7-102">SYNOPSIS</span></span>
<span data-ttu-id="944d7-103">Új PSSpatialSpec típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="944d7-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="944d7-104">A set-AzCosmosDBSqlIndexingPolicy paraméter értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="944d7-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="944d7-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="944d7-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="944d7-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="944d7-106">DESCRIPTION</span></span>
<span data-ttu-id="944d7-107">Az SQL API-SpatialSpec megfelelő objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="944d7-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="944d7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="944d7-108">EXAMPLES</span></span>

### <span data-ttu-id="944d7-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="944d7-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="944d7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="944d7-110">PARAMETERS</span></span>

### <span data-ttu-id="944d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="944d7-111">-DefaultProfile</span></span>
<span data-ttu-id="944d7-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="944d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="944d7-113">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="944d7-113">-Path</span></span>
<span data-ttu-id="944d7-114">A JSON-dokumentumban lévő elérési út a tárgymutatóhoz.</span><span class="sxs-lookup"><span data-stu-id="944d7-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="944d7-115">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="944d7-115">-Type</span></span>
<span data-ttu-id="944d7-116">A karakterláncok tömbje elfogadható értékekkel: pont, LineString, sokszög, többsokszögű.</span><span class="sxs-lookup"><span data-stu-id="944d7-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="944d7-117">A görbék térbeli típusa.</span><span class="sxs-lookup"><span data-stu-id="944d7-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="944d7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="944d7-118">CommonParameters</span></span>
<span data-ttu-id="944d7-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="944d7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="944d7-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="944d7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="944d7-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="944d7-121">INPUTS</span></span>

### <span data-ttu-id="944d7-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="944d7-122">None</span></span>

## <span data-ttu-id="944d7-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="944d7-123">OUTPUTS</span></span>

### <span data-ttu-id="944d7-124">Microsoft. Azure. Command. CosmosDB. models. PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="944d7-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="944d7-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="944d7-125">NOTES</span></span>

## <span data-ttu-id="944d7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="944d7-126">RELATED LINKS</span></span>
