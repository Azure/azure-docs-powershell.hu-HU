---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348906"
---
# <span data-ttu-id="58957-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="58957-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="58957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58957-102">SYNOPSIS</span></span>
<span data-ttu-id="58957-103">Létrehoz egy új FogasDB UniqueKeyPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="58957-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="58957-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58957-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58957-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58957-105">DESCRIPTION</span></span>
<span data-ttu-id="58957-106">A **New-AzCosmosDBGremlinUniqueKeyPolicy** parancsmag létrehoz egy új, PSUniqueKeyPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="58957-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="58957-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58957-107">EXAMPLES</span></span>

### <span data-ttu-id="58957-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="58957-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="58957-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58957-109">PARAMETERS</span></span>

### <span data-ttu-id="58957-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58957-110">-DefaultProfile</span></span>
<span data-ttu-id="58957-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58957-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58957-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="58957-112">-UniqueKey</span></span>
<span data-ttu-id="58957-113">PSUniqueKey típusú objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="58957-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="58957-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58957-114">CommonParameters</span></span>
<span data-ttu-id="58957-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58957-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58957-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58957-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58957-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58957-117">INPUTS</span></span>

### <span data-ttu-id="58957-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="58957-118">None</span></span>

## <span data-ttu-id="58957-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58957-119">OUTPUTS</span></span>

### <span data-ttu-id="58957-120">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="58957-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="58957-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58957-121">NOTES</span></span>

## <span data-ttu-id="58957-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58957-122">RELATED LINKS</span></span>
