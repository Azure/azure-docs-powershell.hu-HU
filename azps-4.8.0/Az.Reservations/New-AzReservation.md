---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183356"
---
# <span data-ttu-id="509b6-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="509b6-101">New-AzReservation</span></span>

## <span data-ttu-id="509b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="509b6-102">SYNOPSIS</span></span>
<span data-ttu-id="509b6-103">Foglalás vásárlása</span><span class="sxs-lookup"><span data-stu-id="509b6-103">Purchase a reservation</span></span>

## <span data-ttu-id="509b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="509b6-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="509b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="509b6-105">DESCRIPTION</span></span>
<span data-ttu-id="509b6-106">Foglalási példány vásárlása és kedvezmény megszerzése</span><span class="sxs-lookup"><span data-stu-id="509b6-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="509b6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="509b6-107">EXAMPLES</span></span>

### <span data-ttu-id="509b6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="509b6-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="509b6-109">Az ár kiszámítása után az ügyfél az Purcahse által nyújtott calculatePrice</span><span class="sxs-lookup"><span data-stu-id="509b6-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="509b6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="509b6-110">PARAMETERS</span></span>

### <span data-ttu-id="509b6-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="509b6-111">-AppliedScope</span></span>
<span data-ttu-id="509b6-112">Az előfizetést, amelyre a kedvezményt alkalmazni fogják.</span><span class="sxs-lookup"><span data-stu-id="509b6-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="509b6-113">Kötelező, ha a--alkalmazott-scope-Type egyetlen.</span><span class="sxs-lookup"><span data-stu-id="509b6-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="509b6-114">Do not not adja meg, hogy a---alkalmazott-típus van-e megosztva.</span><span class="sxs-lookup"><span data-stu-id="509b6-114">Do not specify if --applied-scope-type is Shared.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="509b6-115">-AppliedScopeType</span></span>
<span data-ttu-id="509b6-116">Az alkalmazott hatókör típusa a foglalás "single" vagy "Shared" vagy "Shared" értékkel való frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="509b6-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="509b6-117">-BillingPlan</span></span>
<span data-ttu-id="509b6-118">Az SKU-hoz elérhető számlázási terv beállításai.</span><span class="sxs-lookup"><span data-stu-id="509b6-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="509b6-119">"Havonta" vagy "előre"</span><span class="sxs-lookup"><span data-stu-id="509b6-119">"Monthly" or "Upfront"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="509b6-120">-BillingScopeId</span></span>
<span data-ttu-id="509b6-121">Előfizetést, amelyet a foglalás megvásárlásakor kell fizetni.</span><span class="sxs-lookup"><span data-stu-id="509b6-121">Subscription that will be charged for purchasing Reservation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="509b6-122">-DefaultProfile</span></span>
<span data-ttu-id="509b6-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="509b6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="509b6-124">-DisplayName</span></span>
<span data-ttu-id="509b6-125">Felhasználóbarát név: a felhasználók egyszerűen azonosíthatják a foglalást.</span><span class="sxs-lookup"><span data-stu-id="509b6-125">Friendly name for user to easily identified the reservation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="509b6-126">-InstanceFlexibility</span></span>
<span data-ttu-id="509b6-127">{{Fill InstanceFlexibility Description}}</span><span class="sxs-lookup"><span data-stu-id="509b6-127">{{ Fill InstanceFlexibility Description }}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="509b6-128">-Location</span></span>
<span data-ttu-id="509b6-129">Az a hely, ahol a SKU elérhető.</span><span class="sxs-lookup"><span data-stu-id="509b6-129">Location that the SKU is available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-130">-Mennyiség</span><span class="sxs-lookup"><span data-stu-id="509b6-130">-Quantity</span></span>
<span data-ttu-id="509b6-131">Az ár vagy a beszerzés kiszámítására szolgáló termék mennyisége.</span><span class="sxs-lookup"><span data-stu-id="509b6-131">Quantity of product for calculating price or purchasing.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-132">-Renew</span><span class="sxs-lookup"><span data-stu-id="509b6-132">-Renew</span></span>
<span data-ttu-id="509b6-133">A True beállítás értéke automatikusan új foglalást vásárol a lejárati dátum időpontjában.</span><span class="sxs-lookup"><span data-stu-id="509b6-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="509b6-134">-ReservationOrderId</span></span>
<span data-ttu-id="509b6-135">A megvásárolt foglalási megrendelés azonosítója, a fenntartási feltételek szerinti generálás – rendelés kiszámítása.</span><span class="sxs-lookup"><span data-stu-id="509b6-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="509b6-136">-ReservedResourceType</span></span>
<span data-ttu-id="509b6-137">Annak az erőforrásnak a típusa, amelyre a SKU-t be kell írni.</span><span class="sxs-lookup"><span data-stu-id="509b6-137">Type of the resource for which the skus should be provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="509b6-138">-Sku</span></span>
<span data-ttu-id="509b6-139">SKU neve</span><span class="sxs-lookup"><span data-stu-id="509b6-139">Sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-140">Távú</span><span class="sxs-lookup"><span data-stu-id="509b6-140">-Term</span></span>
<span data-ttu-id="509b6-141">A rendelkezésre álló Foglalási feltételek az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="509b6-141">Available reservation terms for this resource.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="509b6-142">-Confirm</span></span>
<span data-ttu-id="509b6-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="509b6-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="509b6-144">-WhatIf</span></span>
<span data-ttu-id="509b6-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="509b6-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="509b6-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="509b6-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="509b6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="509b6-147">CommonParameters</span></span>
<span data-ttu-id="509b6-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="509b6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="509b6-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="509b6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="509b6-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="509b6-150">INPUTS</span></span>

### <span data-ttu-id="509b6-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="509b6-151">None</span></span>

## <span data-ttu-id="509b6-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="509b6-152">OUTPUTS</span></span>

### <span data-ttu-id="509b6-153">Microsoft. Azure. Management. Reservations. models. ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="509b6-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="509b6-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="509b6-154">NOTES</span></span>

## <span data-ttu-id="509b6-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="509b6-155">RELATED LINKS</span></span>
