---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468601"
---
# <span data-ttu-id="77869-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="77869-101">Update-AzReservation</span></span>

## <span data-ttu-id="77869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77869-102">SYNOPSIS</span></span>
<span data-ttu-id="77869-103">Frissítse az `Reservation` a.</span><span class="sxs-lookup"><span data-stu-id="77869-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="77869-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77869-104">SYNTAX</span></span>

### <span data-ttu-id="77869-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77869-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77869-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="77869-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77869-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77869-107">DESCRIPTION</span></span>
<span data-ttu-id="77869-108">Frissíti az alkalmazott `Reservation` hatókört.</span><span class="sxs-lookup"><span data-stu-id="77869-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="77869-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77869-109">EXAMPLES</span></span>

### <span data-ttu-id="77869-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="77869-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="77869-111">A megadott AppliedScopeType értéket `Reservation` "Egyszeres" és InstanceFlexibility "Be" típusra frissíti.</span><span class="sxs-lookup"><span data-stu-id="77869-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="77869-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="77869-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="77869-113">A megadott AppliedScopeType értéket `Reservation` "Megosztott" és InstanceFlexibility "Kikapcsolva" értékre frissíti.</span><span class="sxs-lookup"><span data-stu-id="77869-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="77869-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77869-114">PARAMETERS</span></span>

### <span data-ttu-id="77869-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="77869-115">-AppliedScope</span></span>
<span data-ttu-id="77869-116">SubscriptionId for this `Reservation` to be applied</span><span class="sxs-lookup"><span data-stu-id="77869-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="77869-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="77869-117">-AppliedScopeType</span></span>
<span data-ttu-id="77869-118">Az alkalmazott hatókör típusa</span><span class="sxs-lookup"><span data-stu-id="77869-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="77869-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77869-119">-DefaultProfile</span></span>
<span data-ttu-id="77869-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77869-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77869-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="77869-121">-InstanceFlexibility</span></span>
<span data-ttu-id="77869-122">Ha van ilyen, akkor frissíti a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="77869-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="77869-123">Ha nincs megadva, a meglévő érték változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="77869-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="77869-124">-Name</span><span class="sxs-lookup"><span data-stu-id="77869-124">-Name</span></span>
<span data-ttu-id="77869-125">Foglalás neve</span><span class="sxs-lookup"><span data-stu-id="77869-125">Name of Reservation</span></span>

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

### <span data-ttu-id="77869-126">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="77869-126">-Reservation</span></span>
<span data-ttu-id="77869-127">Pipe object parameter for `Reservation`</span><span class="sxs-lookup"><span data-stu-id="77869-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="77869-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="77869-128">-ReservationId</span></span>
<span data-ttu-id="77869-129">A `Reservation` frissítenie kell azonosítója</span><span class="sxs-lookup"><span data-stu-id="77869-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="77869-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="77869-130">-ReservationOrderId</span></span>
<span data-ttu-id="77869-131">A `ReservationOrder` frissítenie kell azonosítója</span><span class="sxs-lookup"><span data-stu-id="77869-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="77869-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77869-132">-Confirm</span></span>
<span data-ttu-id="77869-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="77869-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77869-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77869-134">-WhatIf</span></span>
<span data-ttu-id="77869-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="77869-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77869-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77869-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77869-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77869-137">CommonParameters</span></span>
<span data-ttu-id="77869-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77869-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77869-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77869-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77869-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77869-140">INPUTS</span></span>

### <span data-ttu-id="77869-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="77869-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="77869-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77869-142">OUTPUTS</span></span>

### <span data-ttu-id="77869-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="77869-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="77869-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77869-144">NOTES</span></span>

## <span data-ttu-id="77869-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77869-145">RELATED LINKS</span></span>
