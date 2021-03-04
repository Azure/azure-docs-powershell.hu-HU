---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: a69297afe49bb7cda0abc95cf97b371e04cac0ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924818"
---
# Remove-AzActivityLogAlert

## SYNOPSIS
Eltávolít egy tevékenységnapló-riasztást.

## SZINTAXIS

### RemoveByNameAndResourceGroup
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByInputObject
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceId
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzActivityLogAlert** parancsmag eltávolítja a tevékenységnapló-riasztást.
Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen javítja az erőforrást.
Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.

## PÉLDÁK

### 1. példa: Tevékenységnapló-riasztás eltávolítása
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

Eltávolít egy tevékenységnapló-riasztást, amely bemenetként a név és az erőforráscsoport nevét használja.

### 2. példa: Tevékenységnapló-riasztás eltávolítása a PSActivityLogAlertResource használatával bemenetként
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

Tevékenységnapló-riasztás eltávolítása a PSActivityLogAlertResource beviteli mező használatával.

### 3. példa: A ActivityLogAlert eltávolítása a ResourceId paraméterrel
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

Ez a parancs eltávolítja a ActivityLogAlert paramétert az Erőforrásazonosító paraméter használatával a pipe-ból.

## PARAMETERS

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

### -InputObject
Beállítja a hívás InputObject tags tulajdonságát a szükséges név és az erőforráscsoport nevének tulajdonságainak kibontása érdekében.

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A tevékenységnapló-riasztás neve.

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a neve, amelyben a riasztási erőforrás létezik.

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Beállítja a hívás ResourceId tags tulajdonságát a szükséges név, az erőforráscsoport nevének tulajdonságainak kibontása érdekében.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource

## KIMENETEK

### Microsoft.Azure.AzureOperationResponse

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Enable-AzActivityLogAlert](./Enable-AzActivityLogAlert.md)

[Disable-AzActivityLogAlert](./Disable-AzActivityLogAlert.md)

[Set-AzActivityLogAlert](./Set-AzActivityLogAlert.md)

[Get-AzActivityLogAlert](./Get-AzActivityLogAlert.md)

[New-AzActionGroup](./New-AzActionGroup.md)

[New-AzActivityLogAlertCondition](./New-AzActivityLogAlertCondition.md)

