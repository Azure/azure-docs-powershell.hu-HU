---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionMarketplace.md
ms.openlocfilehash: 7ac3a179139a9e196b81d3ae323e665f793f4702
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494097"
---
# <span data-ttu-id="c9146-101">Get-AzureRmConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="c9146-101">Get-AzureRmConsumptionMarketplace</span></span>

## <span data-ttu-id="c9146-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9146-102">SYNOPSIS</span></span>
<span data-ttu-id="c9146-103">Az előfizetés piacának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c9146-103">Get marketplaces of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9146-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9146-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9146-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9146-105">DESCRIPTION</span></span>
<span data-ttu-id="c9146-106">A **Get-AzureRmConsumptionMarketplace** parancsmag az előfizetés piacait kapja.</span><span class="sxs-lookup"><span data-stu-id="c9146-106">The **Get-AzureRmConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="c9146-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9146-107">EXAMPLES</span></span>

### <span data-ttu-id="c9146-108">Példa 1: a piactérek használatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c9146-108">Example 1: Get marketplaces usage</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionMarketplace -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

### <span data-ttu-id="c9146-109">2. példa: a piactér kihasználtságának beszerzése dátumtartomány használatával</span><span class="sxs-lookup"><span data-stu-id="c9146-109">Example 2: Get marketplace usage with date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionMarketplace -StartDate 2018-01-03 -EndDate 2018-01-20 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201803-1/providers/Microsoft.Consumption/marketplaces/0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  0ec2bd1e-1cd6-0c75-3661-eaf3f635df33
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-01-04T00:00:00Z
UsageStart:  2018-01-03T00:00:00Z
```

### <span data-ttu-id="c9146-110">3. példa: a piactér BillingPeriodName beszerzése</span><span class="sxs-lookup"><span data-stu-id="c9146-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionMarketplace -BillingPeriodName 201801-1 -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201801-1/providers/Microsoft.Consumption/marketplaces/ea82233a-9f76-7eaa-4478-42bd61cf6287
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  ea82233a-9f76-7eaa-4478-42bd61cf6287
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2017-10-29T00:00:00Z
UsageStart:  2017-10-28T00:00:00Z
```

### <span data-ttu-id="c9146-111">4. példa: a piactér használatát a példánynév szűrővel érheti el</span><span class="sxs-lookup"><span data-stu-id="c9146-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionMarketplace -InstanceName TestVM -Top 10
BillingPeriodId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1
ConsumedQuantity:  24
Currency:  USD
Id:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/providers/Microsoft.Billing/billingPeriods/201807-1/providers/Microsoft.Consumption/marketplaces/018b7291-57a5-e194-65ea-28c3f1db76aa
InstanceId:  subscriptions/6b74c45b-9597-4939-a202-36b2ee8fbb3d/resourceGroups/TESTRG1/providers/Microsoft.Compute/virtualMachines/TestVM
InstanceName:  TestVM
IsEstimated:  false
Name:  018b7291-57a5-e194-65ea-28c3f1db76aa
OfferName:  2b380487-dc18-4e5d-981f-1ee2cc59e776
PretaxCost:  0
ResourceRate:  0
SubscriptionGuid:  6b74c45b-9597-4939-a202-36b2ee8fbb3d
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  2018-04-29T00:00:00Z
UsageStart:  2018-04-28T00:00:00Z
```

## <span data-ttu-id="c9146-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9146-112">PARAMETERS</span></span>

### <span data-ttu-id="c9146-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="c9146-113">-BillingPeriodName</span></span>
<span data-ttu-id="c9146-114">Egy adott számlázási időszak neve, amely a hozzárendelni kívánt piactért kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c9146-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="c9146-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9146-115">-DefaultProfile</span></span>
<span data-ttu-id="c9146-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9146-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9146-117">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c9146-117">-EndDate</span></span>
<span data-ttu-id="c9146-118">A szűrni kívánt piacok záró dátuma (UTC-ben).</span><span class="sxs-lookup"><span data-stu-id="c9146-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="c9146-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c9146-119">-InstanceId</span></span>
<span data-ttu-id="c9146-120">A szűrni kívánt piacok példányának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c9146-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="c9146-121">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="c9146-121">-InstanceName</span></span>
<span data-ttu-id="c9146-122">A szűrni kívánt piacok példányának neve.</span><span class="sxs-lookup"><span data-stu-id="c9146-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="c9146-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c9146-123">-ResourceGroup</span></span>
<span data-ttu-id="c9146-124">A szűrni kívánt piacok erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="c9146-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="c9146-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c9146-125">-StartDate</span></span>
<span data-ttu-id="c9146-126">A szűrni kívánt piacok kezdési dátuma (UTC-ben)</span><span class="sxs-lookup"><span data-stu-id="c9146-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="c9146-127">-Top</span><span class="sxs-lookup"><span data-stu-id="c9146-127">-Top</span></span>
<span data-ttu-id="c9146-128">Adja meg, hogy legfeljebb hány rekordot szeretne megadni.</span><span class="sxs-lookup"><span data-stu-id="c9146-128">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="c9146-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9146-129">CommonParameters</span></span>
<span data-ttu-id="c9146-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9146-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9146-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9146-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9146-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9146-132">INPUTS</span></span>

### <span data-ttu-id="c9146-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="c9146-133">None</span></span>

## <span data-ttu-id="c9146-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9146-134">OUTPUTS</span></span>

### <span data-ttu-id="c9146-135">Microsoft. Azure. commands. fogyasztás. models. PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="c9146-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="c9146-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9146-136">NOTES</span></span>

## <span data-ttu-id="c9146-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9146-137">RELATED LINKS</span></span>
