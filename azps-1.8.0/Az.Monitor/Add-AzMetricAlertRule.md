---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: ed5649ead1c0e043ed3d97cb957d6b405967f450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835134"
---
# Add-AzMetricAlertRule

## Áttekintés
Metrika-alapú figyelmeztetési szabály hozzáadása vagy frissítése

## SZINTAXISA

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Add-AzMetricAlertRule** parancsmag metrikus-alapú figyelmeztetési szabályt ad hozzá vagy frissít.
A hozzáadott szabály erőforrás-csoporthoz van társítva, és nevet tartalmaz.
Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.

## Példák

### Példa 1: metrikus figyelmeztetési szabály hozzáadása webhelyhez
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

Ez a parancs metrikus figyelmeztetési szabályt hoz létre egy webhelyhez.

### 2. példa: szabály letiltása
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

Ez a parancs letiltja a szabályt.
Ha a szabály nem létezik, akkor az a letiltott állapotot hozza létre.
Ha a szabály létezik, akkor az csak letiltja.

### 3. példa: szabály felvétele műveletekkel
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

Ez a parancs metrikus figyelmeztetési szabályt hoz létre egy webhelyhez.

## PARAMÉTEREK

### -Műveletek
A műveletek vesszővel elválasztott listáját adja meg.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Leírás
A szabály leírását adja meg.

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

### -DisableRule
Letiltja a szabályt.
Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.

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

### -Hely
A szabály helyének meghatározása.

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

### -MetricName
Annak a metrikának a nevét adja meg, amelyre a szabály figyel.
Csak metrikus alapú szabályok esetén adja meg ezt a paramétert.

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

### -Name (név)
A szabály nevét adja meg.

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

### -Operátor
A szabály feltételéhez tartozó relációs operátort adja meg.
A paraméter elfogadható értékei a következők:
- GreaterThan
- GreaterThanOrEqual
-  LessThan
- LessThanOrEqual

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

### -ResourceGroupName
A szabály erőforráscsoport-csoportjának nevét adja meg.

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

### -TargetResourceId
A szabály által figyelt erőforrás AZONOSÍTÓját adja meg. Megjegyzés: Ez a tulajdonság nem frissíthető egy meglévő figyelmeztetési szabályhoz.

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

### -Küszöb
A szabály küszöbét adja meg.

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

### -TimeAggregationOperator
A szabály értékelése során az időablakra érvényes összesítési operátort adja meg.

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

### -WindowSize
A szabály időablakának méretét adja meg az adatainak számításához.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. időszak

### Microsoft. Azure. Management. monitor. Management. models. ConditionOperator

### System. Double

### System. String

### System. null ' 1 [[Microsoft. Azure. Management. monitor. Management. models. TimeAggregationOperator, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]

### System. Management. Automation. SwitchParameter

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. models. RuleAction, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]

## KIMENETEK

### Microsoft. Azure. commands. OutputClasses. PSAddAlertRuleOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzActivityLogAlert](./Set-AzActivityLogAlert.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[Get-AzAlertHistory](./Get-AzAlertHistory.md)

[Get-AzAlertRule](./Get-AzAlertRule.md)

[Új – AzAlertRuleEmail](./New-AzAlertRuleEmail.md)

[Új – AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)

[Remove-AzAlertRule](./Remove-AzAlertRule.md)


