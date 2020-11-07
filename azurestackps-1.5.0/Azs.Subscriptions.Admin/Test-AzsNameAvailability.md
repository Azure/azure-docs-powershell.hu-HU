---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 267a5bf4c3f864c987c0bc747eefce9dd3ffe6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671744"
---
# <span data-ttu-id="a4cf0-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a4cf0-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="a4cf0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cf0-103">A megadott előfizetéses erőforrástípus és név avaialbility adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a4cf0-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="a4cf0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4cf0-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="a4cf0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4cf0-105">DESCRIPTION</span></span>
<span data-ttu-id="a4cf0-106">A megadott előfizetéses erőforrástípus és név avaialbility adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a4cf0-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="a4cf0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4cf0-107">EXAMPLES</span></span>

### <span data-ttu-id="a4cf0-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4cf0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="a4cf0-109">A megadott előfizetéses erőforrástípus és név avaialbility adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="a4cf0-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="a4cf0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4cf0-110">PARAMETERS</span></span>

### <span data-ttu-id="a4cf0-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4cf0-111">-Name</span></span>
<span data-ttu-id="a4cf0-112">A hitelesíteni kívánt erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a4cf0-112">The resource name to verify.</span></span>

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

### <span data-ttu-id="a4cf0-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a4cf0-113">-ResourceType</span></span>
<span data-ttu-id="a4cf0-114">Az ellenőrizni kívánt erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="a4cf0-114">The resource type to verify.</span></span>

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

### <span data-ttu-id="a4cf0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cf0-115">CommonParameters</span></span>
<span data-ttu-id="a4cf0-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4cf0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cf0-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4cf0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cf0-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4cf0-118">INPUTS</span></span>

## <span data-ttu-id="a4cf0-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4cf0-119">OUTPUTS</span></span>

### <span data-ttu-id="a4cf0-120">Microsoft. AzureStack. Management. Subscriptions. admin. models. CheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a4cf0-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="a4cf0-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4cf0-121">NOTES</span></span>

## <span data-ttu-id="a4cf0-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4cf0-122">RELATED LINKS</span></span>

