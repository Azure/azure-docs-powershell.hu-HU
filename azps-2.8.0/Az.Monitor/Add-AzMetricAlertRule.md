---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: 2ab8c489906ff48e15db24c2ff50511ee77bd29d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665874"
---
# <span data-ttu-id="05529-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="05529-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="05529-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05529-102">SYNOPSIS</span></span>
<span data-ttu-id="05529-103">Metrika-alapú figyelmeztetési szabály hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="05529-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="05529-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05529-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05529-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05529-105">DESCRIPTION</span></span>
<span data-ttu-id="05529-106">A **Add-AzMetricAlertRule** parancsmag metrikus-alapú figyelmeztetési szabályt ad hozzá vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="05529-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="05529-107">A hozzáadott szabály erőforrás-csoporthoz van társítva, és nevet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="05529-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="05529-108">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="05529-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="05529-109">Példák</span><span class="sxs-lookup"><span data-stu-id="05529-109">EXAMPLES</span></span>

### <span data-ttu-id="05529-110">Példa 1: metrikus figyelmeztetési szabály hozzáadása webhelyhez</span><span class="sxs-lookup"><span data-stu-id="05529-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="05529-111">Ez a parancs metrikus figyelmeztetési szabályt hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="05529-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="05529-112">2. példa: szabály letiltása</span><span class="sxs-lookup"><span data-stu-id="05529-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="05529-113">Ez a parancs letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="05529-113">This command disables a rule.</span></span>
<span data-ttu-id="05529-114">Ha a szabály nem létezik, akkor az a letiltott állapotot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="05529-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="05529-115">Ha a szabály létezik, akkor az csak letiltja.</span><span class="sxs-lookup"><span data-stu-id="05529-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="05529-116">3. példa: szabály felvétele műveletekkel</span><span class="sxs-lookup"><span data-stu-id="05529-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="05529-117">Ez a parancs metrikus figyelmeztetési szabályt hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="05529-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="05529-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05529-118">PARAMETERS</span></span>

### <span data-ttu-id="05529-119">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="05529-119">-Action</span></span>
<span data-ttu-id="05529-120">A műveletek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="05529-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="05529-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05529-121">-DefaultProfile</span></span>
<span data-ttu-id="05529-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="05529-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05529-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="05529-123">-Description</span></span>
<span data-ttu-id="05529-124">A szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="05529-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="05529-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="05529-125">-DisableRule</span></span>
<span data-ttu-id="05529-126">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="05529-126">Disables the rule.</span></span>
<span data-ttu-id="05529-127">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="05529-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="05529-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="05529-128">-Location</span></span>
<span data-ttu-id="05529-129">A szabály helyének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="05529-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="05529-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="05529-130">-MetricName</span></span>
<span data-ttu-id="05529-131">Annak a metrikának a nevét adja meg, amelyre a szabály figyel.</span><span class="sxs-lookup"><span data-stu-id="05529-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="05529-132">Csak metrikus alapú szabályok esetén adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="05529-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="05529-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05529-133">-Name</span></span>
<span data-ttu-id="05529-134">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05529-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="05529-135">-Operátor</span><span class="sxs-lookup"><span data-stu-id="05529-135">-Operator</span></span>
<span data-ttu-id="05529-136">A szabály feltételéhez tartozó relációs operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="05529-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="05529-137">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="05529-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="05529-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="05529-138">GreaterThan</span></span>
- <span data-ttu-id="05529-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="05529-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="05529-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="05529-140">LessThan</span></span>
- <span data-ttu-id="05529-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="05529-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="05529-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05529-142">-ResourceGroupName</span></span>
<span data-ttu-id="05529-143">A szabály erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05529-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="05529-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="05529-144">-TargetResourceId</span></span>
<span data-ttu-id="05529-145">A szabály által figyelt erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="05529-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="05529-146">Megjegyzés: Ez a tulajdonság nem frissíthető egy meglévő figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="05529-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="05529-147">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="05529-147">-Threshold</span></span>
<span data-ttu-id="05529-148">A szabály küszöbét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05529-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="05529-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="05529-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="05529-150">A szabály értékelése során az időablakra érvényes összesítési operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="05529-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="05529-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="05529-151">-WindowSize</span></span>
<span data-ttu-id="05529-152">A szabály időablakának méretét adja meg az adatainak számításához.</span><span class="sxs-lookup"><span data-stu-id="05529-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="05529-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="05529-153">-Confirm</span></span>
<span data-ttu-id="05529-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="05529-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05529-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05529-155">-WhatIf</span></span>
<span data-ttu-id="05529-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="05529-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05529-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05529-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05529-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05529-158">CommonParameters</span></span>
<span data-ttu-id="05529-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05529-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05529-160">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="05529-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05529-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05529-161">INPUTS</span></span>

### <span data-ttu-id="05529-162">System. időszak</span><span class="sxs-lookup"><span data-stu-id="05529-162">System.TimeSpan</span></span>

### <span data-ttu-id="05529-163">Microsoft. Azure. Management. monitor. Management. models. ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="05529-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="05529-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="05529-164">System.Double</span></span>

### <span data-ttu-id="05529-165">System. String</span><span class="sxs-lookup"><span data-stu-id="05529-165">System.String</span></span>

### <span data-ttu-id="05529-166">System. null ' 1 [[Microsoft. Azure. Management. monitor. Management. models. TimeAggregationOperator, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="05529-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="05529-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="05529-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="05529-168">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. models. RuleAction, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="05529-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="05529-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05529-169">OUTPUTS</span></span>

### <span data-ttu-id="05529-170">Microsoft. Azure. commands. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="05529-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="05529-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05529-171">NOTES</span></span>

## <span data-ttu-id="05529-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05529-172">RELATED LINKS</span></span>

[<span data-ttu-id="05529-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="05529-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="05529-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="05529-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="05529-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="05529-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="05529-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="05529-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="05529-177">Új – AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="05529-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="05529-178">Új – AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="05529-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="05529-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="05529-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


