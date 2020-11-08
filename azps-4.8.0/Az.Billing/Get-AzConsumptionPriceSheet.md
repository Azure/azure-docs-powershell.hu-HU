---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
ms.openlocfilehash: 999466a754fdeeb98a3d8aaefd91f0b65a2810f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182586"
---
# <span data-ttu-id="3ee1a-101">Get-AzConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="3ee1a-101">Get-AzConsumptionPriceSheet</span></span>

## <span data-ttu-id="3ee1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ee1a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee1a-103">Az előfizetés árlista-lapjainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ee1a-103">Get price sheets of the subscription.</span></span>

## <span data-ttu-id="3ee1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ee1a-104">SYNTAX</span></span>

```
Get-AzConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ee1a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ee1a-105">DESCRIPTION</span></span>
<span data-ttu-id="3ee1a-106">A **Get-AzConsumptionPriceSheet** parancsmag az előfizetés árlista-lapjait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-106">The **Get-AzConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="3ee1a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3ee1a-107">EXAMPLES</span></span>

### <span data-ttu-id="3ee1a-108">Példa 1: árlista beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ee1a-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="3ee1a-109">2. példa: árlista beszerzése a MeterDetails kibontásával</span><span class="sxs-lookup"><span data-stu-id="3ee1a-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -ExpandMeterDetail
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterDetails:  MeterCategory:  Virtual Machines
                             MeterLocation:  US North Central
                             MeterName:  Compute Hours
                             MeterSubCategory:  Standard_D11_v2 VM_Promo (Windows)
                             Unit:  Hours
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="3ee1a-110">3. példa: az BillingPeriodName lekérése</span><span class="sxs-lookup"><span data-stu-id="3ee1a-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -BillingPeriodName 201712
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  46367D67-1E4C-4ED4-8267-4477083F581C
              PartNumber:  AAA-53590
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.37
```

### <span data-ttu-id="3ee1a-111">4. példa: az árlista első 5 rekordjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ee1a-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -Top 5
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

## <span data-ttu-id="3ee1a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ee1a-112">PARAMETERS</span></span>

### <span data-ttu-id="3ee1a-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="3ee1a-113">-BillingPeriodName</span></span>
<span data-ttu-id="3ee1a-114">Egy adott számlázási időszak neve, amely a hozzárendelni kívánt árlista beszerzésére használható.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="3ee1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee1a-115">-DefaultProfile</span></span>
<span data-ttu-id="3ee1a-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ee1a-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="3ee1a-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="3ee1a-118">Az MeterDetails alapján bontsa ki az árlistát.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-118">Expand the price sheets based on MeterDetails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee1a-119">-Top</span><span class="sxs-lookup"><span data-stu-id="3ee1a-119">-Top</span></span>
<span data-ttu-id="3ee1a-120">Adja meg, hogy legfeljebb hány rekordot szeretne megadni.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee1a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee1a-121">CommonParameters</span></span>
<span data-ttu-id="3ee1a-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ee1a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee1a-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee1a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee1a-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ee1a-124">INPUTS</span></span>

### <span data-ttu-id="3ee1a-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="3ee1a-125">None</span></span>

## <span data-ttu-id="3ee1a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ee1a-126">OUTPUTS</span></span>

### <span data-ttu-id="3ee1a-127">Microsoft. Azure. commands. fogyasztás. models. PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="3ee1a-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="3ee1a-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ee1a-128">NOTES</span></span>

## <span data-ttu-id="3ee1a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ee1a-129">RELATED LINKS</span></span>
