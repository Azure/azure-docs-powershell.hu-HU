---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: b2984ffc8b2c268f5298d88e9dc64e0729798e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943041"
---
# <span data-ttu-id="11640-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="11640-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="11640-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11640-102">SYNOPSIS</span></span>
<span data-ttu-id="11640-103">Létrehoz egy új FogasDB UniqueKeyPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="11640-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="11640-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11640-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11640-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11640-105">DESCRIPTION</span></span>
<span data-ttu-id="11640-106">A **New-AzCosmosDBGremlinUniqueKeyPolicy** parancsmag létrehoz egy új, PSUniqueKeyPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="11640-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="11640-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11640-107">EXAMPLES</span></span>

### <span data-ttu-id="11640-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="11640-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="11640-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11640-109">PARAMETERS</span></span>

### <span data-ttu-id="11640-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11640-110">-DefaultProfile</span></span>
<span data-ttu-id="11640-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11640-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11640-112">-Path</span><span class="sxs-lookup"><span data-stu-id="11640-112">-Path</span></span>
<span data-ttu-id="11640-113">Útvonalértékeket tartalmazó karakterlánc tömbje</span><span class="sxs-lookup"><span data-stu-id="11640-113">Array of string of path values</span></span>

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

### <span data-ttu-id="11640-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11640-114">CommonParameters</span></span>
<span data-ttu-id="11640-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11640-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11640-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11640-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11640-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11640-117">INPUTS</span></span>

### <span data-ttu-id="11640-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="11640-118">None</span></span>

## <span data-ttu-id="11640-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11640-119">OUTPUTS</span></span>

### <span data-ttu-id="11640-120">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="11640-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="11640-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11640-121">NOTES</span></span>

## <span data-ttu-id="11640-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11640-122">RELATED LINKS</span></span>
