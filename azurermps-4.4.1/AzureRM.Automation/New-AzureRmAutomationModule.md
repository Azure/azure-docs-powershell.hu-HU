---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: e2de3546f805e006bd7f48e2ee7f95b8f3347544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505672"
---
# New-AzureRmAutomationModule

## Áttekintés
Modul importálása automatizálásra.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmAutomationModule [-Name] <String> -ContentLinkUri <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmAutomationModule** parancsmag modult importál az Azure automatizálásba.
Ez a parancs a. zip fájlnév-kiterjesztésű tömörített fájlt fogadja el.
A fájl egy olyan mappát tartalmaz, amely az alábbi típusú fájlokat tartalmazza: 

- wps_2 modul, amelynek. psm1 vagy. dll fájlnév-kiterjesztése van 
- wps_2 Module manifest (. psd1 fájlnév-kiterjesztéssel)

A. zip fájl neve, a mappa neve és a mappa fájlnevének egyeznie kell.

Adja meg a. zip fájlt URL-címként, amelyet az automatizálási szolgáltatás tud elérni.

Ha a parancsmaggal vagy a Set-AzureRmAutomationModule parancsmaggal importál egy wps_2 modult automatizálásra, a művelet aszinkron.
A parancs azt fejezi ki, hogy az importálás sikerül vagy sikertelen.
A következő parancs futtatásával ellenőrizheti, hogy sikerült-e:

`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName

Ellenőrizze, hogy a **ProvisioningState** tulajdonság értéke sikeres volt-e.

## Példák

### 1. példa: modul importálása
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

Ez a parancs a ContosoModule nevű modult importálja a Contoso17 nevű automatizálási fiókba.
A modul az Azure Blob-ban tárolódik egy contosostorage nevű tárterület-fiókban, valamint egy modul nevű tárolóban.

## PARAMÉTEREK

### -AutomationAccountName
Annak az automatizálási fióknak a neve, amelyhez a parancsmag modult importál.

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
Egy zip-csomag URL-címe.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Annak az erőforráscsoport a nevét adja meg, amelyhez a parancsmag modult importál.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. Module

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmAutomationModule](./Get-AzureRmAutomationModule.md)

[Remove-AzureRmAutomationModule](./Remove-AzureRmAutomationModule.md)

[Set-AzureRmAutomationModule](./Set-AzureRmAutomationModule.md)


