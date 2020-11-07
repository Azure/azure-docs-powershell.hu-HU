---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840345"
---
# <span data-ttu-id="b2c42-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="b2c42-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="b2c42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2c42-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c42-103">A felhasználói előfizetések listájának beszerzése rendszergazdaként.</span><span class="sxs-lookup"><span data-stu-id="b2c42-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="b2c42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2c42-104">SYNTAX</span></span>

### <span data-ttu-id="b2c42-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2c42-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="b2c42-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b2c42-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="b2c42-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2c42-107">DESCRIPTION</span></span>
<span data-ttu-id="b2c42-108">A felhasználói előfizetések listájának beszerzése rendszergazdaként.</span><span class="sxs-lookup"><span data-stu-id="b2c42-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="b2c42-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b2c42-109">EXAMPLES</span></span>

### <span data-ttu-id="b2c42-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b2c42-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="b2c42-111">A felhasználói előfizetések listájának beszerzése rendszergazdaként.</span><span class="sxs-lookup"><span data-stu-id="b2c42-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="b2c42-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2c42-112">PARAMETERS</span></span>

### <span data-ttu-id="b2c42-113">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b2c42-113">-Filter</span></span>
<span data-ttu-id="b2c42-114">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="b2c42-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="b2c42-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2c42-115">-SubscriptionId</span></span>
<span data-ttu-id="b2c42-116">Előfizetés azonosítója paraméter</span><span class="sxs-lookup"><span data-stu-id="b2c42-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="b2c42-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c42-117">CommonParameters</span></span>
<span data-ttu-id="b2c42-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2c42-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c42-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c42-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c42-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2c42-120">INPUTS</span></span>

## <span data-ttu-id="b2c42-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2c42-121">OUTPUTS</span></span>

### <span data-ttu-id="b2c42-122">Microsoft. AzureStack. Management. Subscriptions. admin. models. előfizetés</span><span class="sxs-lookup"><span data-stu-id="b2c42-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="b2c42-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2c42-123">NOTES</span></span>

## <span data-ttu-id="b2c42-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2c42-124">RELATED LINKS</span></span>

