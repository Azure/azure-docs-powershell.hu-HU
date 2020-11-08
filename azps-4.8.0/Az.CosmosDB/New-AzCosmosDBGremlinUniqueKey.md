---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185090"
---
# <span data-ttu-id="e4fbd-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="e4fbd-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="e4fbd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e4fbd-103">Új CosmosDB-UniqueKeyPolicy objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e4fbd-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="e4fbd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4fbd-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4fbd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="e4fbd-106">A **New-AzCosmosDBGremlinUniqueKeyPolicy** parancsmag új, PSUniqueKeyPolicy típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e4fbd-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="e4fbd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4fbd-107">EXAMPLES</span></span>

### <span data-ttu-id="e4fbd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e4fbd-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="e4fbd-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4fbd-109">PARAMETERS</span></span>

### <span data-ttu-id="e4fbd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4fbd-110">-DefaultProfile</span></span>
<span data-ttu-id="e4fbd-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4fbd-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4fbd-112">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="e4fbd-112">-Path</span></span>
<span data-ttu-id="e4fbd-113">Az elérésiút-értékek karakterláncának tömbje</span><span class="sxs-lookup"><span data-stu-id="e4fbd-113">Array of string of path values</span></span>

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

### <span data-ttu-id="e4fbd-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fbd-114">CommonParameters</span></span>
<span data-ttu-id="e4fbd-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4fbd-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fbd-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e4fbd-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fbd-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4fbd-117">INPUTS</span></span>

### <span data-ttu-id="e4fbd-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="e4fbd-118">None</span></span>

## <span data-ttu-id="e4fbd-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4fbd-119">OUTPUTS</span></span>

### <span data-ttu-id="e4fbd-120">Microsoft. Azure. Command. CosmosDB. models. PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="e4fbd-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="e4fbd-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4fbd-121">NOTES</span></span>

## <span data-ttu-id="e4fbd-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4fbd-122">RELATED LINKS</span></span>
