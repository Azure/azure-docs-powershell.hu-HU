---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 0317f21231edd2608492d37609ab4f4849ba9c20
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195765"
---
# <span data-ttu-id="87066-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="87066-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="87066-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87066-102">SYNOPSIS</span></span>
<span data-ttu-id="87066-103">V2 (nem klasszikus) metrika-alapú figyelmeztetési szabály hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="87066-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="87066-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87066-104">SYNTAX</span></span>

### <span data-ttu-id="87066-105">CreateAlertByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87066-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87066-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="87066-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87066-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="87066-107">DESCRIPTION</span></span>
<span data-ttu-id="87066-108">**V2 (nem klasszikus) metrika-alapú figyelmeztetési szabály** hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="87066-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="87066-109">A hozzáadott szabály erőforrás-csoporthoz van társítva, és nevet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="87066-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="87066-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="87066-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="87066-111">Példák</span><span class="sxs-lookup"><span data-stu-id="87066-111">EXAMPLES</span></span>

### <span data-ttu-id="87066-112">1. példa: metrikus figyelmeztetési szabály hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="87066-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="87066-113">Ez a parancs metrikus figyelmeztetési szabályt hoz létre a virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="87066-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="87066-114">$condition a [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) parancsmag kimenete, és a $Act a [New-AzActionGroup](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup) parancsmag kimenete.</span><span class="sxs-lookup"><span data-stu-id="87066-114">$condition is the output of [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet and $act is the output of [New-AzActionGroup](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup) cmdlet</span></span>

### <span data-ttu-id="87066-115">2. példa: metrikus figyelmeztetési szabály hozzáadása az előfizetésben szereplő összes virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="87066-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="87066-116">Ez a parancs metrikus figyelmeztetési szabályt hoz létre a eastus-előfizetésben lévő összes virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="87066-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="87066-117">3. példa: metrikus figyelmeztetési szabály letiltása</span><span class="sxs-lookup"><span data-stu-id="87066-117">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="87066-118">Ez a parancs a metrika riasztási szabályait letiltja.</span><span class="sxs-lookup"><span data-stu-id="87066-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="87066-119">Itt dolgozunk a [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2) a [bővítmények AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span><span class="sxs-lookup"><span data-stu-id="87066-119">Here, we are piping output of [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2) to [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span></span> 

### <span data-ttu-id="87066-120">4. példa: metrikus figyelmeztetési szabály hozzáadása dimenziókkal</span><span class="sxs-lookup"><span data-stu-id="87066-120">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="87066-121">Ha összetettebb metrikus figyelmeztetési szabályt szeretne létrehozni, például a dimenzióértékek kijelölésével vagy több feltétel megadásával, használhatja a segítő parancsmagokat a [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) és a [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span><span class="sxs-lookup"><span data-stu-id="87066-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) and [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span></span>

<span data-ttu-id="87066-122">A fenti parancsmagok halmaza metrikus figyelmeztetési szabályt hoz létre a méretekkel.</span><span class="sxs-lookup"><span data-stu-id="87066-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="87066-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87066-123">PARAMETERS</span></span>

### <span data-ttu-id="87066-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="87066-124">-ActionGroup</span></span>
<span data-ttu-id="87066-125">A szabály műveleti csoportja</span><span class="sxs-lookup"><span data-stu-id="87066-125">The Action Group for rule</span></span>

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

### <span data-ttu-id="87066-126">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="87066-126">-ActionGroupId</span></span>
<span data-ttu-id="87066-127">A műveleti csoport azonosítója a szabályhoz</span><span class="sxs-lookup"><span data-stu-id="87066-127">The Action Group id for rule</span></span>

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

### <span data-ttu-id="87066-128">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="87066-128">-Condition</span></span>
<span data-ttu-id="87066-129">A szabály feltétele</span><span class="sxs-lookup"><span data-stu-id="87066-129">The condition for rule</span></span>

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

### <span data-ttu-id="87066-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87066-130">-DefaultProfile</span></span>
<span data-ttu-id="87066-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87066-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87066-132">-Leírás</span><span class="sxs-lookup"><span data-stu-id="87066-132">-Description</span></span>
<span data-ttu-id="87066-133">A metrikus figyelmeztetési szabály leírása</span><span class="sxs-lookup"><span data-stu-id="87066-133">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="87066-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="87066-134">-DisableRule</span></span>
<span data-ttu-id="87066-135">A szabály letiltása (állapot) jelző</span><span class="sxs-lookup"><span data-stu-id="87066-135">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="87066-136">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="87066-136">-Frequency</span></span>
<span data-ttu-id="87066-137">A szabály kiértékelésének gyakorisága</span><span class="sxs-lookup"><span data-stu-id="87066-137">The evaluation frequency for rule</span></span>

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

### <span data-ttu-id="87066-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87066-138">-Name</span></span>
<span data-ttu-id="87066-139">A metrikus figyelmeztetési szabály neve</span><span class="sxs-lookup"><span data-stu-id="87066-139">The name of metric alert rule</span></span>

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

### <span data-ttu-id="87066-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87066-140">-ResourceGroupName</span></span>
<span data-ttu-id="87066-141">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="87066-141">The Resource Group Name</span></span>

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

### <span data-ttu-id="87066-142">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="87066-142">-Severity</span></span>
<span data-ttu-id="87066-143">A metrika figyelmeztetési szabályának súlyossága</span><span class="sxs-lookup"><span data-stu-id="87066-143">The severity for the metric alert rule</span></span>

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

### <span data-ttu-id="87066-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="87066-144">-TargetResourceId</span></span>
<span data-ttu-id="87066-145">A cél erőforrás-azonosító a szabályhoz</span><span class="sxs-lookup"><span data-stu-id="87066-145">The target resource id for rule</span></span>

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

### <span data-ttu-id="87066-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="87066-146">-TargetResourceRegion</span></span>
<span data-ttu-id="87066-147">A cél erőforrás terület a szabályhoz</span><span class="sxs-lookup"><span data-stu-id="87066-147">The target resource region for rule</span></span>

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

### <span data-ttu-id="87066-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="87066-148">-TargetResourceScope</span></span>
<span data-ttu-id="87066-149">A cél erőforrás hatóköre a szabályhoz</span><span class="sxs-lookup"><span data-stu-id="87066-149">The target resource scope for rule</span></span>

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

### <span data-ttu-id="87066-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="87066-150">-TargetResourceType</span></span>
<span data-ttu-id="87066-151">A cél erőforrástípus a szabályhoz</span><span class="sxs-lookup"><span data-stu-id="87066-151">The target resource type for rule</span></span>

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

### <span data-ttu-id="87066-152">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="87066-152">-WindowSize</span></span>
<span data-ttu-id="87066-153">A szabály ablakának mérete</span><span class="sxs-lookup"><span data-stu-id="87066-153">The window size for rule</span></span>

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

### <span data-ttu-id="87066-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87066-154">-Confirm</span></span>
<span data-ttu-id="87066-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87066-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87066-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87066-156">-WhatIf</span></span>
<span data-ttu-id="87066-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87066-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87066-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87066-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87066-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87066-159">CommonParameters</span></span>
<span data-ttu-id="87066-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87066-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87066-161">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="87066-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87066-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87066-162">INPUTS</span></span>

### <span data-ttu-id="87066-163">System. String</span><span class="sxs-lookup"><span data-stu-id="87066-163">System.String</span></span>

### <span data-ttu-id="87066-164">System. időszak</span><span class="sxs-lookup"><span data-stu-id="87066-164">System.TimeSpan</span></span>

### <span data-ttu-id="87066-165">System. string []</span><span class="sxs-lookup"><span data-stu-id="87066-165">System.String[]</span></span>

### <span data-ttu-id="87066-166">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. OutputClasses. IPSMultiMetricCriteria, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="87066-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="87066-167">Microsoft. Azure. Management. monitor. models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="87066-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="87066-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87066-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="87066-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="87066-169">System.Int32</span></span>

## <span data-ttu-id="87066-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87066-170">OUTPUTS</span></span>

### <span data-ttu-id="87066-171">Microsoft. Azure. commands. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="87066-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="87066-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87066-172">NOTES</span></span>

## <span data-ttu-id="87066-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87066-173">RELATED LINKS</span></span>