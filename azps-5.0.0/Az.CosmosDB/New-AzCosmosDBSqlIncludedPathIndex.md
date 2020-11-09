---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
ms.openlocfilehash: f6bd378ac39c0e00975616b08d3bb9c14358d5d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299249"
---
# <span data-ttu-id="ac057-101">New-AzCosmosDBSqlIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="ac057-101">New-AzCosmosDBSqlIncludedPathIndex</span></span>

## <span data-ttu-id="ac057-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac057-102">SYNOPSIS</span></span>
<span data-ttu-id="ac057-103">Új PSIndexes típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ac057-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="ac057-104">A set-AzCosmosDBSqlIncludedPath paraméter értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="ac057-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIncludedPath.</span></span>

## <span data-ttu-id="ac057-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac057-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac057-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac057-106">DESCRIPTION</span></span>
<span data-ttu-id="ac057-107">Az SQL API IncludedPath's indexének megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="ac057-107">Object corresponding to Sql API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="ac057-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ac057-108">EXAMPLES</span></span>

### <span data-ttu-id="ac057-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac057-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="ac057-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac057-110">PARAMETERS</span></span>

### <span data-ttu-id="ac057-111">-Adattípus</span><span class="sxs-lookup"><span data-stu-id="ac057-111">-DataType</span></span>
<span data-ttu-id="ac057-112">Az az adattípus, amelyre az indexelési viselkedés vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="ac057-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="ac057-113">A lehetséges értékek a következők: "string", "szám", "pont", "sokszög", "LineString", "multisokszög"</span><span class="sxs-lookup"><span data-stu-id="ac057-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="ac057-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac057-114">-DefaultProfile</span></span>
<span data-ttu-id="ac057-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac057-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac057-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="ac057-116">-Kind</span></span>
<span data-ttu-id="ac057-117">Az index típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac057-117">Indicates the type of index.</span></span>
<span data-ttu-id="ac057-118">A lehetséges értékek a következők: "hash", "méréstartomány", "térbeli"</span><span class="sxs-lookup"><span data-stu-id="ac057-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="ac057-119">-Precíziós</span><span class="sxs-lookup"><span data-stu-id="ac057-119">-Precision</span></span>
<span data-ttu-id="ac057-120">Az index pontossága.</span><span class="sxs-lookup"><span data-stu-id="ac057-120">The precision of the index.</span></span>
<span data-ttu-id="ac057-121">-1 a maximális pontosság.</span><span class="sxs-lookup"><span data-stu-id="ac057-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="ac057-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac057-122">CommonParameters</span></span>
<span data-ttu-id="ac057-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac057-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac057-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ac057-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac057-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac057-125">INPUTS</span></span>

### <span data-ttu-id="ac057-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="ac057-126">None</span></span>

## <span data-ttu-id="ac057-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac057-127">OUTPUTS</span></span>

### <span data-ttu-id="ac057-128">Microsoft. Azure. Command. CosmosDB. models. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="ac057-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="ac057-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac057-129">NOTES</span></span>

## <span data-ttu-id="ac057-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac057-130">RELATED LINKS</span></span>
