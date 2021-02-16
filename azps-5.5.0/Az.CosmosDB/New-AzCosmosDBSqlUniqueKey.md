---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167842"
---
# <span data-ttu-id="30786-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="30786-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="30786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30786-102">SYNOPSIS</span></span>
<span data-ttu-id="30786-103">Létrehoz egy új FogasDB Sql UniqueKey objektumot.</span><span class="sxs-lookup"><span data-stu-id="30786-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="30786-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30786-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30786-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30786-105">DESCRIPTION</span></span>
<span data-ttu-id="30786-106">A **New-AzCosmosDBSqlUniqueKey** parancsmag létrehoz egy PSUniqueKey típusú új objektumot.</span><span class="sxs-lookup"><span data-stu-id="30786-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="30786-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30786-107">EXAMPLES</span></span>

### <span data-ttu-id="30786-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="30786-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="30786-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30786-109">PARAMETERS</span></span>

### <span data-ttu-id="30786-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30786-110">-DefaultProfile</span></span>
<span data-ttu-id="30786-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30786-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30786-112">-Path</span><span class="sxs-lookup"><span data-stu-id="30786-112">-Path</span></span>
<span data-ttu-id="30786-113">Útvonalértékeket tartalmazó karakterlánc tömbje</span><span class="sxs-lookup"><span data-stu-id="30786-113">Array of string of path values</span></span>

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

### <span data-ttu-id="30786-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30786-114">CommonParameters</span></span>
<span data-ttu-id="30786-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30786-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30786-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30786-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30786-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30786-117">INPUTS</span></span>

### <span data-ttu-id="30786-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="30786-118">None</span></span>

## <span data-ttu-id="30786-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30786-119">OUTPUTS</span></span>

### <span data-ttu-id="30786-120">Microsoft.Azure.Commands.CossDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="30786-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="30786-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30786-121">NOTES</span></span>

## <span data-ttu-id="30786-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30786-122">RELATED LINKS</span></span>
