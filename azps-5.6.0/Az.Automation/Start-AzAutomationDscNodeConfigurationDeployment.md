---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 477b8f5853d9a5dbe3dd030e7419316825088807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921473"
---
# Start-AzAutomationDscNodeConfigurationDeployment

## SYNOPSIS
DSC-csomópont-konfigurációt telepít az automatizálásban.

## SZINTAXIS

### ByAll (alapértelmezett)
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Start-AzAutomationDscNodeConfigurationDeployment** parancsmag egy DSC-csomópont-konfigurációt telepít az Azure Automationben.

## PÉLDÁK

### 1. példa: Azure DSC-csomópont konfigurációjának üzembe helyezése az Automatizálásban
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

A fenti parancs a "Config01.Node1" nevű DSC-csomópont-konfigurációt telepíti a Csomópontnevek adott kétdimenziós tömbjéhez. A telepítés szakaszos módon történik.

### 2. példa: Azure DSC-csomópont konfigurációjának ütemezése az Automatizálásban
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

A fenti parancs a "Config01.Node1" nevű DSC-csomópont-konfigurációt a csomópontnevek adott kétdimenziós tömbjére ütemezi. A telepítés szakaszos módon történik, és az ütemezés alapján hajtódik végre.

## PARAMETERS

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.

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
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Input object for Piping

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NodeConfigurationName
A parancsmag által üzembe helyezett DSC-csomópont-konfiguráció nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeName
Megadja azoknak a csomópontoknak a nevét, amelyekre a csomópont-konfigurációt telepíteni szeretné.

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag konfigurációt fordít.

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

### -Schedule
Automatizálási ütemezési objektum a telepítési feladat ütemezéséhez.

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment

## KIMENETEK

### Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Start-AzAutomationDscCompilationJob](./Start-AzAutomationDscCompilationJob.md)

[Import-AzAutomationDscNodeConfiguration](./Import-AzAutomationDscNodeConfiguration.md)

[Stop-AzAutomationDscNodeConfigurationDeployment](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[Get-AzAutomationDscNodeConfigurationDeployment](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[Get-AzAutomationDscNodeConfigurationDeploymentSchedule](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[New-AzAutomationSchedule](./New-AzAutomationSchedule.md)
