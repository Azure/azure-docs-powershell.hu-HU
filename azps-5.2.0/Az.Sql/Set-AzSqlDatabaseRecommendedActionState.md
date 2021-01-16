---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 6d634760080e3fb26153b747e733369b20bc8336
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344034"
---
# <span data-ttu-id="b47cd-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b47cd-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="b47cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b47cd-102">SYNOPSIS</span></span>
<span data-ttu-id="b47cd-103">Frissíti egy Azure SQL-adatbázis ajánlott műveletének állapotát.</span><span class="sxs-lookup"><span data-stu-id="b47cd-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="b47cd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b47cd-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b47cd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b47cd-105">DESCRIPTION</span></span>
<span data-ttu-id="b47cd-106">A **Set-AzSqlDatabaseRecomstateActionState** parancsmag frissíti az Azure SQL-adatbázis ajánlott műveletének állapotát.</span><span class="sxs-lookup"><span data-stu-id="b47cd-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="b47cd-107">Ez lehetővé teszi egy javasolt művelet alkalmazását, visszaalakulát vagy elvetettét az új állapot alapján.</span><span class="sxs-lookup"><span data-stu-id="b47cd-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="b47cd-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b47cd-108">EXAMPLES</span></span>

### <span data-ttu-id="b47cd-109">1. példa: Javasolt műveletállapot alkalmazása függőben</span><span class="sxs-lookup"><span data-stu-id="b47cd-109">Example 1: Apply a recommended action state to pending</span></span>
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

<span data-ttu-id="b47cd-110">Ez a parancs frissíti a WIRunner nevű adatbázishoz tartozó IR_ \[ test_schema \] _ \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893 nevű javasolt művelet \] állapotát.</span><span class="sxs-lookup"><span data-stu-id="b47cd-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="b47cd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b47cd-111">PARAMETERS</span></span>

### <span data-ttu-id="b47cd-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="b47cd-112">-AdvisorName</span></span>
<span data-ttu-id="b47cd-113">Annak a tanácsadónak a nevét adja meg, amelyhez ez az ajánlott művelet tartozik.</span><span class="sxs-lookup"><span data-stu-id="b47cd-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="b47cd-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b47cd-114">-DatabaseName</span></span>
<span data-ttu-id="b47cd-115">Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag az ajánlott műveletállapotot állítja be.</span><span class="sxs-lookup"><span data-stu-id="b47cd-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="b47cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47cd-116">-DefaultProfile</span></span>
<span data-ttu-id="b47cd-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b47cd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b47cd-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="b47cd-118">-RecommendedActionName</span></span>
<span data-ttu-id="b47cd-119">Annak az ajánlott műveletnek a nevét adja meg, amelynek az állapotát frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="b47cd-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="b47cd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b47cd-120">-ResourceGroupName</span></span>
<span data-ttu-id="b47cd-121">Az adatbázist tartalmazó kiszolgáló erőforráscsoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b47cd-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="b47cd-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b47cd-122">-ServerName</span></span>
<span data-ttu-id="b47cd-123">Annak a kiszolgálónak a neve, amelyben az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="b47cd-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="b47cd-124">-State</span><span class="sxs-lookup"><span data-stu-id="b47cd-124">-State</span></span>
<span data-ttu-id="b47cd-125">Azt az új értéket adja meg, amelyre a parancsmag frissíti az ajánlott művelet állapotát.</span><span class="sxs-lookup"><span data-stu-id="b47cd-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="b47cd-126">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="b47cd-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b47cd-127">Aktív</span><span class="sxs-lookup"><span data-stu-id="b47cd-127">Active</span></span>
- <span data-ttu-id="b47cd-128">Függőben</span><span class="sxs-lookup"><span data-stu-id="b47cd-128">Pending</span></span>
- <span data-ttu-id="b47cd-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="b47cd-129">PendingRevert</span></span>
- <span data-ttu-id="b47cd-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="b47cd-130">RevertCancelled</span></span>
- <span data-ttu-id="b47cd-131">Figyelmen kívül hagyva</span><span class="sxs-lookup"><span data-stu-id="b47cd-131">Ignored</span></span>
- <span data-ttu-id="b47cd-132">Megoldva</span><span class="sxs-lookup"><span data-stu-id="b47cd-132">Resolved</span></span>

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

### <span data-ttu-id="b47cd-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b47cd-133">-Confirm</span></span>
<span data-ttu-id="b47cd-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b47cd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b47cd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b47cd-135">-WhatIf</span></span>
<span data-ttu-id="b47cd-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b47cd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b47cd-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b47cd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b47cd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47cd-138">CommonParameters</span></span>
<span data-ttu-id="b47cd-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b47cd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47cd-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b47cd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47cd-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b47cd-141">INPUTS</span></span>

### <span data-ttu-id="b47cd-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b47cd-142">System.String</span></span>

### <span data-ttu-id="b47cd-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b47cd-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="b47cd-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b47cd-144">OUTPUTS</span></span>

### <span data-ttu-id="b47cd-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecombaseActionModel</span><span class="sxs-lookup"><span data-stu-id="b47cd-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="b47cd-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b47cd-146">NOTES</span></span>
* <span data-ttu-id="b47cd-147">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, adatbázis, mssql, tanácsadó, ajánlottaction</span><span class="sxs-lookup"><span data-stu-id="b47cd-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="b47cd-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b47cd-148">RELATED LINKS</span></span>

[<span data-ttu-id="b47cd-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b47cd-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="b47cd-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="b47cd-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="b47cd-151">Get-AzSqlServerRecomsqlAction</span><span class="sxs-lookup"><span data-stu-id="b47cd-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="b47cd-152">Get-AzSqlElasticPoolRecomasticAction</span><span class="sxs-lookup"><span data-stu-id="b47cd-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="b47cd-153">Set-AzSqlElasticPoolRecomstateActionState</span><span class="sxs-lookup"><span data-stu-id="b47cd-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="b47cd-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b47cd-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="b47cd-155">Set-AzSqlElasticPoolRecomstateActionState</span><span class="sxs-lookup"><span data-stu-id="b47cd-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="b47cd-156">Set-AzSqlServerRecomstateActionState</span><span class="sxs-lookup"><span data-stu-id="b47cd-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="b47cd-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b47cd-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="b47cd-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b47cd-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="b47cd-159">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b47cd-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
