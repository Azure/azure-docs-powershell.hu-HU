---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: fa10c44186de06de758e4f7878bb7c8da61c4d6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004805"
---
# Publish-AzAutomationRunbook

## SYNOPSIS
Közzétesz egy runbookot.

## SZINTAXIS

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Publish-AzAutomationRunbook** parancsmag közzétesz egy runbookot az Azure Automation éles környezetében való használatra.

## PÉLDÁK

### 1. példa: Runbook közzététele
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

Ez a parancs közzéteszi a Runbk01 nevű runbookot a Contoso17 nevű Azure Automation-fiókban.

## PARAMETERS

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag közzétesz egy runbookot.

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

### -Name
A parancsmag által közzétett runbook nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja közzétesz egy runbookot.

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

## KIMENETEK

### Microsoft.Azure.Commands.Automation.Model.Runbook

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Export-AzAutomationRunbook](./Export-AzAutomationRunbook.md)

[Get-AzAutomationRunbook](./Get-AzAutomationRunbook.md)

[Import-AzAutomationRunbook](./Import-AzAutomationRunbook.md)

[New-AzAutomationRunbook](./New-AzAutomationRunbook.md)

[New-AzAutomationRunbook](./New-AzAutomationRunbook.md)

[Remove-AzAutomationRunbook](./Remove-AzAutomationRunbook.md)

[Set-AzAutomationRunbook](./Set-AzAutomationRunbook.md)

[Start-AzAutomationRunbook](./Start-AzAutomationRunbook.md)


