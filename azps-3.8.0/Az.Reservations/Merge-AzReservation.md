---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011311"
---
# <span data-ttu-id="cab45-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="cab45-101">Merge-AzReservation</span></span>

## <span data-ttu-id="cab45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cab45-102">SYNOPSIS</span></span>
<span data-ttu-id="cab45-103">Két s egyesítése `Reservation`</span><span class="sxs-lookup"><span data-stu-id="cab45-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="cab45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cab45-104">SYNTAX</span></span>

### <span data-ttu-id="cab45-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cab45-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cab45-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="cab45-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cab45-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cab45-107">DESCRIPTION</span></span>
<span data-ttu-id="cab45-108">A megadott EK egyesítése új értékre `Reservation` `Reservation`</span><span class="sxs-lookup"><span data-stu-id="cab45-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="cab45-109">Az egyesített két s-féle `Reservation` tulajdonságnak azonos tulajdonságokkal kell rendelkeznie.</span><span class="sxs-lookup"><span data-stu-id="cab45-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="cab45-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cab45-110">EXAMPLES</span></span>

### <span data-ttu-id="cab45-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cab45-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="cab45-112">A két megadott s-szám egyesítése `Reservation``Reservation`</span><span class="sxs-lookup"><span data-stu-id="cab45-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="cab45-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cab45-113">PARAMETERS</span></span>

### <span data-ttu-id="cab45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab45-114">-DefaultProfile</span></span>
<span data-ttu-id="cab45-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cab45-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab45-116">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="cab45-116">-Reservation</span></span>
<span data-ttu-id="cab45-117">Két ReservationIds pontosvesszővel elválasztott karakterlánca egyesítéshez</span><span class="sxs-lookup"><span data-stu-id="cab45-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab45-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="cab45-118">-ReservationId</span></span>
<span data-ttu-id="cab45-119">A `ReservationOrder` két `Reservation` s betűt tartalmazó ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="cab45-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab45-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="cab45-120">-ReservationOrderId</span></span>
<span data-ttu-id="cab45-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="cab45-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="cab45-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cab45-122">-Confirm</span></span>
<span data-ttu-id="cab45-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cab45-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cab45-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cab45-124">-WhatIf</span></span>
<span data-ttu-id="cab45-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cab45-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cab45-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cab45-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cab45-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab45-127">CommonParameters</span></span>
<span data-ttu-id="cab45-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cab45-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab45-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cab45-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab45-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cab45-130">INPUTS</span></span>

### <span data-ttu-id="cab45-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="cab45-131">None</span></span>

## <span data-ttu-id="cab45-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cab45-132">OUTPUTS</span></span>

### <span data-ttu-id="cab45-133">Microsoft. Azure. commands. Reservations. models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="cab45-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="cab45-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cab45-134">NOTES</span></span>

## <span data-ttu-id="cab45-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cab45-135">RELATED LINKS</span></span>
