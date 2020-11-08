---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015659"
---
# Get-AzureAutomationCredential

## Áttekintés

Azure Automation hitelesítő adatokat kap.

## SZINTAXISA

### ByAll (alapértelmezett)
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByName
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

A **Get-AzureAutomationCredential** parancsmag egy vagy több Microsoft Azure automatizálási hitelesítő adatokat kap.
Alapértelmezés szerint minden hitelesítő adatot visszaad a rendszer.
A megadott hitelesítő adatok megadásához adja meg a nevét.

## Példák

### Példa 1: a hitelesítő adatok beszerzése
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

Ez a parancs a Contoso17 nevű automatizálási fiók minden hitelesítő adatait beolvassa.

### 2. példa: hitelesítő adatok beszerzése
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

Ez a parancs a MyCredential nevű hitelesítő adatokat kapja meg.

## PARAMÉTEREK

### -AutomationAccountName
Az automatizálási fiók nevét adja meg a beolvasandó hitelesítő adatokkal.

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
A lekérdezni kívánt hitelesítő adatok nevét adja meg.

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

### Microsoft. Azure. Command. Automation. Model. CredentialInfo

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureAutomationCredential](./New-AzureAutomationCredential.md)

[Remove-AzureAutomationCredential](./Remove-AzureAutomationCredential.md)

[Set-AzureAutomationCredential](./Set-AzureAutomationCredential.md)


