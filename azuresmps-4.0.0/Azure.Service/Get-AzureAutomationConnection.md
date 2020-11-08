---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016370"
---
# Get-AzureAutomationConnection

## Áttekintés

Azure automatizálási kapcsolatot kap.

## SZINTAXISA

### ByAll (alapértelmezett)
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByConnectionName
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByConnectionTypeName
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

A **Get-AzureAutomationConnection** parancsmag egy vagy több Microsoft Azure automatizálási kapcsolatot kap.
Alapértelmezés szerint minden kapcsolat visszaadva van.
Ha meghatározott kapcsolatot szeretne kapni, adja meg a nevét.
Ha egy bizonyos típus minden kapcsolatát meg szeretné kapni, adja meg a kapcsolat típusának nevét.

## Példák

### Példa 1: az összes kapcsolat beolvasása
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

Ez a parancs a Contoso17 nevű automatizálási fiók összes kapcsolatát beilleszti.

### 2. példa: egy típus összes kapcsolatának beolvasása
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

Ez a parancs minden Azure-kapcsolatot beolvas a Contoso17 nevű automatizálási fiókban.

### 3. példa: kapcsolat kérése
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

Ez a parancs a kapcsolatom nevű kapcsolatot kapja meg.

## PARAMÉTEREK

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelyben a lekérdezni kívánt kapcsolat látható.

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

### -ConnectionTypeName
A lekérdezni kívánt kapcsolatok kapcsolati típusának nevét adja meg.

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A lekérdezni kívánt kapcsolat nevét adja meg.

```yaml
Type: String
Parameter Sets: ByConnectionName
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

### Microsoft. Azure. Command. Automation. Model. Connection

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureAutomationConnection](./New-AzureAutomationConnection.md)

[Remove-AzureAutomationConnection](./Remove-AzureAutomationConnection.md)

[Set-AzureAutomationConnectionFieldValue](./Set-AzureAutomationConnectionFieldValue.md)


