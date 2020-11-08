---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017136"
---
# <span data-ttu-id="96cce-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="96cce-101">New-AzsPlan</span></span>

## <span data-ttu-id="96cce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96cce-102">SYNOPSIS</span></span>
<span data-ttu-id="96cce-103">Új csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="96cce-103">Creates a new plan</span></span>

## <span data-ttu-id="96cce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96cce-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96cce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96cce-105">DESCRIPTION</span></span>
<span data-ttu-id="96cce-106">Új csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="96cce-106">Creates a new plan</span></span>

## <span data-ttu-id="96cce-107">Példák</span><span class="sxs-lookup"><span data-stu-id="96cce-107">EXAMPLES</span></span>

### <span data-ttu-id="96cce-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="96cce-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="96cce-109">Új csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="96cce-109">Creates a new plan</span></span>

## <span data-ttu-id="96cce-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96cce-110">PARAMETERS</span></span>

### <span data-ttu-id="96cce-111">-Leírás</span><span class="sxs-lookup"><span data-stu-id="96cce-111">-Description</span></span>
<span data-ttu-id="96cce-112">A terv leírása.</span><span class="sxs-lookup"><span data-stu-id="96cce-112">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="96cce-113">-DisplayName</span></span>
<span data-ttu-id="96cce-114">Megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="96cce-114">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="96cce-115">-ExternalReferenceId</span></span>
<span data-ttu-id="96cce-116">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="96cce-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="96cce-117">-Location</span></span>
<span data-ttu-id="96cce-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="96cce-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96cce-119">-Name</span></span>
<span data-ttu-id="96cce-120">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="96cce-120">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="96cce-121">-QuotaIds</span></span>
<span data-ttu-id="96cce-122">A csomag alatti kvóta-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="96cce-122">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96cce-123">-ResourceGroupName</span></span>
<span data-ttu-id="96cce-124">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="96cce-124">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="96cce-125">-SkuIds</span></span>
<span data-ttu-id="96cce-126">SKU-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="96cce-126">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="96cce-127">-SubscriptionCount</span></span>
<span data-ttu-id="96cce-128">Előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="96cce-128">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96cce-129">-Confirm</span></span>
<span data-ttu-id="96cce-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96cce-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96cce-131">-WhatIf</span></span>
<span data-ttu-id="96cce-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96cce-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96cce-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96cce-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cce-134">CommonParameters</span></span>
<span data-ttu-id="96cce-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96cce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cce-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96cce-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cce-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96cce-137">INPUTS</span></span>

## <span data-ttu-id="96cce-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96cce-138">OUTPUTS</span></span>

### <span data-ttu-id="96cce-139">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. terv</span><span class="sxs-lookup"><span data-stu-id="96cce-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="96cce-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96cce-140">NOTES</span></span>

## <span data-ttu-id="96cce-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96cce-141">RELATED LINKS</span></span>

