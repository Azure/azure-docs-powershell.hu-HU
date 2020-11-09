---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299276"
---
# <span data-ttu-id="c756e-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="c756e-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="c756e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c756e-102">SYNOPSIS</span></span>
<span data-ttu-id="c756e-103">Új CosmosDB MongoDB index létrehozása</span><span class="sxs-lookup"><span data-stu-id="c756e-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="c756e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c756e-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c756e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c756e-105">DESCRIPTION</span></span>
<span data-ttu-id="c756e-106">A **New-AzCosmosDBMongoDBIndex** létrehoz egy új CosmosDB MongoDB indexet.</span><span class="sxs-lookup"><span data-stu-id="c756e-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="c756e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c756e-107">EXAMPLES</span></span>

### <span data-ttu-id="c756e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c756e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="c756e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c756e-109">PARAMETERS</span></span>

### <span data-ttu-id="c756e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c756e-110">-DefaultProfile</span></span>
<span data-ttu-id="c756e-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c756e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c756e-112">-Kulcs</span><span class="sxs-lookup"><span data-stu-id="c756e-112">-Key</span></span>
<span data-ttu-id="c756e-113">A fő értékek tömbje karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="c756e-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c756e-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="c756e-114">-TtlInSeconds</span></span>
<span data-ttu-id="c756e-115">A tárgymutató lejártát követő másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="c756e-115">Number of seconds after which the index expires.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c756e-116">-Unique</span><span class="sxs-lookup"><span data-stu-id="c756e-116">-Unique</span></span>
<span data-ttu-id="c756e-117">Bool: annak jelzése, hogy az index egyedi-e.</span><span class="sxs-lookup"><span data-stu-id="c756e-117">Bool to indicate if the index is unique or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c756e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c756e-118">CommonParameters</span></span>
<span data-ttu-id="c756e-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c756e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c756e-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c756e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c756e-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c756e-121">INPUTS</span></span>

### <span data-ttu-id="c756e-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="c756e-122">None</span></span>

## <span data-ttu-id="c756e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c756e-123">OUTPUTS</span></span>

### <span data-ttu-id="c756e-124">Microsoft. Azure. Command. CosmosDB. models. PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="c756e-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="c756e-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c756e-125">NOTES</span></span>

## <span data-ttu-id="c756e-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c756e-126">RELATED LINKS</span></span>
