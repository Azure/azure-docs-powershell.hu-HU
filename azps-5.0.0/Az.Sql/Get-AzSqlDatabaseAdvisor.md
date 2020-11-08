---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: 05bde2ee8a5bbcae941203115c49ff6b9fbc6bae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186695"
---
# <span data-ttu-id="d99b1-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="d99b1-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="d99b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d99b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d99b1-103">Egy vagy több tanácsadót kap egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="d99b1-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="d99b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d99b1-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d99b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d99b1-105">DESCRIPTION</span></span>
<span data-ttu-id="d99b1-106">A **Get-AzSqlDatabaseAdvisor** parancsmag egy vagy több Azure SQL-adatbázis-tanácsadót kap egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="d99b1-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="d99b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d99b1-107">EXAMPLES</span></span>

### <span data-ttu-id="d99b1-108">Példa 1: a megadott adatbázis összes tanácsadójának listázása</span><span class="sxs-lookup"><span data-stu-id="d99b1-108">Example 1: List all the advisors for the specified database</span></span>
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

<span data-ttu-id="d99b1-109">Ez a parancs megjeleníti a WIRunner nevű adatbázis összes tanácsadóját, amely a Wi-Runner-Ausztrália-Kelet nevű kiszolgálóhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="d99b1-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="d99b1-110">2. példa: a megadott adatbázis egyetlen tanácsadójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d99b1-110">Example 2: Get a single advisor for the specified database</span></span>
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

<span data-ttu-id="d99b1-111">Ez a parancs a CreateIndex nevű tanácsadót kapja a WIRunner nevű adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="d99b1-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="d99b1-112">3. példa: az összes tanácsadó felsorolása a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="d99b1-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="d99b1-113">Ez a parancs beilleszti az "WIRunner" nevű adatbázis összes tanácsadóját a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="d99b1-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="d99b1-114">Mivel a parancs a *ExpandRecommendedActions* paramétert használja, a parancsmag az ajánlott műveleteket kapja meg a válaszsal.</span><span class="sxs-lookup"><span data-stu-id="d99b1-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="d99b1-115">Példa 4: egyetlen tanácsadó beszerzése a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="d99b1-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="d99b1-116">Ez a parancs a CreateIndex nevű tanácsadót a WIRunner nevű adatbázisból kapja meg a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="d99b1-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="d99b1-117">Mivel a parancs a *ExpandRecommendedActions* paramétert használja, a parancsmag az ajánlott műveleteket kapja meg a válaszsal.</span><span class="sxs-lookup"><span data-stu-id="d99b1-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="d99b1-118">Példa 5: a megadott adatbázis összes tanácsadójának listázása szűréssel</span><span class="sxs-lookup"><span data-stu-id="d99b1-118">Example 5: List all the advisors for the specified database using filtering</span></span>
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

<span data-ttu-id="d99b1-119">Ez a parancs megjeleníti a WIRunner nevű adatbázis összes tanácsadóját, amely a Wi-Runner-Ausztrália-Kelet nevű kiszolgálóhoz tartozik, és a "d" betűvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="d99b1-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="d99b1-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d99b1-120">PARAMETERS</span></span>

### <span data-ttu-id="d99b1-121">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="d99b1-121">-AdvisorName</span></span>
<span data-ttu-id="d99b1-122">Annak a tanácsadónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d99b1-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d99b1-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d99b1-123">-DatabaseName</span></span>
<span data-ttu-id="d99b1-124">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja a tanácsadót kéri.</span><span class="sxs-lookup"><span data-stu-id="d99b1-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="d99b1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d99b1-125">-DefaultProfile</span></span>
<span data-ttu-id="d99b1-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d99b1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d99b1-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="d99b1-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="d99b1-128">Azt jelzi, hogy ez a parancsmag az ajánlott műveleteket kapja meg a válaszsal.</span><span class="sxs-lookup"><span data-stu-id="d99b1-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="d99b1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d99b1-129">-ResourceGroupName</span></span>
<span data-ttu-id="d99b1-130">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d99b1-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="d99b1-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d99b1-131">-ServerName</span></span>
<span data-ttu-id="d99b1-132">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d99b1-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="d99b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d99b1-133">CommonParameters</span></span>
<span data-ttu-id="d99b1-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d99b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d99b1-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d99b1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d99b1-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d99b1-136">INPUTS</span></span>

### <span data-ttu-id="d99b1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d99b1-137">System.String</span></span>

### <span data-ttu-id="d99b1-138">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d99b1-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d99b1-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d99b1-139">OUTPUTS</span></span>

### <span data-ttu-id="d99b1-140">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="d99b1-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="d99b1-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d99b1-141">NOTES</span></span>
* <span data-ttu-id="d99b1-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, Database, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="d99b1-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="d99b1-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d99b1-143">RELATED LINKS</span></span>

[<span data-ttu-id="d99b1-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="d99b1-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="d99b1-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="d99b1-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="d99b1-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="d99b1-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="d99b1-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d99b1-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="d99b1-148">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d99b1-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
