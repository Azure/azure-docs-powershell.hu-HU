---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299324"
---
# <span data-ttu-id="327b1-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="327b1-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="327b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="327b1-102">SYNOPSIS</span></span>
<span data-ttu-id="327b1-103">Új PSIncludedPath típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="327b1-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="327b1-104">A set-AzCosmosDBGremlinGraph paraméter értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="327b1-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="327b1-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="327b1-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="327b1-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="327b1-106">DESCRIPTION</span></span>
<span data-ttu-id="327b1-107">Az Gremlin API IncludedPath megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="327b1-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="327b1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="327b1-108">EXAMPLES</span></span>

### <span data-ttu-id="327b1-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="327b1-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="327b1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="327b1-110">PARAMETERS</span></span>

### <span data-ttu-id="327b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327b1-111">-DefaultProfile</span></span>
<span data-ttu-id="327b1-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="327b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="327b1-113">– Index</span><span class="sxs-lookup"><span data-stu-id="327b1-113">-Index</span></span>
<span data-ttu-id="327b1-114">Az útvonal indexelésének listája</span><span class="sxs-lookup"><span data-stu-id="327b1-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="327b1-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="327b1-115">-Path</span></span>
<span data-ttu-id="327b1-116">Az az elérési út, amelyre az indexelési viselkedés vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="327b1-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="327b1-117">Az index elérési útja általában a root karakterrel kezdődik és a végződés a helyettesítő karakterrel (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="327b1-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="327b1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327b1-118">CommonParameters</span></span>
<span data-ttu-id="327b1-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="327b1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327b1-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="327b1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327b1-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="327b1-121">INPUTS</span></span>

### <span data-ttu-id="327b1-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="327b1-122">None</span></span>

## <span data-ttu-id="327b1-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="327b1-123">OUTPUTS</span></span>

### <span data-ttu-id="327b1-124">Microsoft. Azure. Command. CosmosDB. models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="327b1-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="327b1-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="327b1-125">NOTES</span></span>

## <span data-ttu-id="327b1-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="327b1-126">RELATED LINKS</span></span>
