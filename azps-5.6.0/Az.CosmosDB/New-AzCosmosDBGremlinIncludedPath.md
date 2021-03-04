---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: c3022ea8f2ddbfbf0fc2a51bfd63706c4a8ea884
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921345"
---
# <span data-ttu-id="37d43-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="37d43-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="37d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37d43-102">SYNOPSIS</span></span>
<span data-ttu-id="37d43-103">Új, PSIncludedPath típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="37d43-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="37d43-104">A Set-AzCosmosDBGremlinGraph paraméterértékeként is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="37d43-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="37d43-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37d43-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37d43-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37d43-106">DESCRIPTION</span></span>
<span data-ttu-id="37d43-107">A Gremlin API IncludedPath-jának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="37d43-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="37d43-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37d43-108">EXAMPLES</span></span>

### <span data-ttu-id="37d43-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="37d43-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="37d43-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37d43-110">PARAMETERS</span></span>

### <span data-ttu-id="37d43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d43-111">-DefaultProfile</span></span>
<span data-ttu-id="37d43-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37d43-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37d43-113">-Index</span><span class="sxs-lookup"><span data-stu-id="37d43-113">-Index</span></span>
<span data-ttu-id="37d43-114">Az elérési út indexének listája</span><span class="sxs-lookup"><span data-stu-id="37d43-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d43-115">-Path</span><span class="sxs-lookup"><span data-stu-id="37d43-115">-Path</span></span>
<span data-ttu-id="37d43-116">Az az elérési út, amelyre az indexelési viselkedés vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="37d43-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="37d43-117">Az index elérési utak általában a gyökértől kezdődnek, és helyettesítő karakterekkel (/elérési út/\*) végződnek.</span><span class="sxs-lookup"><span data-stu-id="37d43-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="37d43-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d43-118">CommonParameters</span></span>
<span data-ttu-id="37d43-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d43-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d43-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37d43-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d43-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37d43-121">INPUTS</span></span>

### <span data-ttu-id="37d43-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="37d43-122">None</span></span>

## <span data-ttu-id="37d43-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37d43-123">OUTPUTS</span></span>

### <span data-ttu-id="37d43-124">Microsoft.Azure.Commands.EzresDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="37d43-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="37d43-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37d43-125">NOTES</span></span>

## <span data-ttu-id="37d43-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37d43-126">RELATED LINKS</span></span>
