---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025460"
---
# <span data-ttu-id="964f9-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="964f9-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="964f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="964f9-102">SYNOPSIS</span></span>
<span data-ttu-id="964f9-103">Új PSCompositePath típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="964f9-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="964f9-104">A set-AzCosmosDBGremlinGraph paraméter értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="964f9-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="964f9-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="964f9-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="964f9-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="964f9-106">DESCRIPTION</span></span>
<span data-ttu-id="964f9-107">Az Gremlin API CompositePath megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="964f9-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="964f9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="964f9-108">EXAMPLES</span></span>

### <span data-ttu-id="964f9-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="964f9-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="964f9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="964f9-110">PARAMETERS</span></span>

### <span data-ttu-id="964f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964f9-111">-DefaultProfile</span></span>
<span data-ttu-id="964f9-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="964f9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="964f9-113">-Order (rendelés)</span><span class="sxs-lookup"><span data-stu-id="964f9-113">-Order</span></span>
<span data-ttu-id="964f9-114">Az összetett görbékhez beolvassa vagy beállítja a rendezési sorrendet.</span><span class="sxs-lookup"><span data-stu-id="964f9-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="964f9-115">A lehetséges értékek a következők: "növekvő", "csökkenő"</span><span class="sxs-lookup"><span data-stu-id="964f9-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="964f9-116">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="964f9-116">-Path</span></span>
<span data-ttu-id="964f9-117">Az az elérési út, amelyre az indexelési viselkedés vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="964f9-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="964f9-118">Az index elérési útja általában a root karakterrel kezdődik és a végződés a helyettesítő karakterrel (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="964f9-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="964f9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964f9-119">CommonParameters</span></span>
<span data-ttu-id="964f9-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="964f9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964f9-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="964f9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964f9-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="964f9-122">INPUTS</span></span>

### <span data-ttu-id="964f9-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="964f9-123">None</span></span>

## <span data-ttu-id="964f9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="964f9-124">OUTPUTS</span></span>

### <span data-ttu-id="964f9-125">Microsoft. Azure. Command. CosmosDB. models. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="964f9-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="964f9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="964f9-126">NOTES</span></span>

## <span data-ttu-id="964f9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="964f9-127">RELATED LINKS</span></span>
