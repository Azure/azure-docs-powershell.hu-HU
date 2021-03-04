---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: b172c5e22c26cba8d88d188198868da720d611d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938202"
---
# <span data-ttu-id="9e537-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="9e537-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="9e537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e537-102">SYNOPSIS</span></span>
<span data-ttu-id="9e537-103">Létrehoz egy új FogasDB Sql UniqueKey objektumot.</span><span class="sxs-lookup"><span data-stu-id="9e537-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="9e537-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e537-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e537-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e537-105">DESCRIPTION</span></span>
<span data-ttu-id="9e537-106">A **New-AzCosmosDBSqlUniqueKey** parancsmag létrehoz egy PSUniqueKey típusú új objektumot.</span><span class="sxs-lookup"><span data-stu-id="9e537-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="9e537-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e537-107">EXAMPLES</span></span>

### <span data-ttu-id="9e537-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9e537-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="9e537-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e537-109">PARAMETERS</span></span>

### <span data-ttu-id="9e537-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e537-110">-DefaultProfile</span></span>
<span data-ttu-id="9e537-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e537-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e537-112">-Path</span><span class="sxs-lookup"><span data-stu-id="9e537-112">-Path</span></span>
<span data-ttu-id="9e537-113">Útvonalértékeket tartalmazó karakterlánc tömbje</span><span class="sxs-lookup"><span data-stu-id="9e537-113">Array of string of path values</span></span>

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

### <span data-ttu-id="9e537-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e537-114">CommonParameters</span></span>
<span data-ttu-id="9e537-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e537-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e537-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e537-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e537-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e537-117">INPUTS</span></span>

### <span data-ttu-id="9e537-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="9e537-118">None</span></span>

## <span data-ttu-id="9e537-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e537-119">OUTPUTS</span></span>

### <span data-ttu-id="9e537-120">Microsoft.Azure.Commands.CossDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="9e537-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="9e537-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e537-121">NOTES</span></span>

## <span data-ttu-id="9e537-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e537-122">RELATED LINKS</span></span>
