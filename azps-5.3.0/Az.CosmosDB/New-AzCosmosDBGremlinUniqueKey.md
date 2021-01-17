---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477442"
---
# <span data-ttu-id="c6aab-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="c6aab-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="c6aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6aab-102">SYNOPSIS</span></span>
<span data-ttu-id="c6aab-103">Létrehoz egy új FogasDB UniqueKeyPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="c6aab-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="c6aab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c6aab-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6aab-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c6aab-105">DESCRIPTION</span></span>
<span data-ttu-id="c6aab-106">A **New-AzCosmosDBGremlinUniqueKeyPolicy** parancsmag létrehoz egy új, PSUniqueKeyPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="c6aab-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="c6aab-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c6aab-107">EXAMPLES</span></span>

### <span data-ttu-id="c6aab-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c6aab-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="c6aab-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6aab-109">PARAMETERS</span></span>

### <span data-ttu-id="c6aab-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6aab-110">-DefaultProfile</span></span>
<span data-ttu-id="c6aab-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6aab-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6aab-112">-Path</span><span class="sxs-lookup"><span data-stu-id="c6aab-112">-Path</span></span>
<span data-ttu-id="c6aab-113">Útvonalértékeket tartalmazó karakterlánc tömbje</span><span class="sxs-lookup"><span data-stu-id="c6aab-113">Array of string of path values</span></span>

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

### <span data-ttu-id="c6aab-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6aab-114">CommonParameters</span></span>
<span data-ttu-id="c6aab-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6aab-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6aab-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6aab-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6aab-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6aab-117">INPUTS</span></span>

### <span data-ttu-id="c6aab-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="c6aab-118">None</span></span>

## <span data-ttu-id="c6aab-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6aab-119">OUTPUTS</span></span>

### <span data-ttu-id="c6aab-120">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="c6aab-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="c6aab-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c6aab-121">NOTES</span></span>

## <span data-ttu-id="c6aab-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6aab-122">RELATED LINKS</span></span>
