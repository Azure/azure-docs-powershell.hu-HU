---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 90bd9c7943e6e788d81f8ddec85513676afade23
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183485"
---
# Get-AzActionGroup

## Áttekintés
A műveleti csoport (ok) beolvasása

## SZINTAXISA

### BySubscriptionOrResourceGroup (alapértelmezett)
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzActionGroup** parancsmag egy vagy több műveleti csoportot kap.

## Példák

### 1. példa: műveletkérő csoport beszerzése előfizetés-AZONOSÍTÓval
```
PS C:\>Get-AzActionGroup
```

Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes Művelettípus-csoportot.

### 2. példa: az adott erőforráscsoport műveleti csoportjainak beolvasása
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

Ez a parancs megjeleníti a megadott erőforráscsoport műveleti csoportját.

### 3. példa: művelet csoportjának beszerzése
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

Ez a parancs egy (egyetlen elemből álló) műveleti csoporttal sorolja fel a listát.

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
A műveleti csoport neve.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. commands. OutputClasses. PSActionGroupResource

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Új – AzActionGroupReceiver](./New-AzActionGroupReceiver.md)
