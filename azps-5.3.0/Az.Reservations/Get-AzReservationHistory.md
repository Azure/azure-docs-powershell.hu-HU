---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378011"
---
# <span data-ttu-id="03355-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="03355-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="03355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03355-102">SYNOPSIS</span></span>
<span data-ttu-id="03355-103">`Reservation`Korrektúraelőzmények megtekintése.</span><span class="sxs-lookup"><span data-stu-id="03355-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="03355-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03355-104">SYNTAX</span></span>

### <span data-ttu-id="03355-105">CommandLine (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03355-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03355-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="03355-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03355-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03355-107">DESCRIPTION</span></span>
<span data-ttu-id="03355-108">A . `Reservation`</span><span class="sxs-lookup"><span data-stu-id="03355-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="03355-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03355-109">EXAMPLES</span></span>

### <span data-ttu-id="03355-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="03355-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="03355-111">Az adott foglalás korrektúraelőzményének megtekintése</span><span class="sxs-lookup"><span data-stu-id="03355-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="03355-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03355-112">PARAMETERS</span></span>

### <span data-ttu-id="03355-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03355-113">-DefaultProfile</span></span>
<span data-ttu-id="03355-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03355-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03355-115">-Foglalás</span><span class="sxs-lookup"><span data-stu-id="03355-115">-Reservation</span></span>
<span data-ttu-id="03355-116">Pipe object parameter for `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="03355-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="03355-117">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="03355-117">-ReservationId</span></span>
<span data-ttu-id="03355-118">Annak a foglalásazonosítónak a foglalása, amelynek `Reservation` az előzményeit meg kell mutatni</span><span class="sxs-lookup"><span data-stu-id="03355-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="03355-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="03355-119">-ReservationOrderId</span></span>
<span data-ttu-id="03355-120">ReservationOrderId for the `ReservationOrder` contains the `Reservation`</span><span class="sxs-lookup"><span data-stu-id="03355-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="03355-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03355-121">CommonParameters</span></span>
<span data-ttu-id="03355-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03355-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03355-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03355-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03355-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03355-124">INPUTS</span></span>

### <span data-ttu-id="03355-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="03355-125">System.Guid</span></span>

### <span data-ttu-id="03355-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="03355-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="03355-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03355-127">OUTPUTS</span></span>

### <span data-ttu-id="03355-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="03355-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="03355-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03355-129">NOTES</span></span>

## <span data-ttu-id="03355-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03355-130">RELATED LINKS</span></span>
