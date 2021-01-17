---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373056"
---
# Set-AzAutomationModule

## SYNOPSIS
Frissíti a modult az Automatizálásban.

## SZINTAXIS

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzAutomationModule** parancsmag frissíti az Azure Automation egyik modulját.
Ez a parancs elfogad egy .zip kiterjesztésű tömörített fájlt.
A fájl egy mappát tartalmaz, amely az alábbi típusú fájlok egyikét tartalmazza: 
- wps_2 .psm1 vagy .dll kiterjesztésű modul 
- wps_2 .psd1 kiterjesztésű modul jegyzékfájljának. A .zip fájlnak, a mappa nevének és a mappában lévő fájl nevének meg kell egynie.
Adja meg a .zip fájlt URL-címként, amelyhez az automatizálási szolgáltatás hozzáférhet.
Ha ezzel a wps_2 vagy a New-AzAutomationModule parancsmag használatával importál egy modult az automatizálásba, a művelet aszinkron lesz.
A parancs befejezi, hogy az importálás sikeres-e vagy sikertelen.
A sikeres ellenőrzéshez futtassa a következő parancsot: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Ellenőrizze, hogy a **ProvisioningState** tulajdonság értéke Sikeres-e.

## PÉLDÁK

### 1. példa: Modul frissítése
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

Ez a parancs importálja egy ContosoModule nevű meglévő modul frissített verzióját a Contoso17 nevű automatizálási fiókba.  A modult egy Azure-blob tárolja egy contosostorage nevű tárfiókban és egy modulnak nevezett tárolóban.

## PARAMETERS

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja frissíti a modult.

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
Annak a .zip fájlnak az URL-címét adja meg, amely a parancsmag által importálni kívánt modul új verzióját tartalmazza.

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
Annak a modulnak a verzióját adja meg, amelyre ez a parancsmag frissíti az Automatizálást.

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Name
Annak a modulnak a nevét adja meg, amelyből a parancsmag importálja a parancsmagot.

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
Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja frissíti a modult.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Uri

## KIMENETEK

### Microsoft.Azure.Commands.Automation.Model.Module

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[New-AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)


