---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: c67627068ef2fc90f8322b2e8b63dd6cd68acbe3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007973"
---
# <span data-ttu-id="ce380-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce380-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="ce380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce380-102">SYNOPSIS</span></span>
<span data-ttu-id="ce380-103">Új PSConflictResolutionPolicy típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ce380-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="ce380-104">A Set-AzCosmosDBGremlinGraph paraméterértékeként is át lehet adni.</span><span class="sxs-lookup"><span data-stu-id="ce380-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="ce380-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ce380-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce380-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ce380-106">DESCRIPTION</span></span>
<span data-ttu-id="ce380-107">A Gremlin API ConflictResolutionPolicy-jának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="ce380-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="ce380-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ce380-108">EXAMPLES</span></span>

### <span data-ttu-id="ce380-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="ce380-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="ce380-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce380-110">PARAMETERS</span></span>

### <span data-ttu-id="ce380-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="ce380-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="ce380-112">Egyéni típushoz meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="ce380-112">To be provided when the type is custom.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce380-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce380-113">-DefaultProfile</span></span>
<span data-ttu-id="ce380-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce380-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce380-115">-Path</span><span class="sxs-lookup"><span data-stu-id="ce380-115">-Path</span></span>
<span data-ttu-id="ce380-116">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="ce380-116">To be provided when the type is LastWriterWins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce380-117">-Type</span><span class="sxs-lookup"><span data-stu-id="ce380-117">-Type</span></span>
<span data-ttu-id="ce380-118">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="ce380-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce380-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce380-119">CommonParameters</span></span>
<span data-ttu-id="ce380-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce380-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce380-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce380-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce380-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce380-122">INPUTS</span></span>

### <span data-ttu-id="ce380-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="ce380-123">None</span></span>

## <span data-ttu-id="ce380-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce380-124">OUTPUTS</span></span>

### <span data-ttu-id="ce380-125">Microsoft.Azure.Commands.EzresDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce380-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="ce380-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ce380-126">NOTES</span></span>

## <span data-ttu-id="ce380-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce380-127">RELATED LINKS</span></span>
