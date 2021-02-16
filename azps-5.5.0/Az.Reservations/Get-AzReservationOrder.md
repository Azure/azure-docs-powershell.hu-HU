---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169147"
---
# <span data-ttu-id="47dc1-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="47dc1-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="47dc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="47dc1-103">Bej.le `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="47dc1-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="47dc1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47dc1-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47dc1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47dc1-105">DESCRIPTION</span></span>
<span data-ttu-id="47dc1-106">A felhasználó által az aktuális bérlői fiókban elérhető `ReservationOrder` összes szolgáltatás listája.</span><span class="sxs-lookup"><span data-stu-id="47dc1-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="47dc1-107">Ha a ReservationOrderId paraméter be van állítva, szerezze be az adott ReservationOrder paramétert.</span><span class="sxs-lookup"><span data-stu-id="47dc1-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="47dc1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47dc1-108">EXAMPLES</span></span>

### <span data-ttu-id="47dc1-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="47dc1-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="47dc1-110">List all `ReservationOrder` that the user has access to in the current tenant</span><span class="sxs-lookup"><span data-stu-id="47dc1-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="47dc1-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="47dc1-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="47dc1-112">Get `ReservationOrder` with the specified ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="47dc1-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="47dc1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47dc1-113">PARAMETERS</span></span>

### <span data-ttu-id="47dc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47dc1-114">-DefaultProfile</span></span>
<span data-ttu-id="47dc1-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47dc1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47dc1-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="47dc1-116">-ReservationOrderId</span></span>
<span data-ttu-id="47dc1-117">A felhasználó által látni szeretne adott Foglalási Rendelés azonosítója</span><span class="sxs-lookup"><span data-stu-id="47dc1-117">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dc1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47dc1-118">CommonParameters</span></span>
<span data-ttu-id="47dc1-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47dc1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47dc1-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47dc1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47dc1-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47dc1-121">INPUTS</span></span>

### <span data-ttu-id="47dc1-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="47dc1-122">None</span></span>

## <span data-ttu-id="47dc1-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47dc1-123">OUTPUTS</span></span>

### <span data-ttu-id="47dc1-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="47dc1-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="47dc1-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="47dc1-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="47dc1-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47dc1-126">NOTES</span></span>

## <span data-ttu-id="47dc1-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47dc1-127">RELATED LINKS</span></span>
