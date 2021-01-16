---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348978"
---
# <span data-ttu-id="60a89-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="60a89-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="60a89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60a89-102">SYNOPSIS</span></span>
<span data-ttu-id="60a89-103">Új, PSIncludedPath típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="60a89-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="60a89-104">A Set-AzCosmosDBGremlinGraph paraméterértékeként is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="60a89-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="60a89-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60a89-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a89-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60a89-106">DESCRIPTION</span></span>
<span data-ttu-id="60a89-107">A Gremlin API IncludedPath-jának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="60a89-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="60a89-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60a89-108">EXAMPLES</span></span>

### <span data-ttu-id="60a89-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="60a89-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="60a89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60a89-110">PARAMETERS</span></span>

### <span data-ttu-id="60a89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a89-111">-DefaultProfile</span></span>
<span data-ttu-id="60a89-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60a89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a89-113">-Index</span><span class="sxs-lookup"><span data-stu-id="60a89-113">-Index</span></span>
<span data-ttu-id="60a89-114">Az elérési út indexének listája</span><span class="sxs-lookup"><span data-stu-id="60a89-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="60a89-115">-Path</span><span class="sxs-lookup"><span data-stu-id="60a89-115">-Path</span></span>
<span data-ttu-id="60a89-116">Az az elérési út, amelyre az indexelési viselkedés vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="60a89-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="60a89-117">Az index elérési utak általában a gyökértől kezdődnek, és helyettesítő karakterekkel (/elérési út/\*) végződnek.</span><span class="sxs-lookup"><span data-stu-id="60a89-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="60a89-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a89-118">CommonParameters</span></span>
<span data-ttu-id="60a89-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a89-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a89-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60a89-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a89-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60a89-121">INPUTS</span></span>

### <span data-ttu-id="60a89-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="60a89-122">None</span></span>

## <span data-ttu-id="60a89-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60a89-123">OUTPUTS</span></span>

### <span data-ttu-id="60a89-124">Microsoft.Azure.Commands.EzresDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="60a89-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="60a89-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60a89-125">NOTES</span></span>

## <span data-ttu-id="60a89-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60a89-126">RELATED LINKS</span></span>
