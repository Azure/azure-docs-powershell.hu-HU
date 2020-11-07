---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9ff6532cb43d7ece7460651eb4493201de4734b1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840316"
---
# <span data-ttu-id="6029f-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="6029f-101">Set-AzsPlan</span></span>

## <span data-ttu-id="6029f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6029f-102">SYNOPSIS</span></span>
<span data-ttu-id="6029f-103">A megadott csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="6029f-103">Updates the specified plan</span></span>

## <span data-ttu-id="6029f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6029f-104">SYNTAX</span></span>

### <span data-ttu-id="6029f-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6029f-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6029f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6029f-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6029f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6029f-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6029f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6029f-108">DESCRIPTION</span></span>
<span data-ttu-id="6029f-109">A megadott csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="6029f-109">Updates the specified plan</span></span>

## <span data-ttu-id="6029f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6029f-110">EXAMPLES</span></span>

### <span data-ttu-id="6029f-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6029f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="6029f-112">A megadott csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="6029f-112">Updates the specified plan</span></span>

## <span data-ttu-id="6029f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6029f-113">PARAMETERS</span></span>

### <span data-ttu-id="6029f-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6029f-114">-Description</span></span>
<span data-ttu-id="6029f-115">A terv leírása.</span><span class="sxs-lookup"><span data-stu-id="6029f-115">Description of the plan.</span></span>

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

### <span data-ttu-id="6029f-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6029f-116">-DisplayName</span></span>
<span data-ttu-id="6029f-117">Megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="6029f-117">Display name.</span></span>

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

### <span data-ttu-id="6029f-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="6029f-118">-ExternalReferenceId</span></span>
<span data-ttu-id="6029f-119">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="6029f-119">External reference identifier.</span></span>

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

### <span data-ttu-id="6029f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6029f-120">-InputObject</span></span>
<span data-ttu-id="6029f-121">A Microsoft. AzureStack. Management. Subscriptions. admin. models. terv típusú beviteli objektum.</span><span class="sxs-lookup"><span data-stu-id="6029f-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

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

### <span data-ttu-id="6029f-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="6029f-122">-Location</span></span>
<span data-ttu-id="6029f-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="6029f-123">Location of the resource.</span></span>

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

### <span data-ttu-id="6029f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6029f-124">-Name</span></span>
<span data-ttu-id="6029f-125">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="6029f-125">Name of the plan.</span></span>

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

### <span data-ttu-id="6029f-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="6029f-126">-QuotaIds</span></span>
<span data-ttu-id="6029f-127">A csomag alatti kvóta-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="6029f-127">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="6029f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6029f-128">-ResourceGroupName</span></span>
<span data-ttu-id="6029f-129">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="6029f-129">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6029f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6029f-130">-ResourceId</span></span>
<span data-ttu-id="6029f-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6029f-131">The resource id.</span></span>

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

### <span data-ttu-id="6029f-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="6029f-132">-SkuIds</span></span>
<span data-ttu-id="6029f-133">SKU-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="6029f-133">SKU identifiers.</span></span>

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

### <span data-ttu-id="6029f-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="6029f-134">-SubscriptionCount</span></span>
<span data-ttu-id="6029f-135">Előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="6029f-135">Subscription count.</span></span>

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

### <span data-ttu-id="6029f-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6029f-136">-Confirm</span></span>
<span data-ttu-id="6029f-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6029f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6029f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6029f-138">-WhatIf</span></span>
<span data-ttu-id="6029f-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6029f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6029f-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6029f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6029f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6029f-141">CommonParameters</span></span>
<span data-ttu-id="6029f-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6029f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6029f-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6029f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6029f-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6029f-144">INPUTS</span></span>

## <span data-ttu-id="6029f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6029f-145">OUTPUTS</span></span>

### <span data-ttu-id="6029f-146">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. terv</span><span class="sxs-lookup"><span data-stu-id="6029f-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="6029f-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6029f-147">NOTES</span></span>

## <span data-ttu-id="6029f-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6029f-148">RELATED LINKS</span></span>

