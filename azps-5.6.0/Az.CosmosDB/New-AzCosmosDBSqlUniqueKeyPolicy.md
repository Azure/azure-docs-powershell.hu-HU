---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: 6ef9e9b4fe2332af22bb8bdab1334096860f53ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936225"
---
# <span data-ttu-id="9e494-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="9e494-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="9e494-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e494-102">SYNOPSIS</span></span>
<span data-ttu-id="9e494-103">Létrehoz egy új TárolóDB SqlUniqueKeyPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="9e494-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="9e494-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e494-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e494-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e494-105">DESCRIPTION</span></span>
<span data-ttu-id="9e494-106">A **New-AzCosmosDBSqlUniqueKeyPolicy** parancsmag létrehoz egy új, PSSqlUniqueKeyPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="9e494-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="9e494-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e494-107">EXAMPLES</span></span>

### <span data-ttu-id="9e494-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9e494-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="9e494-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e494-109">PARAMETERS</span></span>

### <span data-ttu-id="9e494-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e494-110">-DefaultProfile</span></span>
<span data-ttu-id="9e494-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e494-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e494-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="9e494-112">-UniqueKey</span></span>
<span data-ttu-id="9e494-113">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9e494-113">Database name.</span></span>

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

### <span data-ttu-id="9e494-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e494-114">CommonParameters</span></span>
<span data-ttu-id="9e494-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e494-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e494-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e494-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e494-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e494-117">INPUTS</span></span>

### <span data-ttu-id="9e494-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="9e494-118">None</span></span>

## <span data-ttu-id="9e494-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e494-119">OUTPUTS</span></span>

### <span data-ttu-id="9e494-120">Microsoft.Azure.Commands.CossDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="9e494-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="9e494-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e494-121">NOTES</span></span>

## <span data-ttu-id="9e494-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e494-122">RELATED LINKS</span></span>
