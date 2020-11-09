---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299354"
---
# <span data-ttu-id="1f827-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f827-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="1f827-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f827-102">SYNOPSIS</span></span>
<span data-ttu-id="1f827-103">Új PSConflictResolutionPolicy típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="1f827-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="1f827-104">A set-AzCosmosDBGremlinGraph paraméter értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="1f827-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="1f827-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f827-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f827-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f827-106">DESCRIPTION</span></span>
<span data-ttu-id="1f827-107">Az Gremlin API ConflictResolutionPolicy megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="1f827-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="1f827-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1f827-108">EXAMPLES</span></span>

### <span data-ttu-id="1f827-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1f827-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="1f827-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f827-110">PARAMETERS</span></span>

### <span data-ttu-id="1f827-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="1f827-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="1f827-112">Adja meg, ha a típus egyéni.</span><span class="sxs-lookup"><span data-stu-id="1f827-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="1f827-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f827-113">-DefaultProfile</span></span>
<span data-ttu-id="1f827-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f827-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f827-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="1f827-115">-Path</span></span>
<span data-ttu-id="1f827-116">Adja meg, hogy a típus LastWriterWins-e.</span><span class="sxs-lookup"><span data-stu-id="1f827-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="1f827-117">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="1f827-117">-Type</span></span>
<span data-ttu-id="1f827-118">Megadhatja az értékeket: LastWriterWins, egyéni, manuális.</span><span class="sxs-lookup"><span data-stu-id="1f827-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="1f827-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f827-119">CommonParameters</span></span>
<span data-ttu-id="1f827-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f827-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f827-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1f827-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f827-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f827-122">INPUTS</span></span>

### <span data-ttu-id="1f827-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="1f827-123">None</span></span>

## <span data-ttu-id="1f827-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f827-124">OUTPUTS</span></span>

### <span data-ttu-id="1f827-125">Microsoft. Azure. Command. CosmosDB. models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f827-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="1f827-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f827-126">NOTES</span></span>

## <span data-ttu-id="1f827-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f827-127">RELATED LINKS</span></span>
