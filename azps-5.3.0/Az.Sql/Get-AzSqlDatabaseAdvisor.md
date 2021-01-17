---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: 05bde2ee8a5bbcae941203115c49ff6b9fbc6bae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375114"
---
# <span data-ttu-id="adb96-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="adb96-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="adb96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adb96-102">SYNOPSIS</span></span>
<span data-ttu-id="adb96-103">Egy vagy több tanácsadót kap egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="adb96-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="adb96-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="adb96-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adb96-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="adb96-105">DESCRIPTION</span></span>
<span data-ttu-id="adb96-106">A **Get-AzSqlDatabaseAdvisor** parancsmag egy vagy több Azure SQL-adatbázis tanácsadót kap egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="adb96-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="adb96-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="adb96-107">EXAMPLES</span></span>

### <span data-ttu-id="adb96-108">1. példa: A megadott adatbázis tanácsadóinak felsorolása</span><span class="sxs-lookup"><span data-stu-id="adb96-108">Example 1: List all the advisors for the specified database</span></span>
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

<span data-ttu-id="adb96-109">Ez a parancs felsorolja a WIRunner nevű adatbázis összes tanácsadóját, amely a Wi-runner-australia-east nevű kiszolgálóhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="adb96-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="adb96-110">2. példa: Egyetlen tanácsadó lekérte a megadott adatbázist</span><span class="sxs-lookup"><span data-stu-id="adb96-110">Example 2: Get a single advisor for the specified database</span></span>
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

<span data-ttu-id="adb96-111">Ez a parancs a WIRunner nevű adatbázis CreateIndex nevű tanácsadóját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="adb96-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="adb96-112">3. példa: Az összes tanácsadó felsorolása a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="adb96-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="adb96-113">Ez a parancs a "WIRunner" nevű adatbázis összes tanácsadóját megkapja a válaszban javasolt műveletekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="adb96-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="adb96-114">Mivel a parancs *a ExpandRecomactions* paramétert használja, a parancsmag megkapja a válaszként javasolt műveleteket.</span><span class="sxs-lookup"><span data-stu-id="adb96-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="adb96-115">4. példa: Egyetlen tanácsadó lekérte a válaszban szereplő javasolt műveleteket</span><span class="sxs-lookup"><span data-stu-id="adb96-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="adb96-116">Ez a parancs a WiRunner nevű adatbázis CreateIndex nevű tanácsadóját kapja meg a válaszban szereplő javasolt műveletekkel együtt.</span><span class="sxs-lookup"><span data-stu-id="adb96-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="adb96-117">Mivel a parancs *a ExpandRecomactions* paramétert használja, a parancsmag megkapja a válaszként javasolt műveleteket.</span><span class="sxs-lookup"><span data-stu-id="adb96-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="adb96-118">5. példa: A megadott adatbázis tanácsadóinak felsorolása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="adb96-118">Example 5: List all the advisors for the specified database using filtering</span></span>
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

<span data-ttu-id="adb96-119">Ez a parancs felsorolja a WIRunner nevű adatbázis összes tanácsadóját, amely a wi-runner-australia-east kiszolgálóhoz tartozik, és a "d" betűvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="adb96-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="adb96-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adb96-120">PARAMETERS</span></span>

### <span data-ttu-id="adb96-121">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="adb96-121">-AdvisorName</span></span>
<span data-ttu-id="adb96-122">Megadja annak a tanácsadónak a nevét, akitől a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="adb96-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="adb96-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="adb96-123">-DatabaseName</span></span>
<span data-ttu-id="adb96-124">Megadja annak az adatbázisnak a nevét, amelyhez a parancsmag a tanácsadót kéri.</span><span class="sxs-lookup"><span data-stu-id="adb96-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="adb96-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb96-125">-DefaultProfile</span></span>
<span data-ttu-id="adb96-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="adb96-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adb96-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="adb96-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="adb96-128">Azt jelzi, hogy ez a parancsmag kapja meg a javasolt műveleteket a válaszokkal együtt.</span><span class="sxs-lookup"><span data-stu-id="adb96-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="adb96-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb96-129">-ResourceGroupName</span></span>
<span data-ttu-id="adb96-130">Az adatbázist tartalmazó kiszolgáló erőforráscsoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="adb96-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="adb96-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="adb96-131">-ServerName</span></span>
<span data-ttu-id="adb96-132">Az adatbázist tartalmazó kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="adb96-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="adb96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb96-133">CommonParameters</span></span>
<span data-ttu-id="adb96-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb96-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adb96-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb96-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adb96-136">INPUTS</span></span>

### <span data-ttu-id="adb96-137">System.String</span><span class="sxs-lookup"><span data-stu-id="adb96-137">System.String</span></span>

### <span data-ttu-id="adb96-138">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="adb96-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="adb96-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adb96-139">OUTPUTS</span></span>

### <span data-ttu-id="adb96-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="adb96-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="adb96-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="adb96-141">NOTES</span></span>
* <span data-ttu-id="adb96-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, adatbázis, mssql, tanácsadó</span><span class="sxs-lookup"><span data-stu-id="adb96-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="adb96-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adb96-143">RELATED LINKS</span></span>

[<span data-ttu-id="adb96-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="adb96-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="adb96-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="adb96-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="adb96-146">Get-AzSqlDatabaseRecomdataAction</span><span class="sxs-lookup"><span data-stu-id="adb96-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="adb96-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="adb96-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="adb96-148">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="adb96-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
