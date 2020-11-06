---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 992dc949ec4c17529415beeeb2cf2a831d4d2a68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494274"
---
# <span data-ttu-id="cd93b-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="cd93b-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="cd93b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd93b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd93b-103">Frissíti az Azure SQL rugalmas készlet állapotát javasolt művelet állapotát.</span><span class="sxs-lookup"><span data-stu-id="cd93b-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd93b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd93b-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd93b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd93b-105">DESCRIPTION</span></span>
<span data-ttu-id="cd93b-106">A **set-AzureRmSqlElasticPoolRecommendedActionState** parancsmag frissíti az Azure SQL rugalmas készlet javasolt műveletének állapotát.</span><span class="sxs-lookup"><span data-stu-id="cd93b-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="cd93b-107">Ez a parancsmag az új állapoton alapuló javasolt műveleteket alkalmazza, visszaállította vagy elveti.</span><span class="sxs-lookup"><span data-stu-id="cd93b-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="cd93b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cd93b-108">EXAMPLES</span></span>

### <span data-ttu-id="cd93b-109">Példa 1: a javasolt művelet állapotának frissítése függőben</span><span class="sxs-lookup"><span data-stu-id="cd93b-109">Example 1: Update the state of a recommended action to Pending</span></span>
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

<span data-ttu-id="cd93b-110">Ez a parancs frissíti a rugalmas alkalmazáskészlet IR_ \[ test_schema \] _ \[ Test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 függőben állapotot.</span><span class="sxs-lookup"><span data-stu-id="cd93b-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="cd93b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd93b-111">PARAMETERS</span></span>

### <span data-ttu-id="cd93b-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="cd93b-112">-AdvisorName</span></span>
<span data-ttu-id="cd93b-113">Annak a tanácsadónak a nevét adja meg, amelyhez az ajánlott tevékenység tartozik.</span><span class="sxs-lookup"><span data-stu-id="cd93b-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd93b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd93b-114">-DefaultProfile</span></span>
<span data-ttu-id="cd93b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cd93b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd93b-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="cd93b-116">-ElasticPoolName</span></span>
<span data-ttu-id="cd93b-117">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd93b-117">Specifies name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd93b-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="cd93b-118">-RecommendedActionName</span></span>
<span data-ttu-id="cd93b-119">Annak a javasolt tevékenységnek a neve, amelyhez a parancsmag frissíti az államot.</span><span class="sxs-lookup"><span data-stu-id="cd93b-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd93b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd93b-120">-ResourceGroupName</span></span>
<span data-ttu-id="cd93b-121">Annak a kiszolgálónak az erőforráscsoport nevét adja meg, amely a rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cd93b-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd93b-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="cd93b-122">-ServerName</span></span>
<span data-ttu-id="cd93b-123">Annak a kiszolgálónak a nevét adja meg, ahol a rugalmas készlet be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="cd93b-123">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd93b-124">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="cd93b-124">-State</span></span>
<span data-ttu-id="cd93b-125">Azt az értéket adja meg, amelyre a parancsmag a javasolt műveleti állapotot frissíti.</span><span class="sxs-lookup"><span data-stu-id="cd93b-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="cd93b-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="cd93b-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cd93b-127">Active</span><span class="sxs-lookup"><span data-stu-id="cd93b-127">Active</span></span>
- <span data-ttu-id="cd93b-128">Függőben</span><span class="sxs-lookup"><span data-stu-id="cd93b-128">Pending</span></span>
- <span data-ttu-id="cd93b-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="cd93b-129">PendingRevert</span></span>
- <span data-ttu-id="cd93b-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="cd93b-130">RevertCancelled</span></span>
- <span data-ttu-id="cd93b-131">Hagyva</span><span class="sxs-lookup"><span data-stu-id="cd93b-131">Ignored</span></span>
- <span data-ttu-id="cd93b-132">Megoldódott</span><span class="sxs-lookup"><span data-stu-id="cd93b-132">Resolved</span></span>

```yaml
Type: RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd93b-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cd93b-133">-Confirm</span></span>
<span data-ttu-id="cd93b-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cd93b-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd93b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd93b-135">-WhatIf</span></span>
<span data-ttu-id="cd93b-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cd93b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd93b-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd93b-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd93b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd93b-138">CommonParameters</span></span>
<span data-ttu-id="cd93b-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd93b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd93b-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd93b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd93b-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd93b-141">INPUTS</span></span>

### <span data-ttu-id="cd93b-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="cd93b-142">None</span></span>
<span data-ttu-id="cd93b-143">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cd93b-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd93b-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd93b-144">OUTPUTS</span></span>

## <span data-ttu-id="cd93b-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd93b-145">NOTES</span></span>
* <span data-ttu-id="cd93b-146">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, elasticpool, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="cd93b-146">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="cd93b-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd93b-147">RELATED LINKS</span></span>

[<span data-ttu-id="cd93b-148">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="cd93b-148">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="cd93b-149">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="cd93b-149">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="cd93b-150">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="cd93b-150">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="cd93b-151">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="cd93b-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
