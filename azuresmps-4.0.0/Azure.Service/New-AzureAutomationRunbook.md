---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015934"
---
# New-AzureAutomationRunbook

## Áttekintés

Létrehoz egy runbook.

## SZINTAXISA

### ByRunbookName (alapértelmezett)
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPath
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

A **New-AzureAutomationRunbook** parancsmag egy új, üres Microsoft Azure automatizálási runbook hoz létre.
Adjon meg egy nevet az új runbook létrehozásához.

A runbook importálásához megadhatja a Windows PowerShell-parancsfájlok (. ps1) elérési útját is.
Az importálandó parancsfájl csak egy Windows PowerShell-munkafolyamat-definíciót tartalmazhat.
Ennek a Windows PowerShell-munkafolyamatnak a neve a runbook neve lesz.

## Példák

### Példa 1: runbook létrehozása
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

Ez a parancs létrehoz egy Runbook02 nevű új runbook a Contoso17 nevű automatizálási fiókban.

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

### -Leírás
A runbook leírását adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A runbook nevét adja meg.

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path (elérési út)
Az elérési utat adja meg.

```yaml
Type: String
Parameter Sets: ByPath
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

### -Címkék
A runbook címkéit adja meg.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. Runbook

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureAutomationRunbook](./Get-AzureAutomationRunbook.md)

[Közzététel – AzureAutomationRunbook](./Publish-AzureAutomationRunbook.md)

[Remove-AzureAutomationRunbook](./Remove-AzureAutomationRunbook.md)

[Set-AzureAutomationRunbook](./Set-AzureAutomationRunbook.md)

[Start-AzureAutomationRunbook](./Start-AzureAutomationRunbook.md)


