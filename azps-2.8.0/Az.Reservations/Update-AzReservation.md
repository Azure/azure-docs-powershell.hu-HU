---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 7e7b32322d6c6a131ee906c56b0c4fbdd0a5d63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838187"
---
# <span data-ttu-id="ec602-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="ec602-101">Update-AzReservation</span></span>

## <span data-ttu-id="ec602-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec602-102">SYNOPSIS</span></span>
<span data-ttu-id="ec602-103">Update a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="ec602-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="ec602-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec602-104">SYNTAX</span></span>

### <span data-ttu-id="ec602-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec602-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec602-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="ec602-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec602-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec602-107">DESCRIPTION</span></span>
<span data-ttu-id="ec602-108">Frissíti az alkalmazott hatóköröket `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="ec602-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="ec602-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ec602-109">EXAMPLES</span></span>

### <span data-ttu-id="ec602-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ec602-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="ec602-111">Frissíti a megadott AppliedScopeType az `Reservation` egy-és InstanceFlexibility be értékre.</span><span class="sxs-lookup"><span data-stu-id="ec602-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="ec602-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="ec602-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="ec602-113">A megadott AppliedScopeType frissíti a `Reservation` megosztott és a InstanceFlexibility.</span><span class="sxs-lookup"><span data-stu-id="ec602-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="ec602-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec602-114">PARAMETERS</span></span>

### <span data-ttu-id="ec602-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="ec602-115">-AppliedScope</span></span>
<span data-ttu-id="ec602-116">A SubscriptionId `Reservation` alkalmazása</span><span class="sxs-lookup"><span data-stu-id="ec602-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="ec602-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="ec602-117">-AppliedScopeType</span></span>
<span data-ttu-id="ec602-118">Az alkalmazott hatókör típusa</span><span class="sxs-lookup"><span data-stu-id="ec602-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="ec602-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec602-119">-DefaultProfile</span></span>
<span data-ttu-id="ec602-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec602-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec602-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="ec602-121">-InstanceFlexibility</span></span>
<span data-ttu-id="ec602-122">Ha van, frissíti a InstanceFlexibility értékét `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="ec602-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="ec602-123">Ha nincs megadva, a meglévő érték változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="ec602-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="ec602-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec602-124">-Name</span></span>
<span data-ttu-id="ec602-125">A foglalás neve</span><span class="sxs-lookup"><span data-stu-id="ec602-125">Name of Reservation</span></span>

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

### <span data-ttu-id="ec602-126">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="ec602-126">-Reservation</span></span>
<span data-ttu-id="ec602-127">Pipe Object paraméter `Reservation`</span><span class="sxs-lookup"><span data-stu-id="ec602-127">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec602-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="ec602-128">-ReservationId</span></span>
<span data-ttu-id="ec602-129">A frissítés azonosítója `Reservation`</span><span class="sxs-lookup"><span data-stu-id="ec602-129">Id of the `Reservation` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec602-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="ec602-130">-ReservationOrderId</span></span>
<span data-ttu-id="ec602-131">A frissítés azonosítója `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="ec602-131">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec602-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec602-132">-Confirm</span></span>
<span data-ttu-id="ec602-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec602-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec602-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec602-134">-WhatIf</span></span>
<span data-ttu-id="ec602-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec602-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec602-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec602-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec602-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec602-137">CommonParameters</span></span>
<span data-ttu-id="ec602-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec602-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec602-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec602-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec602-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec602-140">INPUTS</span></span>

### <span data-ttu-id="ec602-141">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="ec602-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="ec602-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec602-142">OUTPUTS</span></span>

### <span data-ttu-id="ec602-143">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="ec602-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="ec602-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec602-144">NOTES</span></span>

## <span data-ttu-id="ec602-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec602-145">RELATED LINKS</span></span>
