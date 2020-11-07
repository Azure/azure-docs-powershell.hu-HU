---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
ms.openlocfilehash: 4b000ef101b07bf882accb10b0256e0dbea513b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680743"
---
# <span data-ttu-id="4fb43-101">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4fb43-101">Set-AzureRmSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="4fb43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fb43-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb43-103">Frissíti az Azure SQL Server által javasolt műveletek állapotát.</span><span class="sxs-lookup"><span data-stu-id="4fb43-103">Updates the state of an Azure SQL Server recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fb43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fb43-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fb43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fb43-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb43-106">A **set-AzureRmSqlServerRecommendedActionState** parancsmag frissíti az Azure SQL Server által javasolt műveletek állapotát.</span><span class="sxs-lookup"><span data-stu-id="4fb43-106">The **Set-AzureRmSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="4fb43-107">Ez a parancsmag az új állapot alapján az ajánlott lépéseket alkalmazza, visszaállítja vagy elveti.</span><span class="sxs-lookup"><span data-stu-id="4fb43-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="4fb43-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4fb43-108">EXAMPLES</span></span>

### <span data-ttu-id="4fb43-109">Example1: a megadott javasolt tevékenység állapotának frissítése függőben</span><span class="sxs-lookup"><span data-stu-id="4fb43-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="4fb43-110">A kiszolgáló által javasolt "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" a "függőben" állapotú műveletek</span><span class="sxs-lookup"><span data-stu-id="4fb43-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="4fb43-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fb43-111">PARAMETERS</span></span>

### <span data-ttu-id="4fb43-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="4fb43-112">-AdvisorName</span></span>
<span data-ttu-id="4fb43-113">Az ajánlott műveleteket tartalmazó tanácsadó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fb43-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="4fb43-114">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="4fb43-114">-RecommendedActionName</span></span>
<span data-ttu-id="4fb43-115">Annak a javasolt tevékenységnek a neve, amelyhez a parancsmag frissíti az államot.</span><span class="sxs-lookup"><span data-stu-id="4fb43-115">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="4fb43-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb43-116">-ResourceGroupName</span></span>
<span data-ttu-id="4fb43-117">A kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fb43-117">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="4fb43-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4fb43-118">-ServerName</span></span>
<span data-ttu-id="4fb43-119">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fb43-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="4fb43-120">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="4fb43-120">-State</span></span>
<span data-ttu-id="4fb43-121">Azt az új értéket adja meg, amelyre a parancsmag a javasolt műveleti állapotot frissíti.</span><span class="sxs-lookup"><span data-stu-id="4fb43-121">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="4fb43-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4fb43-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fb43-123">Active</span><span class="sxs-lookup"><span data-stu-id="4fb43-123">Active</span></span>
- <span data-ttu-id="4fb43-124">Függőben</span><span class="sxs-lookup"><span data-stu-id="4fb43-124">Pending</span></span>
- <span data-ttu-id="4fb43-125">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="4fb43-125">PendingRevert</span></span>
- <span data-ttu-id="4fb43-126">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="4fb43-126">RevertCancelled</span></span>
- <span data-ttu-id="4fb43-127">Hagyva</span><span class="sxs-lookup"><span data-stu-id="4fb43-127">Ignored</span></span>
- <span data-ttu-id="4fb43-128">Megoldódott</span><span class="sxs-lookup"><span data-stu-id="4fb43-128">Resolved</span></span>

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

### <span data-ttu-id="4fb43-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4fb43-129">-Confirm</span></span>
<span data-ttu-id="4fb43-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fb43-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fb43-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fb43-131">-WhatIf</span></span>
<span data-ttu-id="4fb43-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4fb43-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fb43-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fb43-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fb43-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb43-134">-DefaultProfile</span></span>
<span data-ttu-id="4fb43-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fb43-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fb43-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb43-136">CommonParameters</span></span>
<span data-ttu-id="4fb43-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fb43-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb43-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb43-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb43-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fb43-139">INPUTS</span></span>

## <span data-ttu-id="4fb43-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fb43-140">OUTPUTS</span></span>

### <span data-ttu-id="4fb43-141">Microsoft. Azure. Command. SQL. RecommendedAction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="4fb43-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="4fb43-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fb43-142">NOTES</span></span>
* <span data-ttu-id="4fb43-143">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, Server, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="4fb43-143">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="4fb43-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fb43-144">RELATED LINKS</span></span>

[<span data-ttu-id="4fb43-145">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="4fb43-145">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="4fb43-146">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="4fb43-146">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="4fb43-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4fb43-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="4fb43-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="4fb43-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="4fb43-149">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4fb43-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
