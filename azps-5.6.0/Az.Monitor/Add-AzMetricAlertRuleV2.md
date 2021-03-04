---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: f679b674de8ed2f860278cb3a384f73ed17e5f54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932746"
---
# <span data-ttu-id="4d39b-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4d39b-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="4d39b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d39b-102">SYNOPSIS</span></span>
<span data-ttu-id="4d39b-103">V2-es (nem klasszikus) metrikus riasztási szabályt ad hozzá vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="4d39b-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="4d39b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d39b-104">SYNTAX</span></span>

### <span data-ttu-id="4d39b-105">CreateAlertByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d39b-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d39b-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="4d39b-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d39b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d39b-107">DESCRIPTION</span></span>
<span data-ttu-id="4d39b-108">V2 **-es (nem klasszikus) metrikus alapú riasztási** szabályt ad hozzá vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="4d39b-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="4d39b-109">A hozzáadott szabály egy erőforráscsoporthoz van társítva, és neve is van.</span><span class="sxs-lookup"><span data-stu-id="4d39b-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="4d39b-110">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="4d39b-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="4d39b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d39b-111">EXAMPLES</span></span>

### <span data-ttu-id="4d39b-112">1. példa: Metrikus riasztási szabály hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="4d39b-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="4d39b-113">Ez a parancs metrikus riasztási szabályt hoz létre egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="4d39b-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="4d39b-114">$condition a [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) parancsmag kimenete, a $act pedig a [New-AzActionGroup](https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroup) parancsmag kimenete.</span><span class="sxs-lookup"><span data-stu-id="4d39b-114">$condition is the output of [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet and $act is the output of [New-AzActionGroup](https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroup) cmdlet</span></span>

### <span data-ttu-id="4d39b-115">2. példa: Metrikus riasztási szabály hozzáadása egy előfizetés összes virtuális gépéhez</span><span class="sxs-lookup"><span data-stu-id="4d39b-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="4d39b-116">Ez a parancs metrikus riasztási szabályt hoz létre az előfizetés összes, eastusban lévő virtuális gépéhez</span><span class="sxs-lookup"><span data-stu-id="4d39b-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="4d39b-117">3. példa: Metrikus riasztási szabály letiltása</span><span class="sxs-lookup"><span data-stu-id="4d39b-117">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="4d39b-118">Ez a parancs letiltja a metrikus riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="4d39b-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="4d39b-119">A [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2) kimenetét az [Add-AzMetricAlertRuleV2-re](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2) szeretnénk kivezetni.</span><span class="sxs-lookup"><span data-stu-id="4d39b-119">Here, we are piping output of [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2) to [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrulev2)</span></span> 

### <span data-ttu-id="4d39b-120">4. példa: Metrikus riasztási szabály hozzáadása dimenziókkal</span><span class="sxs-lookup"><span data-stu-id="4d39b-120">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="4d39b-121">A [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) és [a New-AzMetricAlertRuleV2DimensionSelection és a New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria)súgó parancsmagok használatával összetettebb riasztási szabályt hozhat létre, például a dimenzióértékek kiválasztását vagy több feltételt is.</span><span class="sxs-lookup"><span data-stu-id="4d39b-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) and [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span></span>

<span data-ttu-id="4d39b-122">A parancsmagok fölött metrikus riasztási szabályt hozhat létre dimenziókkal.</span><span class="sxs-lookup"><span data-stu-id="4d39b-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="4d39b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d39b-123">PARAMETERS</span></span>

### <span data-ttu-id="4d39b-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="4d39b-124">-ActionGroup</span></span>
<span data-ttu-id="4d39b-125">The Action Group for rule</span><span class="sxs-lookup"><span data-stu-id="4d39b-125">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-126">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="4d39b-126">-ActionGroupId</span></span>
<span data-ttu-id="4d39b-127">A szabály műveletcsoport-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4d39b-127">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-128">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="4d39b-128">-Condition</span></span>
<span data-ttu-id="4d39b-129">A szabály feltétele</span><span class="sxs-lookup"><span data-stu-id="4d39b-129">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d39b-130">-DefaultProfile</span></span>
<span data-ttu-id="4d39b-131">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d39b-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d39b-132">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4d39b-132">-Description</span></span>
<span data-ttu-id="4d39b-133">A metrikus riasztási szabály leírása</span><span class="sxs-lookup"><span data-stu-id="4d39b-133">The description of the metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="4d39b-134">-DisableRule</span></span>
<span data-ttu-id="4d39b-135">A szabály (állapot) letiltására vonatkozó jelölő</span><span class="sxs-lookup"><span data-stu-id="4d39b-135">The disable rule (status) flag</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-136">-Frequency</span><span class="sxs-lookup"><span data-stu-id="4d39b-136">-Frequency</span></span>
<span data-ttu-id="4d39b-137">A szabály kiértékelési gyakorisága</span><span class="sxs-lookup"><span data-stu-id="4d39b-137">The evaluation frequency for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4d39b-138">-Name</span></span>
<span data-ttu-id="4d39b-139">A metrikus riasztási szabály neve</span><span class="sxs-lookup"><span data-stu-id="4d39b-139">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d39b-140">-ResourceGroupName</span></span>
<span data-ttu-id="4d39b-141">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4d39b-141">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-142">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="4d39b-142">-Severity</span></span>
<span data-ttu-id="4d39b-143">A metrikus riasztási szabály súlyossága</span><span class="sxs-lookup"><span data-stu-id="4d39b-143">The severity for the metric alert rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4d39b-144">-TargetResourceId</span></span>
<span data-ttu-id="4d39b-145">A szabály célerőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4d39b-145">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="4d39b-146">-TargetResourceRegion</span></span>
<span data-ttu-id="4d39b-147">A szabály célerőforrás-régiója</span><span class="sxs-lookup"><span data-stu-id="4d39b-147">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="4d39b-148">-TargetResourceScope</span></span>
<span data-ttu-id="4d39b-149">A szabály célerőforrás-hatóköre</span><span class="sxs-lookup"><span data-stu-id="4d39b-149">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="4d39b-150">-TargetResourceType</span></span>
<span data-ttu-id="4d39b-151">A szabály célerőforrás-típusa</span><span class="sxs-lookup"><span data-stu-id="4d39b-151">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-152">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="4d39b-152">-WindowSize</span></span>
<span data-ttu-id="4d39b-153">A szabály ablakmérete</span><span class="sxs-lookup"><span data-stu-id="4d39b-153">The window size for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d39b-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d39b-154">-Confirm</span></span>
<span data-ttu-id="4d39b-155">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4d39b-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d39b-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d39b-156">-WhatIf</span></span>
<span data-ttu-id="4d39b-157">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4d39b-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d39b-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d39b-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d39b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d39b-159">CommonParameters</span></span>
<span data-ttu-id="4d39b-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d39b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d39b-161">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d39b-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d39b-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d39b-162">INPUTS</span></span>

### <span data-ttu-id="4d39b-163">System.String</span><span class="sxs-lookup"><span data-stu-id="4d39b-163">System.String</span></span>

### <span data-ttu-id="4d39b-164">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="4d39b-164">System.TimeSpan</span></span>

### <span data-ttu-id="4d39b-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4d39b-165">System.String[]</span></span>

### <span data-ttu-id="4d39b-166">System.Collections.Generic.List'1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4d39b-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4d39b-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span><span class="sxs-lookup"><span data-stu-id="4d39b-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="4d39b-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d39b-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4d39b-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4d39b-169">System.Int32</span></span>

## <span data-ttu-id="4d39b-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d39b-170">OUTPUTS</span></span>

### <span data-ttu-id="4d39b-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4d39b-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="4d39b-172">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d39b-172">NOTES</span></span>

## <span data-ttu-id="4d39b-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d39b-173">RELATED LINKS</span></span>
