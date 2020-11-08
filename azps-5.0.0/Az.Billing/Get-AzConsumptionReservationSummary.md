---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a76254f1aeb369e6f93ed8edccfd6f74ff79ceb0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194812"
---
# <span data-ttu-id="484a0-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="484a0-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="484a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="484a0-102">SYNOPSIS</span></span>
<span data-ttu-id="484a0-103">Foglalási összesítések beszerzése napi vagy havi gabona esetén</span><span class="sxs-lookup"><span data-stu-id="484a0-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="484a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="484a0-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="484a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="484a0-105">DESCRIPTION</span></span>
<span data-ttu-id="484a0-106">A **Get-AzConsumptionReservationSummary** parancsmag napi vagy havi gabona foglalási összefoglalókat kap.</span><span class="sxs-lookup"><span data-stu-id="484a0-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="484a0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="484a0-107">EXAMPLES</span></span>

### <span data-ttu-id="484a0-108">Példa 1: foglalási összesítések beszerzése a havi gabona foglalási rendelési azonosítójával</span><span class="sxs-lookup"><span data-stu-id="484a0-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="484a0-109">2. példa: foglalási összesítések beszerzése a havi gabona foglalási rendelési azonosítójával és a foglalási azonosítóval</span><span class="sxs-lookup"><span data-stu-id="484a0-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="484a0-110">3. példa: foglalási összesítések beszerzése a napi gabona időtartományához tartozó foglalási rendelési azonosítóval</span><span class="sxs-lookup"><span data-stu-id="484a0-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="484a0-111">Példa 4: foglalási összesítések beszerzése foglalási megrendelési azonosítóval és a napi gabona foglalási azonosítójával</span><span class="sxs-lookup"><span data-stu-id="484a0-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="484a0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="484a0-112">PARAMETERS</span></span>

### <span data-ttu-id="484a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="484a0-113">-DefaultProfile</span></span>
<span data-ttu-id="484a0-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="484a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="484a0-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="484a0-115">-EndDate</span></span>
<span data-ttu-id="484a0-116">A záró (éééé-hh-nn) a foglalási összefoglalóban, csak a napi gabona esetében szükséges.</span><span class="sxs-lookup"><span data-stu-id="484a0-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="484a0-117">-Grain</span><span class="sxs-lookup"><span data-stu-id="484a0-117">-Grain</span></span>
<span data-ttu-id="484a0-118">A foglalás összefoglalójának időpontja naponta vagy havonta lehet.</span><span class="sxs-lookup"><span data-stu-id="484a0-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="484a0-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="484a0-119">-ReservationId</span></span>
<span data-ttu-id="484a0-120">Egy foglalás azonosítója egy foglalási rendelésen belül.</span><span class="sxs-lookup"><span data-stu-id="484a0-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="484a0-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="484a0-121">-ReservationOrderId</span></span>
<span data-ttu-id="484a0-122">Egy foglalási vásárlás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="484a0-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="484a0-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="484a0-123">-StartDate</span></span>
<span data-ttu-id="484a0-124">A foglalás összefoglalójának kezdési (éééé-hh-nn), csak a napi gabona esetén szükséges.</span><span class="sxs-lookup"><span data-stu-id="484a0-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="484a0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="484a0-125">CommonParameters</span></span>
<span data-ttu-id="484a0-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="484a0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="484a0-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="484a0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="484a0-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="484a0-128">INPUTS</span></span>

### <span data-ttu-id="484a0-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="484a0-129">None</span></span>

## <span data-ttu-id="484a0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="484a0-130">OUTPUTS</span></span>

### <span data-ttu-id="484a0-131">Microsoft. Azure. commands. fogyasztás. models. PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="484a0-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="484a0-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="484a0-132">NOTES</span></span>

## <span data-ttu-id="484a0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="484a0-133">RELATED LINKS</span></span>
