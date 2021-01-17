---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480579"
---
# <span data-ttu-id="89aee-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="89aee-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="89aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89aee-102">SYNOPSIS</span></span>
<span data-ttu-id="89aee-103">Létrehoz egy új, PSIndexes típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="89aee-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="89aee-104">Paraméterértékként a Set-AzCosmosDBGremlinIncludedPath paraméterértékeként is átadott.</span><span class="sxs-lookup"><span data-stu-id="89aee-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="89aee-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89aee-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89aee-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89aee-106">DESCRIPTION</span></span>
<span data-ttu-id="89aee-107">A Gremlin API IncludedPath-indexének megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="89aee-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="89aee-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89aee-108">EXAMPLES</span></span>

### <span data-ttu-id="89aee-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="89aee-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="89aee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89aee-110">PARAMETERS</span></span>

### <span data-ttu-id="89aee-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="89aee-111">-DataType</span></span>
<span data-ttu-id="89aee-112">Adattípus, amelyre az indexelési viselkedés vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="89aee-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="89aee-113">Lehetséges értékek: "Karakterlánc", "Szám", "Pont", "Sokszög", "LineString", "MultiPolygon"</span><span class="sxs-lookup"><span data-stu-id="89aee-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="89aee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89aee-114">-DefaultProfile</span></span>
<span data-ttu-id="89aee-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89aee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89aee-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="89aee-116">-Kind</span></span>
<span data-ttu-id="89aee-117">Az index típusát jelzi.</span><span class="sxs-lookup"><span data-stu-id="89aee-117">Indicates the type of index.</span></span>
<span data-ttu-id="89aee-118">Lehetséges értékek: "Kivonat", "Tartomány", "Térbeli"</span><span class="sxs-lookup"><span data-stu-id="89aee-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="89aee-119">-Pontosság</span><span class="sxs-lookup"><span data-stu-id="89aee-119">-Precision</span></span>
<span data-ttu-id="89aee-120">Az index pontossága.</span><span class="sxs-lookup"><span data-stu-id="89aee-120">The precision of the index.</span></span>
<span data-ttu-id="89aee-121">-1 a maximális pontosság.</span><span class="sxs-lookup"><span data-stu-id="89aee-121">-1 is maximum precision.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89aee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89aee-122">CommonParameters</span></span>
<span data-ttu-id="89aee-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89aee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89aee-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89aee-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89aee-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89aee-125">INPUTS</span></span>

### <span data-ttu-id="89aee-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="89aee-126">None</span></span>

## <span data-ttu-id="89aee-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89aee-127">OUTPUTS</span></span>

### <span data-ttu-id="89aee-128">Microsoft.Azure.Commands.CossDB.Models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="89aee-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="89aee-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89aee-129">NOTES</span></span>

## <span data-ttu-id="89aee-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89aee-130">RELATED LINKS</span></span>
