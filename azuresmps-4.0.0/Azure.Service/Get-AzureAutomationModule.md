---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016368"
---
# Get-AzureAutomationModule

## Áttekintés

Az Azure automatizálási moduljának beszerzése

## SZINTAXISA

### ByAll (alapértelmezett)
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByName
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

A **Get-AzureAutomationModule** parancsmag egy vagy több Microsoft Azure automatizálási modult kap.
Alapértelmezés szerint az összes modult adja vissza.
Ha egy adott modult szeretne beszerezni, adja meg a nevét.

## Példák

### Példa 1: az összes modul beolvasása
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

Ez a parancs a Contoso17 nevű Azure automatizálási fiók összes modulját beilleszti.

### 2. példa: modul beszerzése
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

Ez a parancs egy ContosoModule nevű modult kap a Contoso17 nevű Azure automatizálási fiókban.

## PARAMÉTEREK

### -AutomationAccountName
A lekérdezni kívánt automatizálási fiók nevét adja meg a runbook.

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
A lekérdezni kívánt modul nevét adja meg.

```yaml
Type: String
Parameter Sets: ByName
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. Module

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureAutomationModule](./New-AzureAutomationModule.md)

[Remove-AzureAutomationModule](./Remove-AzureAutomationModule.md)

[Set-AzureAutomationModule](./Set-AzureAutomationModule.md)


