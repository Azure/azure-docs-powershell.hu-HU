---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016357"
---
# Get-AzureAutomationScheduledRunbook

## Áttekintés

Az Azure automatizálási runbooks és a hozzájuk kapcsolódó ütemterveket kapja meg.

## SZINTAXISA

### ByAll (alapértelmezett)
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByJobScheduleId
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByScheduleName
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

A **Get-AzureAutomationScheduledRunbook** egy vagy több Azure automatizálási runbooks és kapcsolódó ütemtervet kap.
Alapértelmezés szerint minden ütemezett runbooks visszaadott.

Ha meghatározott ütemezett runbook szeretne kapni, adja meg a runbook nevét és az ütemezés nevét.
Ha a runbook társított összes ütemezést meg szeretné kapni, akkor csak a runbook nevét adja meg.
Ha az ütemtervhez társított összes runbooks meg szeretné kapni, akkor csak az ütemezés nevét adja meg.

## Példák

### Példa 1: az ütemezett runbooks beszerzése
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

Ez a parancs a Contoso17 nevű automatizálási fiók minden ütemezett runbooks megkapja.

### 2. példa: a runbook társított összes ütemezés beolvasása
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

Ez a parancs a Contoso17 nevű automatizálási fiókban minden ütemezett runbooks bekerül az runbook Runbk01.

### 3. példa: az ütemtervhez társított összes runbooks beszerzése
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

Ez a parancs a Contoso17 nevű automatizálási fiók ütemezési Schedule01 minden ütemezett runbooks megkapja.

## PARAMÉTEREK

### -AutomationAccountName
Az Azure automatizálási fiók nevét adja meg.

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

### -JobScheduleId
Az ütemezett feladat AZONOSÍTÓját adja meg.

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

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

### -RunbookName
Egy runbook nevét adja meg.

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Az ütemezés nevét adja meg.

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. JobSchedule

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Register-AzureAutomationScheduledRunbook](./Register-AzureAutomationScheduledRunbook.md)

[Regisztráció törlése – AzureAutomationScheduledRunbook](./Unregister-AzureAutomationScheduledRunbook.md)


