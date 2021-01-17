---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479065"
---
# Sync-AzAnalysisServicesInstance

## SYNOPSIS

Szinkronizál egy megadott adatbázist az Analysis Services-kiszolgáló adott példányában az aktuálisan naplózott környezet összes lekérdezési méretkorlátpéldányával a Add-AzAnalysisServicesAccount parancsban megadottak szerint

## SZINTAXIS

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS

A Sync-AzAnalysisServicesInstance parancsmag szinkronizálja az Analysis Services-kiszolgáló adott példányában lévő megadott adatbázist az aktuálisan bejelentkezett környezet összes lekérdezési méretkorlátpéldányával, az Add-AzAnalysisServicesAccount parancsban megadottak szerint.

## PÉLDÁK

### 1. példa

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

Ez a parancs szinkronizálja a "contoso" nevű kiszolgáló SalesOrders nevű adatbázisát westus.asazure.windows.net feltéve, hogy a felhasználó bejelentkezett ebbe a környezetbe egy Add-AzAnalysisServicesAccount paranccsal.

## PARAMETERS

### -Database

A szinkronizálni kíván adatbázis identitása

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Instance

Az újraindítani szükséges Analysis Services-kiszolgálói példány neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails

## MEGJEGYZÉSEK

Alias: Sync-AzAsInstance

## KAPCSOLÓDÓ HIVATKOZÁSOK
