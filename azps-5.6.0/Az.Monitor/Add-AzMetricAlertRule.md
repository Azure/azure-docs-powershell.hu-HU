---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: a38dbb3e608390369a31d9376923328d9550cbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932753"
---
# <span data-ttu-id="cef07-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="cef07-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="cef07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef07-102">SYNOPSIS</span></span>
<span data-ttu-id="cef07-103">Metrikus alapú riasztási szabályt ad hozzá vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="cef07-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="cef07-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cef07-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef07-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cef07-105">DESCRIPTION</span></span>
<span data-ttu-id="cef07-106">Az **Add-AzMetricAlertRule** parancsmag metrikus alapú riasztási szabályt ad hozzá vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="cef07-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="cef07-107">A hozzáadott szabály egy erőforráscsoporthoz van társítva, és neve is van.</span><span class="sxs-lookup"><span data-stu-id="cef07-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="cef07-108">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="cef07-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="cef07-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cef07-109">EXAMPLES</span></span>

### <span data-ttu-id="cef07-110">1. példa: Metrikus riasztási szabály hozzáadása webhelyhez</span><span class="sxs-lookup"><span data-stu-id="cef07-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="cef07-111">Ez a parancs metrikus riasztási szabályt hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="cef07-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="cef07-112">2. példa: Szabály letiltása</span><span class="sxs-lookup"><span data-stu-id="cef07-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="cef07-113">Ez a parancs letilt egy szabályt.</span><span class="sxs-lookup"><span data-stu-id="cef07-113">This command disables a rule.</span></span>
<span data-ttu-id="cef07-114">Ha a szabály nem létezik, letiltja azt.</span><span class="sxs-lookup"><span data-stu-id="cef07-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="cef07-115">Ha a szabály létezik, akkor egyszerűen letiltja.</span><span class="sxs-lookup"><span data-stu-id="cef07-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="cef07-116">3. példa: Szabály hozzáadása műveletekkel</span><span class="sxs-lookup"><span data-stu-id="cef07-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="cef07-117">Ez a parancs metrikus riasztási szabályt hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="cef07-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="cef07-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cef07-118">PARAMETERS</span></span>

### <span data-ttu-id="cef07-119">-Művelet</span><span class="sxs-lookup"><span data-stu-id="cef07-119">-Action</span></span>
<span data-ttu-id="cef07-120">A műveletek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cef07-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="cef07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef07-121">-DefaultProfile</span></span>
<span data-ttu-id="cef07-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cef07-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cef07-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="cef07-123">-Description</span></span>
<span data-ttu-id="cef07-124">Megadja a szabály leírását.</span><span class="sxs-lookup"><span data-stu-id="cef07-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="cef07-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="cef07-125">-DisableRule</span></span>
<span data-ttu-id="cef07-126">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="cef07-126">Disables the rule.</span></span>
<span data-ttu-id="cef07-127">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="cef07-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="cef07-128">-Location</span><span class="sxs-lookup"><span data-stu-id="cef07-128">-Location</span></span>
<span data-ttu-id="cef07-129">Megadja azt a helyet, ahol a szabály definiálva van.</span><span class="sxs-lookup"><span data-stu-id="cef07-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="cef07-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="cef07-130">-MetricName</span></span>
<span data-ttu-id="cef07-131">A szabály által figyelt metrikus neve.</span><span class="sxs-lookup"><span data-stu-id="cef07-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="cef07-132">Ezt a paramétert csak metrikus alapú szabályokhoz adja meg.</span><span class="sxs-lookup"><span data-stu-id="cef07-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="cef07-133">-Name</span><span class="sxs-lookup"><span data-stu-id="cef07-133">-Name</span></span>
<span data-ttu-id="cef07-134">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cef07-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="cef07-135">-Operátor</span><span class="sxs-lookup"><span data-stu-id="cef07-135">-Operator</span></span>
<span data-ttu-id="cef07-136">A szabály feltételének relációs operátorát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cef07-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="cef07-137">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="cef07-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cef07-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="cef07-138">GreaterThan</span></span>
- <span data-ttu-id="cef07-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="cef07-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="cef07-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="cef07-140">LessThan</span></span>
- <span data-ttu-id="cef07-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="cef07-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="cef07-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef07-142">-ResourceGroupName</span></span>
<span data-ttu-id="cef07-143">A szabály erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cef07-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="cef07-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="cef07-144">-TargetResourceId</span></span>
<span data-ttu-id="cef07-145">Annak az erőforrásnak az azonosítója, amit a szabály figyel.</span><span class="sxs-lookup"><span data-stu-id="cef07-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="cef07-146">MEGJEGYZÉS: Ez a tulajdonság nem frissíthető meglévő riasztási szabály esetén.</span><span class="sxs-lookup"><span data-stu-id="cef07-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="cef07-147">-Threshold</span><span class="sxs-lookup"><span data-stu-id="cef07-147">-Threshold</span></span>
<span data-ttu-id="cef07-148">A szabály küszöbértékét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cef07-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="cef07-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="cef07-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="cef07-150">Megadja azt az összegzési operátort, amely a szabály kiértékelése során az időablakra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="cef07-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="cef07-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="cef07-151">-WindowSize</span></span>
<span data-ttu-id="cef07-152">Megadja, hogy a szabály milyen időkeretet számolja ki az adatokkal.</span><span class="sxs-lookup"><span data-stu-id="cef07-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="cef07-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cef07-153">-Confirm</span></span>
<span data-ttu-id="cef07-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cef07-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef07-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef07-155">-WhatIf</span></span>
<span data-ttu-id="cef07-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cef07-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cef07-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cef07-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef07-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef07-158">CommonParameters</span></span>
<span data-ttu-id="cef07-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef07-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef07-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cef07-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef07-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cef07-161">INPUTS</span></span>

### <span data-ttu-id="cef07-162">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="cef07-162">System.TimeSpan</span></span>

### <span data-ttu-id="cef07-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="cef07-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="cef07-164">System.Double</span><span class="sxs-lookup"><span data-stu-id="cef07-164">System.Double</span></span>

### <span data-ttu-id="cef07-165">System.String</span><span class="sxs-lookup"><span data-stu-id="cef07-165">System.String</span></span>

### <span data-ttu-id="cef07-166">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="cef07-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cef07-167">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cef07-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="cef07-168">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="cef07-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cef07-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cef07-169">OUTPUTS</span></span>

### <span data-ttu-id="cef07-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cef07-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="cef07-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cef07-171">NOTES</span></span>

## <span data-ttu-id="cef07-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cef07-172">RELATED LINKS</span></span>

[<span data-ttu-id="cef07-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cef07-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="cef07-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="cef07-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="cef07-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="cef07-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="cef07-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="cef07-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="cef07-177">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="cef07-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="cef07-178">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="cef07-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="cef07-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="cef07-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


