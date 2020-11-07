---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: c159ab71befb52e8131ade0b90e69c4ba8158885
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667655"
---
# <span data-ttu-id="41226-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="41226-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="41226-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41226-102">SYNOPSIS</span></span>
<span data-ttu-id="41226-103">Költségvetés frissítése előfizetés vagy erőforráscsoport esetén</span><span class="sxs-lookup"><span data-stu-id="41226-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="41226-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41226-104">SYNTAX</span></span>

### <span data-ttu-id="41226-105">Előfizetés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41226-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41226-106">Értesítés</span><span class="sxs-lookup"><span data-stu-id="41226-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41226-107">Csővezeték</span><span class="sxs-lookup"><span data-stu-id="41226-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41226-108">Csővezetékek és értesítések</span><span class="sxs-lookup"><span data-stu-id="41226-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41226-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="41226-109">DESCRIPTION</span></span>
<span data-ttu-id="41226-110">A Set-AzConsumptionBudget parancsmag előfizetésben vagy erőforráscsoportben frissíti a költségvetést.</span><span class="sxs-lookup"><span data-stu-id="41226-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="41226-111">Példák</span><span class="sxs-lookup"><span data-stu-id="41226-111">EXAMPLES</span></span>

### <span data-ttu-id="41226-112">Példa 1: költségvetés frissítése új összeggel az előfizetési szint költségvetés nevével</span><span class="sxs-lookup"><span data-stu-id="41226-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
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

### <span data-ttu-id="41226-113">2. példa: költségvetés frissítése értesítésben, ha a költség vagy a használat eléri az összeg 90 százalékát az előfizetési szinten.</span><span class="sxs-lookup"><span data-stu-id="41226-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
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

### <span data-ttu-id="41226-114">3. példa: költségvetés frissítése új összeggel az erőforrás csoport szintjén</span><span class="sxs-lookup"><span data-stu-id="41226-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
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

## <span data-ttu-id="41226-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41226-115">PARAMETERS</span></span>

### <span data-ttu-id="41226-116">-Összeg</span><span class="sxs-lookup"><span data-stu-id="41226-116">-Amount</span></span>
<span data-ttu-id="41226-117">Költségvetés összege.</span><span class="sxs-lookup"><span data-stu-id="41226-117">Amount of a budget.</span></span>

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

### <span data-ttu-id="41226-118">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="41226-118">-Category</span></span>
<span data-ttu-id="41226-119">A költségvetés kategóriája lehet költség vagy felhasználás.</span><span class="sxs-lookup"><span data-stu-id="41226-119">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="41226-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="41226-120">-ContactEmail</span></span>
<span data-ttu-id="41226-121">E-mail-címek: a költségvetési értesítést a küszöb túllépése után küldheti el.</span><span class="sxs-lookup"><span data-stu-id="41226-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="41226-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="41226-122">-ContactGroup</span></span>
<span data-ttu-id="41226-123">A műveleti csoportok a költségvetési értesítés küldéséhez a küszöb túllépése után.</span><span class="sxs-lookup"><span data-stu-id="41226-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="41226-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="41226-124">-ContactRole</span></span>
<span data-ttu-id="41226-125">A partnerek szerepkörei a költségvetési értesítés elküldéséhez a küszöb túllépése esetén</span><span class="sxs-lookup"><span data-stu-id="41226-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="41226-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41226-126">-DefaultProfile</span></span>
<span data-ttu-id="41226-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41226-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41226-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="41226-128">-EndDate</span></span>
<span data-ttu-id="41226-129">Záró dátum (éééé-hh-nn) a költségvetés időszakában.</span><span class="sxs-lookup"><span data-stu-id="41226-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="41226-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41226-130">-InputObject</span></span>
<span data-ttu-id="41226-131">Költségvetés objektum.</span><span class="sxs-lookup"><span data-stu-id="41226-131">Budget object.</span></span>

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

### <span data-ttu-id="41226-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="41226-132">-MeterFilter</span></span>
<span data-ttu-id="41226-133">Vesszővel elválasztott mérőműszerek listája a szűréshez.</span><span class="sxs-lookup"><span data-stu-id="41226-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="41226-134">Kötelező, ha a kategória használatos.</span><span class="sxs-lookup"><span data-stu-id="41226-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="41226-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41226-135">-Name</span></span>
<span data-ttu-id="41226-136">A költségvetés neve</span><span class="sxs-lookup"><span data-stu-id="41226-136">Name of a budget.</span></span>

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

### <span data-ttu-id="41226-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="41226-137">-NotificationEnabled</span></span>
<span data-ttu-id="41226-138">Az értesítés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="41226-138">The notification is enabled.</span></span>
<span data-ttu-id="41226-139">Ha nincs megadva, az értesítés alapértelmezés szerint le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="41226-139">If not specified, the notification is disabled by default.</span></span>

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

### <span data-ttu-id="41226-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="41226-140">-NotificationKey</span></span>
<span data-ttu-id="41226-141">Egy költségvetéshez kapcsolódó értesítés kulcsát, amelyről értesítést kell létrehozni az értesítés engedélyezve kapcsolóval, az értesítési küszöböt, a kontakt e-maileket, a partnercsoport vagy a kontakt szerepköröket.</span><span class="sxs-lookup"><span data-stu-id="41226-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="41226-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="41226-142">-NotificationThreshold</span></span>
<span data-ttu-id="41226-143">Az értesítéshez társított küszöb érték</span><span class="sxs-lookup"><span data-stu-id="41226-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="41226-144">Az értesítést akkor küldi a rendszer, amikor a költség vagy a használat túllépte a küszöböt.</span><span class="sxs-lookup"><span data-stu-id="41226-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="41226-145">A százalékos érték mindig 0 és 1000 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="41226-145">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="41226-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="41226-146">-ResourceFilter</span></span>
<span data-ttu-id="41226-147">A szűrni kívánt erőforrás-példányok vesszővel elválasztott listája.</span><span class="sxs-lookup"><span data-stu-id="41226-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="41226-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="41226-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="41226-149">Vesszővel elválasztott erőforráscsoportok listája a szűréshez.</span><span class="sxs-lookup"><span data-stu-id="41226-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="41226-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41226-150">-ResourceGroupName</span></span>
<span data-ttu-id="41226-151">Egy költségvetés erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="41226-151">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="41226-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="41226-152">-StartDate</span></span>
<span data-ttu-id="41226-153">Kezdési dátum (éééé-hh-nn) a költségvetés időszakában</span><span class="sxs-lookup"><span data-stu-id="41226-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="41226-154">A havi időgabona esetén nem az aktuális hónap előtt.</span><span class="sxs-lookup"><span data-stu-id="41226-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="41226-155">Negyedéves gabona esetén nem kell három hónapnál régebbit kiszámítani.</span><span class="sxs-lookup"><span data-stu-id="41226-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="41226-156">Éves időtartamú gabona esetén nem kell tizenkét hónapnál régebbinek lennie.</span><span class="sxs-lookup"><span data-stu-id="41226-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="41226-157">A jövőbeli kezdési dátum három hónapnál nem több.</span><span class="sxs-lookup"><span data-stu-id="41226-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="41226-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="41226-158">-TimeGrain</span></span>
<span data-ttu-id="41226-159">A költségvetés időkerete lehet havi, negyedéves vagy évenkénti.</span><span class="sxs-lookup"><span data-stu-id="41226-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="41226-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41226-160">-Confirm</span></span>
<span data-ttu-id="41226-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41226-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41226-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41226-162">-WhatIf</span></span>
<span data-ttu-id="41226-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41226-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41226-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41226-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41226-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41226-165">CommonParameters</span></span>
<span data-ttu-id="41226-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41226-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41226-167">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41226-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41226-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41226-168">INPUTS</span></span>

### <span data-ttu-id="41226-169">Microsoft. Azure. commands. fogyasztás. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="41226-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="41226-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41226-170">OUTPUTS</span></span>

### <span data-ttu-id="41226-171">Microsoft. Azure. commands. fogyasztás. models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="41226-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="41226-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41226-172">NOTES</span></span>

## <span data-ttu-id="41226-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41226-173">RELATED LINKS</span></span>
