---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 593e299a6d7a1aa8131848f6de5f6c7aec8bd8c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013645"
---
# <span data-ttu-id="77d6e-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="77d6e-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="77d6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="77d6e-103">Új CosmosDB-UniqueKeyPolicy objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="77d6e-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="77d6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77d6e-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77d6e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="77d6e-105">DESCRIPTION</span></span>
<span data-ttu-id="77d6e-106">A **New-AzCosmosDBGremlinUniqueKeyPolicy** parancsmag új, PSUniqueKeyPolicy típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="77d6e-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="77d6e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="77d6e-107">EXAMPLES</span></span>

### <span data-ttu-id="77d6e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="77d6e-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="77d6e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77d6e-109">PARAMETERS</span></span>

### <span data-ttu-id="77d6e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d6e-110">-DefaultProfile</span></span>
<span data-ttu-id="77d6e-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77d6e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77d6e-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="77d6e-112">-UniqueKey</span></span>
<span data-ttu-id="77d6e-113">A PSUniqueKey típusú objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="77d6e-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77d6e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d6e-114">CommonParameters</span></span>
<span data-ttu-id="77d6e-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77d6e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d6e-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="77d6e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d6e-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77d6e-117">INPUTS</span></span>

### <span data-ttu-id="77d6e-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="77d6e-118">None</span></span>

## <span data-ttu-id="77d6e-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77d6e-119">OUTPUTS</span></span>

### <span data-ttu-id="77d6e-120">Microsoft. Azure. Command. CosmosDB. models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="77d6e-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="77d6e-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77d6e-121">NOTES</span></span>

## <span data-ttu-id="77d6e-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77d6e-122">RELATED LINKS</span></span>
