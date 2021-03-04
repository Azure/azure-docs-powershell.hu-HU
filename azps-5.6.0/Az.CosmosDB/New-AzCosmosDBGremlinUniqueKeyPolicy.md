---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 54f7a1cb17413fe9d6703dbd0e909555e0c3926a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921337"
---
# <span data-ttu-id="00aea-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="00aea-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="00aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00aea-102">SYNOPSIS</span></span>
<span data-ttu-id="00aea-103">Létrehoz egy új FogasDB UniqueKeyPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="00aea-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="00aea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00aea-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00aea-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00aea-105">DESCRIPTION</span></span>
<span data-ttu-id="00aea-106">A **New-AzCosmosDBGremlinUniqueKeyPolicy** parancsmag létrehoz egy új, PSUniqueKeyPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="00aea-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="00aea-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00aea-107">EXAMPLES</span></span>

### <span data-ttu-id="00aea-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="00aea-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="00aea-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00aea-109">PARAMETERS</span></span>

### <span data-ttu-id="00aea-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00aea-110">-DefaultProfile</span></span>
<span data-ttu-id="00aea-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00aea-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00aea-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="00aea-112">-UniqueKey</span></span>
<span data-ttu-id="00aea-113">PSUniqueKey típusú objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="00aea-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="00aea-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00aea-114">CommonParameters</span></span>
<span data-ttu-id="00aea-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00aea-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00aea-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00aea-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00aea-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00aea-117">INPUTS</span></span>

### <span data-ttu-id="00aea-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="00aea-118">None</span></span>

## <span data-ttu-id="00aea-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00aea-119">OUTPUTS</span></span>

### <span data-ttu-id="00aea-120">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="00aea-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="00aea-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00aea-121">NOTES</span></span>

## <span data-ttu-id="00aea-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00aea-122">RELATED LINKS</span></span>
