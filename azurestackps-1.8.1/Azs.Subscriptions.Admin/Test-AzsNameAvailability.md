---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840830"
---
# <span data-ttu-id="e4aab-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e4aab-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="e4aab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4aab-102">SYNOPSIS</span></span>
<span data-ttu-id="e4aab-103">A megadott előfizetéses erőforrástípus és név avaialbility adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e4aab-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="e4aab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4aab-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="e4aab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4aab-105">DESCRIPTION</span></span>
<span data-ttu-id="e4aab-106">A megadott előfizetéses erőforrástípus és név avaialbility adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e4aab-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="e4aab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4aab-107">EXAMPLES</span></span>

### <span data-ttu-id="e4aab-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4aab-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="e4aab-109">A megadott előfizetéses erőforrástípus és név avaialbility adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e4aab-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="e4aab-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4aab-110">PARAMETERS</span></span>

### <span data-ttu-id="e4aab-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4aab-111">-Name</span></span>
<span data-ttu-id="e4aab-112">A hitelesíteni kívánt erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e4aab-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="e4aab-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e4aab-113">-ResourceType</span></span>
<span data-ttu-id="e4aab-114">Az ellenőrizni kívánt erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="e4aab-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="e4aab-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4aab-115">CommonParameters</span></span>
<span data-ttu-id="e4aab-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4aab-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4aab-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4aab-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4aab-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4aab-118">INPUTS</span></span>

## <span data-ttu-id="e4aab-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4aab-119">OUTPUTS</span></span>

### <span data-ttu-id="e4aab-120">Microsoft. AzureStack. Management. Subscriptions. admin. models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e4aab-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="e4aab-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4aab-121">NOTES</span></span>

## <span data-ttu-id="e4aab-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4aab-122">RELATED LINKS</span></span>

