---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7b4d445ede7bae59431707f3ff6bc587effde21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498695"
---
# <span data-ttu-id="d1c66-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d1c66-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="d1c66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1c66-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c66-103">Az Azure SQL rugalmas alkalmazáskészlet tanácsadójának automatikus végrehajtási állapotát frissíti.</span><span class="sxs-lookup"><span data-stu-id="d1c66-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1c66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1c66-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1c66-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1c66-105">DESCRIPTION</span></span>
<span data-ttu-id="d1c66-106">A **set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** parancsmag az Azure SQL elasztikus Pool tanácsadójának automatikus végrehajtás tulajdonságát állítja be.</span><span class="sxs-lookup"><span data-stu-id="d1c66-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="d1c66-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d1c66-107">EXAMPLES</span></span>

### <span data-ttu-id="d1c66-108">1. példa: az automatikus végrehajtás engedélyezése egy tanácsadónál</span><span class="sxs-lookup"><span data-stu-id="d1c66-108">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="d1c66-109">Ez a parancs beállítja egy CreateIndex nevű tanácsadó automatikus végrehajtási állapotát.</span><span class="sxs-lookup"><span data-stu-id="d1c66-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="d1c66-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1c66-110">PARAMETERS</span></span>

### <span data-ttu-id="d1c66-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="d1c66-111">-AdvisorName</span></span>
<span data-ttu-id="d1c66-112">Annak a tanácsadónak a nevét adja meg, amelynek a parancsmagja frissíti az automatikus végrehajtás állapotát.</span><span class="sxs-lookup"><span data-stu-id="d1c66-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="d1c66-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="d1c66-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="d1c66-114">Új értéket ad meg, amelyre ez a parancsmag frissíti az automatikus végrehajtási állapotot.</span><span class="sxs-lookup"><span data-stu-id="d1c66-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="d1c66-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d1c66-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1c66-116">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="d1c66-116">Enabled</span></span>
- <span data-ttu-id="d1c66-117">Tiltva</span><span class="sxs-lookup"><span data-stu-id="d1c66-117">Disabled</span></span>
- <span data-ttu-id="d1c66-118">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="d1c66-118">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c66-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c66-119">-DefaultProfile</span></span>
<span data-ttu-id="d1c66-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d1c66-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1c66-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d1c66-121">-ElasticPoolName</span></span>
<span data-ttu-id="d1c66-122">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1c66-122">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="d1c66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c66-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1c66-124">Annak a kiszolgálónak az erőforráscsoport nevét adja meg, amely a rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d1c66-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="d1c66-125">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d1c66-125">-ServerName</span></span>
<span data-ttu-id="d1c66-126">Annak a kiszolgálónak a nevét adja meg, ahol a rugalmas készlet be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="d1c66-126">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="d1c66-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1c66-127">-Confirm</span></span>
<span data-ttu-id="d1c66-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1c66-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c66-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1c66-129">-WhatIf</span></span>
<span data-ttu-id="d1c66-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1c66-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1c66-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1c66-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c66-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c66-132">CommonParameters</span></span>
<span data-ttu-id="d1c66-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1c66-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c66-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1c66-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c66-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1c66-135">INPUTS</span></span>

### <span data-ttu-id="d1c66-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="d1c66-136">None</span></span>
<span data-ttu-id="d1c66-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d1c66-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1c66-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1c66-138">OUTPUTS</span></span>

### <span data-ttu-id="d1c66-139">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="d1c66-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="d1c66-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1c66-140">NOTES</span></span>
* <span data-ttu-id="d1c66-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, elasztikus Pool, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="d1c66-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="d1c66-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1c66-142">RELATED LINKS</span></span>

[<span data-ttu-id="d1c66-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="d1c66-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="d1c66-144">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d1c66-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
