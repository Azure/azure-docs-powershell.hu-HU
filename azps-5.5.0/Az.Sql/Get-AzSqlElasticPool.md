---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: ebc9386df78af1a730578c57e3957a869bbc299b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144155"
---
# <span data-ttu-id="ccc9f-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccc9f-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="ccc9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccc9f-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc9f-103">Rugalmas készleteket és azok tulajdonságértékeket kap egy Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="ccc9f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ccc9f-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccc9f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ccc9f-105">DESCRIPTION</span></span>
<span data-ttu-id="ccc9f-106">A **Get-AzSqlElasticPool** parancsmag rugalmas készleteket és azok tulajdonságértékét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="ccc9f-107">Adja meg egy meglévő rugalmas készlet nevét, hogy csak az adott készlet tulajdonságértékét lássa.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="ccc9f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ccc9f-108">EXAMPLES</span></span>

### <span data-ttu-id="ccc9f-109">1. példa: Az összes rugalmas készlet behozatka</span><span class="sxs-lookup"><span data-stu-id="ccc9f-109">Example 1: Get all elastic pools</span></span>
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

<span data-ttu-id="ccc9f-110">Ez a parancs a Kiszolgáló01 nevű kiszolgálón található összes rugalmas készletet beveszi.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="ccc9f-111">2. példa: Egy adott rugalmas készlet lekérte</span><span class="sxs-lookup"><span data-stu-id="ccc9f-111">Example 2: Get a specific elastic pool</span></span>
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

<span data-ttu-id="ccc9f-112">Ez a parancs a RugalmasPool0127 nevű rugalmas készletet kapja meg a Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="ccc9f-113">3. példa: Metrikák lekérte az Azure SQL Rugalmas adatbáziskészlethez</span><span class="sxs-lookup"><span data-stu-id="ccc9f-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
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

<span data-ttu-id="ccc9f-114">Ez a parancs az Azure SQL rugalmassági adatbáziskészletének RugalmasságPool01 nevű metrikákat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="ccc9f-115">4. példa: Az összes rugalmas készlet behozása a -ElasticPoolName "ElasticPool\*" szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="ccc9f-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
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

<span data-ttu-id="ccc9f-116">Ez a parancs a Kiszolgáló01 kiszolgáló összes rugalmas készletét a "Rugalmasságpool" kezdetűre kapja.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="ccc9f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccc9f-117">PARAMETERS</span></span>

### <span data-ttu-id="ccc9f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc9f-118">-DefaultProfile</span></span>
<span data-ttu-id="ccc9f-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ccc9f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccc9f-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ccc9f-120">-ElasticPoolName</span></span>
<span data-ttu-id="ccc9f-121">Megadja annak a rugalmas készletnek a nevét, amelybe a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ccc9f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccc9f-122">-ResourceGroupName</span></span>
<span data-ttu-id="ccc9f-123">Annak az erőforráscsoportnak a neve, amely a parancsmag rugalmas készletét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ccc9f-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ccc9f-124">-ServerName</span></span>
<span data-ttu-id="ccc9f-125">Annak a kiszolgálónak a neve, amely a parancsmag rugalmas készletét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ccc9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc9f-126">CommonParameters</span></span>
<span data-ttu-id="ccc9f-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccc9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc9f-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccc9f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc9f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccc9f-129">INPUTS</span></span>

### <span data-ttu-id="ccc9f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ccc9f-130">System.String</span></span>

## <span data-ttu-id="ccc9f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccc9f-131">OUTPUTS</span></span>

### <span data-ttu-id="ccc9f-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="ccc9f-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="ccc9f-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ccc9f-133">NOTES</span></span>

## <span data-ttu-id="ccc9f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccc9f-134">RELATED LINKS</span></span>

[<span data-ttu-id="ccc9f-135">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccc9f-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="ccc9f-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccc9f-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="ccc9f-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ccc9f-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


