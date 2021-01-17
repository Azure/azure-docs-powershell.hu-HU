---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468605"
---
# <span data-ttu-id="de96d-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="de96d-101">New-AzReservation</span></span>

## <span data-ttu-id="de96d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de96d-102">SYNOPSIS</span></span>
<span data-ttu-id="de96d-103">Foglalás vásárlása</span><span class="sxs-lookup"><span data-stu-id="de96d-103">Purchase a reservation</span></span>

## <span data-ttu-id="de96d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="de96d-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de96d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="de96d-105">DESCRIPTION</span></span>
<span data-ttu-id="de96d-106">Foglalási példány vásárlása és előny</span><span class="sxs-lookup"><span data-stu-id="de96d-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="de96d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="de96d-107">EXAMPLES</span></span>

### <span data-ttu-id="de96d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="de96d-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="de96d-109">Az ár kiszámítása után az ügyfél az Ár kiszámításával véglegesen kiszámíthatja a RI által adott adatokat.</span><span class="sxs-lookup"><span data-stu-id="de96d-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="de96d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de96d-110">PARAMETERS</span></span>

### <span data-ttu-id="de96d-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="de96d-111">-AppliedScope</span></span>
<span data-ttu-id="de96d-112">Előfizetés, amely az előny alkalmazását jelenti.</span><span class="sxs-lookup"><span data-stu-id="de96d-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="de96d-113">Kötelező, ha az --applied-scope-type is Single.</span><span class="sxs-lookup"><span data-stu-id="de96d-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="de96d-114">Ne adja meg, hogy az --applied-scope-type megosztott-e.</span><span class="sxs-lookup"><span data-stu-id="de96d-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="de96d-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="de96d-115">-AppliedScopeType</span></span>
<span data-ttu-id="de96d-116">Az alkalmazott hatókör típusa a foglalás "Egyszeres" vagy "Megosztott" típussal való frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="de96d-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="de96d-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="de96d-117">-BillingPlan</span></span>
<span data-ttu-id="de96d-118">Az ehhez az termékváltozathoz elérhető számlázási csomagbeállítások.</span><span class="sxs-lookup"><span data-stu-id="de96d-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="de96d-119">"Havi" vagy "Előd"</span><span class="sxs-lookup"><span data-stu-id="de96d-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="de96d-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="de96d-120">-BillingScopeId</span></span>
<span data-ttu-id="de96d-121">Előfizetés, amely a Foglalás megvásárlásáért fizetendő.</span><span class="sxs-lookup"><span data-stu-id="de96d-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="de96d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de96d-122">-DefaultProfile</span></span>
<span data-ttu-id="de96d-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de96d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de96d-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="de96d-124">-DisplayName</span></span>
<span data-ttu-id="de96d-125">Felhasználóbarát név a felhasználó számára, hogy egyszerűen azonosítsa a foglalást.</span><span class="sxs-lookup"><span data-stu-id="de96d-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="de96d-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="de96d-126">-InstanceFlexibility</span></span>
<span data-ttu-id="de96d-127">{{ Fill InstanceFlexibility Description }}</span><span class="sxs-lookup"><span data-stu-id="de96d-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="de96d-128">-Location</span><span class="sxs-lookup"><span data-stu-id="de96d-128">-Location</span></span>
<span data-ttu-id="de96d-129">Az a hely, ahol a termékváltozat elérhető.</span><span class="sxs-lookup"><span data-stu-id="de96d-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="de96d-130">-Mennyiség</span><span class="sxs-lookup"><span data-stu-id="de96d-130">-Quantity</span></span>
<span data-ttu-id="de96d-131">Az ár vagy a vásárlás kiszámítására használt termék mennyisége.</span><span class="sxs-lookup"><span data-stu-id="de96d-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="de96d-132">-Megújítás</span><span class="sxs-lookup"><span data-stu-id="de96d-132">-Renew</span></span>
<span data-ttu-id="de96d-133">Ha ezt igazra állítva be van állítva, a rendszer automatikusan új foglalást vásárol a lejárati dátumon.</span><span class="sxs-lookup"><span data-stu-id="de96d-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="de96d-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="de96d-134">-ReservationOrderId</span></span>
<span data-ttu-id="de96d-135">A megvásárolni szükséges foglalási rendelés azonosítója, generálás foglalási megrendelés alapján kiszámítva.</span><span class="sxs-lookup"><span data-stu-id="de96d-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="de96d-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="de96d-136">-ReservedResourceType</span></span>
<span data-ttu-id="de96d-137">Annak az erőforrásnak a típusa, amelyhez meg kell adni az új adatokat.</span><span class="sxs-lookup"><span data-stu-id="de96d-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="de96d-138">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="de96d-138">-Sku</span></span>
<span data-ttu-id="de96d-139">Termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="de96d-139">Sku name</span></span>

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

### <span data-ttu-id="de96d-140">-Term</span><span class="sxs-lookup"><span data-stu-id="de96d-140">-Term</span></span>
<span data-ttu-id="de96d-141">Az erőforráshoz rendelkezésre álló foglalási feltételek.</span><span class="sxs-lookup"><span data-stu-id="de96d-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="de96d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de96d-142">-Confirm</span></span>
<span data-ttu-id="de96d-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="de96d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de96d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de96d-144">-WhatIf</span></span>
<span data-ttu-id="de96d-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="de96d-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de96d-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de96d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de96d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de96d-147">CommonParameters</span></span>
<span data-ttu-id="de96d-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de96d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de96d-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de96d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de96d-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de96d-150">INPUTS</span></span>

### <span data-ttu-id="de96d-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="de96d-151">None</span></span>

## <span data-ttu-id="de96d-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de96d-152">OUTPUTS</span></span>

### <span data-ttu-id="de96d-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="de96d-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="de96d-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="de96d-154">NOTES</span></span>

## <span data-ttu-id="de96d-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de96d-155">RELATED LINKS</span></span>
