---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: f8347fca355080f11e69bae9793cc0367325ce98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680599"
---
# <span data-ttu-id="ce7a3-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="ce7a3-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="ce7a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce7a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7a3-103">Az előfizetés használati adatainak megtekintése.</span><span class="sxs-lookup"><span data-stu-id="ce7a3-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce7a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce7a3-104">SYNTAX</span></span>

### <span data-ttu-id="ce7a3-105">Előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce7a3-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce7a3-106">Számla</span><span class="sxs-lookup"><span data-stu-id="ce7a3-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce7a3-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="ce7a3-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce7a3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce7a3-108">DESCRIPTION</span></span>
<span data-ttu-id="ce7a3-109">A **Get-AzureRmConsumptionUsageDetail** parancsmag az előfizetés használati adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ce7a3-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="ce7a3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ce7a3-110">EXAMPLES</span></span>

### <span data-ttu-id="ce7a3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ce7a3-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="ce7a3-112">A megadott nevű számla használati adatainak megtekintése, valamint a MeterDetails tulajdonság felvétele az eredménybe.</span><span class="sxs-lookup"><span data-stu-id="ce7a3-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="ce7a3-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ce7a3-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="ce7a3-114">A számlázási időszak használati adatait adja meg a megadott névvel, és vegye fel a AdditionalProperties tulajdonságot az eredménybe.</span><span class="sxs-lookup"><span data-stu-id="ce7a3-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="ce7a3-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="ce7a3-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="ce7a3-116">Az 2017-01-17-től 2017-01-19-ig terjedő előfizetés használati adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ce7a3-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="ce7a3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce7a3-117">PARAMETERS</span></span>

### <span data-ttu-id="ce7a3-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="ce7a3-118">-BillingPeriodName</span></span>
<span data-ttu-id="ce7a3-119">Egy adott számlázási időszak neve a hozzárendelni kívánt használati adatok beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="ce7a3-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7a3-120">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ce7a3-120">-EndDate</span></span>
<span data-ttu-id="ce7a3-121">A használat befejezési dátuma (UTC-ben).</span><span class="sxs-lookup"><span data-stu-id="ce7a3-121">The end date (in UTC) of the usages.</span></span>

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

### <span data-ttu-id="ce7a3-122">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="ce7a3-122">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="ce7a3-123">További tulajdonságok felvétele a használatokban</span><span class="sxs-lookup"><span data-stu-id="ce7a3-123">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="ce7a3-124">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="ce7a3-124">-IncludeMeterDetails</span></span>
<span data-ttu-id="ce7a3-125">A használati adatok tartalmazzák a mérőműszer adatait.</span><span class="sxs-lookup"><span data-stu-id="ce7a3-125">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="ce7a3-126">-InvoiceName</span><span class="sxs-lookup"><span data-stu-id="ce7a3-126">-InvoiceName</span></span>
<span data-ttu-id="ce7a3-127">Egy adott számla neve a hozzárendelni kívánt használati adatok beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="ce7a3-127">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7a3-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ce7a3-128">-MaxCount</span></span>
<span data-ttu-id="ce7a3-129">Adja meg, hogy legfeljebb hány rekordot szeretne megadni.</span><span class="sxs-lookup"><span data-stu-id="ce7a3-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="ce7a3-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ce7a3-130">-StartDate</span></span>
<span data-ttu-id="ce7a3-131">A használat kezdési dátuma (UTC-ben)</span><span class="sxs-lookup"><span data-stu-id="ce7a3-131">The start date (in UTC) of the usages.</span></span>

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

### <span data-ttu-id="ce7a3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce7a3-132">-DefaultProfile</span></span>
<span data-ttu-id="ce7a3-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce7a3-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce7a3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7a3-134">CommonParameters</span></span>
<span data-ttu-id="ce7a3-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce7a3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7a3-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce7a3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7a3-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce7a3-137">INPUTS</span></span>

### <span data-ttu-id="ce7a3-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="ce7a3-138">None</span></span>

## <span data-ttu-id="ce7a3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce7a3-139">OUTPUTS</span></span>

### <span data-ttu-id="ce7a3-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. fogyasztás. models. PSUsageDetail, Microsoft. Azure. commands. fogyasztás, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ce7a3-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ce7a3-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce7a3-141">NOTES</span></span>

## <span data-ttu-id="ce7a3-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce7a3-142">RELATED LINKS</span></span>

