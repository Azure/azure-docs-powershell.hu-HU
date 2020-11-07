---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 17be83253d452b4c347154f8c0e392277287d0b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835129"
---
# <span data-ttu-id="f6899-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f6899-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="f6899-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6899-102">SYNOPSIS</span></span>
<span data-ttu-id="f6899-103">V2 (nem klasszikus) metrika-alapú figyelmeztetési szabály hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="f6899-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="f6899-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6899-104">SYNTAX</span></span>

### <span data-ttu-id="f6899-105">CreateAlertByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6899-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6899-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="f6899-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6899-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6899-107">DESCRIPTION</span></span>
<span data-ttu-id="f6899-108">**V2 (nem klasszikus) metrika-alapú figyelmeztetési szabály** hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="f6899-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="f6899-109">A hozzáadott szabály erőforrás-csoporthoz van társítva, és nevet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="f6899-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="f6899-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="f6899-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f6899-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f6899-111">EXAMPLES</span></span>

### <span data-ttu-id="f6899-112">1. példa: metrikus figyelmeztetési szabály hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="f6899-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name PS3182019 -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1", "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="f6899-113">Ez a parancs metrikus figyelmeztetési szabályt hoz létre a virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="f6899-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="f6899-114">a $condition a New-AzMetricAlertRuleV2Criteria parancsmag kimenete, a $act pedig New-AzActionGroup parancsmag kimenete</span><span class="sxs-lookup"><span data-stu-id="f6899-114">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="f6899-115">2. példa: metrikus figyelmeztetési szabály hozzáadása az előfizetésben szereplő összes virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="f6899-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name AllVM -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/AllVM
Name                 : AllVM
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="f6899-116">Ez a parancs metrikus figyelmeztetési szabályt hoz létre a eastus-előfizetésben lévő összes virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="f6899-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="f6899-117">3. példa: metrikus figyelmeztetési szabály letiltása</span><span class="sxs-lookup"><span data-stu-id="f6899-117">Example 3: Disable a metric alert rule</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest  -Name TestAlertRule | Add-AzMetricAlertRuleV2 -DisableRule
Description          : This new Metric alert rule was created from Powershell version: 1.0.1
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo1}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/TestAlertRule
Name                 : TestAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="f6899-118">Ez a parancs a metrika riasztási szabályait letiltja.</span><span class="sxs-lookup"><span data-stu-id="f6899-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="f6899-119">A Get-AzMetricAlertRuleV2 a Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f6899-119">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="f6899-120">4. példa: metrikus figyelmeztetési szabály hozzáadása dimenziókkal</span><span class="sxs-lookup"><span data-stu-id="f6899-120">Example 4: Add a metric alert rule with dimensions</span></span>

```powershell
PS C:\>$act = New-AzActionGroup -ActionGroupId "/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo"
PS C:\>$dim1 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest"
PS C:\>$dim2 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/location" -ValuesToInclude "*"
PS C:\>$criteria = New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -DimensionSelection $dim1,$dim2 -TimeAggregation Average -Operator GreaterThan -Threshold 2
PS C:\>Add-AzMetricAlertRuleV2 -Name AlertWithDim -ResourceGroupName alertstest -WindowSize 00:05:00 -Frequency 00:05:00 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction" -Condition $criteria -ActionGroup $act -DisableRule -Severity 4
Description          : This new Metric alert rule was created from Powershell version: 1.0.0
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/AlertWithDim
Name                 : AlertWithDim
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :

```

<span data-ttu-id="f6899-121">Ha összetettebb metrikus figyelmeztetési szabályt szeretne létrehozni, például a dimenzióértékek kiválasztásával vagy több feltétel megadásával, használhatja a segítő parancsmagokat New-AzMetricAlertRuleV2DimensionSelection és a New-AzMetricAlertRuleV2Criteria.</span><span class="sxs-lookup"><span data-stu-id="f6899-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="f6899-122">A fenti parancsmagok halmaza metrikus figyelmeztetési szabályt hoz létre a méretekkel.</span><span class="sxs-lookup"><span data-stu-id="f6899-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>
## <span data-ttu-id="f6899-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6899-123">PARAMETERS</span></span>

### <span data-ttu-id="f6899-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="f6899-124">-ActionGroup</span></span>
<span data-ttu-id="f6899-125">A szabály műveleti csoportja</span><span class="sxs-lookup"><span data-stu-id="f6899-125">The Action Group for rule</span></span>

```yaml
Type: ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-126">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="f6899-126">-Condition</span></span>
<span data-ttu-id="f6899-127">A szabály feltétele</span><span class="sxs-lookup"><span data-stu-id="f6899-127">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6899-128">-Confirm</span></span>
<span data-ttu-id="f6899-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6899-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6899-130">-DefaultProfile</span></span>
<span data-ttu-id="f6899-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6899-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-132">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f6899-132">-Description</span></span>
<span data-ttu-id="f6899-133">A metrikus figyelmeztetési szabály leírása</span><span class="sxs-lookup"><span data-stu-id="f6899-133">The description of the metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="f6899-134">-DisableRule</span></span>
<span data-ttu-id="f6899-135">A szabály letiltása (állapot) jelző</span><span class="sxs-lookup"><span data-stu-id="f6899-135">The disable rule (status) flag</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-136">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="f6899-136">-Frequency</span></span>
<span data-ttu-id="f6899-137">A szabály kiértékelésének gyakorisága</span><span class="sxs-lookup"><span data-stu-id="f6899-137">The evaluation frequency for rule</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6899-138">-Name</span></span>
<span data-ttu-id="f6899-139">A metrikus figyelmeztetési szabály neve</span><span class="sxs-lookup"><span data-stu-id="f6899-139">The name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6899-140">-ResourceGroupName</span></span>
<span data-ttu-id="f6899-141">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f6899-141">The Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-142">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="f6899-142">-Severity</span></span>
<span data-ttu-id="f6899-143">A metrika figyelmeztetési szabályának súlyossága</span><span class="sxs-lookup"><span data-stu-id="f6899-143">The severity for the metric alert rule</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f6899-144">-TargetResourceId</span></span>
<span data-ttu-id="f6899-145">A cél erőforrás-azonosító a szabályhoz</span><span class="sxs-lookup"><span data-stu-id="f6899-145">The target resource id for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="f6899-146">-TargetResourceRegion</span></span>
<span data-ttu-id="f6899-147">A cél erőforrás terület a szabályhoz</span><span class="sxs-lookup"><span data-stu-id="f6899-147">The target resource region for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="f6899-148">-TargetResourceScope</span></span>
<span data-ttu-id="f6899-149">A cél erőforrás hatóköre a szabályhoz</span><span class="sxs-lookup"><span data-stu-id="f6899-149">The target resource scope for rule</span></span>

```yaml
Type: String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="f6899-150">-TargetResourceType</span></span>
<span data-ttu-id="f6899-151">A cél erőforrástípus a szabályhoz</span><span class="sxs-lookup"><span data-stu-id="f6899-151">The target resource type for rule</span></span>

```yaml
Type: String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6899-152">-WhatIf</span></span>
<span data-ttu-id="f6899-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6899-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6899-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6899-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-155">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="f6899-155">-WindowSize</span></span>
<span data-ttu-id="f6899-156">A szabály ablakának mérete</span><span class="sxs-lookup"><span data-stu-id="f6899-156">The window size for rule</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6899-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6899-157">CommonParameters</span></span>
<span data-ttu-id="f6899-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6899-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f6899-159">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6899-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6899-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6899-160">INPUTS</span></span>

### <span data-ttu-id="f6899-161">System. String</span><span class="sxs-lookup"><span data-stu-id="f6899-161">System.String</span></span>

### <span data-ttu-id="f6899-162">System. időszak</span><span class="sxs-lookup"><span data-stu-id="f6899-162">System.TimeSpan</span></span>

### <span data-ttu-id="f6899-163">System. string []</span><span class="sxs-lookup"><span data-stu-id="f6899-163">System.String[]</span></span>

### <span data-ttu-id="f6899-164">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. OutputClasses. PSMetricCriteria, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f6899-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f6899-165">Microsoft. Azure. Management. monitor. models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="f6899-165">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="f6899-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f6899-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f6899-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f6899-167">System.Int32</span></span>

## <span data-ttu-id="f6899-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6899-168">OUTPUTS</span></span>

### <span data-ttu-id="f6899-169">Microsoft. Azure. commands. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f6899-169">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="f6899-170">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6899-170">NOTES</span></span>

## <span data-ttu-id="f6899-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6899-171">RELATED LINKS</span></span>
