---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166195"
---
# <span data-ttu-id="622f1-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="622f1-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="622f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="622f1-102">SYNOPSIS</span></span>
<span data-ttu-id="622f1-103">Új PSConflictResolutionPolicy típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="622f1-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="622f1-104">Paraméterértékként is át lehet adni a Set-AzCosmosDBGremlinGraph paraméterként.</span><span class="sxs-lookup"><span data-stu-id="622f1-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="622f1-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="622f1-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="622f1-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="622f1-106">DESCRIPTION</span></span>
<span data-ttu-id="622f1-107">A Gremlin API ConflictResolutionPolicy-jának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="622f1-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="622f1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="622f1-108">EXAMPLES</span></span>

### <span data-ttu-id="622f1-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="622f1-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="622f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="622f1-110">PARAMETERS</span></span>

### <span data-ttu-id="622f1-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="622f1-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="622f1-112">A típus egyéni típusának meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="622f1-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="622f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622f1-113">-DefaultProfile</span></span>
<span data-ttu-id="622f1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="622f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="622f1-115">-Path</span><span class="sxs-lookup"><span data-stu-id="622f1-115">-Path</span></span>
<span data-ttu-id="622f1-116">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="622f1-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="622f1-117">-Type</span><span class="sxs-lookup"><span data-stu-id="622f1-117">-Type</span></span>
<span data-ttu-id="622f1-118">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="622f1-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="622f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622f1-119">CommonParameters</span></span>
<span data-ttu-id="622f1-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="622f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622f1-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="622f1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622f1-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="622f1-122">INPUTS</span></span>

### <span data-ttu-id="622f1-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="622f1-123">None</span></span>

## <span data-ttu-id="622f1-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="622f1-124">OUTPUTS</span></span>

### <span data-ttu-id="622f1-125">Microsoft.Azure.Commands.EzresDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="622f1-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="622f1-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="622f1-126">NOTES</span></span>

## <span data-ttu-id="622f1-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="622f1-127">RELATED LINKS</span></span>
