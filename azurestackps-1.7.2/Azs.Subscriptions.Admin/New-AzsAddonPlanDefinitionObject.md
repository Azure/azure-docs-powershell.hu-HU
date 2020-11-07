---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838337"
---
# <span data-ttu-id="daee1-101">New-AzsAddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="daee1-101">New-AzsAddonPlanDefinitionObject</span></span>

## <span data-ttu-id="daee1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="daee1-102">SYNOPSIS</span></span>
<span data-ttu-id="daee1-103">Annak a kívánt csomagnak a nevét tartalmazza, amelyet fel szeretne venni az ajánlatból, vagy le szeretne kapcsolni.</span><span class="sxs-lookup"><span data-stu-id="daee1-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="daee1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="daee1-104">SYNTAX</span></span>

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="daee1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="daee1-105">DESCRIPTION</span></span>
<span data-ttu-id="daee1-106">Annak a kívánt csomagnak a nevét tartalmazza, amelyet fel szeretne venni az ajánlatból, vagy le szeretne kapcsolni.</span><span class="sxs-lookup"><span data-stu-id="daee1-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="daee1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="daee1-107">EXAMPLES</span></span>

### <span data-ttu-id="daee1-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="daee1-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="daee1-109">Új terv-definíciós objektum létrehozása a megadott tervhez az 500 beszerzési korlátozásával.</span><span class="sxs-lookup"><span data-stu-id="daee1-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="daee1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="daee1-110">PARAMETERS</span></span>

### <span data-ttu-id="daee1-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="daee1-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="daee1-112">Egyetlen előfizetéssel megszerezhető példányok maximális száma</span><span class="sxs-lookup"><span data-stu-id="daee1-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="daee1-113">Ha nincs megadva, a feltételezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="daee1-113">If not specified, the assumed value is 1.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daee1-114">-PlanId</span><span class="sxs-lookup"><span data-stu-id="daee1-114">-PlanId</span></span>
<span data-ttu-id="daee1-115">Terv azonosítója</span><span class="sxs-lookup"><span data-stu-id="daee1-115">Plan identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daee1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daee1-116">CommonParameters</span></span>
<span data-ttu-id="daee1-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="daee1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daee1-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daee1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daee1-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="daee1-119">INPUTS</span></span>

## <span data-ttu-id="daee1-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="daee1-120">OUTPUTS</span></span>

## <span data-ttu-id="daee1-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="daee1-121">NOTES</span></span>

## <span data-ttu-id="daee1-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="daee1-122">RELATED LINKS</span></span>

