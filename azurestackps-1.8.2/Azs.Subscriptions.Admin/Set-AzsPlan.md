---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9ff6532cb43d7ece7460651eb4493201de4734b1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017002"
---
# <span data-ttu-id="bf0ce-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="bf0ce-101">Set-AzsPlan</span></span>

## <span data-ttu-id="bf0ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0ce-103">A megadott csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="bf0ce-103">Updates the specified plan</span></span>

## <span data-ttu-id="bf0ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf0ce-104">SYNTAX</span></span>

### <span data-ttu-id="bf0ce-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf0ce-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf0ce-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bf0ce-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf0ce-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf0ce-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf0ce-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf0ce-108">DESCRIPTION</span></span>
<span data-ttu-id="bf0ce-109">A megadott csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="bf0ce-109">Updates the specified plan</span></span>

## <span data-ttu-id="bf0ce-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bf0ce-110">EXAMPLES</span></span>

### <span data-ttu-id="bf0ce-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bf0ce-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="bf0ce-112">A megadott csomag frissítése</span><span class="sxs-lookup"><span data-stu-id="bf0ce-112">Updates the specified plan</span></span>

## <span data-ttu-id="bf0ce-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf0ce-113">PARAMETERS</span></span>

### <span data-ttu-id="bf0ce-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="bf0ce-114">-Description</span></span>
<span data-ttu-id="bf0ce-115">A terv leírása.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-115">Description of the plan.</span></span>

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

### <span data-ttu-id="bf0ce-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bf0ce-116">-DisplayName</span></span>
<span data-ttu-id="bf0ce-117">Megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-117">Display name.</span></span>

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

### <span data-ttu-id="bf0ce-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="bf0ce-118">-ExternalReferenceId</span></span>
<span data-ttu-id="bf0ce-119">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="bf0ce-119">External reference identifier.</span></span>

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

### <span data-ttu-id="bf0ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf0ce-120">-InputObject</span></span>
<span data-ttu-id="bf0ce-121">A Microsoft. AzureStack. Management. Subscriptions. admin. models. terv típusú beviteli objektum.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

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

### <span data-ttu-id="bf0ce-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="bf0ce-122">-Location</span></span>
<span data-ttu-id="bf0ce-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-123">Location of the resource.</span></span>

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

### <span data-ttu-id="bf0ce-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf0ce-124">-Name</span></span>
<span data-ttu-id="bf0ce-125">A terv neve.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-125">Name of the plan.</span></span>

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

### <span data-ttu-id="bf0ce-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="bf0ce-126">-QuotaIds</span></span>
<span data-ttu-id="bf0ce-127">A csomag alatti kvóta-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-127">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="bf0ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf0ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="bf0ce-129">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-129">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="bf0ce-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf0ce-130">-ResourceId</span></span>
<span data-ttu-id="bf0ce-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-131">The resource id.</span></span>

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

### <span data-ttu-id="bf0ce-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="bf0ce-132">-SkuIds</span></span>
<span data-ttu-id="bf0ce-133">SKU-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-133">SKU identifiers.</span></span>

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

### <span data-ttu-id="bf0ce-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="bf0ce-134">-SubscriptionCount</span></span>
<span data-ttu-id="bf0ce-135">Előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="bf0ce-135">Subscription count.</span></span>

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

### <span data-ttu-id="bf0ce-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf0ce-136">-Confirm</span></span>
<span data-ttu-id="bf0ce-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf0ce-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf0ce-138">-WhatIf</span></span>
<span data-ttu-id="bf0ce-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf0ce-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf0ce-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf0ce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0ce-141">CommonParameters</span></span>
<span data-ttu-id="bf0ce-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf0ce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0ce-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf0ce-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0ce-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf0ce-144">INPUTS</span></span>

## <span data-ttu-id="bf0ce-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf0ce-145">OUTPUTS</span></span>

### <span data-ttu-id="bf0ce-146">Microsoft. AzureStack. Management. Subscriptions. admin. modellek. terv</span><span class="sxs-lookup"><span data-stu-id="bf0ce-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="bf0ce-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf0ce-147">NOTES</span></span>

## <span data-ttu-id="bf0ce-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf0ce-148">RELATED LINKS</span></span>

