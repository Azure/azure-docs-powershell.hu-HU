---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 76abdc2f7a7099529af87f69af8e37319685aea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495269"
---
# <span data-ttu-id="d8656-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="d8656-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="d8656-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8656-102">SYNOPSIS</span></span>
<span data-ttu-id="d8656-103">Update a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d8656-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8656-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8656-104">SYNTAX</span></span>

### <span data-ttu-id="d8656-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8656-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -AppliedScopeType <String>
 [-AppliedScope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8656-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d8656-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8656-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8656-107">DESCRIPTION</span></span>
<span data-ttu-id="d8656-108">Frissíti az alkalmazott hatóköröket `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d8656-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="d8656-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d8656-109">EXAMPLES</span></span>

### <span data-ttu-id="d8656-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d8656-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="d8656-111">A megadott foglalás AppliedScopeType frissítése egyetlen értékre</span><span class="sxs-lookup"><span data-stu-id="d8656-111">Updates the AppliedScopeType of the specified reservation to Single</span></span>

### <span data-ttu-id="d8656-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d8656-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared"
```

<span data-ttu-id="d8656-113">A megadott foglalás AppliedScopeType frissítése Megosztottra</span><span class="sxs-lookup"><span data-stu-id="d8656-113">Updates the AppliedScopeType of the specified reservation to Shared</span></span>

## <span data-ttu-id="d8656-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8656-114">PARAMETERS</span></span>

### <span data-ttu-id="d8656-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="d8656-115">-AppliedScope</span></span>
<span data-ttu-id="d8656-116">A SubscriptionId `Reservation` alkalmazása</span><span class="sxs-lookup"><span data-stu-id="d8656-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8656-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="d8656-117">-AppliedScopeType</span></span>
<span data-ttu-id="d8656-118">A frissítendő típus típusa `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d8656-118">Type of the `Reservation` to be updated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Single, Shared

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8656-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8656-119">-DefaultProfile</span></span>
<span data-ttu-id="d8656-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8656-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8656-121">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="d8656-121">-Reservation</span></span>
<span data-ttu-id="d8656-122">Pipe Object paraméter `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d8656-122">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8656-123">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d8656-123">-ReservationId</span></span>
<span data-ttu-id="d8656-124">A frissítés azonosítója `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d8656-124">Id of the `Reservation` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8656-125">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d8656-125">-ReservationOrderId</span></span>
<span data-ttu-id="d8656-126">A frissítés azonosítója `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d8656-126">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8656-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d8656-127">-Confirm</span></span>
<span data-ttu-id="d8656-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d8656-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8656-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8656-129">-WhatIf</span></span>
<span data-ttu-id="d8656-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d8656-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8656-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8656-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8656-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8656-132">CommonParameters</span></span>
<span data-ttu-id="d8656-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8656-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8656-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8656-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8656-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8656-135">INPUTS</span></span>

### <span data-ttu-id="d8656-136">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d8656-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d8656-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8656-137">OUTPUTS</span></span>

### <span data-ttu-id="d8656-138">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d8656-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d8656-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8656-139">NOTES</span></span>

## <span data-ttu-id="d8656-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8656-140">RELATED LINKS</span></span>

