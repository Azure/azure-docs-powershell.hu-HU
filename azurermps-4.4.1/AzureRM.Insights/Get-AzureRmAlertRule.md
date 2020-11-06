---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 65c5bc7a2767fd00497b487783c4e6f0ce6d6723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504932"
---
# Get-AzureRmAlertRule

## Áttekintés
Figyelmeztetési szabályokat kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Get-AzureRmAlertRule parancsmag paraméterei
```
Get-AzureRmAlertRule -ResourceGroup <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Get-AzureRmAlertRule parancsmag paraméterei név használatával
```
Get-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Get-AzureRmAlertRule parancsmag paraméterei a cél erőforrás URI azonosítóval
```
Get-AzureRmAlertRule -ResourceGroup <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmAlertRule** parancsmag az adott erőforráscsoport nevével vagy URI-ja, vagy az összes figyelmeztetési szabály alapján értesítést kap.

## Példák

### 1. példa: az erőforrás-csoportokra vonatkozó figyelmeztetési szabályok beszerzése
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

Ez a parancs a Default-Web-CentralUS nevű erőforráscsoport figyelmeztetési szabályait kapja meg.
A kimenet nem tartalmaz részleteket a szabályokról, mert a *DetailedOutput* paraméter nincs megadva.

### 2. példa: figyelmeztetési szabály kérése név alapján
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

Ez a parancs a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt kapja meg.
Mivel a *DetailedOutput* paraméter nincs megadva, a kimenet csak az értesítési szabályról tartalmaz alapvető információkat.

### 3. példa: figyelmeztetési szabály beszerzése név szerint részletes kimenettel
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

Ez a parancs a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt kapja meg.
A *DetailedOutput* paraméter meg van adva, így a kimenet részletezve van.

## PARAMÉTEREK

### -DetailedOutput
A kimenet minden részletét megjeleníti.

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

### -Name (név)
A beolvasott figyelmeztetési szabály nevét adja meg.

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Az erőforráscsoport nevét adja meg.

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

### -TargetResourceId
A cél erőforrás AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using target resource uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. detekintés. OutputClasses. PSManagementItemDescriptor]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[Add-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Add-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[Get-AzureRmAlertHistory](./Get-AzureRmAlertHistory.md)

[Remove-AzureRmAlertRule](./Remove-AzureRmAlertRule.md)


