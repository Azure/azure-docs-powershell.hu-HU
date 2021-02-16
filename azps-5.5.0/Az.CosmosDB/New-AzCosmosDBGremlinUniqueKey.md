---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144483"
---
# <span data-ttu-id="20c7a-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="20c7a-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="20c7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="20c7a-103">Létrehoz egy új FogasDB UniqueKeyPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="20c7a-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="20c7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="20c7a-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c7a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="20c7a-105">DESCRIPTION</span></span>
<span data-ttu-id="20c7a-106">A **New-AzCosmosDBGremlinUniqueKeyPolicy** parancsmag létrehoz egy új, PSUniqueKeyPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="20c7a-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="20c7a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="20c7a-107">EXAMPLES</span></span>

### <span data-ttu-id="20c7a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="20c7a-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="20c7a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20c7a-109">PARAMETERS</span></span>

### <span data-ttu-id="20c7a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c7a-110">-DefaultProfile</span></span>
<span data-ttu-id="20c7a-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20c7a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c7a-112">-Path</span><span class="sxs-lookup"><span data-stu-id="20c7a-112">-Path</span></span>
<span data-ttu-id="20c7a-113">Útvonalértékeket tartalmazó karakterlánc tömbje</span><span class="sxs-lookup"><span data-stu-id="20c7a-113">Array of string of path values</span></span>

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

### <span data-ttu-id="20c7a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c7a-114">CommonParameters</span></span>
<span data-ttu-id="20c7a-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c7a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c7a-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20c7a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c7a-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20c7a-117">INPUTS</span></span>

### <span data-ttu-id="20c7a-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="20c7a-118">None</span></span>

## <span data-ttu-id="20c7a-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20c7a-119">OUTPUTS</span></span>

### <span data-ttu-id="20c7a-120">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="20c7a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="20c7a-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="20c7a-121">NOTES</span></span>

## <span data-ttu-id="20c7a-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20c7a-122">RELATED LINKS</span></span>
