---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013642"
---
# <span data-ttu-id="b0552-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b0552-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="b0552-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0552-102">SYNOPSIS</span></span>
<span data-ttu-id="b0552-103">Új PSSqlConflictResolutionPolicy típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="b0552-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="b0552-104">A set-AzCosmosDBSqlContainer paraméter értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="b0552-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="b0552-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0552-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0552-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0552-106">DESCRIPTION</span></span>
<span data-ttu-id="b0552-107">Az SQL API ConflictResolutionPolicy megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="b0552-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="b0552-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b0552-108">EXAMPLES</span></span>

### <span data-ttu-id="b0552-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b0552-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="b0552-110">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="b0552-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="b0552-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0552-111">PARAMETERS</span></span>

### <span data-ttu-id="b0552-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="b0552-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="b0552-113">Adja meg, ha a típus egyéni.</span><span class="sxs-lookup"><span data-stu-id="b0552-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="b0552-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0552-114">-DefaultProfile</span></span>
<span data-ttu-id="b0552-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0552-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0552-116">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="b0552-116">-Path</span></span>
<span data-ttu-id="b0552-117">Adja meg, hogy a típus LastWriterWins-e.</span><span class="sxs-lookup"><span data-stu-id="b0552-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="b0552-118">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="b0552-118">-Type</span></span>
<span data-ttu-id="b0552-119">Megadhatja az értékeket: LastWriterWins, egyéni, manuális.</span><span class="sxs-lookup"><span data-stu-id="b0552-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="b0552-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0552-120">CommonParameters</span></span>
<span data-ttu-id="b0552-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0552-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0552-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b0552-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0552-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0552-123">INPUTS</span></span>

### <span data-ttu-id="b0552-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="b0552-124">None</span></span>

## <span data-ttu-id="b0552-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0552-125">OUTPUTS</span></span>

### <span data-ttu-id="b0552-126">Microsoft. Azure. Command. CosmosDB. models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b0552-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="b0552-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0552-127">NOTES</span></span>

## <span data-ttu-id="b0552-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0552-128">RELATED LINKS</span></span>
