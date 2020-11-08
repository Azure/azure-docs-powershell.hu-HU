---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b08aed00a4c16bd2031608ff795a4dde8491859
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94017071"
---
# <span data-ttu-id="0c606-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="0c606-101">Set-AzsOffer</span></span>

## <span data-ttu-id="0c606-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c606-102">SYNOPSIS</span></span>
<span data-ttu-id="0c606-103">Frissítse az ajánlatot.</span><span class="sxs-lookup"><span data-stu-id="0c606-103">Update the offer.</span></span>

## <span data-ttu-id="0c606-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c606-104">SYNTAX</span></span>

### <span data-ttu-id="0c606-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c606-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c606-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0c606-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c606-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c606-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c606-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c606-108">DESCRIPTION</span></span>
<span data-ttu-id="0c606-109">Frissítse az ajánlatot.</span><span class="sxs-lookup"><span data-stu-id="0c606-109">Update the offer.</span></span>

## <span data-ttu-id="0c606-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0c606-110">EXAMPLES</span></span>

### <span data-ttu-id="0c606-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0c606-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="0c606-112">Frissítse az ajánlatot.</span><span class="sxs-lookup"><span data-stu-id="0c606-112">Update the offer.</span></span>

## <span data-ttu-id="0c606-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c606-113">PARAMETERS</span></span>

### <span data-ttu-id="0c606-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="0c606-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="0c606-115">Azon bővítmény-tervekre mutató hivatkozások, amelyeket a bérlő az ajánlat részeként tetszés szerint tud beszerezni.</span><span class="sxs-lookup"><span data-stu-id="0c606-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c606-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="0c606-116">-BasePlanIds</span></span>
<span data-ttu-id="0c606-117">Azoknak az alapterveknek az azonosítói, amelyek azonnal elérhetővé válnak a bérlői webhelyre, amikor a bérlő előfizet az ajánlatra.</span><span class="sxs-lookup"><span data-stu-id="0c606-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

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

### <span data-ttu-id="0c606-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0c606-118">-Description</span></span>
<span data-ttu-id="0c606-119">Az ajánlat leírása.</span><span class="sxs-lookup"><span data-stu-id="0c606-119">Description of offer.</span></span>

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

### <span data-ttu-id="0c606-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0c606-120">-DisplayName</span></span>
<span data-ttu-id="0c606-121">Az ajánlat megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="0c606-121">Display name of offer.</span></span>

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

### <span data-ttu-id="0c606-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="0c606-122">-ExternalReferenceId</span></span>
<span data-ttu-id="0c606-123">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="0c606-123">External reference identifier.</span></span>

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

### <span data-ttu-id="0c606-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c606-124">-InputObject</span></span>
<span data-ttu-id="0c606-125">A Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer típusú beviteli objektum.</span><span class="sxs-lookup"><span data-stu-id="0c606-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

```yaml
Type: Offer
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c606-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="0c606-126">-Location</span></span>
<span data-ttu-id="0c606-127">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="0c606-127">Location of the resource.</span></span>

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

### <span data-ttu-id="0c606-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="0c606-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="0c606-129">Fiók maximális előfizetése.</span><span class="sxs-lookup"><span data-stu-id="0c606-129">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="0c606-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c606-130">-Name</span></span>
<span data-ttu-id="0c606-131">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="0c606-131">Name of an offer.</span></span>

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

### <span data-ttu-id="0c606-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c606-132">-ResourceGroupName</span></span>
<span data-ttu-id="0c606-133">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="0c606-133">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="0c606-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c606-134">-ResourceId</span></span>
<span data-ttu-id="0c606-135">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0c606-135">The resource id.</span></span>

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

### <span data-ttu-id="0c606-136">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="0c606-136">-State</span></span>
<span data-ttu-id="0c606-137">Kisegítő lehetőségek állapota</span><span class="sxs-lookup"><span data-stu-id="0c606-137">Offer accessibility state.</span></span>

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

### <span data-ttu-id="0c606-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="0c606-138">-SubscriptionCount</span></span>
<span data-ttu-id="0c606-139">Aktuális előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="0c606-139">Current subscription count.</span></span>

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

### <span data-ttu-id="0c606-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c606-140">-Confirm</span></span>
<span data-ttu-id="0c606-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c606-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c606-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c606-142">-WhatIf</span></span>
<span data-ttu-id="0c606-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0c606-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c606-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c606-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c606-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c606-145">CommonParameters</span></span>
<span data-ttu-id="0c606-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c606-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c606-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c606-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c606-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c606-148">INPUTS</span></span>

## <span data-ttu-id="0c606-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c606-149">OUTPUTS</span></span>

### <span data-ttu-id="0c606-150">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="0c606-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="0c606-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c606-151">NOTES</span></span>

## <span data-ttu-id="0c606-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c606-152">RELATED LINKS</span></span>

