---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: d809a7d01e6b4d477a72d26df11d73e87678d7e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382659"
---
# Get-AzMetricAlertRuleV2

## SYNOPSIS
V2-es (nem klasszikus) metrikus riasztási szabályokat kap

## SZINTAXIS

### ByResourceGroupName (alapértelmezett)
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByRuleName
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByRuleId
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzMetricAlertRuleV2** parancsmag egy metrikus riasztási szabályt kap név vagy URI alapján, illetve egy adott erőforráscsoportból vagy előfizetésből származó összes metrikus riasztási szabályt.

## PÉLDÁK

### 1. példa: Az aktuális előfizetés összes metrikus riasztási szabályának be szereznie
```powershell
PS C:\>Get-AzMetricAlertRuleV2
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : metricResourceGroup
Description          : fdafda
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/microsoft.insights/metricAlerts/Rule1
Name                 : Rule1
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}

Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : SampleResourceGroup
Description          : Testing 1 minute granuarity
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/Microsoft.Compute/virtualMachines/SCCMDemo4}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:01:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/Rule2
Name                 : Rule2
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

Ez a parancs az aktuális előfizetés összes metrikus riasztási szabályát beveszi.

### 2. példa: Az erőforráscsoport összes metrikus riasztási szabályának be szereznie

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/pr
                       oviders/microsoft.insights/actiongroups/emails}
ResourceGroup        : metricAlertsRG
Description          : Test Classic VM alert - CPU Usage
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Micr
                       osoft.ClassicCompute/virtualMachines/VM1}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.ClassicCompute/virtualMachines
TargetResourceRegion : southcentralus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/micro
                       soft.insights/metricAlerts/Test%20Classic%20VM%20alert%20-%20CPU%20Usage
Name                 : Test Classic VM alert - CPU Usage
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

Ez a parancs beszerzi az összes metrikus riasztási szabályt a metricAlertsRG nevű erőforráscsoportban.

### 3. példa: Metrikus riasztási szabály lekérte név szerint

```powershell
PS C:\> Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG -Name PS3182019

Criteria             : {metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
ResourceGroup        : metricAlertsRG
Description          : This is description 
Severity             : 1
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

Ez a parancs a PS3182019 metrikus riasztási szabályt kapja meg a metricAlertsRG nevű erőforráscsoportban.

### 4. példa: Metrikus riasztási szabály lekérte szabályazonosító szerint

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/emails}
ResourceGroup        : SampleResourceGroup
Description          : Test Description
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : 
TargetResourceRegion : 
AutoMitigate         : 
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
Name                 : MyMetricAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

Ez a parancs a metrikus riasztási szabályt kapja meg a megadott erőforrás-azonosítóval.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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
A metrikus riasztási szabály neve

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A ResourceGroupName

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A metrikus riasztási szabály szabályazonosítója

```yaml
Type: System.String
Parameter Sets: ByRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
