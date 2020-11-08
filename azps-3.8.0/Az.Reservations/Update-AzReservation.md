---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002855"
---
# <span data-ttu-id="8bbc0-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="8bbc0-101">Update-AzReservation</span></span>

## <span data-ttu-id="8bbc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8bbc0-102">SYNOPSIS</span></span>
<span data-ttu-id="8bbc0-103">Update a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="8bbc0-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="8bbc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8bbc0-104">SYNTAX</span></span>

### <span data-ttu-id="8bbc0-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8bbc0-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bbc0-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="8bbc0-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bbc0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8bbc0-107">DESCRIPTION</span></span>
<span data-ttu-id="8bbc0-108">Frissíti az alkalmazott hatóköröket `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="8bbc0-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="8bbc0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8bbc0-109">EXAMPLES</span></span>

### <span data-ttu-id="8bbc0-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8bbc0-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="8bbc0-111">Frissíti a megadott AppliedScopeType az `Reservation` egy-és InstanceFlexibility be értékre.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="8bbc0-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="8bbc0-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="8bbc0-113">A megadott AppliedScopeType frissíti a `Reservation` megosztott és a InstanceFlexibility.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="8bbc0-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8bbc0-114">PARAMETERS</span></span>

### <span data-ttu-id="8bbc0-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="8bbc0-115">-AppliedScope</span></span>
<span data-ttu-id="8bbc0-116">A SubscriptionId `Reservation` alkalmazása</span><span class="sxs-lookup"><span data-stu-id="8bbc0-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="8bbc0-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="8bbc0-117">-AppliedScopeType</span></span>
<span data-ttu-id="8bbc0-118">Az alkalmazott hatókör típusa</span><span class="sxs-lookup"><span data-stu-id="8bbc0-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="8bbc0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bbc0-119">-DefaultProfile</span></span>
<span data-ttu-id="8bbc0-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bbc0-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="8bbc0-121">-InstanceFlexibility</span></span>
<span data-ttu-id="8bbc0-122">Ha van, frissíti a InstanceFlexibility értékét `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="8bbc0-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="8bbc0-123">Ha nincs megadva, a meglévő érték változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="8bbc0-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8bbc0-124">-Name</span></span>
<span data-ttu-id="8bbc0-125">A foglalás neve</span><span class="sxs-lookup"><span data-stu-id="8bbc0-125">Name of Reservation</span></span>

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

### <span data-ttu-id="8bbc0-126">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="8bbc0-126">-Reservation</span></span>
<span data-ttu-id="8bbc0-127">Pipe Object paraméter `Reservation`</span><span class="sxs-lookup"><span data-stu-id="8bbc0-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="8bbc0-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="8bbc0-128">-ReservationId</span></span>
<span data-ttu-id="8bbc0-129">A frissítés azonosítója `Reservation`</span><span class="sxs-lookup"><span data-stu-id="8bbc0-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="8bbc0-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="8bbc0-130">-ReservationOrderId</span></span>
<span data-ttu-id="8bbc0-131">A frissítés azonosítója `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="8bbc0-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="8bbc0-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8bbc0-132">-Confirm</span></span>
<span data-ttu-id="8bbc0-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bbc0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bbc0-134">-WhatIf</span></span>
<span data-ttu-id="8bbc0-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8bbc0-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bbc0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bbc0-137">CommonParameters</span></span>
<span data-ttu-id="8bbc0-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8bbc0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bbc0-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8bbc0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bbc0-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bbc0-140">INPUTS</span></span>

### <span data-ttu-id="8bbc0-141">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="8bbc0-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="8bbc0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8bbc0-142">OUTPUTS</span></span>

### <span data-ttu-id="8bbc0-143">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="8bbc0-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="8bbc0-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8bbc0-144">NOTES</span></span>

## <span data-ttu-id="8bbc0-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8bbc0-145">RELATED LINKS</span></span>
