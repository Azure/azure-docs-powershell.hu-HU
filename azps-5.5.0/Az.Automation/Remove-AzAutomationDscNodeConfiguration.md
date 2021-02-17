---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 16e0f858b11e98df3599a568805e72f7ae8f6a8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205494"
---
# Remove-AzAutomationDscNodeConfiguration

## SYNOPSIS
Eltávolítja a metaadatokat a DSC csomópont-konfigurációiból az Automatizálásban.

## SZINTAXIS

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzAutomationDscNodeConfiguration** parancsmag eltávolítja a metaadatokat az APS kívánt állapotkonfigurációs (DSC) csomópont-konfigurációiból az Azure Automationben.
Az automatizálás a DSC-csomópont konfigurációját Felügyelt objektumformátum (MOF) konfigurációs dokumentumként tárolja.

## PÉLDÁK

### 1. példa

Eltávolítja a metaadatokat a DSC csomópont-konfigurációiból az Automatizálásban. (automatikusan generált)

<!-- Aladdin Generated Example -->
```powershell
Remove-AzAutomationDscNodeConfiguration -AutomationAccountName 'AutomationAccount01' -IgnoreNodeMappings -Name 'Configuration01' -ResourceGroupName myresourcegroup
```

## PARAMETERS

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amely azokat a DSC-csomópont-konfigurációkat tartalmazza, amelyek metaadatait a parancsmag eltávolítja.

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
ps_force

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreNodeMappings
Azt jelzi, hogy ez a parancsmag figyelmen kívül hagyja a csomópontok megfeleltetését.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Annak a DSC-csomópont-konfigurációnak a nevét adja meg, amelynek a parancsmagja eltávolítja a metaadatokat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.
Ez a parancsmag eltávolítja a DSC-csomópont-konfigurációk metaadatait a paraméter által megadott erőforráscsoportban.

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

### System.Void

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationDscNodeConfiguration](./Get-AzAutomationDscNodeConfiguration.md)

[Import-AzAutomationDscNodeConfiguration](./Import-AzAutomationDscNodeConfiguration.md)

[Azure Automation-parancsmagok](/powershell/module/Az.Automation/)
