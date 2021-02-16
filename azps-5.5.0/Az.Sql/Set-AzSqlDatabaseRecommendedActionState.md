---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 6d634760080e3fb26153b747e733369b20bc8336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168627"
---
# Set-AzSqlDatabaseRecommendedActionState

## SYNOPSIS
Frissíti egy Azure SQL-adatbázis ajánlott műveletének állapotát.

## SZINTAXIS

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzSqlDatabaseRecomstateActionState** parancsmag frissíti az Azure SQL-adatbázis ajánlott műveletének állapotát.
Ez lehetővé teszi, hogy az új állapot alapján egy javasolt műveletet alkalmazzanak, visszaállítsunk vagy elvetsünk.

## PÉLDÁK

### 1. példa: Javasolt műveletállapot alkalmazása függőben
```
PS C:\>Set-AzSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

Ez a parancs frissíti a WIRunner nevű adatbázishoz tartozó IR_ \[ test_schema \] _ \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893 nevű javasolt művelet \] állapotát.

## PARAMETERS

### -AdvisorName
Annak a tanácsadónak a nevét adja meg, amelyhez ez az ajánlott művelet tartozik.

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

### -DatabaseName
Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag az ajánlott műveletállapotot állítja be.

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

### -RecommendedActionName
Annak az ajánlott műveletnek a nevét adja meg, amelynek az állapotát frissíteni kell.

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
Az adatbázist tartalmazó kiszolgáló erőforráscsoportjának nevét adja meg.

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

### -ServerName
Annak a kiszolgálónak a neve, amelyben az adatbázis található.

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

### -State
Azt az új értéket adja meg, amelyre a parancsmag frissíti az ajánlott művelet állapotát.
A paraméter elfogadható értékei a következőek:
- Aktív
- Függőben
- PendingRevert
- RevertCancelled
- Figyelmen kívül hagyva
- Megoldva

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState

## KIMENETEK

### Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecombaseActionModel

## MEGJEGYZÉSEK
* Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, adatbázis, mssql, tanácsadó, ajánlottaction

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzSqlServerAdvisor](./Get-AzSqlServerAdvisor.md)

[Get-AzSqlElasticPoolAdvisor](./Get-AzSqlElasticPoolAdvisor.md)

[Get-AzSqlServerRecomsqlAction](./Get-AzSqlServerRecommendedAction.md)

[Get-AzSqlElasticPoolRecomasticAction](./Get-AzSqlElasticPoolRecommendedAction.md)

[Set-AzSqlElasticPoolRecomstateActionState](./Set-AzSqlElasticPoolRecommendedActionState.md)

[Set-AzSqlElasticPoolAdvisorAutoExecuteStatus](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[Set-AzSqlElasticPoolRecomstateActionState](./Set-AzSqlElasticPoolRecommendedActionState.md)

[Set-AzSqlServerRecomstateActionState](./Set-AzSqlServerRecommendedActionState.md)

[Set-AzSqlElasticPoolAdvisorAutoExecuteStatus](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[Set-AzSqlServerAdvisorAutoExecuteStatus](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)
