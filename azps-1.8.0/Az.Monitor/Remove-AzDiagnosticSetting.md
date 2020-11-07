---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f99a7cfb18b585e1187cac62eb586bac37dad55d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670795"
---
# Remove-AzDiagnosticSetting

## Áttekintés
Diagnosztikai beállítás eltávolítása az erőforráshoz.

## SZINTAXISA

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzDiagnosticSetting** parancsmag eltávolítja az adott erőforrás diagnosztikai beállítását.
Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.

## Példák

### 1. példa: az alapértelmezett diagnosztikai beállítás (szolgáltatás) eltávolítása egy erőforráshoz
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

Ez a parancs eltávolítja a Resource01 nevű erőforrás alapértelmezett diagnosztikai beállítását (szolgáltatást).

### 2. példa: az alapértelmezett diagnosztikai beállítás eltávolítása egy erőforrás megadott nevével
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

Ez a parancs eltávolítja a myDiagSetting nevű diagnosztikai beállítást az Resource01 nevű erőforráshoz.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
A diagnosztikai beállítás neve. Ha nem adja meg a "szolgáltatás" hívás alapértelmezett hívását a korábbi API-ban, és ez a parancsmag csak a metrikák/naplók minden kategóriáját letiltja.

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

### -ResourceId
Az erőforrás AZONOSÍTÓját adja meg.

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

### System. String

## KIMENETEK

### Microsoft. Azure. AzureOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
