---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016223"
---
# New-AzureAutomationModule

## Áttekintés

Modul importálása automatizálásra.

## SZINTAXISA

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

A **New-AzureAutomationModule** parancsmag modult importál az Azure automatizálásba.
A modul egy. zip kiterjesztésű tömörített fájl, amely egy olyan mappát tartalmaz, amely az alábbi fájltípusok egyikét tartalmazza:

- Windows PowerShell-modul (psm1-fájl) 

- Windows PowerShell-modul jegyzékfájlja (psd1-fájl) 

- Egy kódösszeállítás (dll-fájl)

A zip-fájl, a zip-fájl mappája és a mappában lévő fájl (. psm1, PSD. 1 vagy. dll) neveinek egyezniük kell.

## Példák

### 1. példa: modul importálása
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

Ez a parancs a ContosoModule nevű modult importálja a Contoso17 nevű automatizálási fiókba.
A modul az Azure Blob-ban tárolódik egy contosostorage nevű tárterület-fiókban, valamint egy modul nevű tárolóban.

## PARAMÉTEREK

### -AutomationAccountName
Annak az automatizálási fióknak a neve, amelyet a modul tárol.

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

### -ContentLink
Nyilvános URL-cím, például webhely vagy Azure Blob-tárhely, amely a modul elérési útját adja meg.
Ennek a helynek nyilvánosan elérhetőnek kell lennie.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A modul nevét adja meg.

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
Egy vagy több, a modulhoz kapcsolódó címkét ad meg.

```yaml
Type: IDictionary
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

### Microsoft. Azure. Command. Automation. Model. Module

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureAutomationModule](./Get-AzureAutomationModule.md)

[Remove-AzureAutomationModule](./Remove-AzureAutomationModule.md)

[Set-AzureAutomationModule](./Set-AzureAutomationModule.md)


