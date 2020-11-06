---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5a03216c0a1d507731be75b63277cdd46e3be46d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494601"
---
# <span data-ttu-id="fbc4d-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="fbc4d-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="fbc4d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbc4d-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc4d-103">Az Azure SQL rugalmas alkalmazáskészlet tanácsadójának automatikus végrehajtási állapotát frissíti.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbc4d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbc4d-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbc4d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbc4d-105">DESCRIPTION</span></span>
<span data-ttu-id="fbc4d-106">A **set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** parancsmag az Azure SQL elasztikus Pool tanácsadójának automatikus végrehajtás tulajdonságát állítja be.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="fbc4d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fbc4d-107">EXAMPLES</span></span>

### <span data-ttu-id="fbc4d-108">1. példa: az automatikus végrehajtás engedélyezése egy tanácsadónál</span><span class="sxs-lookup"><span data-stu-id="fbc4d-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="fbc4d-109">Ez a parancs beállítja egy CreateIndex nevű tanácsadó automatikus végrehajtási állapotát.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="fbc4d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbc4d-110">PARAMETERS</span></span>

### <span data-ttu-id="fbc4d-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="fbc4d-111">-AdvisorName</span></span>
<span data-ttu-id="fbc4d-112">Annak a tanácsadónak a nevét adja meg, amelynek a parancsmagja frissíti az automatikus végrehajtás állapotát.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="fbc4d-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="fbc4d-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="fbc4d-114">Új értéket ad meg, amelyre ez a parancsmag frissíti az automatikus végrehajtási állapotot.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="fbc4d-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fbc4d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fbc4d-116">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="fbc4d-116">Enabled</span></span>
- <span data-ttu-id="fbc4d-117">Tiltva</span><span class="sxs-lookup"><span data-stu-id="fbc4d-117">Disabled</span></span>
- <span data-ttu-id="fbc4d-118">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="fbc4d-118">Default</span></span>

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

### <span data-ttu-id="fbc4d-119">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fbc4d-119">-ElasticPoolName</span></span>
<span data-ttu-id="fbc4d-120">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-120">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="fbc4d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc4d-121">-ResourceGroupName</span></span>
<span data-ttu-id="fbc4d-122">Annak a kiszolgálónak az erőforráscsoport nevét adja meg, amely a rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-122">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="fbc4d-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fbc4d-123">-ServerName</span></span>
<span data-ttu-id="fbc4d-124">Annak a kiszolgálónak a nevét adja meg, ahol a rugalmas készlet be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-124">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="fbc4d-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fbc4d-125">-Confirm</span></span>
<span data-ttu-id="fbc4d-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbc4d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbc4d-127">-WhatIf</span></span>
<span data-ttu-id="fbc4d-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbc4d-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbc4d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc4d-130">-DefaultProfile</span></span>
<span data-ttu-id="fbc4d-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbc4d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbc4d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc4d-132">CommonParameters</span></span>
<span data-ttu-id="fbc4d-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbc4d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc4d-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbc4d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc4d-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbc4d-135">INPUTS</span></span>

## <span data-ttu-id="fbc4d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbc4d-136">OUTPUTS</span></span>

### <span data-ttu-id="fbc4d-137">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="fbc4d-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="fbc4d-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbc4d-138">NOTES</span></span>
* <span data-ttu-id="fbc4d-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, elasztikus Pool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="fbc4d-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="fbc4d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbc4d-140">RELATED LINKS</span></span>

[<span data-ttu-id="fbc4d-141">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="fbc4d-141">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="fbc4d-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fbc4d-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
