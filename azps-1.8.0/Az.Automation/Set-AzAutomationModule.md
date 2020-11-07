---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: d9c036c7047ee0d568f5e1451bce46dfe2903e29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671503"
---
# Set-AzAutomationModule

## Áttekintés
Frissít egy modult az automatizálásban.

## SZINTAXISA

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzAutomationModule** parancsmag az Azure automatizálás modulban frissíti a modult.
Ez a parancs a. zip fájlnév-kiterjesztésű tömörített fájlt fogadja el.
A fájl egy olyan mappát tartalmaz, amely az alábbi típusú fájlokat tartalmazza: 
- wps_2 modul, amelynek. psm1 vagy. dll fájlnév-kiterjesztése van 
- wps_2 Module manifest (. psd1 fájlnév-kiterjesztéssel): a. zip fájl neve, a mappa neve és a mappában lévő fájl neve kell, hogy legyen.
Adja meg a. zip fájlt URL-címként, amelyet az automatizálási szolgáltatás tud elérni.
Ha a parancsmaggal vagy a New-AzAutomationModule parancsmaggal importál egy wps_2 modult automatizálásra, a művelet aszinkron.
A parancs azt fejezi ki, hogy az importálás sikerül vagy sikertelen.
Annak ellenőrzéséhez, hogy sikerült-e, futtassa a következő parancsot: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName ellenőrizze a **ProvisioningState** tulajdonság értékét a sikeres érték eléréséhez.

## Példák

### Példa 1: modul frissítése
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

Ez a parancs a ContosoModule nevű meglévő modul frissített verzióját importálja a Contoso17 nevű automatizálási fiókba.  A modul az Azure Blob-ban tárolódik egy contosostorage nevű tárterület-fiókban, valamint egy modul nevű tárolóban.

## PARAMÉTEREK

### -AutomationAccountName
Annak az automatizálási fióknak a neve, amelyhez a parancsmag egy modult frissít.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkUri
Annak a. zip fájlnak az URL-címét adja meg, amely a parancsmag által importált modul új verzióját tartalmazza.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
Annak a modulnak a verziója, amelyre ez a parancsmag frissíti az automatizálást.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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
Annak a modulnak a nevét adja meg, amelyre a parancsmag importál.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a csoportnak a neve, amelyhez a parancsmag egy modult frissít.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. URI

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. Module

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Új – AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)


