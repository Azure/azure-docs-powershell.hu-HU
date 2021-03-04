---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: e5742cde3a39cb2bf7dc96b952b3129d353235f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935274"
---
# <span data-ttu-id="9c835-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c835-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="9c835-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c835-102">SYNOPSIS</span></span>
<span data-ttu-id="9c835-103">Létrehoz egy új PSSqlConflictResolutionPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="9c835-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="9c835-104">A Set-AzCosmosDBSqlContainer paraméterértékeként is át lehetadva.</span><span class="sxs-lookup"><span data-stu-id="9c835-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="9c835-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9c835-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c835-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9c835-106">DESCRIPTION</span></span>
<span data-ttu-id="9c835-107">Az Sql API ConflictResolutionPolicy-jának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="9c835-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="9c835-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9c835-108">EXAMPLES</span></span>

### <span data-ttu-id="9c835-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="9c835-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="9c835-110">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="9c835-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="9c835-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c835-111">PARAMETERS</span></span>

### <span data-ttu-id="9c835-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="9c835-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="9c835-113">Egyéni típushoz meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="9c835-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="9c835-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c835-114">-DefaultProfile</span></span>
<span data-ttu-id="9c835-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c835-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c835-116">-Path</span><span class="sxs-lookup"><span data-stu-id="9c835-116">-Path</span></span>
<span data-ttu-id="9c835-117">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="9c835-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="9c835-118">-Type</span><span class="sxs-lookup"><span data-stu-id="9c835-118">-Type</span></span>
<span data-ttu-id="9c835-119">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="9c835-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="9c835-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c835-120">CommonParameters</span></span>
<span data-ttu-id="9c835-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c835-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c835-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c835-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c835-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c835-123">INPUTS</span></span>

### <span data-ttu-id="9c835-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="9c835-124">None</span></span>

## <span data-ttu-id="9c835-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c835-125">OUTPUTS</span></span>

### <span data-ttu-id="9c835-126">Microsoft.Azure.Commands.EzresDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c835-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="9c835-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9c835-127">NOTES</span></span>

## <span data-ttu-id="9c835-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c835-128">RELATED LINKS</span></span>
