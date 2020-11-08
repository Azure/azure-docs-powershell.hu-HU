---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
ms.openlocfilehash: 3032824d51e7892c21830decbdb1c92d03d7a2e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017563"
---
# <span data-ttu-id="97bf8-101">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="97bf8-101">Get-AzSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="97bf8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="97bf8-103">Egy vagy több tanácsadót kap egy Azure SQL elasztikus poolban.</span><span class="sxs-lookup"><span data-stu-id="97bf8-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="97bf8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97bf8-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97bf8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="97bf8-106">A **Get-AzSqlElasticPoolAdvisor** parancsmag egy vagy több Azure SQL elasztikus Pool-tanácsadót kap az Azure SQL rugalmas készletéhez.</span><span class="sxs-lookup"><span data-stu-id="97bf8-106">The **Get-AzSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="97bf8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97bf8-107">EXAMPLES</span></span>

### <span data-ttu-id="97bf8-108">1. példa: a megadott rugalmas készlet összes tanácsadójának felsorolása</span><span class="sxs-lookup"><span data-stu-id="97bf8-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool"
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="97bf8-109">A parancs megjeleníti a WIRunnerPool nevű rugalmas készlet összes tanácsadóját.</span><span class="sxs-lookup"><span data-stu-id="97bf8-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="97bf8-110">2. példa: egyetlen tanácsadót kap a megadott rugalmas készlethez</span><span class="sxs-lookup"><span data-stu-id="97bf8-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="97bf8-111">Ez a parancs a CreateIndex nevű tanácsadót a WIRunnerPool nevű rugalmas készlethez kapja.</span><span class="sxs-lookup"><span data-stu-id="97bf8-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="97bf8-112">3. példa: az összes tanácsadó felsorolása a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="97bf8-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="97bf8-113">Ez a parancs a rugalmas készlet összes tanácsadóját beilleszti a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="97bf8-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="97bf8-114">Példa 4: egyetlen tanácsadó beszerzése a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="97bf8-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="97bf8-115">Ez a parancs a CreateIndex nevű tanácsadót a Wi-Runner-Ausztrália-Kelet nevű kiszolgálóról kapja meg, a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="97bf8-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="97bf8-116">5. példa: a megadott rugalmas készlet összes tanácsadójának listája szűréssel</span><span class="sxs-lookup"><span data-stu-id="97bf8-116">Example 5: List all the advisors for the specified elastic pool using filtering</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName d*
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="97bf8-117">A parancs megjeleníti a WIRunnerPool nevű rugalmas készlet minden tanácsadóját, amely a "d" betűvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="97bf8-117">The command gets lists all the advisors for the elastic pool named WIRunnerPool that start with the letter "d".</span></span>

## <span data-ttu-id="97bf8-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97bf8-118">PARAMETERS</span></span>

### <span data-ttu-id="97bf8-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="97bf8-119">-AdvisorName</span></span>
<span data-ttu-id="97bf8-120">Annak a tanácsadónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="97bf8-120">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="97bf8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97bf8-121">-DefaultProfile</span></span>
<span data-ttu-id="97bf8-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97bf8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97bf8-123">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="97bf8-123">-ElasticPoolName</span></span>
<span data-ttu-id="97bf8-124">Annak a rugalmas készletnek a neve, amelyhez a parancsmag kéri a tanácsadót.</span><span class="sxs-lookup"><span data-stu-id="97bf8-124">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="97bf8-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="97bf8-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="97bf8-126">Jelzi, hogy a parancsmag a válaszban szereplő ajánlott műveleteket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="97bf8-126">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="97bf8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97bf8-127">-ResourceGroupName</span></span>
<span data-ttu-id="97bf8-128">Annak a kiszolgálónak az erőforráscsoport nevét adja meg, amely a rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="97bf8-128">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="97bf8-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="97bf8-129">-ServerName</span></span>
<span data-ttu-id="97bf8-130">Annak a kiszolgálónak a nevét adja meg, ahol a rugalmas készlet be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="97bf8-130">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="97bf8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97bf8-131">CommonParameters</span></span>
<span data-ttu-id="97bf8-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97bf8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97bf8-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="97bf8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97bf8-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97bf8-134">INPUTS</span></span>

### <span data-ttu-id="97bf8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="97bf8-135">System.String</span></span>

### <span data-ttu-id="97bf8-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="97bf8-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="97bf8-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97bf8-137">OUTPUTS</span></span>

### <span data-ttu-id="97bf8-138">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="97bf8-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="97bf8-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97bf8-139">NOTES</span></span>
* <span data-ttu-id="97bf8-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, elasticpool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="97bf8-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="97bf8-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97bf8-141">RELATED LINKS</span></span>

[<span data-ttu-id="97bf8-142">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="97bf8-142">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="97bf8-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="97bf8-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="97bf8-144">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="97bf8-144">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="97bf8-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="97bf8-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="97bf8-146">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="97bf8-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
