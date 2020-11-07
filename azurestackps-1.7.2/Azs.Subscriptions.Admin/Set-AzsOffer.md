---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 285b9509241e9035c007f871ac6395008a1f9cde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839905"
---
# <span data-ttu-id="df977-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="df977-101">Set-AzsOffer</span></span>

## <span data-ttu-id="df977-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df977-102">SYNOPSIS</span></span>
<span data-ttu-id="df977-103">Frissítse az ajánlatot.</span><span class="sxs-lookup"><span data-stu-id="df977-103">Update the offer.</span></span>

## <span data-ttu-id="df977-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df977-104">SYNTAX</span></span>

### <span data-ttu-id="df977-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df977-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df977-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="df977-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df977-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="df977-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df977-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="df977-108">DESCRIPTION</span></span>
<span data-ttu-id="df977-109">Frissítse az ajánlatot.</span><span class="sxs-lookup"><span data-stu-id="df977-109">Update the offer.</span></span>

## <span data-ttu-id="df977-110">Példák</span><span class="sxs-lookup"><span data-stu-id="df977-110">EXAMPLES</span></span>

### <span data-ttu-id="df977-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="df977-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="df977-112">Frissítse az ajánlatot.</span><span class="sxs-lookup"><span data-stu-id="df977-112">Update the offer.</span></span>

## <span data-ttu-id="df977-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df977-113">PARAMETERS</span></span>

### <span data-ttu-id="df977-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="df977-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="df977-115">Azon bővítmény-tervekre mutató hivatkozások, amelyeket a bérlő az ajánlat részeként tetszés szerint tud beszerezni.</span><span class="sxs-lookup"><span data-stu-id="df977-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

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

### <span data-ttu-id="df977-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="df977-116">-BasePlanIds</span></span>
<span data-ttu-id="df977-117">Azoknak az alapterveknek az azonosítói, amelyek azonnal elérhetővé válnak a bérlői webhelyre, amikor a bérlő előfizet az ajánlatra.</span><span class="sxs-lookup"><span data-stu-id="df977-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

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

### <span data-ttu-id="df977-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="df977-118">-Description</span></span>
<span data-ttu-id="df977-119">Az ajánlat leírása.</span><span class="sxs-lookup"><span data-stu-id="df977-119">Description of offer.</span></span>

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

### <span data-ttu-id="df977-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="df977-120">-DisplayName</span></span>
<span data-ttu-id="df977-121">Az ajánlat megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="df977-121">Display name of offer.</span></span>

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

### <span data-ttu-id="df977-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="df977-122">-ExternalReferenceId</span></span>
<span data-ttu-id="df977-123">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="df977-123">External reference identifier.</span></span>

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

### <span data-ttu-id="df977-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df977-124">-InputObject</span></span>
<span data-ttu-id="df977-125">A Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer típusú beviteli objektum.</span><span class="sxs-lookup"><span data-stu-id="df977-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

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

### <span data-ttu-id="df977-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="df977-126">-Location</span></span>
<span data-ttu-id="df977-127">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="df977-127">Location of the resource.</span></span>

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

### <span data-ttu-id="df977-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="df977-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="df977-129">Fiók maximális előfizetése.</span><span class="sxs-lookup"><span data-stu-id="df977-129">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="df977-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df977-130">-Name</span></span>
<span data-ttu-id="df977-131">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="df977-131">Name of an offer.</span></span>

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

### <span data-ttu-id="df977-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df977-132">-ResourceGroupName</span></span>
<span data-ttu-id="df977-133">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="df977-133">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="df977-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df977-134">-ResourceId</span></span>
<span data-ttu-id="df977-135">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="df977-135">The resource id.</span></span>

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

### <span data-ttu-id="df977-136">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="df977-136">-State</span></span>
<span data-ttu-id="df977-137">Kisegítő lehetőségek állapota</span><span class="sxs-lookup"><span data-stu-id="df977-137">Offer accessibility state.</span></span>

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

### <span data-ttu-id="df977-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="df977-138">-SubscriptionCount</span></span>
<span data-ttu-id="df977-139">Aktuális előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="df977-139">Current subscription count.</span></span>

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

### <span data-ttu-id="df977-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df977-140">-Confirm</span></span>
<span data-ttu-id="df977-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df977-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df977-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df977-142">-WhatIf</span></span>
<span data-ttu-id="df977-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df977-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df977-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df977-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df977-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df977-145">CommonParameters</span></span>
<span data-ttu-id="df977-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df977-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df977-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df977-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df977-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df977-148">INPUTS</span></span>

## <span data-ttu-id="df977-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df977-149">OUTPUTS</span></span>

### <span data-ttu-id="df977-150">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="df977-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="df977-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df977-151">NOTES</span></span>

## <span data-ttu-id="df977-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df977-152">RELATED LINKS</span></span>

