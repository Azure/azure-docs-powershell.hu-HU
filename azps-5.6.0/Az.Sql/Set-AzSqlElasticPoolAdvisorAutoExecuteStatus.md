---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: aa181dcb171a1842c2b6158078e60b717b33d579
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919106"
---
# <span data-ttu-id="42dec-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="42dec-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="42dec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42dec-102">SYNOPSIS</span></span>
<span data-ttu-id="42dec-103">Frissíti az Azure SQL rugalmassági készlet tanácsadója automatikus végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="42dec-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="42dec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="42dec-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42dec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="42dec-105">DESCRIPTION</span></span>
<span data-ttu-id="42dec-106">A **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** parancsmag beállítja az Azure SQL rugalmassági készlet tanácsadója automatikus futtatás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="42dec-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="42dec-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="42dec-107">EXAMPLES</span></span>

### <span data-ttu-id="42dec-108">1. példa: Tanácsadó automatikus végrehajtásának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="42dec-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="42dec-109">Ezzel a paranccsal engedélyezettre állítja a CreateIndex nevű tanácsadó automatikus végrehajtási állapotát.</span><span class="sxs-lookup"><span data-stu-id="42dec-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="42dec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42dec-110">PARAMETERS</span></span>

### <span data-ttu-id="42dec-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="42dec-111">-AdvisorName</span></span>
<span data-ttu-id="42dec-112">Annak a tanácsadónak a nevét adja meg, amelynek a parancsmagja frissíti az automatikus végrehajtás állapotát.</span><span class="sxs-lookup"><span data-stu-id="42dec-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="42dec-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="42dec-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="42dec-114">Egy új értéket ad meg, amelynek a parancsmagja frissíti az automatikus végrehajtás állapotát.</span><span class="sxs-lookup"><span data-stu-id="42dec-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="42dec-115">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="42dec-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42dec-116">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="42dec-116">Enabled</span></span>
- <span data-ttu-id="42dec-117">Letiltva</span><span class="sxs-lookup"><span data-stu-id="42dec-117">Disabled</span></span>
- <span data-ttu-id="42dec-118">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="42dec-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dec-119">-DefaultProfile</span></span>
<span data-ttu-id="42dec-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="42dec-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42dec-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="42dec-121">-ElasticPoolName</span></span>
<span data-ttu-id="42dec-122">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42dec-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="42dec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42dec-123">-ResourceGroupName</span></span>
<span data-ttu-id="42dec-124">A rugalmas készletet tartalmazó kiszolgáló erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="42dec-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="42dec-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42dec-125">-ServerName</span></span>
<span data-ttu-id="42dec-126">Annak a kiszolgálónak a nevét adja meg, amelynél a rugalmas készlet található.</span><span class="sxs-lookup"><span data-stu-id="42dec-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="42dec-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42dec-127">-Confirm</span></span>
<span data-ttu-id="42dec-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="42dec-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42dec-129">-WhatIf</span></span>
<span data-ttu-id="42dec-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="42dec-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42dec-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="42dec-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dec-132">CommonParameters</span></span>
<span data-ttu-id="42dec-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42dec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42dec-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42dec-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dec-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42dec-135">INPUTS</span></span>

### <span data-ttu-id="42dec-136">System.String</span><span class="sxs-lookup"><span data-stu-id="42dec-136">System.String</span></span>

### <span data-ttu-id="42dec-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="42dec-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="42dec-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42dec-138">OUTPUTS</span></span>

### <span data-ttu-id="42dec-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="42dec-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="42dec-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="42dec-140">NOTES</span></span>
* <span data-ttu-id="42dec-141">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, sql, rugalmas készlet, mssql, tanácsadó</span><span class="sxs-lookup"><span data-stu-id="42dec-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="42dec-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42dec-142">RELATED LINKS</span></span>

[<span data-ttu-id="42dec-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="42dec-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="42dec-144">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="42dec-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
