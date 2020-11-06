---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
ms.openlocfilehash: f06481984ef478a6bf3af51de1796855c265c2c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498755"
---
# <span data-ttu-id="e0694-101">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e0694-101">Get-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="e0694-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0694-102">SYNOPSIS</span></span>
<span data-ttu-id="e0694-103">A rugalmas készleteket és azok tulajdonságát Azure SQL-adatbázisban kapja.</span><span class="sxs-lookup"><span data-stu-id="e0694-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0694-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0694-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0694-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0694-105">DESCRIPTION</span></span>
<span data-ttu-id="e0694-106">A **Get-AzureRmSqlElasticPool** parancsmag rugalmas készleteket és a hozzájuk tartozó tulajdonságértékeket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e0694-106">The **Get-AzureRmSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="e0694-107">A meglévő rugalmas készlet nevének meghatározása, hogy csak az adott poolhoz tartozó tulajdonságértékeket láthassa.</span><span class="sxs-lookup"><span data-stu-id="e0694-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="e0694-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e0694-108">EXAMPLES</span></span>

### <span data-ttu-id="e0694-109">Példa 1: a rugalmas medencék beszerzése</span><span class="sxs-lookup"><span data-stu-id="e0694-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="e0694-110">Ez a parancs a Server01 nevű kiszolgálón minden rugalmas készletet megkapja.</span><span class="sxs-lookup"><span data-stu-id="e0694-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="e0694-111">2. példa: speciális elasztikus Pool beszerzése</span><span class="sxs-lookup"><span data-stu-id="e0694-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
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

<span data-ttu-id="e0694-112">Ez a parancs a Server01 nevű kiszolgálón a ElasticPool0127 nevű rugalmas készletet kapja.</span><span class="sxs-lookup"><span data-stu-id="e0694-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="e0694-113">3 Példa: az Azure SQL elasztikus adatbázis-készlet metrikájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e0694-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-Metrics -TimeGrain 0:5:0
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

<span data-ttu-id="e0694-114">Ez a parancs a ElasticPool01 nevű Azure SQL elasztikus adatbázis-készlet metrikáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="e0694-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

## <span data-ttu-id="e0694-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0694-115">PARAMETERS</span></span>

### <span data-ttu-id="e0694-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0694-116">-DefaultProfile</span></span>
<span data-ttu-id="e0694-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e0694-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0694-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e0694-118">-ElasticPoolName</span></span>
<span data-ttu-id="e0694-119">Itt adhatja meg annak a rugalmas készletnek a nevét, amelyik a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="e0694-119">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0694-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0694-120">-ResourceGroupName</span></span>
<span data-ttu-id="e0694-121">Annak a csoportnak a neve, amely a parancsmag által beolvasott rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e0694-121">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e0694-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e0694-122">-ServerName</span></span>
<span data-ttu-id="e0694-123">Megadja annak a kiszolgálónak a nevét, amely a parancsmag által beolvasott rugalmas készletet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e0694-123">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0694-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0694-124">CommonParameters</span></span>
<span data-ttu-id="e0694-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0694-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0694-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0694-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0694-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0694-127">INPUTS</span></span>

### <span data-ttu-id="e0694-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="e0694-128">None</span></span>
<span data-ttu-id="e0694-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e0694-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0694-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0694-130">OUTPUTS</span></span>

### <span data-ttu-id="e0694-131">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="e0694-131">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="e0694-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0694-132">NOTES</span></span>

## <span data-ttu-id="e0694-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0694-133">RELATED LINKS</span></span>

[<span data-ttu-id="e0694-134">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e0694-134">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e0694-135">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e0694-135">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e0694-136">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e0694-136">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


