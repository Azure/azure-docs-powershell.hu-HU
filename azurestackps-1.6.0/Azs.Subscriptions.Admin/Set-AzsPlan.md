---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f03365a81fc53af14e3fc9e686504ef3e4387c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491211"
---
# <span data-ttu-id="64795-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="64795-101">Set-AzsPlan</span></span>

## <span data-ttu-id="64795-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64795-102">SYNOPSIS</span></span>
<span data-ttu-id="64795-103">A megadott csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="64795-103">Updates the specified plan</span></span>

## <span data-ttu-id="64795-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64795-104">SYNTAX</span></span>

### <span data-ttu-id="64795-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64795-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64795-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="64795-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64795-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="64795-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64795-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="64795-108">DESCRIPTION</span></span>
<span data-ttu-id="64795-109">A megadott csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="64795-109">Updates the specified plan</span></span>

## <span data-ttu-id="64795-110">Példák</span><span class="sxs-lookup"><span data-stu-id="64795-110">EXAMPLES</span></span>

### <span data-ttu-id="64795-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="64795-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="64795-112">A megadott csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="64795-112">Updates the specified plan</span></span>

## <span data-ttu-id="64795-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64795-113">PARAMETERS</span></span>

### <span data-ttu-id="64795-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="64795-114">-Description</span></span>
<span data-ttu-id="64795-115">A terv leírása.</span><span class="sxs-lookup"><span data-stu-id="64795-115">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64795-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="64795-116">-DisplayName</span></span>
<span data-ttu-id="64795-117">Megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="64795-117">Display name.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64795-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="64795-118">-ExternalReferenceId</span></span>
<span data-ttu-id="64795-119">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="64795-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64795-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64795-120">-InputObject</span></span>
<span data-ttu-id="64795-121">A Microsoft. AzureStack. Management. Subscriptions. admin. models. terv típusú beviteli objektum.</span><span class="sxs-lookup"><span data-stu-id="64795-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64795-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="64795-122">-Location</span></span>
<span data-ttu-id="64795-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="64795-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64795-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64795-124">-Name</span></span>
<span data-ttu-id="64795-125">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="64795-125">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64795-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="64795-126">-QuotaIds</span></span>
<span data-ttu-id="64795-127">A csomag alatti kvóta-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="64795-127">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64795-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64795-128">-ResourceGroupName</span></span>
<span data-ttu-id="64795-129">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="64795-129">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64795-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64795-130">-ResourceId</span></span>
<span data-ttu-id="64795-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="64795-131">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64795-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="64795-132">-SkuIds</span></span>
<span data-ttu-id="64795-133">SKU-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="64795-133">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64795-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="64795-134">-SubscriptionCount</span></span>
<span data-ttu-id="64795-135">Előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="64795-135">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64795-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64795-136">-Confirm</span></span>
<span data-ttu-id="64795-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64795-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64795-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64795-138">-WhatIf</span></span>
<span data-ttu-id="64795-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64795-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64795-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64795-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64795-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64795-141">CommonParameters</span></span>
<span data-ttu-id="64795-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64795-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64795-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64795-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64795-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64795-144">INPUTS</span></span>

## <span data-ttu-id="64795-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64795-145">OUTPUTS</span></span>

### <span data-ttu-id="64795-146">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. terv</span><span class="sxs-lookup"><span data-stu-id="64795-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="64795-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64795-147">NOTES</span></span>

## <span data-ttu-id="64795-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64795-148">RELATED LINKS</span></span>

