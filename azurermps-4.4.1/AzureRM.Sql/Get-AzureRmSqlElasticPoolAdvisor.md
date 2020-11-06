---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolAdvisor.md
ms.openlocfilehash: f68666d7a83190dee4b8052769b4daed0e61c159
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494620"
---
# <span data-ttu-id="79128-101">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="79128-101">Get-AzureRmSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="79128-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79128-102">SYNOPSIS</span></span>
<span data-ttu-id="79128-103">Egy vagy több tanácsadót kap egy Azure SQL elasztikus poolban.</span><span class="sxs-lookup"><span data-stu-id="79128-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79128-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79128-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79128-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="79128-105">DESCRIPTION</span></span>
<span data-ttu-id="79128-106">A **Get-AzureRmSqlElasticPoolAdvisor** parancsmag egy vagy több Azure SQL elasztikus Pool-tanácsadót kap az Azure SQL rugalmas készletéhez.</span><span class="sxs-lookup"><span data-stu-id="79128-106">The **Get-AzureRmSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="79128-107">Példák</span><span class="sxs-lookup"><span data-stu-id="79128-107">EXAMPLES</span></span>

### <span data-ttu-id="79128-108">1. példa: a megadott rugalmas készlet összes tanácsadójának felsorolása</span><span class="sxs-lookup"><span data-stu-id="79128-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -PoolName "WIRunnerPool"
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

<span data-ttu-id="79128-109">A parancs megjeleníti a WIRunnerPool nevű rugalmas készlet összes tanácsadóját.</span><span class="sxs-lookup"><span data-stu-id="79128-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="79128-110">2. példa: egyetlen tanácsadót kap a megadott rugalmas készlethez</span><span class="sxs-lookup"><span data-stu-id="79128-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
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

<span data-ttu-id="79128-111">Ez a parancs a CreateIndex nevű tanácsadót a WIRunnerPool nevű rugalmas készlethez kapja.</span><span class="sxs-lookup"><span data-stu-id="79128-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="79128-112">3. példa: az összes tanácsadó felsorolása a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="79128-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
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

<span data-ttu-id="79128-113">Ez a parancs a rugalmas készlet összes tanácsadóját beilleszti a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="79128-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="79128-114">Példa 4: egyetlen tanácsadó beszerzése a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="79128-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="79128-115">Ez a parancs a CreateIndex nevű tanácsadót a Wi-Runner-Ausztrália-Kelet nevű kiszolgálóról kapja meg, a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="79128-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

## <span data-ttu-id="79128-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79128-116">PARAMETERS</span></span>

### <span data-ttu-id="79128-117">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="79128-117">-AdvisorName</span></span>
<span data-ttu-id="79128-118">Annak a tanácsadónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="79128-118">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="79128-119">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="79128-119">-ElasticPoolName</span></span>
<span data-ttu-id="79128-120">Annak a rugalmas készletnek a neve, amelyhez a parancsmag kéri a tanácsadót.</span><span class="sxs-lookup"><span data-stu-id="79128-120">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="79128-121">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="79128-121">-ExpandRecommendedActions</span></span>
<span data-ttu-id="79128-122">Jelzi, hogy a parancsmag a válaszban szereplő ajánlott műveleteket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="79128-122">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="79128-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79128-123">-ResourceGroupName</span></span>
<span data-ttu-id="79128-124">Annak a kiszolgálónak az erőforráscsoport nevét adja meg, amely a rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="79128-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="79128-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="79128-125">-ServerName</span></span>
<span data-ttu-id="79128-126">Annak a kiszolgálónak a nevét adja meg, ahol a rugalmas készlet be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="79128-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="79128-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79128-127">-DefaultProfile</span></span>
<span data-ttu-id="79128-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79128-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79128-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79128-129">CommonParameters</span></span>
<span data-ttu-id="79128-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79128-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79128-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79128-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79128-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79128-132">INPUTS</span></span>

## <span data-ttu-id="79128-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79128-133">OUTPUTS</span></span>

### <span data-ttu-id="79128-134">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="79128-134">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="79128-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79128-135">NOTES</span></span>
* <span data-ttu-id="79128-136">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, elasticpool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="79128-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="79128-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79128-137">RELATED LINKS</span></span>

[<span data-ttu-id="79128-138">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="79128-138">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="79128-139">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="79128-139">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="79128-140">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="79128-140">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="79128-141">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="79128-141">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="79128-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="79128-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
