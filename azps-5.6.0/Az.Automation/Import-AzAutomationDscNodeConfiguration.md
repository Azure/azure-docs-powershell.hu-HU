---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3680d277addba29444f3f2955d7cca28505435a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014038"
---
# Import-AzAutomationDscNodeConfiguration

## SYNOPSIS
MOF-dokumentumot importál DSC-csomópont-konfigurációként az Automatizálásban.

## SZINTAXIS

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Az **Import-AzAutomationDscConfiguration** parancsmag egy Felügyelt objektumformátum (MOF) konfigurációs dokumentumot importál az Azure Automation alkalmazásba kívánt állapotkonfiguráció (DSC) csomópont-konfigurációként.
Adja meg egy .mof fájl elérési útját.

## PÉLDÁK

### 1. példa: DSC-csomópont konfigurációjának importálása az automatizálásba
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

Ez a parancs egy DSC-csomópont-konfigurációt importál a webserver.mof nevű fájlból a Contoso17 nevű automatizálási fiókba a ContosoConfiguration DSC-konfiguráció alatt.
A parancs a Force *paramétert* adja meg.
Ha létezik egy ContosoConfiguration.webserver nevű meglévő DSC-csomópont-konfiguráció, ez a parancs helyettesíti azt.

### 2. példa: DSC-csomópont konfigurációjának importálása az Automatizálásba, és hozzon létre egy új buildverziót, és ne írja felül a meglévő NodeConfigurációt.
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

Ez a parancs egy DSC-csomópont-konfigurációt importál a webserver.mof nevű fájlból a Contoso17 nevű automatizálási fiókba a ContosoConfiguration DSC-konfiguráció alatt.
A parancs a Force *paramétert* adja meg.
Ha létezik egy ContosoConfiguration.webserver nevű meglévő DSC-csomópont-konfiguráció, ez a parancs hozzáad egy új buildverziót ContosoConfiguration[2].webserver néven.

## PARAMETERS

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelybe ez a parancsmag egy DSC-csomópont-konfigurációt importál.

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

### -ConfigurationName
Az Automatizálásban egy olyan DSC-konfiguráció nevét adja meg, amely az importálni szükséges csomópont-konfiguráció névtere és tárolója.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### -Force
Azt jelzi, hogy ez a parancsmag lecserél egy meglévő DSC-csomópont-konfigurációt az Automatizálásban.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncrementNodeConfigurationBuild
Létrehozza a csomópont konfigurációjának új verzióját.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Annak az MOF konfigurációs dokumentumnak az elérési útját adja meg, amelybe ez a parancsmag importálva van.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja DSC-csomópont-konfigurációt importál.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Automation.Model.NodeConfiguration

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Export-AzAutomationDscConfiguration](./Export-AzAutomationDscConfiguration.md)

[Get-AzAutomationDscConfiguration](./Get-AzAutomationDscConfiguration.md)


