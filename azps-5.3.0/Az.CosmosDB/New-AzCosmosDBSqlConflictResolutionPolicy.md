---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480566"
---
# <span data-ttu-id="fec2a-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fec2a-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="fec2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fec2a-102">SYNOPSIS</span></span>
<span data-ttu-id="fec2a-103">Létrehoz egy új PSSqlConflictResolutionPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="fec2a-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="fec2a-104">A Set-AzCosmosDBSqlContainer paraméterértékeként is át lehetadva.</span><span class="sxs-lookup"><span data-stu-id="fec2a-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="fec2a-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fec2a-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fec2a-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fec2a-106">DESCRIPTION</span></span>
<span data-ttu-id="fec2a-107">Az Sql API ConflictResolutionPolicy-jának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="fec2a-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="fec2a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fec2a-108">EXAMPLES</span></span>

### <span data-ttu-id="fec2a-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="fec2a-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="fec2a-110">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="fec2a-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="fec2a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fec2a-111">PARAMETERS</span></span>

### <span data-ttu-id="fec2a-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="fec2a-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="fec2a-113">Egyéni típushoz meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="fec2a-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="fec2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec2a-114">-DefaultProfile</span></span>
<span data-ttu-id="fec2a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fec2a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fec2a-116">-Path</span><span class="sxs-lookup"><span data-stu-id="fec2a-116">-Path</span></span>
<span data-ttu-id="fec2a-117">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="fec2a-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="fec2a-118">-Type</span><span class="sxs-lookup"><span data-stu-id="fec2a-118">-Type</span></span>
<span data-ttu-id="fec2a-119">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="fec2a-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="fec2a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec2a-120">CommonParameters</span></span>
<span data-ttu-id="fec2a-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec2a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec2a-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fec2a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec2a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fec2a-123">INPUTS</span></span>

### <span data-ttu-id="fec2a-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="fec2a-124">None</span></span>

## <span data-ttu-id="fec2a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fec2a-125">OUTPUTS</span></span>

### <span data-ttu-id="fec2a-126">Microsoft.Azure.Commands.EzresDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fec2a-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="fec2a-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fec2a-127">NOTES</span></span>

## <span data-ttu-id="fec2a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fec2a-128">RELATED LINKS</span></span>
