---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3FC9E586-3962-437E-B89F-BB4EA1FBF403
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendedAction.md
ms.openlocfilehash: 1b7f309aca65683bc9a15784f07ec2fbda4c66c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494888"
---
# <span data-ttu-id="6f22d-101">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="6f22d-101">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>

## <span data-ttu-id="6f22d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f22d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f22d-103">Egy vagy több javasolt műveletet kap egy Azure SQL elasztikus Pool tanácsadóban.</span><span class="sxs-lookup"><span data-stu-id="6f22d-103">Gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f22d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f22d-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f22d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f22d-105">DESCRIPTION</span></span>
<span data-ttu-id="6f22d-106">A **Get-AzureRmSqlElasticPoolRecommendedAction** parancsmag egy vagy több ajánlott műveletet kap egy Azure SQL elasztikus Pool tanácsadóban.</span><span class="sxs-lookup"><span data-stu-id="6f22d-106">The **Get-AzureRmSqlElasticPoolRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="6f22d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6f22d-107">EXAMPLES</span></span>

### <span data-ttu-id="6f22d-108">Példa 1: egy tanácsadó összes ajánlott műveletének listázása</span><span class="sxs-lookup"><span data-stu-id="6f22d-108">Example 1: List all recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
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

ElasticPoolName            : WIRunnerPool
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

ElasticPoolName            : WIRunnerPool
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

<span data-ttu-id="6f22d-109">Ez a parancs felsorolja a CreateIndex nevű tanácsadó által az WIRunnerPool nevű rugalmas készlethez elérhető összes javasolt műveletet.</span><span class="sxs-lookup"><span data-stu-id="6f22d-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="6f22d-110">2. példa: egyetlen ajánlott művelet beszerzése egy tanácsadó számára</span><span class="sxs-lookup"><span data-stu-id="6f22d-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="6f22d-111">Ez a parancs \[ beolvassa a IR_ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 a CreateIndex nevű tanácsadóból.</span><span class="sxs-lookup"><span data-stu-id="6f22d-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="6f22d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f22d-112">PARAMETERS</span></span>

### <span data-ttu-id="6f22d-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="6f22d-113">-AdvisorName</span></span>
<span data-ttu-id="6f22d-114">Annak a tanácsadónak a nevét adja meg, amelyhez a parancsmag ajánlott műveleteket kér.</span><span class="sxs-lookup"><span data-stu-id="6f22d-114">Specifies the name of the advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="6f22d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f22d-115">-DefaultProfile</span></span>
<span data-ttu-id="6f22d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6f22d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f22d-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6f22d-117">-ElasticPoolName</span></span>
<span data-ttu-id="6f22d-118">Annak a rugalmas készletnek a neve, amelyhez a parancsmag az ajánlott műveleteket kéri.</span><span class="sxs-lookup"><span data-stu-id="6f22d-118">Specifies the name of the elastic pool for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="6f22d-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="6f22d-119">-RecommendedActionName</span></span>
<span data-ttu-id="6f22d-120">Annak a javasolt tevékenységnek a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="6f22d-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6f22d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f22d-121">-ResourceGroupName</span></span>
<span data-ttu-id="6f22d-122">Annak a kiszolgálónak az erőforráscsoport nevét adja meg, amely a rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6f22d-122">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="6f22d-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6f22d-123">-ServerName</span></span>
<span data-ttu-id="6f22d-124">Annak a kiszolgálónak a nevét adja meg, ahol a rugalmas készlet be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="6f22d-124">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="6f22d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f22d-125">CommonParameters</span></span>
<span data-ttu-id="6f22d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f22d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f22d-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f22d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f22d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f22d-128">INPUTS</span></span>

### <span data-ttu-id="6f22d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6f22d-129">System.String</span></span>

## <span data-ttu-id="6f22d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f22d-130">OUTPUTS</span></span>

### <span data-ttu-id="6f22d-131">Microsoft. Azure. Command. SQL. RecommendedAction. Model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="6f22d-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="6f22d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f22d-132">NOTES</span></span>
* <span data-ttu-id="6f22d-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, elasticpool, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="6f22d-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="6f22d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f22d-134">RELATED LINKS</span></span>

[<span data-ttu-id="6f22d-135">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="6f22d-135">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="6f22d-136">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="6f22d-136">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="6f22d-137">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="6f22d-137">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="6f22d-138">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="6f22d-138">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="6f22d-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6f22d-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
