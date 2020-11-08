---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180617"
---
# <span data-ttu-id="58c1d-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="58c1d-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="58c1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="58c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="58c1d-103">Költségvetés létrehozása előfizetésben vagy erőforrás-csoportban</span><span class="sxs-lookup"><span data-stu-id="58c1d-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="58c1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="58c1d-104">SYNTAX</span></span>

### <span data-ttu-id="58c1d-105">Előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="58c1d-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58c1d-106">Értesítés</span><span class="sxs-lookup"><span data-stu-id="58c1d-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c1d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="58c1d-107">DESCRIPTION</span></span>
<span data-ttu-id="58c1d-108">Az New-AzConsumptionBudget parancsmag előfizetésben vagy erőforráscsoporthoz hoz létre költségvetést.</span><span class="sxs-lookup"><span data-stu-id="58c1d-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="58c1d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="58c1d-109">EXAMPLES</span></span>

### <span data-ttu-id="58c1d-110">Példa 1: költség-költségvetés létrehozása költségvetés nevével az előfizetési szinten</span><span class="sxs-lookup"><span data-stu-id="58c1d-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="58c1d-111">2. példa: költség-költségvetés létrehozása egy költségvetés nevével az erőforrás csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="58c1d-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="58c1d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="58c1d-112">PARAMETERS</span></span>

### <span data-ttu-id="58c1d-113">-Összeg</span><span class="sxs-lookup"><span data-stu-id="58c1d-113">-Amount</span></span>
<span data-ttu-id="58c1d-114">Költségvetés összege.</span><span class="sxs-lookup"><span data-stu-id="58c1d-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-115">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="58c1d-115">-Category</span></span>
<span data-ttu-id="58c1d-116">A költségvetés kategóriája lehet költség vagy felhasználás.</span><span class="sxs-lookup"><span data-stu-id="58c1d-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="58c1d-117">-ContactEmail</span></span>
<span data-ttu-id="58c1d-118">E-mail-címek: a költségvetési értesítést a küszöb túllépése után küldheti el.</span><span class="sxs-lookup"><span data-stu-id="58c1d-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="58c1d-119">-ContactGroup</span></span>
<span data-ttu-id="58c1d-120">A műveleti csoportok a költségvetési értesítés küldéséhez a küszöb túllépése után.</span><span class="sxs-lookup"><span data-stu-id="58c1d-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="58c1d-121">-ContactRole</span></span>
<span data-ttu-id="58c1d-122">A partnerek szerepkörei a költségvetési értesítés elküldéséhez a küszöb túllépése esetén</span><span class="sxs-lookup"><span data-stu-id="58c1d-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c1d-123">-DefaultProfile</span></span>
<span data-ttu-id="58c1d-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58c1d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c1d-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="58c1d-125">-EndDate</span></span>
<span data-ttu-id="58c1d-126">Záró dátum (éééé-hh-nn) a költségvetés időszakában.</span><span class="sxs-lookup"><span data-stu-id="58c1d-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="58c1d-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="58c1d-127">-MeterFilter</span></span>
<span data-ttu-id="58c1d-128">Vesszővel elválasztott mérőműszerek listája a szűréshez.</span><span class="sxs-lookup"><span data-stu-id="58c1d-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="58c1d-129">Kötelező, ha a kategória használatos.</span><span class="sxs-lookup"><span data-stu-id="58c1d-129">Required if category is usage.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="58c1d-130">-Name</span></span>
<span data-ttu-id="58c1d-131">A költségvetés neve</span><span class="sxs-lookup"><span data-stu-id="58c1d-131">Name of a budget.</span></span>

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

### <span data-ttu-id="58c1d-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="58c1d-132">-NotificationEnabled</span></span>
<span data-ttu-id="58c1d-133">Az értesítés engedélyezve van vagy nem.</span><span class="sxs-lookup"><span data-stu-id="58c1d-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="58c1d-134">-NotificationKey</span></span>
<span data-ttu-id="58c1d-135">Egy költségvetéshez kapcsolódó értesítés kulcsát, amelyről értesítést kell létrehozni az értesítés engedélyezve kapcsolóval, az értesítési küszöböt, a kontakt e-maileket, a partnercsoport vagy a kontakt szerepköröket.</span><span class="sxs-lookup"><span data-stu-id="58c1d-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="58c1d-136">-NotificationThreshold</span></span>
<span data-ttu-id="58c1d-137">Az értesítéshez társított küszöb érték</span><span class="sxs-lookup"><span data-stu-id="58c1d-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="58c1d-138">Az értesítést akkor küldi a rendszer, amikor a költség vagy a használat túllépte a küszöböt.</span><span class="sxs-lookup"><span data-stu-id="58c1d-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="58c1d-139">A százalékos érték mindig 0 és 1000 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="58c1d-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="58c1d-140">-ResourceFilter</span></span>
<span data-ttu-id="58c1d-141">A szűrni kívánt erőforrás-példányok vesszővel elválasztott listája.</span><span class="sxs-lookup"><span data-stu-id="58c1d-141">Comma-separated list of resource instances to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="58c1d-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="58c1d-143">Vesszővel elválasztott erőforráscsoportok listája a szűréshez.</span><span class="sxs-lookup"><span data-stu-id="58c1d-143">Comma-separated list of resource groups to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c1d-144">-ResourceGroupName</span></span>
<span data-ttu-id="58c1d-145">Egy költségvetés erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="58c1d-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="58c1d-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="58c1d-146">-StartDate</span></span>
<span data-ttu-id="58c1d-147">Kezdési dátum (éééé-hh-nn) a költségvetés időszakában</span><span class="sxs-lookup"><span data-stu-id="58c1d-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="58c1d-148">A havi időgabona esetén nem az aktuális hónap előtt.</span><span class="sxs-lookup"><span data-stu-id="58c1d-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="58c1d-149">Negyedéves gabona esetén nem kell három hónapnál régebbit kiszámítani.</span><span class="sxs-lookup"><span data-stu-id="58c1d-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="58c1d-150">Éves időtartamú gabona esetén nem kell tizenkét hónapnál régebbinek lennie.</span><span class="sxs-lookup"><span data-stu-id="58c1d-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="58c1d-151">A jövőbeli kezdési dátum három hónapnál nem több.</span><span class="sxs-lookup"><span data-stu-id="58c1d-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="58c1d-152">-TimeGrain</span></span>
<span data-ttu-id="58c1d-153">A költségvetés időkerete lehet havi, negyedéves vagy évenkénti.</span><span class="sxs-lookup"><span data-stu-id="58c1d-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="58c1d-154">-Confirm</span></span>
<span data-ttu-id="58c1d-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="58c1d-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58c1d-156">-WhatIf</span></span>
<span data-ttu-id="58c1d-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="58c1d-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58c1d-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58c1d-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c1d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c1d-159">CommonParameters</span></span>
<span data-ttu-id="58c1d-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="58c1d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c1d-161">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c1d-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c1d-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="58c1d-162">INPUTS</span></span>

### <span data-ttu-id="58c1d-163">Nincs</span><span class="sxs-lookup"><span data-stu-id="58c1d-163">None</span></span>

## <span data-ttu-id="58c1d-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58c1d-164">OUTPUTS</span></span>

### <span data-ttu-id="58c1d-165">Microsoft. Azure. commands. fogyasztás. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="58c1d-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="58c1d-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="58c1d-166">NOTES</span></span>

## <span data-ttu-id="58c1d-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58c1d-167">RELATED LINKS</span></span>
