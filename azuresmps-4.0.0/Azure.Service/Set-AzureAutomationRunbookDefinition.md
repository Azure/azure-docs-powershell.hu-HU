---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016070"
---
# Set-AzureAutomationRunbookDefinition

## Áttekintés

Frissíti a runbook vázlat definícióját.

## SZINTAXISA

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

A **set-AzureAutomationRunbookDefinition** parancsmag frissíti a Microsoft Azure automatizálási runbook vázlatának definícióját.
Adjon meg egy olyan Windows PowerShell-parancsfájlt (. ps1) tartalmazó fájlt, amely a Piszkozat runbook runbook válik.

Ha már létezik Piszkozat-definíció, a *felülírás* paraméterrel kényszerítheti a parancsmagot, hogy felülírja a meglévő piszkozatot.

## Példák

### Példa 1: egy runbook meglévő vázlat definíciójának felülírása
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

Ez a parancs felülírja a runbook meglévő Piszkozat-definícióját.

## PARAMÉTEREK

### -AutomationAccountName
Az automatizálási fiók nevét adja meg.

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

### -Name (név)
Egy nevet ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Átír
Azt jelzi, hogy felülír-e egy meglévő Piszkozat definíciót.

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

### -Path (elérési út)
A runbook elérési útját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

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

### Microsoft. Azure. Command. Automation. Model. RunbookDefinition

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureAutomationRunbookDefinition](./Get-AzureAutomationRunbookDefinition.md)


