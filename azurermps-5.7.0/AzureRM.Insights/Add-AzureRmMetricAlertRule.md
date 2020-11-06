---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 097f3562ca326275c050054fd07d11d349cf98d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495351"
---
# <span data-ttu-id="2bf96-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2bf96-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="2bf96-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2bf96-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf96-103">Metrika-alapú figyelmeztetési szabály hozzáadása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="2bf96-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bf96-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2bf96-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bf96-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2bf96-105">DESCRIPTION</span></span>
<span data-ttu-id="2bf96-106">A **Add-AzureRmMetricAlertRule** parancsmag metrikus-alapú figyelmeztetési szabályt ad hozzá vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="2bf96-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="2bf96-107">A hozzáadott szabály erőforrás-csoporthoz van társítva, és nevet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="2bf96-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="2bf96-108">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="2bf96-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2bf96-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2bf96-109">EXAMPLES</span></span>

### <span data-ttu-id="2bf96-110">Példa 1: metrikus figyelmeztetési szabály hozzáadása webhelyhez</span><span class="sxs-lookup"><span data-stu-id="2bf96-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="2bf96-111">Ez a parancs metrikus figyelmeztetési szabályt hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="2bf96-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="2bf96-112">2. példa: szabály letiltása</span><span class="sxs-lookup"><span data-stu-id="2bf96-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="2bf96-113">Ez a parancs letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="2bf96-113">This command disables a rule.</span></span>
<span data-ttu-id="2bf96-114">Ha a szabály nem létezik, akkor az a letiltott állapotot hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2bf96-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="2bf96-115">Ha a szabály létezik, akkor az csak letiltja.</span><span class="sxs-lookup"><span data-stu-id="2bf96-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="2bf96-116">3. példa: szabály felvétele műveletekkel</span><span class="sxs-lookup"><span data-stu-id="2bf96-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="2bf96-117">Ez a parancs metrikus figyelmeztetési szabályt hoz létre egy webhelyhez.</span><span class="sxs-lookup"><span data-stu-id="2bf96-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="2bf96-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2bf96-118">PARAMETERS</span></span>

### <span data-ttu-id="2bf96-119">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="2bf96-119">-Action</span></span>
<span data-ttu-id="2bf96-120">A műveletek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bf96-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf96-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf96-121">-DefaultProfile</span></span>
<span data-ttu-id="2bf96-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2bf96-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf96-123">-Leírás</span><span class="sxs-lookup"><span data-stu-id="2bf96-123">-Description</span></span>
<span data-ttu-id="2bf96-124">A szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bf96-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="2bf96-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="2bf96-125">-DisableRule</span></span>
<span data-ttu-id="2bf96-126">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="2bf96-126">Disables the rule.</span></span>
<span data-ttu-id="2bf96-127">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2bf96-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="2bf96-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="2bf96-128">-Location</span></span>
<span data-ttu-id="2bf96-129">A szabály helyének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="2bf96-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="2bf96-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="2bf96-130">-MetricName</span></span>
<span data-ttu-id="2bf96-131">Annak a metrikának a nevét adja meg, amelyre a szabály figyel.</span><span class="sxs-lookup"><span data-stu-id="2bf96-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="2bf96-132">Csak metrikus alapú szabályok esetén adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="2bf96-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="2bf96-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2bf96-133">-Name</span></span>
<span data-ttu-id="2bf96-134">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bf96-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="2bf96-135">-Operátor</span><span class="sxs-lookup"><span data-stu-id="2bf96-135">-Operator</span></span>
<span data-ttu-id="2bf96-136">A szabály feltételéhez tartozó relációs operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bf96-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="2bf96-137">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2bf96-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2bf96-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="2bf96-138">GreaterThan</span></span>
- <span data-ttu-id="2bf96-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="2bf96-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="2bf96-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="2bf96-140">LessThan</span></span>
- <span data-ttu-id="2bf96-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="2bf96-141">LessThanOrEqual</span></span>

```yaml
Type: ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf96-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bf96-142">-ResourceGroupName</span></span>
<span data-ttu-id="2bf96-143">A szabály erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bf96-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="2bf96-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2bf96-144">-TargetResourceId</span></span>
<span data-ttu-id="2bf96-145">A szabály által figyelt erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bf96-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="2bf96-146">Megjegyzés: Ez a tulajdonság nem frissíthető egy meglévő figyelmeztetési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="2bf96-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="2bf96-147">-Küszöb</span><span class="sxs-lookup"><span data-stu-id="2bf96-147">-Threshold</span></span>
<span data-ttu-id="2bf96-148">A szabály küszöbét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bf96-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf96-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="2bf96-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="2bf96-150">A szabály értékelése során az időablakra érvényes összesítési operátort adja meg.</span><span class="sxs-lookup"><span data-stu-id="2bf96-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: TimeAggregationOperator
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf96-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="2bf96-151">-WindowSize</span></span>
<span data-ttu-id="2bf96-152">A szabály időablakának méretét adja meg az adatainak számításához.</span><span class="sxs-lookup"><span data-stu-id="2bf96-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="2bf96-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf96-153">CommonParameters</span></span>
<span data-ttu-id="2bf96-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2bf96-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf96-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bf96-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf96-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bf96-156">INPUTS</span></span>

### <span data-ttu-id="2bf96-157">Nincs</span><span class="sxs-lookup"><span data-stu-id="2bf96-157">None</span></span>
<span data-ttu-id="2bf96-158">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2bf96-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2bf96-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bf96-159">OUTPUTS</span></span>

### <span data-ttu-id="2bf96-160">Microsoft. Azure. commands. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2bf96-160">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="2bf96-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2bf96-161">NOTES</span></span>

## <span data-ttu-id="2bf96-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2bf96-162">RELATED LINKS</span></span>

[<span data-ttu-id="2bf96-163">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2bf96-163">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2bf96-164">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2bf96-164">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="2bf96-165">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="2bf96-165">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="2bf96-166">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="2bf96-166">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="2bf96-167">Új – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="2bf96-167">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="2bf96-168">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="2bf96-168">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="2bf96-169">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="2bf96-169">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


