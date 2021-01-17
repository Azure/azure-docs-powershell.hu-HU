---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478121"
---
# <span data-ttu-id="d6e2e-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="d6e2e-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="d6e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e2e-103">Költségvetés létrehozása előfizetésben vagy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="d6e2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d6e2e-104">SYNTAX</span></span>

### <span data-ttu-id="d6e2e-105">Előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6e2e-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e2e-106">Értesítés</span><span class="sxs-lookup"><span data-stu-id="d6e2e-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6e2e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d6e2e-107">DESCRIPTION</span></span>
<span data-ttu-id="d6e2e-108">A New-AzConsumptionBudget parancsmag költségvetést hoz létre előfizetésben vagy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="d6e2e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d6e2e-109">EXAMPLES</span></span>

### <span data-ttu-id="d6e2e-110">1. példa: Költségvetés létrehozása előfizetési szinten költségvetésnévvel</span><span class="sxs-lookup"><span data-stu-id="d6e2e-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
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

### <span data-ttu-id="d6e2e-111">2. példa: Költségvetés létrehozása erőforráscsoport szinten költségvetésnévvel</span><span class="sxs-lookup"><span data-stu-id="d6e2e-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
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

## <span data-ttu-id="d6e2e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6e2e-112">PARAMETERS</span></span>

### <span data-ttu-id="d6e2e-113">-Amount</span><span class="sxs-lookup"><span data-stu-id="d6e2e-113">-Amount</span></span>
<span data-ttu-id="d6e2e-114">Költségvetés összege.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="d6e2e-115">-Category</span><span class="sxs-lookup"><span data-stu-id="d6e2e-115">-Category</span></span>
<span data-ttu-id="d6e2e-116">A költségvetés kategóriája lehet költség vagy használat.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="d6e2e-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="d6e2e-117">-ContactEmail</span></span>
<span data-ttu-id="d6e2e-118">E-mail-címek, amelyekre a küszöbérték túllépése esetén a költségvetési értesítést el kell küldeni.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="d6e2e-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="d6e2e-119">-ContactGroup</span></span>
<span data-ttu-id="d6e2e-120">Műveletcsoportok, amelyek a küszöbérték túllépése esetén a költségvetési értesítést küldik.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="d6e2e-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="d6e2e-121">-ContactRole</span></span>
<span data-ttu-id="d6e2e-122">Kapcsolattartási szerepkörök a küszöbérték túllépése esetén a költségvetési értesítés elküldése érdekében.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="d6e2e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e2e-123">-DefaultProfile</span></span>
<span data-ttu-id="d6e2e-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6e2e-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d6e2e-125">-EndDate</span></span>
<span data-ttu-id="d6e2e-126">A költségvetés időszakának záró dátuma (YYYY-HH-DD az UTC-ben).</span><span class="sxs-lookup"><span data-stu-id="d6e2e-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="d6e2e-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="d6e2e-127">-MeterFilter</span></span>
<span data-ttu-id="d6e2e-128">Pontosvesszővel elválasztott lista, amely alapján szűrni kell a métereket.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="d6e2e-129">Kötelező, ha a kategória használati.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="d6e2e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="d6e2e-130">-Name</span></span>
<span data-ttu-id="d6e2e-131">A költségvetés neve.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-131">Name of a budget.</span></span>

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

### <span data-ttu-id="d6e2e-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="d6e2e-132">-NotificationEnabled</span></span>
<span data-ttu-id="d6e2e-133">Az értesítés engedélyezve van vagy sem.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="d6e2e-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="d6e2e-134">-NotificationKey</span></span>
<span data-ttu-id="d6e2e-135">A költségvetéshez társított értesítés kulcsa, amely értesítés létrehozásához értesítési kapcsolót, értesítési küszöbértéket, kapcsolati e-maileket, partnercsoportokat vagy partneri szerepköröket kell létrehoznia.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="d6e2e-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="d6e2e-136">-NotificationThreshold</span></span>
<span data-ttu-id="d6e2e-137">Értesítéshez társított küszöbérték.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="d6e2e-138">A rendszer értesítést küld, ha a költség vagy a használat túllépte a küszöbértéket.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="d6e2e-139">Ennek mindig százaléknak kell lennie, és 0 és 1000 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="d6e2e-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="d6e2e-140">-ResourceFilter</span></span>
<span data-ttu-id="d6e2e-141">Azon erőforráspéldányok vesszővel elválasztott listája, amelyekre szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="d6e2e-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="d6e2e-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="d6e2e-143">Azon erőforráscsoportok vesszővel elválasztott listája, amelyekre szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="d6e2e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e2e-144">-ResourceGroupName</span></span>
<span data-ttu-id="d6e2e-145">Költségvetés erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="d6e2e-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d6e2e-146">-StartDate</span></span>
<span data-ttu-id="d6e2e-147">A költségvetés időszakának kezdő dátuma (YYYY-HH-DD az UTC-ben).</span><span class="sxs-lookup"><span data-stu-id="d6e2e-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="d6e2e-148">A havi időkorrekta esetén az aktuális hónap előtt nem.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="d6e2e-149">A negyedéves időszakra vonatkozó három hónapnál nem korábban.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="d6e2e-150">Az éves berekedő szemcse esetén tizenkét hónapnál nem korábbi.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="d6e2e-151">A jövőbeli kezdési dátum nem lehet három hónapnál tovább.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="d6e2e-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="d6e2e-152">-TimeGrain</span></span>
<span data-ttu-id="d6e2e-153">A költségvetés időkorrekta lehet havi, negyedéves vagy éves.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="d6e2e-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6e2e-154">-Confirm</span></span>
<span data-ttu-id="d6e2e-155">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6e2e-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6e2e-156">-WhatIf</span></span>
<span data-ttu-id="d6e2e-157">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6e2e-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6e2e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e2e-159">CommonParameters</span></span>
<span data-ttu-id="d6e2e-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6e2e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e2e-161">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6e2e-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e2e-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6e2e-162">INPUTS</span></span>

### <span data-ttu-id="d6e2e-163">Nincs</span><span class="sxs-lookup"><span data-stu-id="d6e2e-163">None</span></span>

## <span data-ttu-id="d6e2e-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6e2e-164">OUTPUTS</span></span>

### <span data-ttu-id="d6e2e-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="d6e2e-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="d6e2e-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d6e2e-166">NOTES</span></span>

## <span data-ttu-id="d6e2e-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6e2e-167">RELATED LINKS</span></span>
