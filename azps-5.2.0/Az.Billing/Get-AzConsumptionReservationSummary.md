---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a76254f1aeb369e6f93ed8edccfd6f74ff79ceb0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335753"
---
# <span data-ttu-id="0b0fa-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="0b0fa-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="0b0fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="0b0fa-103">Foglalási összegzést kap a napi vagy havi adatokról.</span><span class="sxs-lookup"><span data-stu-id="0b0fa-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="0b0fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b0fa-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b0fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b0fa-105">DESCRIPTION</span></span>
<span data-ttu-id="0b0fa-106">A **Get-AzConstionReservationSummary** parancsmag foglalási összegzést kap a napi vagy havi héjra.</span><span class="sxs-lookup"><span data-stu-id="0b0fa-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="0b0fa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b0fa-107">EXAMPLES</span></span>

### <span data-ttu-id="0b0fa-108">1. példa: Foglalási összegzések lekérte a havi foglalási rendelés azonosítójával</span><span class="sxs-lookup"><span data-stu-id="0b0fa-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
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

### <span data-ttu-id="0b0fa-109">2. példa: Foglalási összegzések a foglalási rendelés azonosítójával és a havi foglalásazonosítóval</span><span class="sxs-lookup"><span data-stu-id="0b0fa-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
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

### <span data-ttu-id="0b0fa-110">3. példa: Foglalási összegzések lekérte a foglalási rendelés azonosítóját a megadott napi dátumtartományhoz</span><span class="sxs-lookup"><span data-stu-id="0b0fa-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
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

### <span data-ttu-id="0b0fa-111">4. példa: Foglalási összegzések a foglalási rendelés azonosítójával és a foglalásazonosítóval a naponta megadott dátumtartományhoz</span><span class="sxs-lookup"><span data-stu-id="0b0fa-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
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

## <span data-ttu-id="0b0fa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b0fa-112">PARAMETERS</span></span>

### <span data-ttu-id="0b0fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b0fa-113">-DefaultProfile</span></span>
<span data-ttu-id="0b0fa-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b0fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b0fa-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0b0fa-115">-EndDate</span></span>
<span data-ttu-id="0b0fa-116">A foglalás összesítésének záró adatai (YYYY-HH-DD az UTC-ben) csak a napi adatokhoz szükségesek.</span><span class="sxs-lookup"><span data-stu-id="0b0fa-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="0b0fa-117">-Grain</span><span class="sxs-lookup"><span data-stu-id="0b0fa-117">-Grain</span></span>
<span data-ttu-id="0b0fa-118">A foglalás összefoglalásának időkorrekta lehet napi vagy havi.</span><span class="sxs-lookup"><span data-stu-id="0b0fa-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

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

### <span data-ttu-id="0b0fa-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="0b0fa-119">-ReservationId</span></span>
<span data-ttu-id="0b0fa-120">A foglalási rendelésen belüli foglalás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0b0fa-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="0b0fa-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="0b0fa-121">-ReservationOrderId</span></span>
<span data-ttu-id="0b0fa-122">A foglalási vásárlás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0b0fa-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="0b0fa-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="0b0fa-123">-StartDate</span></span>
<span data-ttu-id="0b0fa-124">A foglalás összefoglalásának kezdési adatai (YYYY-HH-DD az UTC-ben) csak a napi adatokhoz szükségesek.</span><span class="sxs-lookup"><span data-stu-id="0b0fa-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="0b0fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b0fa-125">CommonParameters</span></span>
<span data-ttu-id="0b0fa-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b0fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b0fa-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b0fa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b0fa-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b0fa-128">INPUTS</span></span>

### <span data-ttu-id="0b0fa-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="0b0fa-129">None</span></span>

## <span data-ttu-id="0b0fa-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b0fa-130">OUTPUTS</span></span>

### <span data-ttu-id="0b0fa-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="0b0fa-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="0b0fa-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b0fa-132">NOTES</span></span>

## <span data-ttu-id="0b0fa-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b0fa-133">RELATED LINKS</span></span>
