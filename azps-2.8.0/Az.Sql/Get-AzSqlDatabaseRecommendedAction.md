---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EF6C862B-A89C-48AB-A590-92CFA387305F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRecommendedAction.md
ms.openlocfilehash: 8fe3df1a786f0263fcf618c2a385398ef193cd1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839241"
---
# <span data-ttu-id="1035d-101">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1035d-101">Get-AzSqlDatabaseRecommendedAction</span></span>

## <span data-ttu-id="1035d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1035d-102">SYNOPSIS</span></span>
<span data-ttu-id="1035d-103">Egy vagy több javasolt műveletet kap egy Azure SQL-adatbázis-tanácsadóban.</span><span class="sxs-lookup"><span data-stu-id="1035d-103">Gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="1035d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1035d-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1035d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1035d-105">DESCRIPTION</span></span>
<span data-ttu-id="1035d-106">A **Get-AzSqlDatabaseRecommendedAction** parancsmag legalább egy javasolt műveletet kap egy Azure SQL-adatbázis-tanácsadóhoz.</span><span class="sxs-lookup"><span data-stu-id="1035d-106">The **Get-AzSqlDatabaseRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="1035d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1035d-107">EXAMPLES</span></span>

### <span data-ttu-id="1035d-108">Példa 1: egy tanácsadó összes ajánlott műveletének listázása</span><span class="sxs-lookup"><span data-stu-id="1035d-108">Example 1: List all the recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.236046_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.236046]]...} 
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
ObservedImpact             : {SpaceChange}
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.239359_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.239359]]...} 
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
RevertActionDuration       : PT10S
RevertActionInitiatedBy    : System
RevertActionInitiatedTime  : 4/21/2016 3:24:47 PM
RevertActionStartTime      : 4/21/2016 3:24:47 PM
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="1035d-109">Ez a parancs a CreateIndex nevű tanácsadó által elérhető összes javasolt műveletet felsorolja a Wi-Runner-Ausztrália-Kelet nevű adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="1035d-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the database named wi-runner-australia-east.</span></span>

### <span data-ttu-id="1035d-110">2. példa: egyetlen ajánlott művelet beszerzése egy tanácsadó számára</span><span class="sxs-lookup"><span data-stu-id="1035d-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="1035d-111">Ez a parancs beolvassa a IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 a CreateIndex nevű tanácsadóhoz.</span><span class="sxs-lookup"><span data-stu-id="1035d-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 for the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="1035d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1035d-112">PARAMETERS</span></span>

### <span data-ttu-id="1035d-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="1035d-113">-AdvisorName</span></span>
<span data-ttu-id="1035d-114">Annak a tanácsadónak a nevét adja meg, amelyhez a parancsmag ajánlott műveleteket kér.</span><span class="sxs-lookup"><span data-stu-id="1035d-114">Specifies the name of the Advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="1035d-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1035d-115">-DatabaseName</span></span>
<span data-ttu-id="1035d-116">Annak az adatbázisnak a neve, amelyhez a parancsmag az ajánlott műveleteket kéri.</span><span class="sxs-lookup"><span data-stu-id="1035d-116">Specifies the name of the database for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="1035d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1035d-117">-DefaultProfile</span></span>
<span data-ttu-id="1035d-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1035d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1035d-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="1035d-119">-RecommendedActionName</span></span>
<span data-ttu-id="1035d-120">Annak a javasolt tevékenységnek a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="1035d-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1035d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1035d-121">-ResourceGroupName</span></span>
<span data-ttu-id="1035d-122">Annak a kiszolgálónak az erőforráscsoport nevét adja meg, amely az adatbázist tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1035d-122">Specifies name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="1035d-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1035d-123">-ServerName</span></span>
<span data-ttu-id="1035d-124">Annak a kiszolgálónak a nevét adja meg, amelyen az adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="1035d-124">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="1035d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1035d-125">CommonParameters</span></span>
<span data-ttu-id="1035d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1035d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1035d-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1035d-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1035d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1035d-128">INPUTS</span></span>

### <span data-ttu-id="1035d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1035d-129">System.String</span></span>

## <span data-ttu-id="1035d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1035d-130">OUTPUTS</span></span>

### <span data-ttu-id="1035d-131">Microsoft. Azure. Command. SQL. RecommendedAction. Model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="1035d-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="1035d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1035d-132">NOTES</span></span>
* <span data-ttu-id="1035d-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, Database, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="1035d-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="1035d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1035d-134">RELATED LINKS</span></span>

[<span data-ttu-id="1035d-135">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="1035d-135">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="1035d-136">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1035d-136">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="1035d-137">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1035d-137">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="1035d-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="1035d-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
