---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 6d634760080e3fb26153b747e733369b20bc8336
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846613"
---
# <span data-ttu-id="5bf6b-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="5bf6b-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="5bf6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bf6b-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf6b-103">Frissíti az Azure SQL-adatbázis állapotát javasolt művelettel.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="5bf6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bf6b-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf6b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bf6b-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf6b-106">A **set-AzSqlDatabaseRecommendedActionState** parancsmag frissíti az Azure SQL-adatbázis állapotát javasolt művelettel.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="5bf6b-107">Ez lehetővé teszi, hogy egy javasolt művelet alkalmazása, visszahelyezése vagy eldobása az új állapot alapján.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="5bf6b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5bf6b-108">EXAMPLES</span></span>

### <span data-ttu-id="5bf6b-109">1. példa: javasolt műveleti állapot alkalmazása függőben</span><span class="sxs-lookup"><span data-stu-id="5bf6b-109">Example 1: Apply a recommended action state to pending</span></span>
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

<span data-ttu-id="5bf6b-110">Ez a parancs frissíti a IR_ nevű \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 a függőben WIRunner nevű adatbázishoz tartozó állapotot.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="5bf6b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bf6b-111">PARAMETERS</span></span>

### <span data-ttu-id="5bf6b-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="5bf6b-112">-AdvisorName</span></span>
<span data-ttu-id="5bf6b-113">Annak a tanácsadónak a nevét adja meg, amelyhez az ajánlott tevékenység tartozik.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="5bf6b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5bf6b-114">-DatabaseName</span></span>
<span data-ttu-id="5bf6b-115">Annak az adatbázisnak a neve, amelyhez a parancsmag a javasolt műveleti állapotot állítja be.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="5bf6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf6b-116">-DefaultProfile</span></span>
<span data-ttu-id="5bf6b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5bf6b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bf6b-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="5bf6b-118">-RecommendedActionName</span></span>
<span data-ttu-id="5bf6b-119">Annak a javasolt tevékenységnek a nevét adja meg, amelynek a állapotát frissítik.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="5bf6b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf6b-120">-ResourceGroupName</span></span>
<span data-ttu-id="5bf6b-121">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="5bf6b-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5bf6b-122">-ServerName</span></span>
<span data-ttu-id="5bf6b-123">Annak a kiszolgálónak a nevét adja meg, amelyen az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="5bf6b-124">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="5bf6b-124">-State</span></span>
<span data-ttu-id="5bf6b-125">Azt az új értéket adja meg, amelyre a parancsmag a javasolt műveleti állapotot frissíti.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="5bf6b-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5bf6b-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5bf6b-127">Active</span><span class="sxs-lookup"><span data-stu-id="5bf6b-127">Active</span></span>
- <span data-ttu-id="5bf6b-128">Függőben</span><span class="sxs-lookup"><span data-stu-id="5bf6b-128">Pending</span></span>
- <span data-ttu-id="5bf6b-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="5bf6b-129">PendingRevert</span></span>
- <span data-ttu-id="5bf6b-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="5bf6b-130">RevertCancelled</span></span>
- <span data-ttu-id="5bf6b-131">Hagyva</span><span class="sxs-lookup"><span data-stu-id="5bf6b-131">Ignored</span></span>
- <span data-ttu-id="5bf6b-132">Megoldódott</span><span class="sxs-lookup"><span data-stu-id="5bf6b-132">Resolved</span></span>

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

### <span data-ttu-id="5bf6b-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5bf6b-133">-Confirm</span></span>
<span data-ttu-id="5bf6b-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf6b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf6b-135">-WhatIf</span></span>
<span data-ttu-id="5bf6b-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf6b-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf6b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf6b-138">CommonParameters</span></span>
<span data-ttu-id="5bf6b-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bf6b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf6b-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5bf6b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf6b-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bf6b-141">INPUTS</span></span>

### <span data-ttu-id="5bf6b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5bf6b-142">System.String</span></span>

### <span data-ttu-id="5bf6b-143">Microsoft. Azure. Command. SQL. RecommendedAction. parancsmag. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="5bf6b-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="5bf6b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bf6b-144">OUTPUTS</span></span>

### <span data-ttu-id="5bf6b-145">Microsoft. Azure. Command. SQL. RecommendedAction. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="5bf6b-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="5bf6b-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bf6b-146">NOTES</span></span>
* <span data-ttu-id="5bf6b-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, Database, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="5bf6b-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="5bf6b-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bf6b-148">RELATED LINKS</span></span>

[<span data-ttu-id="5bf6b-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="5bf6b-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="5bf6b-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="5bf6b-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="5bf6b-151">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="5bf6b-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="5bf6b-152">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="5bf6b-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="5bf6b-153">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="5bf6b-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="5bf6b-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="5bf6b-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="5bf6b-155">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="5bf6b-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="5bf6b-156">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="5bf6b-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="5bf6b-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="5bf6b-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="5bf6b-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="5bf6b-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="5bf6b-159">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="5bf6b-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
