---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 844e67f7491825fe0484a60d55cb254988cfb5c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011316"
---
# <span data-ttu-id="5a582-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="5a582-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="5a582-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a582-102">SYNOPSIS</span></span>
<span data-ttu-id="5a582-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="5a582-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="5a582-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a582-104">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a582-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a582-105">DESCRIPTION</span></span>
<span data-ttu-id="5a582-106">Az ár kiszámítása a foglalási rendelések elhelyezéséhez</span><span class="sxs-lookup"><span data-stu-id="5a582-106">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="5a582-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5a582-107">EXAMPLES</span></span>

### <span data-ttu-id="5a582-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5a582-108">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="5a582-109">A katalógus beolvasása után az ügyfél a helytől függően eltérő terméket kaphat.</span><span class="sxs-lookup"><span data-stu-id="5a582-109">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="5a582-110">Ezekkel az információkkal ellenőrizze az ár megfelelő használatát</span><span class="sxs-lookup"><span data-stu-id="5a582-110">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="5a582-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a582-111">PARAMETERS</span></span>

### <span data-ttu-id="5a582-112">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="5a582-112">-AppliedScope</span></span>
<span data-ttu-id="5a582-113">Az előfizetést, amelyre a kedvezményt alkalmazni fogják.</span><span class="sxs-lookup"><span data-stu-id="5a582-113">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="5a582-114">Kötelező, ha a--alkalmazott-scope-Type egyetlen.</span><span class="sxs-lookup"><span data-stu-id="5a582-114">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="5a582-115">Do not not adja meg, hogy a---alkalmazott-típus van-e megosztva.</span><span class="sxs-lookup"><span data-stu-id="5a582-115">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="5a582-116">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="5a582-116">-AppliedScopeType</span></span>
<span data-ttu-id="5a582-117">Az alkalmazott hatókör típusa a foglalás "single" vagy "Shared" vagy "Shared" értékkel való frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="5a582-117">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="5a582-118">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="5a582-118">-BillingPlan</span></span>
<span data-ttu-id="5a582-119">Az SKU-hoz elérhető számlázási terv beállításai.</span><span class="sxs-lookup"><span data-stu-id="5a582-119">The billing plan options available for this SKU.</span></span> <span data-ttu-id="5a582-120">"Havonta" vagy "előre"</span><span class="sxs-lookup"><span data-stu-id="5a582-120">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="5a582-121">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="5a582-121">-BillingScopeId</span></span>
<span data-ttu-id="5a582-122">Előfizetést, amelyet a foglalás megvásárlásakor kell fizetni.</span><span class="sxs-lookup"><span data-stu-id="5a582-122">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="5a582-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a582-123">-DefaultProfile</span></span>
<span data-ttu-id="5a582-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a582-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a582-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a582-125">-DisplayName</span></span>
<span data-ttu-id="5a582-126">Felhasználóbarát név: a felhasználók egyszerűen azonosíthatják a foglalást.</span><span class="sxs-lookup"><span data-stu-id="5a582-126">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="5a582-127">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="5a582-127">-InstanceFlexibility</span></span>
<span data-ttu-id="5a582-128">Annak a példánynak a típusa, amely rugalmasságot biztosít a foglalás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="5a582-128">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="5a582-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="5a582-129">-Location</span></span>
<span data-ttu-id="5a582-130">Az a hely, ahol a SKU elérhető.</span><span class="sxs-lookup"><span data-stu-id="5a582-130">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="5a582-131">-Mennyiség</span><span class="sxs-lookup"><span data-stu-id="5a582-131">-Quantity</span></span>
<span data-ttu-id="5a582-132">Az ár vagy a beszerzés kiszámítására szolgáló termék mennyisége.</span><span class="sxs-lookup"><span data-stu-id="5a582-132">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="5a582-133">-Renew</span><span class="sxs-lookup"><span data-stu-id="5a582-133">-Renew</span></span>
<span data-ttu-id="5a582-134">A True beállítás értéke automatikusan új foglalást vásárol a lejárati dátum időpontjában.</span><span class="sxs-lookup"><span data-stu-id="5a582-134">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="5a582-135">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="5a582-135">-ReservedResourceType</span></span>
<span data-ttu-id="5a582-136">Annak az erőforrásnak a típusa, amelyre a SKU-t be kell írni.</span><span class="sxs-lookup"><span data-stu-id="5a582-136">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="5a582-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="5a582-137">-Sku</span></span>
<span data-ttu-id="5a582-138">SKU Name (SKU): a SKU-lista beszerzése a következő paranccsal: a foglalási katalógus megjelenítése</span><span class="sxs-lookup"><span data-stu-id="5a582-138">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="5a582-139">Távú</span><span class="sxs-lookup"><span data-stu-id="5a582-139">-Term</span></span>
<span data-ttu-id="5a582-140">A rendelkezésre álló Foglalási feltételek az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="5a582-140">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="5a582-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a582-141">CommonParameters</span></span>
<span data-ttu-id="5a582-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a582-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a582-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5a582-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a582-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a582-144">INPUTS</span></span>

### <span data-ttu-id="5a582-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="5a582-145">None</span></span>

## <span data-ttu-id="5a582-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a582-146">OUTPUTS</span></span>

### <span data-ttu-id="5a582-147">Microsoft. Azure. Management. Reservations. models. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="5a582-147">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="5a582-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a582-148">NOTES</span></span>

## <span data-ttu-id="5a582-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a582-149">RELATED LINKS</span></span>
