---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 2a49cb88fc25643cd26e7ed75d226b8abf6ee50f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012408"
---
# <span data-ttu-id="852ba-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="852ba-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="852ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="852ba-102">SYNOPSIS</span></span>
<span data-ttu-id="852ba-103">Foglalási adatok beszerzése a megadott Dátumtartomány alapján.</span><span class="sxs-lookup"><span data-stu-id="852ba-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="852ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="852ba-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="852ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="852ba-105">DESCRIPTION</span></span>
<span data-ttu-id="852ba-106">A **Get-AzConsumptionReservationDetail** parancsmag foglalási adatokat kap a megadott dátumtartomány számára.</span><span class="sxs-lookup"><span data-stu-id="852ba-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="852ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="852ba-107">EXAMPLES</span></span>

### <span data-ttu-id="852ba-108">Példa 1: foglalási adatok beszerzése foglalási megrendelési azonosítóval a megadott dátumtartomány szerint</span><span class="sxs-lookup"><span data-stu-id="852ba-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="852ba-109">2. példa: foglalási adatok beszerzése foglalási megrendelési azonosítóval és a megadott dátumtartomány foglalási azonosítójával</span><span class="sxs-lookup"><span data-stu-id="852ba-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="852ba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="852ba-110">PARAMETERS</span></span>

### <span data-ttu-id="852ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="852ba-111">-DefaultProfile</span></span>
<span data-ttu-id="852ba-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="852ba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="852ba-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="852ba-113">-EndDate</span></span>
<span data-ttu-id="852ba-114">A záró adatok (éééé-hh-nn) a foglalás részleteiben.</span><span class="sxs-lookup"><span data-stu-id="852ba-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="852ba-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="852ba-115">-ReservationId</span></span>
<span data-ttu-id="852ba-116">Egy foglalás azonosítója egy foglalási rendelésen belül.</span><span class="sxs-lookup"><span data-stu-id="852ba-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="852ba-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="852ba-117">-ReservationOrderId</span></span>
<span data-ttu-id="852ba-118">Egy foglalási vásárlás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="852ba-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="852ba-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="852ba-119">-StartDate</span></span>
<span data-ttu-id="852ba-120">Az adatok kezdése (éééé-hh-nn) a foglalás részleteiben.</span><span class="sxs-lookup"><span data-stu-id="852ba-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="852ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="852ba-121">CommonParameters</span></span>
<span data-ttu-id="852ba-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="852ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="852ba-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="852ba-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="852ba-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="852ba-124">INPUTS</span></span>

### <span data-ttu-id="852ba-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="852ba-125">None</span></span>

## <span data-ttu-id="852ba-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="852ba-126">OUTPUTS</span></span>

### <span data-ttu-id="852ba-127">Microsoft. Azure. commands. fogyasztás. models. PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="852ba-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="852ba-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="852ba-128">NOTES</span></span>

## <span data-ttu-id="852ba-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="852ba-129">RELATED LINKS</span></span>
