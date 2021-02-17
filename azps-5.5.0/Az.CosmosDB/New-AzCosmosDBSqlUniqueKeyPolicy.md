---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163995"
---
# <span data-ttu-id="40620-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="40620-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="40620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40620-102">SYNOPSIS</span></span>
<span data-ttu-id="40620-103">Létrehoz egy új TárolóDB SqlUniqueKeyPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="40620-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="40620-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40620-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40620-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40620-105">DESCRIPTION</span></span>
<span data-ttu-id="40620-106">A **New-AzCosmosDBSqlUniqueKeyPolicy** parancsmag létrehoz egy új, PSSqlUniqueKeyPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="40620-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="40620-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40620-107">EXAMPLES</span></span>

### <span data-ttu-id="40620-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="40620-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="40620-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40620-109">PARAMETERS</span></span>

### <span data-ttu-id="40620-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40620-110">-DefaultProfile</span></span>
<span data-ttu-id="40620-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40620-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40620-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="40620-112">-UniqueKey</span></span>
<span data-ttu-id="40620-113">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="40620-113">Database name.</span></span>

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

### <span data-ttu-id="40620-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40620-114">CommonParameters</span></span>
<span data-ttu-id="40620-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40620-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40620-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40620-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40620-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40620-117">INPUTS</span></span>

### <span data-ttu-id="40620-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="40620-118">None</span></span>

## <span data-ttu-id="40620-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40620-119">OUTPUTS</span></span>

### <span data-ttu-id="40620-120">Microsoft.Azure.Commands.CossDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="40620-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="40620-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40620-121">NOTES</span></span>

## <span data-ttu-id="40620-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40620-122">RELATED LINKS</span></span>
