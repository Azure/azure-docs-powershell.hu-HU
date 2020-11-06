---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: b4a1204d25852aa75c7b68c90305aefe9cfefe6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504943"
---
# Get-AzureRmActivityLogAlert

## Áttekintés
Egy vagy több tevékenység naplója riasztási erőforrást kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Az alapértelmezett paraméterek a tevékenység-naplózási riasztás beszerzéséhez
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Paraméterek, amelyekkel meggyőződhet arról, hogy a név megadásakor az erőforráscsoport meg van adva
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmActivityLogAlert** parancsmag egy vagy több tevékenység naplójának riasztási erőforrást kap.

## Példák

### Példa 1: műveletnapló értesítéseinek beszerzése előfizetés-AZONOSÍTÓval
```
PS C:\>Get-AzureRmActivityLogAlert
```

Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes tevékenység-naplózási értesítést.

### 2. példa: tevékenység-naplózási értesítések beszerzése az adott erőforráscsoport számára
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

Ez a parancs megjeleníti a műveletnapló riasztásait az adott erőforráscsoport számára.

### 3. példa: tevékenység-naplózási riasztás kérése
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

Ez a parancs egy (egyetlen elemmel rendelkező) tevékenység-naplózási riasztást sorol fel.

## PARAMÉTEREK

### -Name (név)
A műveletnapló riasztásának neve.

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.
Ha a név nem null vagy üres, a paraméternek tartalmaznia kell és nem üres karakterláncot.

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to make sure the resource group is given when the name is given
Aliases: 

Required: False
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

### Nincs

## KIMENETEK

### <System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. detekintést. OutputClasses. PSActivityLogAlertResource]

### Nincs

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureRmActivityLogAlert](./Set-AzureRmActivityLogAlert.md)

[Update-AzureRmActivityLogAlert](./Update-AzureRmActivityLogAlert.md)

[Remove-AzureRmActivityLogAlert](./Remove-AzureRmActivityLogAlert.md)

[Új – AzureRmActionGroup](./New-AzureRmActionGroup.md)

[Új – AzureRmActivityLogAlertCondition](./Get-AzureRmActivityLogAlertCondition.md)
