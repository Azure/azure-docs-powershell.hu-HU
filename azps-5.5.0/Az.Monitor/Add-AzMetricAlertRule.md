---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: cb3669c955182e54b6ddd3623f732402a15ea906
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147427"
---
# <span data-ttu-id="b5cf2-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5cf2-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="b5cf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="b5cf2-103">Metrikus alapú riasztási szabályt ad hozzá vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="b5cf2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5cf2-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5cf2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="b5cf2-106">Az **Add-AzMetricAlertRule** parancsmag metrikus alapú riasztási szabályt ad hozzá vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="b5cf2-107">A hozzáadott szabály egy erőforráscsoporthoz van társítva, és neve is van.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="b5cf2-108">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b5cf2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5cf2-109">EXAMPLES</span></span>

### <span data-ttu-id="b5cf2-110">1. példa: Metrikus riasztási szabály hozzáadása webhelyhez</span><span class="sxs-lookup"><span data-stu-id="b5cf2-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="b5cf2-111">Ez a parancs metrikus riasztási szabályt hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="b5cf2-112">2. példa: Szabály letiltása</span><span class="sxs-lookup"><span data-stu-id="b5cf2-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="b5cf2-113">Ez a parancs letilt egy szabályt.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-113">This command disables a rule.</span></span>
<span data-ttu-id="b5cf2-114">Ha a szabály nem létezik, letiltja azt.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="b5cf2-115">Ha a szabály létezik, akkor egyszerűen letiltja.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="b5cf2-116">3. példa: Szabály hozzáadása műveletekkel</span><span class="sxs-lookup"><span data-stu-id="b5cf2-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="b5cf2-117">Ez a parancs metrikus riasztási szabályt hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="b5cf2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5cf2-118">PARAMETERS</span></span>

### <span data-ttu-id="b5cf2-119">-Action</span><span class="sxs-lookup"><span data-stu-id="b5cf2-119">-Action</span></span>
<span data-ttu-id="b5cf2-120">Vesszővel elválasztott műveletlistát ad meg.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5cf2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5cf2-121">-DefaultProfile</span></span>
<span data-ttu-id="b5cf2-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5cf2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5cf2-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b5cf2-123">-Description</span></span>
<span data-ttu-id="b5cf2-124">Megadja a szabály leírását.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="b5cf2-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="b5cf2-125">-DisableRule</span></span>
<span data-ttu-id="b5cf2-126">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-126">Disables the rule.</span></span>
<span data-ttu-id="b5cf2-127">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="b5cf2-128">-Location</span><span class="sxs-lookup"><span data-stu-id="b5cf2-128">-Location</span></span>
<span data-ttu-id="b5cf2-129">Azt a helyet adja meg, ahol a szabály definiálva van.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="b5cf2-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="b5cf2-130">-MetricName</span></span>
<span data-ttu-id="b5cf2-131">A szabály által figyelt metrikus neve.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="b5cf2-132">Ezt a paramétert csak metrikus alapú szabályokhoz adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="b5cf2-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b5cf2-133">-Name</span></span>
<span data-ttu-id="b5cf2-134">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="b5cf2-135">-Operátor</span><span class="sxs-lookup"><span data-stu-id="b5cf2-135">-Operator</span></span>
<span data-ttu-id="b5cf2-136">A szabály feltételének relációs operátorát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="b5cf2-137">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="b5cf2-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b5cf2-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="b5cf2-138">GreaterThan</span></span>
- <span data-ttu-id="b5cf2-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="b5cf2-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="b5cf2-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="b5cf2-140">LessThan</span></span>
- <span data-ttu-id="b5cf2-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="b5cf2-141">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5cf2-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5cf2-142">-ResourceGroupName</span></span>
<span data-ttu-id="b5cf2-143">A szabály erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="b5cf2-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b5cf2-144">-TargetResourceId</span></span>
<span data-ttu-id="b5cf2-145">Annak az erőforrásnak az azonosítója, amit a szabály figyel.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="b5cf2-146">MEGJEGYZÉS: Ez a tulajdonság nem frissíthető meglévő riasztási szabály esetén.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="b5cf2-147">-Threshold</span><span class="sxs-lookup"><span data-stu-id="b5cf2-147">-Threshold</span></span>
<span data-ttu-id="b5cf2-148">A szabály küszöbértékét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5cf2-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="b5cf2-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="b5cf2-150">Megadja azt az összegzési operátort, amely a szabály kiértékelése során az időablakra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5cf2-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="b5cf2-151">-WindowSize</span></span>
<span data-ttu-id="b5cf2-152">Megadja, hogy a szabály milyen időkeretet számolja ki az adatokkal.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="b5cf2-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5cf2-153">-Confirm</span></span>
<span data-ttu-id="b5cf2-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5cf2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5cf2-155">-WhatIf</span></span>
<span data-ttu-id="b5cf2-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5cf2-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5cf2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5cf2-158">CommonParameters</span></span>
<span data-ttu-id="b5cf2-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5cf2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5cf2-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5cf2-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5cf2-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5cf2-161">INPUTS</span></span>

### <span data-ttu-id="b5cf2-162">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="b5cf2-162">System.TimeSpan</span></span>

### <span data-ttu-id="b5cf2-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="b5cf2-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="b5cf2-164">System.Double</span><span class="sxs-lookup"><span data-stu-id="b5cf2-164">System.Double</span></span>

### <span data-ttu-id="b5cf2-165">System.String</span><span class="sxs-lookup"><span data-stu-id="b5cf2-165">System.String</span></span>

### <span data-ttu-id="b5cf2-166">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b5cf2-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b5cf2-167">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b5cf2-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b5cf2-168">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b5cf2-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b5cf2-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5cf2-169">OUTPUTS</span></span>

### <span data-ttu-id="b5cf2-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b5cf2-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="b5cf2-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5cf2-171">NOTES</span></span>

## <span data-ttu-id="b5cf2-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5cf2-172">RELATED LINKS</span></span>

[<span data-ttu-id="b5cf2-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b5cf2-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="b5cf2-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5cf2-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="b5cf2-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b5cf2-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="b5cf2-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5cf2-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="b5cf2-177">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="b5cf2-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="b5cf2-178">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="b5cf2-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="b5cf2-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5cf2-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


