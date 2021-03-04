---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: a086705465aea30480a4f41f6981a47d8fcc612c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938842"
---
# <span data-ttu-id="0168e-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="0168e-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="0168e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0168e-102">SYNOPSIS</span></span>
<span data-ttu-id="0168e-103">Létrehoz egy új sdb MongoDB indexet.</span><span class="sxs-lookup"><span data-stu-id="0168e-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="0168e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0168e-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0168e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0168e-105">DESCRIPTION</span></span>
<span data-ttu-id="0168e-106">A **New-AzCosmosDBMongoDBIndex létrehoz** egy új, 2010.01.010.000 mongoDB indexet.</span><span class="sxs-lookup"><span data-stu-id="0168e-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="0168e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0168e-107">EXAMPLES</span></span>

### <span data-ttu-id="0168e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0168e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="0168e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0168e-109">PARAMETERS</span></span>

### <span data-ttu-id="0168e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0168e-110">-DefaultProfile</span></span>
<span data-ttu-id="0168e-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0168e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0168e-112">-Key</span><span class="sxs-lookup"><span data-stu-id="0168e-112">-Key</span></span>
<span data-ttu-id="0168e-113">A kulcsértékek tömbje karakterláncokként.</span><span class="sxs-lookup"><span data-stu-id="0168e-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0168e-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="0168e-114">-TtlInSeconds</span></span>
<span data-ttu-id="0168e-115">Az index lejárata utáni másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="0168e-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="0168e-116">-Unique</span><span class="sxs-lookup"><span data-stu-id="0168e-116">-Unique</span></span>
<span data-ttu-id="0168e-117">Bool , amely azt jelzi, hogy az index egyedi-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="0168e-117">Bool to indicate if the index is unique or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0168e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0168e-118">CommonParameters</span></span>
<span data-ttu-id="0168e-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0168e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0168e-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0168e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0168e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0168e-121">INPUTS</span></span>

### <span data-ttu-id="0168e-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="0168e-122">None</span></span>

## <span data-ttu-id="0168e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0168e-123">OUTPUTS</span></span>

### <span data-ttu-id="0168e-124">Microsoft.Azure.Commands.EzresDB.Models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="0168e-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="0168e-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0168e-125">NOTES</span></span>

## <span data-ttu-id="0168e-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0168e-126">RELATED LINKS</span></span>
