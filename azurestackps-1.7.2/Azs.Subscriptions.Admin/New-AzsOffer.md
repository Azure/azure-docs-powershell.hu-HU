---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87ad48de1fa4ae05f90f067e8a0a2eac2c4fdd0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840099"
---
# <span data-ttu-id="8a675-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="8a675-101">New-AzsOffer</span></span>

## <span data-ttu-id="8a675-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a675-102">SYNOPSIS</span></span>
<span data-ttu-id="8a675-103">Új ajánlatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8a675-103">Creates a new offer.</span></span>

## <span data-ttu-id="8a675-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a675-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a675-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a675-105">DESCRIPTION</span></span>
<span data-ttu-id="8a675-106">Az ajánlat létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="8a675-106">Create or update the offer.</span></span>

## <span data-ttu-id="8a675-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8a675-107">EXAMPLES</span></span>

### <span data-ttu-id="8a675-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8a675-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="8a675-109">Új ajánlatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8a675-109">Creates a new offer.</span></span>

## <span data-ttu-id="8a675-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a675-110">PARAMETERS</span></span>

### <span data-ttu-id="8a675-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="8a675-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="8a675-112">Azon bővítmény-tervekre mutató hivatkozások, amelyeket a bérlő az ajánlat részeként tetszés szerint tud beszerezni.</span><span class="sxs-lookup"><span data-stu-id="8a675-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a675-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="8a675-113">-BasePlanIds</span></span>
<span data-ttu-id="8a675-114">Azoknak az alapterveknek az azonosítói, amelyek azonnal elérhetővé válnak a bérlői webhelyre, amikor a bérlő előfizet az ajánlatra.</span><span class="sxs-lookup"><span data-stu-id="8a675-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a675-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8a675-115">-Description</span></span>
<span data-ttu-id="8a675-116">Az ajánlat leírása.</span><span class="sxs-lookup"><span data-stu-id="8a675-116">Description of offer.</span></span>

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

### <span data-ttu-id="8a675-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8a675-117">-DisplayName</span></span>
<span data-ttu-id="8a675-118">Az ajánlat megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="8a675-118">Display name of offer.</span></span>

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

### <span data-ttu-id="8a675-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="8a675-119">-ExternalReferenceId</span></span>
<span data-ttu-id="8a675-120">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="8a675-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a675-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="8a675-121">-Location</span></span>
<span data-ttu-id="8a675-122">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="8a675-122">Location of the resource.</span></span>

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

### <span data-ttu-id="8a675-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="8a675-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="8a675-124">Fiók maximális előfizetése.</span><span class="sxs-lookup"><span data-stu-id="8a675-124">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="8a675-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a675-125">-Name</span></span>
<span data-ttu-id="8a675-126">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="8a675-126">Name of an offer.</span></span>

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

### <span data-ttu-id="8a675-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a675-127">-ResourceGroupName</span></span>
<span data-ttu-id="8a675-128">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="8a675-128">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8a675-129">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="8a675-129">-State</span></span>
<span data-ttu-id="8a675-130">Kisegítő lehetőségek állapota</span><span class="sxs-lookup"><span data-stu-id="8a675-130">Offer accessibility state.</span></span>
<span data-ttu-id="8a675-131">Az alapértelmezett érték a magánjellegű.</span><span class="sxs-lookup"><span data-stu-id="8a675-131">Default value is Private.</span></span>
<span data-ttu-id="8a675-132">Ezt a paramétert egy jövőbeli kiadásban fogja érvényteleníteni</span><span class="sxs-lookup"><span data-stu-id="8a675-132">This parameter will be deprecated in a future release</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a675-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="8a675-133">-SubscriptionCount</span></span>
<span data-ttu-id="8a675-134">Aktuális előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="8a675-134">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a675-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8a675-135">-Confirm</span></span>
<span data-ttu-id="8a675-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8a675-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a675-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a675-137">-WhatIf</span></span>
<span data-ttu-id="8a675-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8a675-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a675-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8a675-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a675-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a675-140">CommonParameters</span></span>
<span data-ttu-id="8a675-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a675-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a675-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a675-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a675-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a675-143">INPUTS</span></span>

## <span data-ttu-id="8a675-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a675-144">OUTPUTS</span></span>

### <span data-ttu-id="8a675-145">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="8a675-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="8a675-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a675-146">NOTES</span></span>

## <span data-ttu-id="8a675-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a675-147">RELATED LINKS</span></span>

