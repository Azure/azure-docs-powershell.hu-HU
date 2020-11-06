---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: e6d451deac5a9539a2972964f1ac2536dcd7992f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501211"
---
# Set-AzureRmAutomationModule

## Áttekintés
Frissít egy modult az automatizálásban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureRmAutomationModule** parancsmag az Azure automatizálás modulban frissíti a modult.
Ez a parancs a. zip fájlnév-kiterjesztésű tömörített fájlt fogadja el.
A fájl egy olyan mappát tartalmaz, amely az alábbi típusú fájlokat tartalmazza: 
- wps_2 modul, amelynek. psm1 vagy. dll fájlnév-kiterjesztése van 
- wps_2 Module manifest (. psd1 fájlnév-kiterjesztéssel): a. zip fájl neve, a mappa neve és a mappában lévő fájl neve kell, hogy legyen.
Adja meg a. zip fájlt URL-címként, amelyet az automatizálási szolgáltatás tud elérni.
Ha a parancsmaggal vagy a New-AzureRmAutomationModule parancsmaggal importál egy wps_2 modult automatizálásra, a művelet aszinkron.
A parancs azt fejezi ki, hogy az importálás sikerül vagy sikertelen.
Annak ellenőrzéséhez, hogy sikerült-e, futtassa a következő parancsot: `PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name ` ModuleName ellenőrizze a **ProvisioningState** tulajdonság értékét a sikeres érték eléréséhez.

## Példák

### Példa 1: modul frissítése
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

[Get-AzureRmAutomationModule](./Get-AzureRmAutomationModule.md)

[Új – AzureRmAutomationModule](./New-AzureRmAutomationModule.md)

[Remove-AzureRmAutomationModule](./Remove-AzureRmAutomationModule.md)


