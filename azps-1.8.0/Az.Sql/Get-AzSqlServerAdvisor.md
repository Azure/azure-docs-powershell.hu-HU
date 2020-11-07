---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 20900527d6a846c02dc0132176b9be961e137973
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668953"
---
# <span data-ttu-id="e41e2-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="e41e2-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="e41e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e41e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e41e2-103">Egy vagy több tanácsadót kap egy Azure SQL Server-kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e41e2-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="e41e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e41e2-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e41e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e41e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e41e2-106">A **Get-AzSqlServerAdvisor** parancsmag egy vagy több Azure SQL Server-tanácsadót kap az Azure SQL Server rendszerhez.</span><span class="sxs-lookup"><span data-stu-id="e41e2-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="e41e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e41e2-107">EXAMPLES</span></span>

### <span data-ttu-id="e41e2-108">1. példa: a kiszolgáló összes tanácsadójának listázása</span><span class="sxs-lookup"><span data-stu-id="e41e2-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

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

<span data-ttu-id="e41e2-109">Ez a parancs a WIRunnersProd nevű erőforráscsoporthoz tartozó Wi-Runner-Ausztrália-Kelet nevű kiszolgáló összes tanácsadójának listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="e41e2-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="e41e2-110">2. példa: a kiszolgáló egyetlen tanácsadójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e41e2-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="e41e2-111">Ez a parancs a CreateIndex nevű tanácsadót kapja meg a Wi-Runner-Ausztrália-Kelet nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e41e2-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="e41e2-112">3. példa: az összes tanácsadó felsorolása a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="e41e2-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
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

<span data-ttu-id="e41e2-113">Ez a parancs a Wi-Runner-Ausztrália-Kelet nevű kiszolgáló összes tanácsadóját bekapja.</span><span class="sxs-lookup"><span data-stu-id="e41e2-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="e41e2-114">Mivel a parancs a *ExpandRecommendedActions* paramétert használja, a parancsmag a válaszban szereplő javasolt műveleteket kapja.</span><span class="sxs-lookup"><span data-stu-id="e41e2-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="e41e2-115">Példa 4: egyetlen tanácsadó beszerzése a válaszban szereplő javasolt műveletekkel</span><span class="sxs-lookup"><span data-stu-id="e41e2-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="e41e2-116">Ez a parancs a CreateIndex nevű tanácsadót a Wi-Runner-Ausztrália-Kelet nevű kiszolgálóról kapja meg, a válaszban szereplő javasolt műveletekkel.</span><span class="sxs-lookup"><span data-stu-id="e41e2-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="e41e2-117">Példa 5: a kiszolgáló összes tanácsadójának listázása szűréssel</span><span class="sxs-lookup"><span data-stu-id="e41e2-117">Example 5: List all the advisors for the server using filtering</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName d*
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

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

<span data-ttu-id="e41e2-118">Ez a parancs a "d" betűvel kezdődő, a Wi-Runner-Ausztrália-Kelet nevű kiszolgáló összes tanácsadójának listáját kapja meg, amely a WIRunnersProd nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="e41e2-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="e41e2-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e41e2-119">PARAMETERS</span></span>

### <span data-ttu-id="e41e2-120">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="e41e2-120">-AdvisorName</span></span>
<span data-ttu-id="e41e2-121">Annak a tanácsadónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="e41e2-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e41e2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e41e2-122">-DefaultProfile</span></span>
<span data-ttu-id="e41e2-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e41e2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e41e2-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="e41e2-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="e41e2-125">Azt jelzi, hogy a parancsmag a válaszban szereplő tanácsadók ajánlott műveleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e41e2-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="e41e2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e41e2-126">-ResourceGroupName</span></span>
<span data-ttu-id="e41e2-127">A kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e41e2-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="e41e2-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e41e2-128">-ServerName</span></span>
<span data-ttu-id="e41e2-129">Annak a kiszolgálónak a nevét adja meg, amelyre a parancsmag kéri.</span><span class="sxs-lookup"><span data-stu-id="e41e2-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="e41e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e41e2-130">CommonParameters</span></span>
<span data-ttu-id="e41e2-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e41e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e41e2-132">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e41e2-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e41e2-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e41e2-133">INPUTS</span></span>

### <span data-ttu-id="e41e2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e41e2-134">System.String</span></span>

### <span data-ttu-id="e41e2-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e41e2-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e41e2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e41e2-136">OUTPUTS</span></span>

### <span data-ttu-id="e41e2-137">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="e41e2-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="e41e2-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e41e2-138">NOTES</span></span>
* <span data-ttu-id="e41e2-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, Server, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="e41e2-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="e41e2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e41e2-140">RELATED LINKS</span></span>

[<span data-ttu-id="e41e2-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="e41e2-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="e41e2-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="e41e2-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="e41e2-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="e41e2-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="e41e2-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e41e2-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="e41e2-145">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e41e2-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

