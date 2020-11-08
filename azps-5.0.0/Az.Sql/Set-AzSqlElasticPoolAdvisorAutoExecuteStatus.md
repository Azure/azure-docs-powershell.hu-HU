---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5e26be318f439556a7083dc4d2bcde154083f5e4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194503"
---
# <span data-ttu-id="fb685-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="fb685-101">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="fb685-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb685-102">SYNOPSIS</span></span>
<span data-ttu-id="fb685-103">Az Azure SQL rugalmas alkalmazáskészlet tanácsadójának automatikus végrehajtási állapotát frissíti.</span><span class="sxs-lookup"><span data-stu-id="fb685-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="fb685-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb685-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb685-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb685-105">DESCRIPTION</span></span>
<span data-ttu-id="fb685-106">A **set-AzSqlElasticPoolAdvisorAutoExecuteStatus** parancsmag az Azure SQL elasztikus Pool tanácsadójának automatikus végrehajtás tulajdonságát állítja be.</span><span class="sxs-lookup"><span data-stu-id="fb685-106">The **Set-AzSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="fb685-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb685-107">EXAMPLES</span></span>

### <span data-ttu-id="fb685-108">1. példa: az automatikus végrehajtás engedélyezése egy tanácsadónál</span><span class="sxs-lookup"><span data-stu-id="fb685-108">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="fb685-109">Ez a parancs beállítja egy CreateIndex nevű tanácsadó automatikus végrehajtási állapotát.</span><span class="sxs-lookup"><span data-stu-id="fb685-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="fb685-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb685-110">PARAMETERS</span></span>

### <span data-ttu-id="fb685-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="fb685-111">-AdvisorName</span></span>
<span data-ttu-id="fb685-112">Annak a tanácsadónak a nevét adja meg, amelynek a parancsmagja frissíti az automatikus végrehajtás állapotát.</span><span class="sxs-lookup"><span data-stu-id="fb685-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="fb685-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="fb685-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="fb685-114">Új értéket ad meg, amelyre ez a parancsmag frissíti az automatikus végrehajtási állapotot.</span><span class="sxs-lookup"><span data-stu-id="fb685-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="fb685-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fb685-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb685-116">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="fb685-116">Enabled</span></span>
- <span data-ttu-id="fb685-117">Tiltva</span><span class="sxs-lookup"><span data-stu-id="fb685-117">Disabled</span></span>
- <span data-ttu-id="fb685-118">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="fb685-118">Default</span></span>

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

### <span data-ttu-id="fb685-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb685-119">-DefaultProfile</span></span>
<span data-ttu-id="fb685-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb685-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb685-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fb685-121">-ElasticPoolName</span></span>
<span data-ttu-id="fb685-122">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb685-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="fb685-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb685-123">-ResourceGroupName</span></span>
<span data-ttu-id="fb685-124">Annak a kiszolgálónak az erőforráscsoport nevét adja meg, amely a rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fb685-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="fb685-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fb685-125">-ServerName</span></span>
<span data-ttu-id="fb685-126">Annak a kiszolgálónak a nevét adja meg, ahol a rugalmas készlet be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="fb685-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="fb685-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb685-127">-Confirm</span></span>
<span data-ttu-id="fb685-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb685-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb685-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb685-129">-WhatIf</span></span>
<span data-ttu-id="fb685-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb685-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb685-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb685-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb685-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb685-132">CommonParameters</span></span>
<span data-ttu-id="fb685-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb685-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb685-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb685-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb685-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb685-135">INPUTS</span></span>

### <span data-ttu-id="fb685-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fb685-136">System.String</span></span>

### <span data-ttu-id="fb685-137">Microsoft. Azure. Command. SQL. Advisor. parancsmag. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="fb685-137">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="fb685-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb685-138">OUTPUTS</span></span>

### <span data-ttu-id="fb685-139">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="fb685-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="fb685-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb685-140">NOTES</span></span>
* <span data-ttu-id="fb685-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, elasztikus Pool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="fb685-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="fb685-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb685-142">RELATED LINKS</span></span>

[<span data-ttu-id="fb685-143">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="fb685-143">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="fb685-144">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fb685-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)