---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
ms.openlocfilehash: 75e584ba9eab2c43aba5fc6a9b5d3cd3b39adc5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494327"
---
# <span data-ttu-id="e4dee-101">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="e4dee-101">Get-AzureRmSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="e4dee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4dee-102">SYNOPSIS</span></span>
<span data-ttu-id="e4dee-103">Egy vagy több tanácsadót kap egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="e4dee-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4dee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4dee-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4dee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4dee-105">DESCRIPTION</span></span>
<span data-ttu-id="e4dee-106">A **Get-AzureRmSqlDatabaseAdvisor** parancsmag egy vagy több Azure SQL-adatbázis-tanácsadót kap egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="e4dee-106">The **Get-AzureRmSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="e4dee-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4dee-107">EXAMPLES</span></span>

### <span data-ttu-id="e4dee-108">Példa 1: a megadott adatbázis összes tanácsadójának listázása</span><span class="sxs-lookup"><span data-stu-id="e4dee-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
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

<span data-ttu-id="e4dee-109">Ez a parancs megjeleníti a WIRunner nevű adatbázis összes tanácsadóját, amely a Wi-Runner-Ausztrália-Kelet nevű kiszolgálóhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="e4dee-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="e4dee-110">2. példa: a megadott adatbázis egyetlen tanácsadójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e4dee-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

<span data-ttu-id="e4dee-111">Ez a parancs a CreateIndex nevű tanácsadót kapja a WIRunner nevű adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="e4dee-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="e4dee-112">3. példa: az összes tanácsadó felsorolása a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="e4dee-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
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

<span data-ttu-id="e4dee-113">Ez a parancs beilleszti az "WIRunner" nevű adatbázis összes tanácsadóját a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="e4dee-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="e4dee-114">Mivel a parancs a *ExpandRecommendedActions* paramétert használja, a parancsmag az ajánlott műveleteket kapja meg a válaszsal.</span><span class="sxs-lookup"><span data-stu-id="e4dee-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="e4dee-115">Példa 4: egyetlen tanácsadó beszerzése a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="e4dee-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="e4dee-116">Ez a parancs a CreateIndex nevű tanácsadót a WIRunner nevű adatbázisból kapja meg a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="e4dee-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="e4dee-117">Mivel a parancs a *ExpandRecommendedActions* paramétert használja, a parancsmag az ajánlott műveleteket kapja meg a válaszsal.</span><span class="sxs-lookup"><span data-stu-id="e4dee-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

## <span data-ttu-id="e4dee-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4dee-118">PARAMETERS</span></span>

### <span data-ttu-id="e4dee-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="e4dee-119">-AdvisorName</span></span>
<span data-ttu-id="e4dee-120">Annak a tanácsadónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="e4dee-120">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e4dee-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4dee-121">-DatabaseName</span></span>
<span data-ttu-id="e4dee-122">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja a tanácsadót kéri.</span><span class="sxs-lookup"><span data-stu-id="e4dee-122">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="e4dee-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4dee-123">-DefaultProfile</span></span>
<span data-ttu-id="e4dee-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e4dee-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4dee-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="e4dee-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="e4dee-126">Azt jelzi, hogy ez a parancsmag az ajánlott műveleteket kapja meg a válaszsal.</span><span class="sxs-lookup"><span data-stu-id="e4dee-126">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4dee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4dee-127">-ResourceGroupName</span></span>
<span data-ttu-id="e4dee-128">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4dee-128">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="e4dee-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e4dee-129">-ServerName</span></span>
<span data-ttu-id="e4dee-130">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4dee-130">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="e4dee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4dee-131">CommonParameters</span></span>
<span data-ttu-id="e4dee-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4dee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4dee-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4dee-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4dee-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4dee-134">INPUTS</span></span>

### <span data-ttu-id="e4dee-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="e4dee-135">None</span></span>
<span data-ttu-id="e4dee-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e4dee-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4dee-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4dee-137">OUTPUTS</span></span>

### <span data-ttu-id="e4dee-138">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="e4dee-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="e4dee-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4dee-139">NOTES</span></span>
* <span data-ttu-id="e4dee-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, Database, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="e4dee-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="e4dee-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4dee-141">RELATED LINKS</span></span>

[<span data-ttu-id="e4dee-142">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="e4dee-142">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="e4dee-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="e4dee-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="e4dee-144">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="e4dee-144">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="e4dee-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e4dee-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="e4dee-146">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e4dee-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
