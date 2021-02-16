---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: e7ba5bc42e08ce73fcfac5fcbb7ea614a43f2b3e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397883"
---
# New-AzAlertRuleEmail

## SYNOPSIS
E-mail műveletet hoz létre egy riasztási szabályhoz.

## SZINTAXIS

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzAlertRuleEmail** parancsmag létrehoz egy e-mail műveletet egy riasztási szabályhoz.

## PÉLDÁK

### 1. példa: Értesítési szabály e-mail-művelet létrehozása szolgáltatástulajdonosoknak
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

Ez a parancs egy riasztási szabály e-mail-műveletet hoz létre, és elküldi azt a szolgáltatástulajdonosoknak, ha riasztási szabály van beszabályzva.

### 2. példa: Értesítési szabály e-mail-művelet létrehozása nem szolgáltatástulajdonosoknak
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

Ez a parancs egy riasztási szabály e-mail-műveletet hoz létre a megadott e-mail-címekhez, de nem a szolgáltatástulajdonosokhoz.

### 3. példa: Értesítési szabály e-mail-művelet létrehozása szolgáltatástulajdonosoknak és nem szolgáltatástulajdonosoknak
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

Ez a parancs egy riasztási szabály e-mail-műveletet hoz létre a megadott címhez és a szolgáltatástulajdonosokhoz.

## PARAMETERS

### -CustomEmail
Vesszővel elválasztott e-mail-címek listáját adja meg.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -SendToServiceOwner
Azt jelzi, hogy ez a művelet e-mailt küld a szolgáltatástulajdonosoknak, amikor a szabály ki van tűzve.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String[]

### System.Management.Automation.SwitchParameter

## KIMENETEK

### Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK


[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


