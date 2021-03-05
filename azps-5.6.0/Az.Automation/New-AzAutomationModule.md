---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 093a6f61668f40b43d2f228035132c010e31d426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012726"
---
# New-AzAutomationModule

## SYNOPSIS
Modult importál az automatizálásba.

## SZINTAXIS

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzAutomationModule** parancsmag egy modult importál az Azure Automatizálásba.
Ez a parancs elfogad egy .zip kiterjesztésű tömörített fájlt.
A fájl egy mappát tartalmaz, amely az alábbi típusú fájlok egyikét tartalmazza: 
- Windows PowerShell-modul, amelynek .psm1 vagy .dll fájlnévkiterjesztése van 
- A Windows PowerShell-modul jegyzékfájljának .psd1 fájlnévkiterjesztéssel, a .zip fájl nevével, a mappa nevével és a mappában lévő fájl nevével azonosnak kell lennie.
Adja meg a .zip fájlt URL-címként, amelyhez az automatizálási szolgáltatás hozzáférhet.
Ha windowsos PowerShell-modult importál az automatizálásba ezzel a parancsmagmal vagy a Set-AzAutomationModule parancsmag használatával, a művelet aszinkron lesz.
A parancs befejezi, hogy az importálás sikeres-e vagy sikertelen.
A sikeres ellenőrzéshez futtassa a következő parancsot: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Ellenőrizze, hogy a **ProvisioningState** tulajdonság értéke Sikeres-e.

## PÉLDÁK

### 1. példa: Modul importálása
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

Ez a parancs importálja a ContosoModule nevű modult a Contoso17 nevű automatizálási fiókba.
A modult egy Azure-blob tárolja egy contosostorage nevű tárfiókban és egy modulnak nevezett tárolóban.

## PARAMETERS

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja importál egy modult.

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
A modul zip csomag url-címe

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
Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja egy modult importál.

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

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


