---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491004"
---
# <span data-ttu-id="c4b46-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="c4b46-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="c4b46-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4b46-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b46-103">A felhasználói előfizetések listájának beszerzése operátorként.</span><span class="sxs-lookup"><span data-stu-id="c4b46-103">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="c4b46-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4b46-104">SYNTAX</span></span>

### <span data-ttu-id="c4b46-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4b46-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="c4b46-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c4b46-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="c4b46-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4b46-107">DESCRIPTION</span></span>
<span data-ttu-id="c4b46-108">A felhasználói előfizetések listájának beszerzése operátorként.</span><span class="sxs-lookup"><span data-stu-id="c4b46-108">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="c4b46-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c4b46-109">EXAMPLES</span></span>

### <span data-ttu-id="c4b46-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4b46-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="c4b46-111">A felhasználói előfizetések listájának beszerzése operátorként.</span><span class="sxs-lookup"><span data-stu-id="c4b46-111">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="c4b46-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4b46-112">PARAMETERS</span></span>

### <span data-ttu-id="c4b46-113">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="c4b46-113">-Filter</span></span>
<span data-ttu-id="c4b46-114">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="c4b46-114">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b46-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4b46-115">-SubscriptionId</span></span>
<span data-ttu-id="c4b46-116">Előfizetés azonosítója paraméter</span><span class="sxs-lookup"><span data-stu-id="c4b46-116">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b46-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b46-117">CommonParameters</span></span>
<span data-ttu-id="c4b46-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4b46-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b46-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4b46-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b46-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4b46-120">INPUTS</span></span>

## <span data-ttu-id="c4b46-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4b46-121">OUTPUTS</span></span>

### <span data-ttu-id="c4b46-122">Microsoft. AzureStack. Management. Subscriptions. admin. models. előfizetés</span><span class="sxs-lookup"><span data-stu-id="c4b46-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="c4b46-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4b46-123">NOTES</span></span>

## <span data-ttu-id="c4b46-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4b46-124">RELATED LINKS</span></span>

