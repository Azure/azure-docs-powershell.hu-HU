---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cce59bbbef69f10f39478d784d688a4f1de312fb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016866"
---
# <span data-ttu-id="55ef9-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="55ef9-101">New-AzsOffer</span></span>

## <span data-ttu-id="55ef9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="55ef9-103">Új ajánlatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="55ef9-103">Creates a new offer.</span></span>

## <span data-ttu-id="55ef9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55ef9-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55ef9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="55ef9-106">Az ajánlat létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="55ef9-106">Create or update the offer.</span></span>

## <span data-ttu-id="55ef9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="55ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="55ef9-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="55ef9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="55ef9-109">Új ajánlatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="55ef9-109">Creates a new offer.</span></span>

## <span data-ttu-id="55ef9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55ef9-110">PARAMETERS</span></span>

### <span data-ttu-id="55ef9-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="55ef9-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="55ef9-112">Azon bővítmény-tervekre mutató hivatkozások, amelyeket a bérlő az ajánlat részeként tetszés szerint tud beszerezni.</span><span class="sxs-lookup"><span data-stu-id="55ef9-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

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

### <span data-ttu-id="55ef9-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="55ef9-113">-BasePlanIds</span></span>
<span data-ttu-id="55ef9-114">Azoknak az alapterveknek az azonosítói, amelyek azonnal elérhetővé válnak a bérlői webhelyre, amikor a bérlő előfizet az ajánlatra.</span><span class="sxs-lookup"><span data-stu-id="55ef9-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

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

### <span data-ttu-id="55ef9-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="55ef9-115">-Description</span></span>
<span data-ttu-id="55ef9-116">Az ajánlat leírása.</span><span class="sxs-lookup"><span data-stu-id="55ef9-116">Description of offer.</span></span>

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

### <span data-ttu-id="55ef9-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="55ef9-117">-DisplayName</span></span>
<span data-ttu-id="55ef9-118">Az ajánlat megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="55ef9-118">Display name of offer.</span></span>

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

### <span data-ttu-id="55ef9-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="55ef9-119">-ExternalReferenceId</span></span>
<span data-ttu-id="55ef9-120">Külső hivatkozási azonosító</span><span class="sxs-lookup"><span data-stu-id="55ef9-120">External reference identifier.</span></span>

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

### <span data-ttu-id="55ef9-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="55ef9-121">-Location</span></span>
<span data-ttu-id="55ef9-122">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="55ef9-122">Location of the resource.</span></span>

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

### <span data-ttu-id="55ef9-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="55ef9-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="55ef9-124">Fiók maximális előfizetése.</span><span class="sxs-lookup"><span data-stu-id="55ef9-124">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="55ef9-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="55ef9-125">-Name</span></span>
<span data-ttu-id="55ef9-126">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="55ef9-126">Name of an offer.</span></span>

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

### <span data-ttu-id="55ef9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ef9-127">-ResourceGroupName</span></span>
<span data-ttu-id="55ef9-128">Az az erőforráscsoport, amelyet az erőforrás a csoportban található.</span><span class="sxs-lookup"><span data-stu-id="55ef9-128">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="55ef9-129">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="55ef9-129">-State</span></span>
<span data-ttu-id="55ef9-130">Kisegítő lehetőségek állapota</span><span class="sxs-lookup"><span data-stu-id="55ef9-130">Offer accessibility state.</span></span>
<span data-ttu-id="55ef9-131">Az alapértelmezett érték a magánjellegű.</span><span class="sxs-lookup"><span data-stu-id="55ef9-131">Default value is Private.</span></span>
<span data-ttu-id="55ef9-132">Ezt a paramétert egy jövőbeli kiadásban fogja érvényteleníteni</span><span class="sxs-lookup"><span data-stu-id="55ef9-132">This parameter will be deprecated in a future release</span></span>

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

### <span data-ttu-id="55ef9-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="55ef9-133">-SubscriptionCount</span></span>
<span data-ttu-id="55ef9-134">Aktuális előfizetés száma</span><span class="sxs-lookup"><span data-stu-id="55ef9-134">Current subscription count.</span></span>

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

### <span data-ttu-id="55ef9-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="55ef9-135">-Confirm</span></span>
<span data-ttu-id="55ef9-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="55ef9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55ef9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55ef9-137">-WhatIf</span></span>
<span data-ttu-id="55ef9-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="55ef9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55ef9-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55ef9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55ef9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ef9-140">CommonParameters</span></span>
<span data-ttu-id="55ef9-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55ef9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ef9-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55ef9-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ef9-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55ef9-143">INPUTS</span></span>

## <span data-ttu-id="55ef9-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55ef9-144">OUTPUTS</span></span>

### <span data-ttu-id="55ef9-145">Microsoft. AzureStack. Management. Subscriptions. admin. models. Offer</span><span class="sxs-lookup"><span data-stu-id="55ef9-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="55ef9-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55ef9-146">NOTES</span></span>

## <span data-ttu-id="55ef9-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55ef9-147">RELATED LINKS</span></span>

