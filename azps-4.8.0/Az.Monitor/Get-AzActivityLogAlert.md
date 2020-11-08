---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 030564f700f399b1880d36e4dac628a9fc3efa35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184445"
---
# Get-AzActivityLogAlert

## Áttekintés
Egy vagy több tevékenység naplója riasztási erőforrást kap.

## SZINTAXISA

### GetByNameAndResourceGroup
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzActivityLogAlert** parancsmag egy vagy több tevékenység naplójának riasztási erőforrást kap.

## Példák

### Példa 1: műveletnapló értesítéseinek beszerzése előfizetés-AZONOSÍTÓval
```
PS C:\>Get-AzActivityLogAlert
```

Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes tevékenység-naplózási értesítést.

### 2. példa: tevékenység-naplózási értesítések beszerzése az adott erőforráscsoport számára
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

Ez a parancs megjeleníti a műveletnapló riasztásait az adott erőforráscsoport számára.

### 3. példa: tevékenység-naplózási riasztás kérése
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

Ez a parancs egy (egyetlen elemmel rendelkező) tevékenység-naplózási riasztást sorol fel.

## PARAMÉTEREK

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

### -Name (név)
A műveletnapló riasztásának neve.

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.
Ha a név nem null vagy üres, a paraméternek tartalmaznia kell és nem üres karakterláncot.

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzActivityLogAlert](./Set-AzActivityLogAlert.md)

[Update-AzActivityLogAlert](./Update-AzActivityLogAlert.md)

[Remove-AzActivityLogAlert](./Remove-AzActivityLogAlert.md)

[Új – AzActionGroup](./New-AzActionGroup.md)

[Új – AzActivityLogAlertCondition](./New-AzActivityLogAlertCondition.md)
