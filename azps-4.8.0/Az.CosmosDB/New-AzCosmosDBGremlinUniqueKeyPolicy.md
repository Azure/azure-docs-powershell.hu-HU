---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024089"
---
# <span data-ttu-id="305c7-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="305c7-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="305c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="305c7-102">SYNOPSIS</span></span>
<span data-ttu-id="305c7-103">Új CosmosDB-UniqueKeyPolicy objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="305c7-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="305c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="305c7-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="305c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="305c7-105">DESCRIPTION</span></span>
<span data-ttu-id="305c7-106">A **New-AzCosmosDBGremlinUniqueKeyPolicy** parancsmag új, PSUniqueKeyPolicy típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="305c7-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="305c7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="305c7-107">EXAMPLES</span></span>

### <span data-ttu-id="305c7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="305c7-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="305c7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="305c7-109">PARAMETERS</span></span>

### <span data-ttu-id="305c7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305c7-110">-DefaultProfile</span></span>
<span data-ttu-id="305c7-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="305c7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="305c7-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="305c7-112">-UniqueKey</span></span>
<span data-ttu-id="305c7-113">A PSUniqueKey típusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="305c7-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305c7-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305c7-114">CommonParameters</span></span>
<span data-ttu-id="305c7-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="305c7-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305c7-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="305c7-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305c7-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="305c7-117">INPUTS</span></span>

### <span data-ttu-id="305c7-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="305c7-118">None</span></span>

## <span data-ttu-id="305c7-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="305c7-119">OUTPUTS</span></span>

### <span data-ttu-id="305c7-120">Microsoft. Azure. Command. CosmosDB. models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="305c7-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="305c7-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="305c7-121">NOTES</span></span>

## <span data-ttu-id="305c7-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="305c7-122">RELATED LINKS</span></span>
