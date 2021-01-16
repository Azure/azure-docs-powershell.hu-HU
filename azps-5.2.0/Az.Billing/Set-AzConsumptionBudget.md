---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: 89d628790297bfb677dab11f0b19ba525d8b9e47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333114"
---
# <span data-ttu-id="ceeeb-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="ceeeb-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="ceeeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceeeb-102">SYNOPSIS</span></span>
<span data-ttu-id="ceeeb-103">Frissítheti a költségvetést akár előfizetésben, akár erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="ceeeb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ceeeb-104">SYNTAX</span></span>

### <span data-ttu-id="ceeeb-105">Előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ceeeb-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceeeb-106">Értesítés</span><span class="sxs-lookup"><span data-stu-id="ceeeb-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceeeb-107">Pipázás</span><span class="sxs-lookup"><span data-stu-id="ceeeb-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ceeeb-108">Pipázás és értesítés</span><span class="sxs-lookup"><span data-stu-id="ceeeb-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceeeb-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ceeeb-109">DESCRIPTION</span></span>
<span data-ttu-id="ceeeb-110">A Set-AzConsumptionBudget parancsmag előfizetésben vagy erőforráscsoportban frissíti a költségvetést.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="ceeeb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ceeeb-111">EXAMPLES</span></span>

### <span data-ttu-id="ceeeb-112">1. példa: Költségvetés frissítése új összeggel, előfizetési szinten költségvetésnévvel</span><span class="sxs-lookup"><span data-stu-id="ceeeb-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="ceeeb-113">2. példa: Költségvetés frissítése értesítéssel, amikor a költség vagy a használat eléri az előfizetési szinten az összeg 90%-os küszöbértékét</span><span class="sxs-lookup"><span data-stu-id="ceeeb-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="ceeeb-114">3. példa: Költségvetés frissítése új összeggel az erőforráscsoport szintjén költségvetésnévvel</span><span class="sxs-lookup"><span data-stu-id="ceeeb-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="ceeeb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceeeb-115">PARAMETERS</span></span>

### <span data-ttu-id="ceeeb-116">-Amount</span><span class="sxs-lookup"><span data-stu-id="ceeeb-116">-Amount</span></span>
<span data-ttu-id="ceeeb-117">Költségvetés összege.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-118">-Category</span><span class="sxs-lookup"><span data-stu-id="ceeeb-118">-Category</span></span>
<span data-ttu-id="ceeeb-119">A költségvetés kategóriája lehet költség vagy használat.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="ceeeb-120">-ContactEmail</span></span>
<span data-ttu-id="ceeeb-121">E-mail-címek, amelyekre a küszöbérték túllépése esetén a költségvetési értesítést el kell küldeni.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="ceeeb-122">-ContactGroup</span></span>
<span data-ttu-id="ceeeb-123">Műveletcsoportok, amelyek a küszöbérték túllépése esetén a költségvetési értesítést küldik.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="ceeeb-124">-ContactRole</span></span>
<span data-ttu-id="ceeeb-125">Kapcsolattartási szerepkörök a küszöbérték túllépése esetén a költségvetési értesítés elküldése érdekében.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceeeb-126">-DefaultProfile</span></span>
<span data-ttu-id="ceeeb-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceeeb-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ceeeb-128">-EndDate</span></span>
<span data-ttu-id="ceeeb-129">A költségvetés időszakának záró dátuma (YYYY-HH-DD az UTC-ben).</span><span class="sxs-lookup"><span data-stu-id="ceeeb-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="ceeeb-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ceeeb-130">-InputObject</span></span>
<span data-ttu-id="ceeeb-131">Budget objektum.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="ceeeb-132">-MeterFilter</span></span>
<span data-ttu-id="ceeeb-133">Pontosvesszővel elválasztott lista, amely alapján szűrni kell a métereket.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="ceeeb-134">Kötelező, ha a kategória használati.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="ceeeb-135">-Name</span><span class="sxs-lookup"><span data-stu-id="ceeeb-135">-Name</span></span>
<span data-ttu-id="ceeeb-136">A költségvetés neve.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="ceeeb-137">-NotificationEnabled</span></span>
<span data-ttu-id="ceeeb-138">Az értesítés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-138">The notification is enabled.</span></span>
<span data-ttu-id="ceeeb-139">Ha nincs megadva, az értesítés alapértelmezés szerint le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="ceeeb-140">-NotificationKey</span></span>
<span data-ttu-id="ceeeb-141">A költségvetéshez társított értesítés kulcsa, amely értesítés létrehozásához értesítési kapcsolót, értesítési küszöbértéket, kapcsolati e-maileket, partnercsoportokat vagy partneri szerepköröket kell létrehoznia.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="ceeeb-142">-NotificationThreshold</span></span>
<span data-ttu-id="ceeeb-143">Értesítéshez társított küszöbérték.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="ceeeb-144">A rendszer értesítést küld, ha a költség vagy a használat túllépte a küszöbértéket.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="ceeeb-145">Ennek mindig százaléknak kell lennie, és 0 és 1000 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="ceeeb-146">-ResourceFilter</span></span>
<span data-ttu-id="ceeeb-147">Azon erőforráspéldányok vesszővel elválasztott listája, amelyekre szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="ceeeb-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="ceeeb-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="ceeeb-149">Azon erőforráscsoportok vesszővel elválasztott listája, amelyekre szűrni kell.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="ceeeb-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceeeb-150">-ResourceGroupName</span></span>
<span data-ttu-id="ceeeb-151">Költségvetés erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ceeeb-152">-StartDate</span></span>
<span data-ttu-id="ceeeb-153">A költségvetés időszakának kezdő dátuma (YYYY-HH-DD az UTC-ben).</span><span class="sxs-lookup"><span data-stu-id="ceeeb-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="ceeeb-154">A havi időkorrekta az aktuális hónap előtt nem.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="ceeeb-155">A negyedéves időszakra vonatkozó három hónapnál nem korábban.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="ceeeb-156">Az éves szemcse esetén tizenkét hónapnál nem korábbi.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="ceeeb-157">A jövőbeli kezdési dátum nem lehet három hónapnál tovább.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="ceeeb-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="ceeeb-158">-TimeGrain</span></span>
<span data-ttu-id="ceeeb-159">A költségvetés időkorrekta lehet havi, negyedéves vagy éves.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeeb-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceeeb-160">-Confirm</span></span>
<span data-ttu-id="ceeeb-161">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceeeb-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceeeb-162">-WhatIf</span></span>
<span data-ttu-id="ceeeb-163">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceeeb-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceeeb-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceeeb-165">CommonParameters</span></span>
<span data-ttu-id="ceeeb-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceeeb-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceeeb-167">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceeeb-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceeeb-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ceeeb-168">INPUTS</span></span>

### <span data-ttu-id="ceeeb-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="ceeeb-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="ceeeb-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceeeb-170">OUTPUTS</span></span>

### <span data-ttu-id="ceeeb-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="ceeeb-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="ceeeb-172">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ceeeb-172">NOTES</span></span>

## <span data-ttu-id="ceeeb-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ceeeb-173">RELATED LINKS</span></span>
