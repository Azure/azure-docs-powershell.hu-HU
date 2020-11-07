---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680541"
---
# <span data-ttu-id="2b1f7-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2b1f7-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="2b1f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1f7-103">Metrika-alapú figyelmeztetési szabály hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="2b1f7-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b1f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b1f7-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b1f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b1f7-105">DESCRIPTION</span></span>
<span data-ttu-id="2b1f7-106">A **Add-AzureRmMetricAlertRule** parancsmag metrikus-alapú figyelmeztetési szabályt ad hozzá vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="2b1f7-107">A hozzáadott szabály erőforrás-csoporthoz van társítva, és nevet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-107">The added rule is associated with a resource group and has a name.</span></span>

## <span data-ttu-id="2b1f7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2b1f7-108">EXAMPLES</span></span>

### <span data-ttu-id="2b1f7-109">Példa 1: metrikus figyelmeztetési szabály hozzáadása webhelyhez</span><span class="sxs-lookup"><span data-stu-id="2b1f7-109">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="2b1f7-110">Ez a parancs metrikus figyelmeztetési szabályt hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-110">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="2b1f7-111">2. példa: szabály letiltása</span><span class="sxs-lookup"><span data-stu-id="2b1f7-111">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="2b1f7-112">Ez a parancs letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-112">This command disables a rule.</span></span>
<span data-ttu-id="2b1f7-113">Ha a szabály nem létezik, akkor az a letiltott állapotot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-113">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="2b1f7-114">Ha a szabály létezik, akkor az csak letiltja.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-114">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="2b1f7-115">3. példa: szabály felvétele műveletekkel</span><span class="sxs-lookup"><span data-stu-id="2b1f7-115">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="2b1f7-116">Ez a parancs metrikus figyelmeztetési szabályt hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-116">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="2b1f7-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b1f7-117">PARAMETERS</span></span>

### <span data-ttu-id="2b1f7-118">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="2b1f7-118">-Actions</span></span>
<span data-ttu-id="2b1f7-119">A műveletek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-119">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="2b1f7-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="2b1f7-120">-Description</span></span>
<span data-ttu-id="2b1f7-121">A szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-121">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="2b1f7-122">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="2b1f7-122">-DisableRule</span></span>
<span data-ttu-id="2b1f7-123">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-123">Disables the rule.</span></span>
<span data-ttu-id="2b1f7-124">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-124">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="2b1f7-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="2b1f7-125">-Location</span></span>
<span data-ttu-id="2b1f7-126">A szabály helyének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="2b1f7-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="2b1f7-127">-MetricName</span></span>
<span data-ttu-id="2b1f7-128">Annak a metrikának a nevét adja meg, amelyre a szabály figyel.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-128">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="2b1f7-129">Csak metrikus alapú szabályok esetén adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-129">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="2b1f7-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b1f7-130">-Name</span></span>
<span data-ttu-id="2b1f7-131">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-131">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="2b1f7-132">-Operátor</span><span class="sxs-lookup"><span data-stu-id="2b1f7-132">-Operator</span></span>
<span data-ttu-id="2b1f7-133">A szabály feltételéhez tartozó relációs operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-133">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="2b1f7-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2b1f7-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b1f7-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="2b1f7-135">GreaterThan</span></span>
- <span data-ttu-id="2b1f7-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="2b1f7-136">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="2b1f7-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="2b1f7-137">LessThan</span></span>
- <span data-ttu-id="2b1f7-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="2b1f7-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="2b1f7-139">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b1f7-139">-ResourceGroup</span></span>
<span data-ttu-id="2b1f7-140">A szabály erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-140">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="2b1f7-141">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2b1f7-141">-TargetResourceId</span></span>
<span data-ttu-id="2b1f7-142">A szabály által figyelt erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-142">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="2b1f7-143">Megjegyzés: Ez a tulajdonság nem frissíthető egy meglévő figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-143">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="2b1f7-144">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="2b1f7-144">-Threshold</span></span>
<span data-ttu-id="2b1f7-145">A szabály küszöbét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-145">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="2b1f7-146">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="2b1f7-146">-TimeAggregationOperator</span></span>
<span data-ttu-id="2b1f7-147">A szabály értékelése során az időablakra érvényes összesítési operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-147">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="2b1f7-148">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="2b1f7-148">-WindowSize</span></span>
<span data-ttu-id="2b1f7-149">A szabály időablakának méretét adja meg az adatainak számításához.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-149">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="2b1f7-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1f7-150">-DefaultProfile</span></span>
<span data-ttu-id="2b1f7-151">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b1f7-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1f7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1f7-152">CommonParameters</span></span>
<span data-ttu-id="2b1f7-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b1f7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1f7-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b1f7-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1f7-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b1f7-155">INPUTS</span></span>

## <span data-ttu-id="2b1f7-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b1f7-156">OUTPUTS</span></span>

### <span data-ttu-id="2b1f7-157">Microsoft. Azure. commands. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2b1f7-157">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="2b1f7-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b1f7-158">NOTES</span></span>

## <span data-ttu-id="2b1f7-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b1f7-159">RELATED LINKS</span></span>

[<span data-ttu-id="2b1f7-160">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="2b1f7-160">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="2b1f7-161">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2b1f7-161">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="2b1f7-162">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="2b1f7-162">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="2b1f7-163">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="2b1f7-163">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="2b1f7-164">Új – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="2b1f7-164">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="2b1f7-165">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="2b1f7-165">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="2b1f7-166">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="2b1f7-166">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


