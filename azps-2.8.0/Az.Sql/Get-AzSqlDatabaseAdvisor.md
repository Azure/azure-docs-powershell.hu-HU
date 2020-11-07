---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: 514a10788c28edacbca53dc8135c8d071aaff56b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839316"
---
# <span data-ttu-id="79004-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="79004-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="79004-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79004-102">SYNOPSIS</span></span>
<span data-ttu-id="79004-103">Egy vagy több tanácsadót kap egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="79004-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="79004-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79004-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79004-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="79004-105">DESCRIPTION</span></span>
<span data-ttu-id="79004-106">A **Get-AzSqlDatabaseAdvisor** parancsmag egy vagy több Azure SQL-adatbázis-tanácsadót kap egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="79004-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="79004-107">Példák</span><span class="sxs-lookup"><span data-stu-id="79004-107">EXAMPLES</span></span>

### <span data-ttu-id="79004-108">Példa 1: a megadott adatbázis összes tanácsadójának listázása</span><span class="sxs-lookup"><span data-stu-id="79004-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="79004-109">Ez a parancs megjeleníti a WIRunner nevű adatbázis összes tanácsadóját, amely a Wi-Runner-Ausztrália-Kelet nevű kiszolgálóhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="79004-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="79004-110">2. példa: a megadott adatbázis egyetlen tanácsadójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="79004-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="79004-111">Ez a parancs a CreateIndex nevű tanácsadót kapja a WIRunner nevű adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="79004-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="79004-112">3. példa: az összes tanácsadó felsorolása a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="79004-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="79004-113">Ez a parancs beilleszti az "WIRunner" nevű adatbázis összes tanácsadóját a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="79004-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="79004-114">Mivel a parancs a *ExpandRecommendedActions* paramétert használja, a parancsmag az ajánlott műveleteket kapja meg a válaszsal.</span><span class="sxs-lookup"><span data-stu-id="79004-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="79004-115">Példa 4: egyetlen tanácsadó beszerzése a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="79004-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="79004-116">Ez a parancs a CreateIndex nevű tanácsadót a WIRunner nevű adatbázisból kapja meg a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="79004-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="79004-117">Mivel a parancs a *ExpandRecommendedActions* paramétert használja, a parancsmag az ajánlott műveleteket kapja meg a válaszsal.</span><span class="sxs-lookup"><span data-stu-id="79004-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="79004-118">Példa 5: a megadott adatbázis összes tanácsadójának listázása szűréssel</span><span class="sxs-lookup"><span data-stu-id="79004-118">Example 5: List all the advisors for the specified database using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName d*
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
```

<span data-ttu-id="79004-119">Ez a parancs megjeleníti a WIRunner nevű adatbázis összes tanácsadóját, amely a Wi-Runner-Ausztrália-Kelet nevű kiszolgálóhoz tartozik, és a "d" betűvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="79004-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="79004-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79004-120">PARAMETERS</span></span>

### <span data-ttu-id="79004-121">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="79004-121">-AdvisorName</span></span>
<span data-ttu-id="79004-122">Annak a tanácsadónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="79004-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="79004-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79004-123">-DatabaseName</span></span>
<span data-ttu-id="79004-124">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja a tanácsadót kéri.</span><span class="sxs-lookup"><span data-stu-id="79004-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="79004-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79004-125">-DefaultProfile</span></span>
<span data-ttu-id="79004-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="79004-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79004-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="79004-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="79004-128">Azt jelzi, hogy ez a parancsmag az ajánlott műveleteket kapja meg a válaszsal.</span><span class="sxs-lookup"><span data-stu-id="79004-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79004-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79004-129">-ResourceGroupName</span></span>
<span data-ttu-id="79004-130">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79004-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="79004-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="79004-131">-ServerName</span></span>
<span data-ttu-id="79004-132">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79004-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="79004-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79004-133">CommonParameters</span></span>
<span data-ttu-id="79004-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79004-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79004-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="79004-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79004-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79004-136">INPUTS</span></span>

### <span data-ttu-id="79004-137">System. String</span><span class="sxs-lookup"><span data-stu-id="79004-137">System.String</span></span>

### <span data-ttu-id="79004-138">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="79004-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="79004-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79004-139">OUTPUTS</span></span>

### <span data-ttu-id="79004-140">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="79004-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="79004-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79004-141">NOTES</span></span>
* <span data-ttu-id="79004-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, Database, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="79004-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="79004-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79004-143">RELATED LINKS</span></span>

[<span data-ttu-id="79004-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="79004-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="79004-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="79004-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="79004-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="79004-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="79004-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="79004-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="79004-148">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="79004-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
