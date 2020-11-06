---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3d93b0d82a2769acce620ce97141be68c003c281
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498743"
---
# <span data-ttu-id="c44a0-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c44a0-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="c44a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c44a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c44a0-103">Rugalmas adatbázis-készletet hoz létre egy SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="c44a0-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c44a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c44a0-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c44a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c44a0-105">DESCRIPTION</span></span>
<span data-ttu-id="c44a0-106">A **New-AzureRmSqlElasticPool** parancsmag létrehoz egy rugalmas adatbázis-készletet egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="c44a0-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="c44a0-107">Több paraméter ( *-DTU,-DatabaseDtuMin és-DatabaseDtuMax* ) szükséges, hogy a beállítás értéke az adott paraméterhez tartozó érvényes értékek listájából származik.</span><span class="sxs-lookup"><span data-stu-id="c44a0-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="c44a0-108">A-DatabaseDtuMax 100-as normál-készlethez például csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="c44a0-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="c44a0-109">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="c44a0-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="c44a0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c44a0-110">EXAMPLES</span></span>

### <span data-ttu-id="c44a0-111">1. példa: rugalmas készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="c44a0-111">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="c44a0-112">Ez a parancs egy rugalmas medencét hoz létre a ElasticPool01 nevű standard szolgáltatási rétegben.</span><span class="sxs-lookup"><span data-stu-id="c44a0-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="c44a0-113">A server01 nevű, ResourceGroup01 nevű Azure-erőforráscsoporthoz rendelt kiszolgáló a rugalmas készletet tárolja.</span><span class="sxs-lookup"><span data-stu-id="c44a0-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="c44a0-114">A parancs a készlet DTU és a készlet adatbázisainak értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c44a0-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="c44a0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c44a0-115">PARAMETERS</span></span>

### <span data-ttu-id="c44a0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c44a0-116">-AsJob</span></span>
<span data-ttu-id="c44a0-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c44a0-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44a0-118">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="c44a0-118">-DatabaseDtuMax</span></span>
<span data-ttu-id="c44a0-119">Megadja, hogy a készletben lévő egyetlen adatbázisból hány adatbázis-átviteli egység (DTU) használható.</span><span class="sxs-lookup"><span data-stu-id="c44a0-119">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="c44a0-120">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c44a0-120">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="c44a0-121">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="c44a0-121">Basic.</span></span> <span data-ttu-id="c44a0-122">5 DTU</span><span class="sxs-lookup"><span data-stu-id="c44a0-122">5 DTUs</span></span>
- <span data-ttu-id="c44a0-123">Standard.</span><span class="sxs-lookup"><span data-stu-id="c44a0-123">Standard.</span></span> <span data-ttu-id="c44a0-124">100 DTU</span><span class="sxs-lookup"><span data-stu-id="c44a0-124">100 DTUs</span></span>
- <span data-ttu-id="c44a0-125">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="c44a0-125">Premium.</span></span> <span data-ttu-id="c44a0-126">125 DTU</span><span class="sxs-lookup"><span data-stu-id="c44a0-126">125 DTUs</span></span>

<span data-ttu-id="c44a0-127">Ha tudni szeretné, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) .</span><span class="sxs-lookup"><span data-stu-id="c44a0-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44a0-128">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="c44a0-128">-DatabaseDtuMin</span></span>
<span data-ttu-id="c44a0-129">Itt adhatja meg, hogy a rugalmas készlet milyen minimális számú DTU a készlet összes adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="c44a0-129">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="c44a0-130">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="c44a0-130">The default value is zero (0).</span></span>

<span data-ttu-id="c44a0-131">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="c44a0-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44a0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c44a0-132">-DefaultProfile</span></span>
<span data-ttu-id="c44a0-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c44a0-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c44a0-134">-Dtu</span><span class="sxs-lookup"><span data-stu-id="c44a0-134">-Dtu</span></span>
<span data-ttu-id="c44a0-135">A rugalmas készlet megosztott DTU teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c44a0-135">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="c44a0-136">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c44a0-136">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="c44a0-137">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="c44a0-137">Basic.</span></span>
<span data-ttu-id="c44a0-138">100 DTU</span><span class="sxs-lookup"><span data-stu-id="c44a0-138">100 DTUs</span></span>
- <span data-ttu-id="c44a0-139">Standard.</span><span class="sxs-lookup"><span data-stu-id="c44a0-139">Standard.</span></span>
<span data-ttu-id="c44a0-140">100 DTU</span><span class="sxs-lookup"><span data-stu-id="c44a0-140">100 DTUs</span></span>
- <span data-ttu-id="c44a0-141">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="c44a0-141">Premium.</span></span>
<span data-ttu-id="c44a0-142">125 DTU</span><span class="sxs-lookup"><span data-stu-id="c44a0-142">125 DTUs</span></span>

<span data-ttu-id="c44a0-143">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="c44a0-143">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44a0-144">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="c44a0-144">-Edition</span></span>
<span data-ttu-id="c44a0-145">A rugalmas készlethez használt Azure SQL-adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c44a0-145">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="c44a0-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c44a0-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c44a0-147">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="c44a0-147">Premium</span></span>
- <span data-ttu-id="c44a0-148">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="c44a0-148">Basic</span></span>
- <span data-ttu-id="c44a0-149">Standard</span><span class="sxs-lookup"><span data-stu-id="c44a0-149">Standard</span></span>
- <span data-ttu-id="c44a0-150">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="c44a0-150">DataWarehouse</span></span>
- <span data-ttu-id="c44a0-151">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="c44a0-151">Stretch</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44a0-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c44a0-152">-ElasticPoolName</span></span>
<span data-ttu-id="c44a0-153">Annak a rugalmas készletnek a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c44a0-153">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44a0-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c44a0-154">-ResourceGroupName</span></span>
<span data-ttu-id="c44a0-155">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag a rugalmas készletet rendeli.</span><span class="sxs-lookup"><span data-stu-id="c44a0-155">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="c44a0-156">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c44a0-156">-ServerName</span></span>
<span data-ttu-id="c44a0-157">A rugalmas készletet tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c44a0-157">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="c44a0-158">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="c44a0-158">-StorageMB</span></span>
<span data-ttu-id="c44a0-159">A rugalmas készlet tárterületének korlátját adja meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="c44a0-159">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="c44a0-160">Ha nem adja meg ezt a paramétert, ez a parancsmag egy olyan értéket számít ki, amely a *DTU* paraméter értékétől függ.</span><span class="sxs-lookup"><span data-stu-id="c44a0-160">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="c44a0-161">Lásd: a [eDTU és a tárolási korlátozások](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) a lehetséges értékekhez.</span><span class="sxs-lookup"><span data-stu-id="c44a0-161">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44a0-162">-Címkék</span><span class="sxs-lookup"><span data-stu-id="c44a0-162">-Tags</span></span>
<span data-ttu-id="c44a0-163">A kulcs-érték párok szótárát adja meg egy kivonatoló táblázat formájában, amelyre ez a parancsmag a rugalmas készletet társítja.</span><span class="sxs-lookup"><span data-stu-id="c44a0-163">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="c44a0-164">Példa:</span><span class="sxs-lookup"><span data-stu-id="c44a0-164">For example:</span></span>

<span data-ttu-id="c44a0-165">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="c44a0-165">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44a0-166">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="c44a0-166">-ZoneRedundant</span></span>
<span data-ttu-id="c44a0-167">A zóna redundancia az Azure SQL rugalmas készlettel való társításhoz</span><span class="sxs-lookup"><span data-stu-id="c44a0-167">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44a0-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c44a0-168">-Confirm</span></span>
<span data-ttu-id="c44a0-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c44a0-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c44a0-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c44a0-170">-WhatIf</span></span>
<span data-ttu-id="c44a0-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c44a0-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c44a0-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c44a0-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c44a0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44a0-173">CommonParameters</span></span>
<span data-ttu-id="c44a0-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c44a0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44a0-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c44a0-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44a0-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c44a0-176">INPUTS</span></span>

### <span data-ttu-id="c44a0-177">Nincs</span><span class="sxs-lookup"><span data-stu-id="c44a0-177">None</span></span>
<span data-ttu-id="c44a0-178">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c44a0-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c44a0-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c44a0-179">OUTPUTS</span></span>

### <span data-ttu-id="c44a0-180">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="c44a0-180">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="c44a0-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c44a0-181">NOTES</span></span>

## <span data-ttu-id="c44a0-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c44a0-182">RELATED LINKS</span></span>

[<span data-ttu-id="c44a0-183">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c44a0-183">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c44a0-184">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="c44a0-184">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="c44a0-185">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="c44a0-185">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="c44a0-186">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c44a0-186">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c44a0-187">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c44a0-187">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c44a0-188">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c44a0-188">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
