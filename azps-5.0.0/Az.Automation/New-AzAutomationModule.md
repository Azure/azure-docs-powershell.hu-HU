---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299804"
---
# New-AzAutomationModule

## Áttekintés
Modul importálása automatizálásra.

## SZINTAXISA

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzAutomationModule** parancsmag modult importál az Azure automatizálásba.
Ez a parancs a. zip fájlnév-kiterjesztésű tömörített fájlt fogadja el.
A fájl egy olyan mappát tartalmaz, amely az alábbi típusú fájlokat tartalmazza: 
- Windows PowerShell-modul (. psm1 vagy. dll fájlnév-kiterjesztéssel) 
- Windows PowerShell-modul jegyzékfájlja (. psd1 fájlnév-kiterjesztéssel): a. zip fájl neve, a mappa neve és a mappában lévő fájl neve meg kell egyeznie.
Adja meg a. zip fájlt URL-címként, amelyet az automatizálási szolgáltatás tud elérni.
Ha a parancsmag vagy az Set-AzAutomationModule parancsmag használatával Windows PowerShell-modult importál automatizálásra, a művelet aszinkron.
A parancs azt fejezi ki, hogy az importálás sikerül vagy sikertelen.
Annak ellenőrzéséhez, hogy sikerült-e, futtassa a következő parancsot: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName ellenőrizze a **ProvisioningState** tulajdonság értékét a sikeres érték eléréséhez.

## Példák

### 1. példa: modul importálása
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
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
A modul ZIP-csomagjának URL-címe

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. URI

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. Module

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


