---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: ebc9386df78af1a730578c57e3957a869bbc299b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180836"
---
# <span data-ttu-id="4066e-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4066e-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="4066e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4066e-102">SYNOPSIS</span></span>
<span data-ttu-id="4066e-103">A rugalmas készleteket és azok tulajdonságát Azure SQL-adatbázisban kapja.</span><span class="sxs-lookup"><span data-stu-id="4066e-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="4066e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4066e-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4066e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4066e-105">DESCRIPTION</span></span>
<span data-ttu-id="4066e-106">A **Get-AzSqlElasticPool** parancsmag rugalmas készleteket és a hozzájuk tartozó tulajdonságértékeket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="4066e-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="4066e-107">A meglévő rugalmas készlet nevének meghatározása, hogy csak az adott poolhoz tartozó tulajdonságértékeket láthassa.</span><span class="sxs-lookup"><span data-stu-id="4066e-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="4066e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4066e-108">EXAMPLES</span></span>

### <span data-ttu-id="4066e-109">Példa 1: a rugalmas medencék beszerzése</span><span class="sxs-lookup"><span data-stu-id="4066e-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="4066e-110">Ez a parancs a Server01 nevű kiszolgálón minden rugalmas készletet megkapja.</span><span class="sxs-lookup"><span data-stu-id="4066e-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="4066e-111">2. példa: speciális elasztikus Pool beszerzése</span><span class="sxs-lookup"><span data-stu-id="4066e-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="4066e-112">Ez a parancs a Server01 nevű kiszolgálón a ElasticPool0127 nevű rugalmas készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="4066e-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="4066e-113">3 Példa: az Azure SQL elasztikus adatbázis-készlet metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4066e-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-AzMetric -TimeGrain 0:5:0 -MetricName storage_percent
DimensionName  : 
DimensionValue : 
Name           : cpu_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : physical_data_read_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : log_write_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : dtu_consumption_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : storage_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent
```

<span data-ttu-id="4066e-114">Ez a parancs a ElasticPool01 nevű Azure SQL elasztikus adatbázis-készlet metrikáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="4066e-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="4066e-115">Példa 4: a rugalmas medencék beszerzése szűréssel – ElasticPoolName "ElasticPool \*"</span><span class="sxs-lookup"><span data-stu-id="4066e-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="4066e-116">Ez a parancs a Server01 nevű kiszolgálón a "ElasticPool" kezdetű teljes rugalmas készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="4066e-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="4066e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4066e-117">PARAMETERS</span></span>

### <span data-ttu-id="4066e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4066e-118">-DefaultProfile</span></span>
<span data-ttu-id="4066e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4066e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4066e-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4066e-120">-ElasticPoolName</span></span>
<span data-ttu-id="4066e-121">Itt adhatja meg annak a rugalmas készletnek a nevét, amelyik a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="4066e-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4066e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4066e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4066e-123">Annak a csoportnak a neve, amely a parancsmag által beolvasott rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4066e-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4066e-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4066e-124">-ServerName</span></span>
<span data-ttu-id="4066e-125">Megadja annak a kiszolgálónak a nevét, amely a parancsmag által beolvasott rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4066e-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4066e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4066e-126">CommonParameters</span></span>
<span data-ttu-id="4066e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4066e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4066e-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4066e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4066e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4066e-129">INPUTS</span></span>

### <span data-ttu-id="4066e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4066e-130">System.String</span></span>

## <span data-ttu-id="4066e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4066e-131">OUTPUTS</span></span>

### <span data-ttu-id="4066e-132">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="4066e-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="4066e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4066e-133">NOTES</span></span>

## <span data-ttu-id="4066e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4066e-134">RELATED LINKS</span></span>

[<span data-ttu-id="4066e-135">Új – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4066e-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="4066e-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4066e-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="4066e-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4066e-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


