---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495274"
---
# <span data-ttu-id="08780-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="08780-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="08780-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08780-102">SYNOPSIS</span></span>
<span data-ttu-id="08780-103">Két s egyesítése `Reservation`</span><span class="sxs-lookup"><span data-stu-id="08780-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08780-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08780-104">SYNTAX</span></span>

### <span data-ttu-id="08780-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08780-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08780-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="08780-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08780-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="08780-107">DESCRIPTION</span></span>
<span data-ttu-id="08780-108">A megadott EK egyesítése új értékre `Reservation` `Reservation`</span><span class="sxs-lookup"><span data-stu-id="08780-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="08780-109">Az egyesített két s-féle `Reservation` tulajdonságnak azonos tulajdonságokkal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="08780-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="08780-110">Példák</span><span class="sxs-lookup"><span data-stu-id="08780-110">EXAMPLES</span></span>

### <span data-ttu-id="08780-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08780-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="08780-112">A két megadott s-szám egyesítése `Reservation``Reservation`</span><span class="sxs-lookup"><span data-stu-id="08780-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="08780-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08780-113">PARAMETERS</span></span>

### <span data-ttu-id="08780-114">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="08780-114">-Reservation</span></span>
<span data-ttu-id="08780-115">Két ReservationIds pontosvesszővel elválasztott karakterlánca egyesítéshez</span><span class="sxs-lookup"><span data-stu-id="08780-115">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08780-116">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="08780-116">-ReservationId</span></span>
<span data-ttu-id="08780-117">A `ReservationOrder` két `Reservation` s betűt tartalmazó ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="08780-117">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08780-118">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="08780-118">-ReservationOrderId</span></span>
<span data-ttu-id="08780-119">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="08780-119">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="08780-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08780-120">-Confirm</span></span>
<span data-ttu-id="08780-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08780-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08780-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08780-122">-WhatIf</span></span>
<span data-ttu-id="08780-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08780-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08780-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08780-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08780-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08780-125">CommonParameters</span></span>
<span data-ttu-id="08780-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08780-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08780-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08780-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08780-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08780-128">INPUTS</span></span>

### <span data-ttu-id="08780-129">Microsoft. Azure. commands. Reservations. models. PSReservation []</span><span class="sxs-lookup"><span data-stu-id="08780-129">Microsoft.Azure.Commands.Reservations.Models.PSReservation[]</span></span>

## <span data-ttu-id="08780-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08780-130">OUTPUTS</span></span>

### <span data-ttu-id="08780-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Reservations. models. PSReservation, Microsoft. Azure. commands. Reservations, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="08780-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="08780-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08780-132">NOTES</span></span>

## <span data-ttu-id="08780-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08780-133">RELATED LINKS</span></span>

