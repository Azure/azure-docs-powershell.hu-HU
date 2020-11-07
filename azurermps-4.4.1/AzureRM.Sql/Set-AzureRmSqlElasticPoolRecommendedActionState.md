---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 1bc5d89a381027bd72697d873308eb85807a6e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679312"
---
# <span data-ttu-id="81c41-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="81c41-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="81c41-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81c41-102">SYNOPSIS</span></span>
<span data-ttu-id="81c41-103">Frissíti az Azure SQL rugalmas készlet állapotát javasolt művelet állapotát.</span><span class="sxs-lookup"><span data-stu-id="81c41-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81c41-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81c41-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c41-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81c41-105">DESCRIPTION</span></span>
<span data-ttu-id="81c41-106">A **set-AzureRmSqlElasticPoolRecommendedActionState** parancsmag frissíti az Azure SQL rugalmas készlet javasolt műveletének állapotát.</span><span class="sxs-lookup"><span data-stu-id="81c41-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="81c41-107">Ez a parancsmag az új állapoton alapuló javasolt műveleteket alkalmazza, visszaállította vagy elveti.</span><span class="sxs-lookup"><span data-stu-id="81c41-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="81c41-108">Példák</span><span class="sxs-lookup"><span data-stu-id="81c41-108">EXAMPLES</span></span>

### <span data-ttu-id="81c41-109">Példa 1: a javasolt művelet állapotának frissítése függőben</span><span class="sxs-lookup"><span data-stu-id="81c41-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="81c41-110">Ez a parancs frissíti a rugalmas alkalmazáskészlet IR_ \[ test_schema \] _ \[ Test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 függőben állapotot.</span><span class="sxs-lookup"><span data-stu-id="81c41-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="81c41-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81c41-111">PARAMETERS</span></span>

### <span data-ttu-id="81c41-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="81c41-112">-AdvisorName</span></span>
<span data-ttu-id="81c41-113">Annak a tanácsadónak a nevét adja meg, amelyhez az ajánlott tevékenység tartozik.</span><span class="sxs-lookup"><span data-stu-id="81c41-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="81c41-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="81c41-114">-ElasticPoolName</span></span>
<span data-ttu-id="81c41-115">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81c41-115">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="81c41-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="81c41-116">-RecommendedActionName</span></span>
<span data-ttu-id="81c41-117">Annak a javasolt tevékenységnek a neve, amelyhez a parancsmag frissíti az államot.</span><span class="sxs-lookup"><span data-stu-id="81c41-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="81c41-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c41-118">-ResourceGroupName</span></span>
<span data-ttu-id="81c41-119">Annak a kiszolgálónak az erőforráscsoport nevét adja meg, amely a rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="81c41-119">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="81c41-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="81c41-120">-ServerName</span></span>
<span data-ttu-id="81c41-121">Annak a kiszolgálónak a nevét adja meg, ahol a rugalmas készlet be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="81c41-121">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="81c41-122">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="81c41-122">-State</span></span>
<span data-ttu-id="81c41-123">Azt az értéket adja meg, amelyre a parancsmag a javasolt műveleti állapotot frissíti.</span><span class="sxs-lookup"><span data-stu-id="81c41-123">Specifies the value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="81c41-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="81c41-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81c41-125">Active</span><span class="sxs-lookup"><span data-stu-id="81c41-125">Active</span></span>
- <span data-ttu-id="81c41-126">Függőben</span><span class="sxs-lookup"><span data-stu-id="81c41-126">Pending</span></span>
- <span data-ttu-id="81c41-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="81c41-127">PendingRevert</span></span>
- <span data-ttu-id="81c41-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="81c41-128">RevertCancelled</span></span>
- <span data-ttu-id="81c41-129">Hagyva</span><span class="sxs-lookup"><span data-stu-id="81c41-129">Ignored</span></span>
- <span data-ttu-id="81c41-130">Megoldódott</span><span class="sxs-lookup"><span data-stu-id="81c41-130">Resolved</span></span>

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

### <span data-ttu-id="81c41-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81c41-131">-Confirm</span></span>
<span data-ttu-id="81c41-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81c41-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c41-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c41-133">-WhatIf</span></span>
<span data-ttu-id="81c41-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81c41-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81c41-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81c41-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c41-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c41-136">-DefaultProfile</span></span>
<span data-ttu-id="81c41-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81c41-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c41-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c41-138">CommonParameters</span></span>
<span data-ttu-id="81c41-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81c41-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c41-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c41-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c41-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81c41-141">INPUTS</span></span>

## <span data-ttu-id="81c41-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81c41-142">OUTPUTS</span></span>

## <span data-ttu-id="81c41-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81c41-143">NOTES</span></span>
* <span data-ttu-id="81c41-144">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, elasticpool, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="81c41-144">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="81c41-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81c41-145">RELATED LINKS</span></span>

[<span data-ttu-id="81c41-146">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="81c41-146">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="81c41-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="81c41-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="81c41-148">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="81c41-148">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="81c41-149">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="81c41-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
