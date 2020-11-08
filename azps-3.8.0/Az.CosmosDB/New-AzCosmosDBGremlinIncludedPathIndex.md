---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012085"
---
# <span data-ttu-id="e8236-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="e8236-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="e8236-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8236-102">SYNOPSIS</span></span>
<span data-ttu-id="e8236-103">Új PSIndexes típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="e8236-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="e8236-104">A set-AzCosmosDBGremlinIncludedPath paraméter értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="e8236-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="e8236-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8236-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8236-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8236-106">DESCRIPTION</span></span>
<span data-ttu-id="e8236-107">Az Gremlin API IncludedPath's indexének megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="e8236-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="e8236-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e8236-108">EXAMPLES</span></span>

### <span data-ttu-id="e8236-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8236-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="e8236-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8236-110">PARAMETERS</span></span>

### <span data-ttu-id="e8236-111">-Adattípus</span><span class="sxs-lookup"><span data-stu-id="e8236-111">-DataType</span></span>
<span data-ttu-id="e8236-112">Az az adattípus, amelyre az indexelési viselkedés vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="e8236-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="e8236-113">A lehetséges értékek a következők: "string", "szám", "pont", "sokszög", "LineString", "multisokszög"</span><span class="sxs-lookup"><span data-stu-id="e8236-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="e8236-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8236-114">-DefaultProfile</span></span>
<span data-ttu-id="e8236-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8236-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8236-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="e8236-116">-Kind</span></span>
<span data-ttu-id="e8236-117">Az index típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8236-117">Indicates the type of index.</span></span>
<span data-ttu-id="e8236-118">A lehetséges értékek a következők: "hash", "méréstartomány", "térbeli"</span><span class="sxs-lookup"><span data-stu-id="e8236-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="e8236-119">-Precíziós</span><span class="sxs-lookup"><span data-stu-id="e8236-119">-Precision</span></span>
<span data-ttu-id="e8236-120">Az index pontossága.</span><span class="sxs-lookup"><span data-stu-id="e8236-120">The precision of the index.</span></span>
<span data-ttu-id="e8236-121">-1 a maximális pontosság.</span><span class="sxs-lookup"><span data-stu-id="e8236-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="e8236-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8236-122">CommonParameters</span></span>
<span data-ttu-id="e8236-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8236-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8236-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e8236-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8236-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8236-125">INPUTS</span></span>

### <span data-ttu-id="e8236-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="e8236-126">None</span></span>

## <span data-ttu-id="e8236-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8236-127">OUTPUTS</span></span>

### <span data-ttu-id="e8236-128">Microsoft. Azure. Command. CosmosDB. models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="e8236-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="e8236-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8236-129">NOTES</span></span>

## <span data-ttu-id="e8236-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8236-130">RELATED LINKS</span></span>
