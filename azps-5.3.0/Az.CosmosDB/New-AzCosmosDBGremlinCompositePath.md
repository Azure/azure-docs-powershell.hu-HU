---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477458"
---
# <span data-ttu-id="d532e-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="d532e-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="d532e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d532e-102">SYNOPSIS</span></span>
<span data-ttu-id="d532e-103">Létrehoz egy új, PSCompositePath típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="d532e-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="d532e-104">A Set-AzCosmosDBGremlinGraph paraméterértékeként is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="d532e-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="d532e-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d532e-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d532e-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d532e-106">DESCRIPTION</span></span>
<span data-ttu-id="d532e-107">A Gremlin API CompositePath-jának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="d532e-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="d532e-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d532e-108">EXAMPLES</span></span>

### <span data-ttu-id="d532e-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="d532e-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="d532e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d532e-110">PARAMETERS</span></span>

### <span data-ttu-id="d532e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d532e-111">-DefaultProfile</span></span>
<span data-ttu-id="d532e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d532e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d532e-113">-Order</span><span class="sxs-lookup"><span data-stu-id="d532e-113">-Order</span></span>
<span data-ttu-id="d532e-114">Összetett elérési utak rendezési sorrendjét állítja be vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="d532e-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="d532e-115">Lehetséges értékek: "Növekvő", "Csökkenő"</span><span class="sxs-lookup"><span data-stu-id="d532e-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="d532e-116">-Path</span><span class="sxs-lookup"><span data-stu-id="d532e-116">-Path</span></span>
<span data-ttu-id="d532e-117">Az az elérési út, amelyre az indexelési viselkedés vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="d532e-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="d532e-118">Az index elérési utak általában a gyökértől kezdődnek, és helyettesítő karakterekkel (/elérési út/\*) végződnek.</span><span class="sxs-lookup"><span data-stu-id="d532e-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="d532e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d532e-119">CommonParameters</span></span>
<span data-ttu-id="d532e-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d532e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d532e-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d532e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d532e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d532e-122">INPUTS</span></span>

### <span data-ttu-id="d532e-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="d532e-123">None</span></span>

## <span data-ttu-id="d532e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d532e-124">OUTPUTS</span></span>

### <span data-ttu-id="d532e-125">Microsoft.Azure.Commands.EzresDB.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="d532e-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="d532e-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d532e-126">NOTES</span></span>

## <span data-ttu-id="d532e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d532e-127">RELATED LINKS</span></span>
