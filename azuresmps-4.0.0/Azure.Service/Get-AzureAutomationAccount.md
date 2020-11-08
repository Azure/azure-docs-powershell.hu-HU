---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016371"
---
# Get-AzureAutomationAccount

## Áttekintés

Azure automatizálási fiókokat kap.

## SZINTAXISA

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

A **Get-AzureAutomationAccount** parancsmag a Microsoft Azure automatizálási fiókokat kapja az előfizetéséhez.
Az automatizálási fiók a többi automatizálási fiók erőforrásaitól elkülönített automatizálási erőforrások tárolója.
Az automatizálási erőforrások közé tartozik a runbooks, a feladatok és az eszközök.

## Példák

### Példa 1: automatizálási fiók beszerzése
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

Ez a parancs a Contoso17 nevű automatizálási fiókot kapja.

## PARAMÉTEREK

### -Hely
Az automatizálási fiókokkal társított Azure-helyet adja meg.

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
Az Azure automatizálási fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
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

### Microsoft. Azure. Command. Automation. Model. AutomationAccount

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureAutomationAccount](./New-AzureAutomationAccount.md)

[Remove-AzureAutomationAccount](./Remove-AzureAutomationAccount.md)


