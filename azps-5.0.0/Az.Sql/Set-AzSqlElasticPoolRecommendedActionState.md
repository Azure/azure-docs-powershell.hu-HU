---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194498"
---
# <span data-ttu-id="2fbef-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="2fbef-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="2fbef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2fbef-102">SYNOPSIS</span></span>
<span data-ttu-id="2fbef-103">Frissíti az Azure SQL rugalmas készlet állapotát javasolt művelet állapotát.</span><span class="sxs-lookup"><span data-stu-id="2fbef-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="2fbef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2fbef-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fbef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2fbef-105">DESCRIPTION</span></span>
<span data-ttu-id="2fbef-106">A **set-AzSqlElasticPoolRecommendedActionState** parancsmag frissíti az Azure SQL rugalmas készlet javasolt műveletének állapotát.</span><span class="sxs-lookup"><span data-stu-id="2fbef-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="2fbef-107">Ez a parancsmag az új állapoton alapuló javasolt műveleteket alkalmazza, visszaállította vagy elveti.</span><span class="sxs-lookup"><span data-stu-id="2fbef-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="2fbef-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2fbef-108">EXAMPLES</span></span>

### <span data-ttu-id="2fbef-109">Példa 1: a javasolt művelet állapotának frissítése függőben</span><span class="sxs-lookup"><span data-stu-id="2fbef-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ElasticPoolName            : WIRunnerPool
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

<span data-ttu-id="2fbef-110">Ez a parancs frissíti a rugalmas alkalmazáskészlet IR_ \[ test_schema \] _ \[ Test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 függőben állapotot.</span><span class="sxs-lookup"><span data-stu-id="2fbef-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="2fbef-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2fbef-111">PARAMETERS</span></span>

### <span data-ttu-id="2fbef-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="2fbef-112">-AdvisorName</span></span>
<span data-ttu-id="2fbef-113">Annak a tanácsadónak a nevét adja meg, amelyhez az ajánlott tevékenység tartozik.</span><span class="sxs-lookup"><span data-stu-id="2fbef-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="2fbef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fbef-114">-DefaultProfile</span></span>
<span data-ttu-id="2fbef-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2fbef-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fbef-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2fbef-116">-ElasticPoolName</span></span>
<span data-ttu-id="2fbef-117">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fbef-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="2fbef-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="2fbef-118">-RecommendedActionName</span></span>
<span data-ttu-id="2fbef-119">Annak a javasolt tevékenységnek a neve, amelyhez a parancsmag frissíti az államot.</span><span class="sxs-lookup"><span data-stu-id="2fbef-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="2fbef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fbef-120">-ResourceGroupName</span></span>
<span data-ttu-id="2fbef-121">Annak a kiszolgálónak az erőforráscsoport nevét adja meg, amely a rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2fbef-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="2fbef-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2fbef-122">-ServerName</span></span>
<span data-ttu-id="2fbef-123">Annak a kiszolgálónak a nevét adja meg, ahol a rugalmas készlet be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="2fbef-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="2fbef-124">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="2fbef-124">-State</span></span>
<span data-ttu-id="2fbef-125">Azt az értéket adja meg, amelyre a parancsmag a javasolt műveleti állapotot frissíti.</span><span class="sxs-lookup"><span data-stu-id="2fbef-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="2fbef-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2fbef-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2fbef-127">Active</span><span class="sxs-lookup"><span data-stu-id="2fbef-127">Active</span></span>
- <span data-ttu-id="2fbef-128">Függőben</span><span class="sxs-lookup"><span data-stu-id="2fbef-128">Pending</span></span>
- <span data-ttu-id="2fbef-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="2fbef-129">PendingRevert</span></span>
- <span data-ttu-id="2fbef-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="2fbef-130">RevertCancelled</span></span>
- <span data-ttu-id="2fbef-131">Hagyva</span><span class="sxs-lookup"><span data-stu-id="2fbef-131">Ignored</span></span>
- <span data-ttu-id="2fbef-132">Megoldódott</span><span class="sxs-lookup"><span data-stu-id="2fbef-132">Resolved</span></span>

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

### <span data-ttu-id="2fbef-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2fbef-133">-Confirm</span></span>
<span data-ttu-id="2fbef-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2fbef-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fbef-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fbef-135">-WhatIf</span></span>
<span data-ttu-id="2fbef-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2fbef-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fbef-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2fbef-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fbef-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fbef-138">CommonParameters</span></span>
<span data-ttu-id="2fbef-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2fbef-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fbef-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2fbef-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fbef-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fbef-141">INPUTS</span></span>

### <span data-ttu-id="2fbef-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2fbef-142">System.String</span></span>

### <span data-ttu-id="2fbef-143">Microsoft. Azure. Command. SQL. RecommendedAction. parancsmag. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="2fbef-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="2fbef-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fbef-144">OUTPUTS</span></span>

### <span data-ttu-id="2fbef-145">Microsoft. Azure. Command. SQL. RecommendedAction. Model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="2fbef-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="2fbef-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2fbef-146">NOTES</span></span>
* <span data-ttu-id="2fbef-147">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, elasticpool, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="2fbef-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="2fbef-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fbef-148">RELATED LINKS</span></span>

[<span data-ttu-id="2fbef-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="2fbef-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="2fbef-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="2fbef-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="2fbef-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="2fbef-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="2fbef-152">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2fbef-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)