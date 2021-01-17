---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 073a059063198e91a1bbcc67814c01c1b786e7c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468606"
---
# <span data-ttu-id="60cf4-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="60cf4-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="60cf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="60cf4-103">Árajánlatot kap a foglaláshoz.</span><span class="sxs-lookup"><span data-stu-id="60cf4-103">Get a quote for the reservation.</span></span> <span data-ttu-id="60cf4-104">Ezt a vásárláshoz `New-AzReservation` továbbkérte.</span><span class="sxs-lookup"><span data-stu-id="60cf4-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="60cf4-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60cf4-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60cf4-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60cf4-106">DESCRIPTION</span></span>
<span data-ttu-id="60cf4-107">Kiszámíthatja a foglalási megrendelés árát.</span><span class="sxs-lookup"><span data-stu-id="60cf4-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="60cf4-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60cf4-108">EXAMPLES</span></span>

### <span data-ttu-id="60cf4-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="60cf4-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="60cf4-110">A katalógus lekérte után az ügyfél a különböző terméket a helytől függően kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="60cf4-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="60cf4-111">Ezeknek az információknak a használatával ellenőrizze a megfelelő árat</span><span class="sxs-lookup"><span data-stu-id="60cf4-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="60cf4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60cf4-112">PARAMETERS</span></span>

### <span data-ttu-id="60cf4-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="60cf4-113">-AppliedScope</span></span>
<span data-ttu-id="60cf4-114">Előfizetés, amely az előny alkalmazását jelenti.</span><span class="sxs-lookup"><span data-stu-id="60cf4-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="60cf4-115">Kötelező, ha az --applied-scope-type is Single.</span><span class="sxs-lookup"><span data-stu-id="60cf4-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="60cf4-116">Ne adja meg, hogy az --applied-scope-type megosztott-e.</span><span class="sxs-lookup"><span data-stu-id="60cf4-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="60cf4-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="60cf4-117">-AppliedScopeType</span></span>
<span data-ttu-id="60cf4-118">Az alkalmazott hatókör típusa a foglalás "Egyszeres" vagy "Megosztott" típussal való frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="60cf4-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="60cf4-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="60cf4-119">-BillingPlan</span></span>
<span data-ttu-id="60cf4-120">Az ehhez az termékváltozathoz elérhető számlázási csomagbeállítások.</span><span class="sxs-lookup"><span data-stu-id="60cf4-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="60cf4-121">"Havi" vagy "Előd"</span><span class="sxs-lookup"><span data-stu-id="60cf4-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="60cf4-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="60cf4-122">-BillingScopeId</span></span>
<span data-ttu-id="60cf4-123">Előfizetés, amely a Foglalás megvásárlásáért fizetendő.</span><span class="sxs-lookup"><span data-stu-id="60cf4-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="60cf4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60cf4-124">-DefaultProfile</span></span>
<span data-ttu-id="60cf4-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60cf4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60cf4-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="60cf4-126">-DisplayName</span></span>
<span data-ttu-id="60cf4-127">Felhasználóbarát név a felhasználó számára, hogy egyszerűen azonosítsa a foglalást.</span><span class="sxs-lookup"><span data-stu-id="60cf4-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="60cf4-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="60cf4-128">-InstanceFlexibility</span></span>
<span data-ttu-id="60cf4-129">A Példány rugalmassága szolgáltatás típusa a foglalás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="60cf4-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="60cf4-130">-Location</span><span class="sxs-lookup"><span data-stu-id="60cf4-130">-Location</span></span>
<span data-ttu-id="60cf4-131">Az a hely, ahol a termékváltozat elérhető.</span><span class="sxs-lookup"><span data-stu-id="60cf4-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="60cf4-132">-Mennyiség</span><span class="sxs-lookup"><span data-stu-id="60cf4-132">-Quantity</span></span>
<span data-ttu-id="60cf4-133">Az ár vagy a vásárlás kiszámítására használt termék mennyisége.</span><span class="sxs-lookup"><span data-stu-id="60cf4-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="60cf4-134">-Megújítás</span><span class="sxs-lookup"><span data-stu-id="60cf4-134">-Renew</span></span>
<span data-ttu-id="60cf4-135">Ha ezt igazra állítva be van állítva, a rendszer automatikusan új foglalást vásárol a lejárati dátumon.</span><span class="sxs-lookup"><span data-stu-id="60cf4-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="60cf4-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="60cf4-136">-ReservedResourceType</span></span>
<span data-ttu-id="60cf4-137">Annak az erőforrásnak a típusa, amelyhez meg kell adni az új adatokat.</span><span class="sxs-lookup"><span data-stu-id="60cf4-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="60cf4-138">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="60cf4-138">-Sku</span></span>
<span data-ttu-id="60cf4-139">Termékváltozat neve, a termékváltozatok listájának lekérte a parancs a foglalási katalógusban</span><span class="sxs-lookup"><span data-stu-id="60cf4-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="60cf4-140">-Term</span><span class="sxs-lookup"><span data-stu-id="60cf4-140">-Term</span></span>
<span data-ttu-id="60cf4-141">Az erőforráshoz rendelkezésre álló foglalási feltételek.</span><span class="sxs-lookup"><span data-stu-id="60cf4-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="60cf4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cf4-142">CommonParameters</span></span>
<span data-ttu-id="60cf4-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60cf4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cf4-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60cf4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cf4-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60cf4-145">INPUTS</span></span>

### <span data-ttu-id="60cf4-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="60cf4-146">None</span></span>

## <span data-ttu-id="60cf4-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60cf4-147">OUTPUTS</span></span>

### <span data-ttu-id="60cf4-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="60cf4-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="60cf4-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60cf4-149">NOTES</span></span>

## <span data-ttu-id="60cf4-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60cf4-150">RELATED LINKS</span></span>
