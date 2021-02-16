---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166194"
---
# <span data-ttu-id="37625-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="37625-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="37625-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37625-102">SYNOPSIS</span></span>
<span data-ttu-id="37625-103">Létrehoz egy új, PSSqlConflictResolutionPolicy típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="37625-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="37625-104">A Set-AzCosmosDBSqlContainer paraméterértékeként is át lehetadva.</span><span class="sxs-lookup"><span data-stu-id="37625-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="37625-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37625-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37625-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37625-106">DESCRIPTION</span></span>
<span data-ttu-id="37625-107">Az Sql API ConflictResolutionPolicy-jának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="37625-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="37625-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37625-108">EXAMPLES</span></span>

### <span data-ttu-id="37625-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="37625-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="37625-110">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="37625-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="37625-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37625-111">PARAMETERS</span></span>

### <span data-ttu-id="37625-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="37625-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="37625-113">A típus egyéni típusának meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="37625-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="37625-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37625-114">-DefaultProfile</span></span>
<span data-ttu-id="37625-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37625-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37625-116">-Path</span><span class="sxs-lookup"><span data-stu-id="37625-116">-Path</span></span>
<span data-ttu-id="37625-117">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="37625-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="37625-118">-Type</span><span class="sxs-lookup"><span data-stu-id="37625-118">-Type</span></span>
<span data-ttu-id="37625-119">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="37625-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="37625-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37625-120">CommonParameters</span></span>
<span data-ttu-id="37625-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37625-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37625-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37625-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37625-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37625-123">INPUTS</span></span>

### <span data-ttu-id="37625-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="37625-124">None</span></span>

## <span data-ttu-id="37625-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37625-125">OUTPUTS</span></span>

### <span data-ttu-id="37625-126">Microsoft.Azure.Commands.EzresDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="37625-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="37625-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37625-127">NOTES</span></span>

## <span data-ttu-id="37625-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37625-128">RELATED LINKS</span></span>
