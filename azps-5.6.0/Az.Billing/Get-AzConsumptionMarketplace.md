---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionmarketplace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionMarketplace.md
ms.openlocfilehash: abf94b678d7c9e4726cf919d4673ea0750a438f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934330"
---
# <span data-ttu-id="59e25-101">Get-AzConsumptionMarketplace</span><span class="sxs-lookup"><span data-stu-id="59e25-101">Get-AzConsumptionMarketplace</span></span>

## <span data-ttu-id="59e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59e25-102">SYNOPSIS</span></span>
<span data-ttu-id="59e25-103">Az előfizetés piacterei.</span><span class="sxs-lookup"><span data-stu-id="59e25-103">Get marketplaces of the subscription.</span></span>

## <span data-ttu-id="59e25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59e25-104">SYNTAX</span></span>

```
Get-AzConsumptionMarketplace [-BillingPeriodName <String>] [-EndDate <DateTime>] [-InstanceId <String>]
 [-InstanceName <String>] [-ResourceGroup <String>] [-StartDate <DateTime>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59e25-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59e25-105">DESCRIPTION</span></span>
<span data-ttu-id="59e25-106">A **Get-AzConstionMarketplace parancsmag** piactereket kap az előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="59e25-106">The **Get-AzConsumptionMarketplace** cmdlet gets marketplaces of the subscription.</span></span>

## <span data-ttu-id="59e25-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59e25-107">EXAMPLES</span></span>

### <span data-ttu-id="59e25-108">1. példa: Piactér-használat</span><span class="sxs-lookup"><span data-stu-id="59e25-108">Example 1: Get marketplaces usage</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -Top 10
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

### <span data-ttu-id="59e25-109">2. példa: Piactér-használat a dátumtartománysal</span><span class="sxs-lookup"><span data-stu-id="59e25-109">Example 2: Get marketplace usage with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -StartDate 2018-01-03 -EndDate 2018-01-20 -Top 10
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

### <span data-ttu-id="59e25-110">3. példa: A BillingPeriodName piactéri használatának lekérte</span><span class="sxs-lookup"><span data-stu-id="59e25-110">Example 3: Get marketplace usage of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -BillingPeriodName 201801-1 -Top 10
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

### <span data-ttu-id="59e25-111">4. példa: Piactér-használat a InstanceName szűrővel</span><span class="sxs-lookup"><span data-stu-id="59e25-111">Example 4: Get marketplace usage with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionMarketplace -InstanceName TestVM -Top 10
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

## <span data-ttu-id="59e25-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59e25-112">PARAMETERS</span></span>

### <span data-ttu-id="59e25-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="59e25-113">-BillingPeriodName</span></span>
<span data-ttu-id="59e25-114">Annak a számlázási időszaknak a neve, amely a piactérhez társítva van.</span><span class="sxs-lookup"><span data-stu-id="59e25-114">Name of a specific billing period to get the marketplace that associate with.</span></span>

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

### <span data-ttu-id="59e25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e25-115">-DefaultProfile</span></span>
<span data-ttu-id="59e25-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59e25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59e25-117">-EndDate</span><span class="sxs-lookup"><span data-stu-id="59e25-117">-EndDate</span></span>
<span data-ttu-id="59e25-118">A szűrendő piacterek záró dátuma (UTC-ben).</span><span class="sxs-lookup"><span data-stu-id="59e25-118">The end date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="59e25-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="59e25-119">-InstanceId</span></span>
<span data-ttu-id="59e25-120">A szűrni megfelelő piacterek példányazonosítója.</span><span class="sxs-lookup"><span data-stu-id="59e25-120">The instance id of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="59e25-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="59e25-121">-InstanceName</span></span>
<span data-ttu-id="59e25-122">A szűrni megfelelő piacterek példányneve.</span><span class="sxs-lookup"><span data-stu-id="59e25-122">The instance name of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="59e25-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="59e25-123">-ResourceGroup</span></span>
<span data-ttu-id="59e25-124">A szűrni szükséges piacterek erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="59e25-124">The resource group of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="59e25-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="59e25-125">-StartDate</span></span>
<span data-ttu-id="59e25-126">A szűrendő piacterek kezdő dátuma (UTC-ben).</span><span class="sxs-lookup"><span data-stu-id="59e25-126">The start date (in UTC) of the marketplaces to filter.</span></span>

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

### <span data-ttu-id="59e25-127">-Top</span><span class="sxs-lookup"><span data-stu-id="59e25-127">-Top</span></span>
<span data-ttu-id="59e25-128">Határozza meg, hogy legfeljebb hány rekordot kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="59e25-128">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="59e25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e25-129">CommonParameters</span></span>
<span data-ttu-id="59e25-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59e25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e25-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59e25-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e25-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59e25-132">INPUTS</span></span>

### <span data-ttu-id="59e25-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="59e25-133">None</span></span>

## <span data-ttu-id="59e25-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59e25-134">OUTPUTS</span></span>

### <span data-ttu-id="59e25-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span><span class="sxs-lookup"><span data-stu-id="59e25-135">Microsoft.Azure.Commands.Consumption.Models.PSMarketplace</span></span>

## <span data-ttu-id="59e25-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59e25-136">NOTES</span></span>

## <span data-ttu-id="59e25-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59e25-137">RELATED LINKS</span></span>
