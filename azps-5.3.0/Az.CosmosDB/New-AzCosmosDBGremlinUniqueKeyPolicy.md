---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480569"
---
# <span data-ttu-id="d7769-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d7769-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="d7769-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7769-102">SYNOPSIS</span></span>
<span data-ttu-id="d7769-103">Létrehoz egy új FogasDB UniqueKeyPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="d7769-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="d7769-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7769-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7769-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7769-105">DESCRIPTION</span></span>
<span data-ttu-id="d7769-106">A **New-AzCosmosDBGremlinUniqueKeyPolicy** parancsmag létrehoz egy új, PSUniqueKeyPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="d7769-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="d7769-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7769-107">EXAMPLES</span></span>

### <span data-ttu-id="d7769-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d7769-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="d7769-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7769-109">PARAMETERS</span></span>

### <span data-ttu-id="d7769-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7769-110">-DefaultProfile</span></span>
<span data-ttu-id="d7769-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7769-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7769-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="d7769-112">-UniqueKey</span></span>
<span data-ttu-id="d7769-113">PSUniqueKey típusú objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="d7769-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7769-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7769-114">CommonParameters</span></span>
<span data-ttu-id="d7769-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7769-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7769-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7769-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7769-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7769-117">INPUTS</span></span>

### <span data-ttu-id="d7769-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7769-118">None</span></span>

## <span data-ttu-id="d7769-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7769-119">OUTPUTS</span></span>

### <span data-ttu-id="d7769-120">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d7769-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="d7769-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7769-121">NOTES</span></span>

## <span data-ttu-id="d7769-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7769-122">RELATED LINKS</span></span>
