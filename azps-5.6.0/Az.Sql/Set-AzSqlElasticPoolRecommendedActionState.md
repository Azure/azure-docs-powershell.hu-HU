---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 5ef58938342845b437d714e44a55256892632546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002950"
---
# <span data-ttu-id="7e8cc-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="7e8cc-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="7e8cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e8cc-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8cc-103">Frissíti az Ajánlott Azure SQL-rugalmassági készlet állapotát.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="7e8cc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e8cc-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e8cc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e8cc-105">DESCRIPTION</span></span>
<span data-ttu-id="7e8cc-106">A **Set-AzSqlElasticPoolRecomasticActionState** parancsmag frissíti az Azure SQL Rugalmas készlet javasolt műveletének állapotát.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="7e8cc-107">Ez a parancsmag az új állapot alapján javasolt, visszaállított vagy elvetett műveletet alkalmaz.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="7e8cc-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e8cc-108">EXAMPLES</span></span>

### <span data-ttu-id="7e8cc-109">1. példa: Az ajánlott művelet állapotának frissítése függőben lévőre</span><span class="sxs-lookup"><span data-stu-id="7e8cc-109">Example 1: Update the state of a recommended action to Pending</span></span>
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

<span data-ttu-id="7e8cc-110">Ez a parancs frissíti a rugalmas készlet javasolt IR_ \[ test_schema \] _ \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893 állapotát \] függőben van.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="7e8cc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e8cc-111">PARAMETERS</span></span>

### <span data-ttu-id="7e8cc-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="7e8cc-112">-AdvisorName</span></span>
<span data-ttu-id="7e8cc-113">Annak a tanácsadónak a nevét adja meg, amelyhez ez az ajánlott művelet tartozik.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="7e8cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8cc-114">-DefaultProfile</span></span>
<span data-ttu-id="7e8cc-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7e8cc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e8cc-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7e8cc-116">-ElasticPoolName</span></span>
<span data-ttu-id="7e8cc-117">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="7e8cc-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="7e8cc-118">-RecommendedActionName</span></span>
<span data-ttu-id="7e8cc-119">Annak az ajánlott műveletnek a nevét adja meg, amelynek a parancsmagja frissíti az állapotot.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="7e8cc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e8cc-120">-ResourceGroupName</span></span>
<span data-ttu-id="7e8cc-121">A rugalmas készletet tartalmazó kiszolgáló erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="7e8cc-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e8cc-122">-ServerName</span></span>
<span data-ttu-id="7e8cc-123">Annak a kiszolgálónak a nevét adja meg, amelynél a rugalmas készlet található.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="7e8cc-124">-State</span><span class="sxs-lookup"><span data-stu-id="7e8cc-124">-State</span></span>
<span data-ttu-id="7e8cc-125">Azt az értéket adja meg, amelynek a parancsmagja frissíti az ajánlott műveletállapotot.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="7e8cc-126">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="7e8cc-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7e8cc-127">Aktív</span><span class="sxs-lookup"><span data-stu-id="7e8cc-127">Active</span></span>
- <span data-ttu-id="7e8cc-128">Függőben</span><span class="sxs-lookup"><span data-stu-id="7e8cc-128">Pending</span></span>
- <span data-ttu-id="7e8cc-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="7e8cc-129">PendingRevert</span></span>
- <span data-ttu-id="7e8cc-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="7e8cc-130">RevertCancelled</span></span>
- <span data-ttu-id="7e8cc-131">Figyelmen kívül hagyva</span><span class="sxs-lookup"><span data-stu-id="7e8cc-131">Ignored</span></span>
- <span data-ttu-id="7e8cc-132">Megoldva</span><span class="sxs-lookup"><span data-stu-id="7e8cc-132">Resolved</span></span>

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

### <span data-ttu-id="7e8cc-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e8cc-133">-Confirm</span></span>
<span data-ttu-id="7e8cc-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e8cc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e8cc-135">-WhatIf</span></span>
<span data-ttu-id="7e8cc-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e8cc-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e8cc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8cc-138">CommonParameters</span></span>
<span data-ttu-id="7e8cc-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e8cc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8cc-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e8cc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8cc-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e8cc-141">INPUTS</span></span>

### <span data-ttu-id="7e8cc-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7e8cc-142">System.String</span></span>

### <span data-ttu-id="7e8cc-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="7e8cc-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="7e8cc-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e8cc-144">OUTPUTS</span></span>

### <span data-ttu-id="7e8cc-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecomasticActionModel</span><span class="sxs-lookup"><span data-stu-id="7e8cc-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="7e8cc-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e8cc-146">NOTES</span></span>
* <span data-ttu-id="7e8cc-147">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, rugalmasság, mssql, tanácsadó, ajánlottaction</span><span class="sxs-lookup"><span data-stu-id="7e8cc-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="7e8cc-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e8cc-148">RELATED LINKS</span></span>

[<span data-ttu-id="7e8cc-149">Get-AzSqlElasticPoolRecomasticAction</span><span class="sxs-lookup"><span data-stu-id="7e8cc-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="7e8cc-150">Set-AzSqlDatabaseRecomstateActionState</span><span class="sxs-lookup"><span data-stu-id="7e8cc-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="7e8cc-151">Set-AzSqlServerRecomstateActionState</span><span class="sxs-lookup"><span data-stu-id="7e8cc-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="7e8cc-152">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7e8cc-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
