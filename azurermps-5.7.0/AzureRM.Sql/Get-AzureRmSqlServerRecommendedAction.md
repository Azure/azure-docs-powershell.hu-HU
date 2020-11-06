---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BB513A53-48A0-4F8F-93F0-D3DFA2C3D523
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerRecommendedAction.md
ms.openlocfilehash: a3fa15b75e2bb8bd8794703a02cede34e534be31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492131"
---
# <span data-ttu-id="24a30-101">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="24a30-101">Get-AzureRmSqlServerRecommendedAction</span></span>

## <span data-ttu-id="24a30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24a30-102">SYNOPSIS</span></span>
<span data-ttu-id="24a30-103">Egy vagy több javasolt műveletet kap az Azure SQL Server-tanácsadóban.</span><span class="sxs-lookup"><span data-stu-id="24a30-103">Gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24a30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24a30-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -AdvisorName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24a30-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="24a30-105">DESCRIPTION</span></span>
<span data-ttu-id="24a30-106">A **Get-AzureRmSqlServerRecommendedAction** parancsmag legalább egy javasolt műveletet kap az Azure SQL Server-tanácsadók számára.</span><span class="sxs-lookup"><span data-stu-id="24a30-106">The **Get-AzureRmSqlServerRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="24a30-107">Példák</span><span class="sxs-lookup"><span data-stu-id="24a30-107">EXAMPLES</span></span>

### <span data-ttu-id="24a30-108">Példa 1: egy adott tanácsadó összes javasolt műveletének beszerzése</span><span class="sxs-lookup"><span data-stu-id="24a30-108">Example 1: Get a list of  all recommended actions for a specific Advisor</span></span>
```
PS C:\>Get-AzureRmSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="24a30-109">Ez a parancs felsorolja az CreateIndex nevű SQL Server-tanácsadó által az összes javasolt műveletet, amely a Wi-Runner-Ausztrália-Kelet nevű kiszolgálón elérhető.</span><span class="sxs-lookup"><span data-stu-id="24a30-109">This command gets a list of all recommended actions of for the SQL Server Advisor named CreateIndex available for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="24a30-110">2. példa: egyetlen ajánlott művelet beszerzése egy tanácsadó számára</span><span class="sxs-lookup"><span data-stu-id="24a30-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName 
IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
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

<span data-ttu-id="24a30-111">Ez a parancs IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 a CreateIndex nevű tanácsadótól kapja meg.</span><span class="sxs-lookup"><span data-stu-id="24a30-111">This command gets a recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="24a30-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24a30-112">PARAMETERS</span></span>

### <span data-ttu-id="24a30-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="24a30-113">-AdvisorName</span></span>
<span data-ttu-id="24a30-114">Annak a tanácsadónak a nevét adja meg, amelynek a parancsmagja a műveleteket kéri.</span><span class="sxs-lookup"><span data-stu-id="24a30-114">Specifies the name of the advisor for which this cmdlet requests actions.</span></span>

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

### <span data-ttu-id="24a30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a30-115">-DefaultProfile</span></span>
<span data-ttu-id="24a30-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="24a30-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24a30-117">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="24a30-117">-RecommendedActionName</span></span>
<span data-ttu-id="24a30-118">Annak a javasolt tevékenységnek a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="24a30-118">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a30-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a30-119">-ResourceGroupName</span></span>
<span data-ttu-id="24a30-120">A kiszolgálót tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="24a30-120">Specifies the name of the resource group of the server that contains this server.</span></span>

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

### <span data-ttu-id="24a30-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="24a30-121">-ServerName</span></span>
<span data-ttu-id="24a30-122">Annak a kiszolgálónak a neve, amelyhez a tanácsadó tartozik.</span><span class="sxs-lookup"><span data-stu-id="24a30-122">Specifies the name of the server the Advisor belongs to.</span></span>

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

### <span data-ttu-id="24a30-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a30-123">CommonParameters</span></span>
<span data-ttu-id="24a30-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24a30-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a30-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a30-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a30-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a30-126">INPUTS</span></span>

### <span data-ttu-id="24a30-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="24a30-127">None</span></span>
<span data-ttu-id="24a30-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="24a30-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24a30-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a30-129">OUTPUTS</span></span>

### <span data-ttu-id="24a30-130">Microsoft. Azure. Command. SQL. RecommendedAction. Model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="24a30-130">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="24a30-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24a30-131">NOTES</span></span>
* <span data-ttu-id="24a30-132">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, Server, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="24a30-132">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="24a30-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24a30-133">RELATED LINKS</span></span>

[<span data-ttu-id="24a30-134">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="24a30-134">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="24a30-135">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="24a30-135">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="24a30-136">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="24a30-136">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="24a30-137">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="24a30-137">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="24a30-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="24a30-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
