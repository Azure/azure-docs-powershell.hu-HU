---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370171"
---
# <span data-ttu-id="aacdf-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="aacdf-101">Get-AzReservation</span></span>

## <span data-ttu-id="aacdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aacdf-102">SYNOPSIS</span></span>
<span data-ttu-id="aacdf-103">Get `Reservation` s in a given reservation Order</span><span class="sxs-lookup"><span data-stu-id="aacdf-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="aacdf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aacdf-104">SYNTAX</span></span>

### <span data-ttu-id="aacdf-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aacdf-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aacdf-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="aacdf-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aacdf-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="aacdf-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aacdf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aacdf-108">DESCRIPTION</span></span>
<span data-ttu-id="aacdf-109">Egyetlen `Reservation` listán belüli `ReservationOrder` lista.</span><span class="sxs-lookup"><span data-stu-id="aacdf-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="aacdf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aacdf-110">EXAMPLES</span></span>

### <span data-ttu-id="aacdf-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="aacdf-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="aacdf-112">A `Reservation` megadott listán belüli "s" `ReservationOrder` lista.</span><span class="sxs-lookup"><span data-stu-id="aacdf-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="aacdf-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="aacdf-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="aacdf-114">Konkrét `Reservation` részleteket olvashat.</span><span class="sxs-lookup"><span data-stu-id="aacdf-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="aacdf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aacdf-115">PARAMETERS</span></span>

### <span data-ttu-id="aacdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aacdf-116">-DefaultProfile</span></span>
<span data-ttu-id="aacdf-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aacdf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aacdf-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="aacdf-118">-ReservationId</span></span>
<span data-ttu-id="aacdf-119">Annak az azonosítónak `Reservation` az azonosítója, amit meg kell nézni</span><span class="sxs-lookup"><span data-stu-id="aacdf-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aacdf-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="aacdf-120">-ReservationOrder</span></span>
<span data-ttu-id="aacdf-121">Pipe object parameter for `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="aacdf-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aacdf-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="aacdf-122">-ReservationOrderId</span></span>
<span data-ttu-id="aacdf-123">A . `ReservationOrder` `Reservation`</span><span class="sxs-lookup"><span data-stu-id="aacdf-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="aacdf-124">Kötelező.</span><span class="sxs-lookup"><span data-stu-id="aacdf-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aacdf-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="aacdf-125">-ReservationOrderPage</span></span>
<span data-ttu-id="aacdf-126">Pipe object parameter for `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="aacdf-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aacdf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aacdf-127">CommonParameters</span></span>
<span data-ttu-id="aacdf-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aacdf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aacdf-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aacdf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aacdf-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aacdf-130">INPUTS</span></span>

### <span data-ttu-id="aacdf-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="aacdf-131">System.Guid</span></span>

### <span data-ttu-id="aacdf-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="aacdf-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="aacdf-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="aacdf-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="aacdf-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aacdf-134">OUTPUTS</span></span>

### <span data-ttu-id="aacdf-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="aacdf-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="aacdf-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="aacdf-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="aacdf-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aacdf-137">NOTES</span></span>

## <span data-ttu-id="aacdf-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aacdf-138">RELATED LINKS</span></span>
