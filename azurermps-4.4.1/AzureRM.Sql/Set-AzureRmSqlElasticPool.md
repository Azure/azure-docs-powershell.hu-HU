---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 512c77862c44af68b26eb300eb9a692c115b0750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494602"
---
# <span data-ttu-id="f9f54-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f9f54-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="f9f54-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9f54-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f54-103">Egy rugalmas adatbázis-készlet tulajdonságait módosítja az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="f9f54-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9f54-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9f54-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9f54-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9f54-105">DESCRIPTION</span></span>
<span data-ttu-id="f9f54-106">A **set-AzureRmSqlElasticPool** parancsmag a rugalmas adatbázis-készlet tulajdonságait egy Azure SQL-adatbázisban módosítja.</span><span class="sxs-lookup"><span data-stu-id="f9f54-106">The **Set-AzureRmSqlElasticPool** cmdlet modifies properties for an elastic database pool in an Azure SQL Database.</span></span> <span data-ttu-id="f9f54-107">Ezzel a parancsmaggal az adatbázis minimális átviteli egységeit (DTU) módosíthatja az adatbázis maximális DTU, a készlet DTU számát és a készlet tárterületének korlátját is.</span><span class="sxs-lookup"><span data-stu-id="f9f54-107">This cmdlet can modify the minimum Database Throughput Units (DTUs) per database in addition to the maximum DTUs per database, the number of DTUs for the pool, and the storage limit for the pool.</span></span>

<span data-ttu-id="f9f54-108">Több paraméter ( *-DTU,-DatabaseDtuMin és-DatabaseDtuMax* ) szükséges, hogy a beállítás értéke az adott paraméterhez tartozó érvényes értékek listájából származik.</span><span class="sxs-lookup"><span data-stu-id="f9f54-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="f9f54-109">A-DatabaseDtuMax 100-as normál-készlethez például csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="f9f54-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="f9f54-110">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="f9f54-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="f9f54-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f9f54-111">EXAMPLES</span></span>

### <span data-ttu-id="f9f54-112">Példa 1: rugalmas készlet tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="f9f54-112">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="f9f54-113">Ez a parancs módosítja a elasticpool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="f9f54-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="f9f54-114">A parancs beállítja a rugalmas készlet DTU számát a 1000-ra, és beállítja a minimális és a maximális DTU.</span><span class="sxs-lookup"><span data-stu-id="f9f54-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="f9f54-115">2. példa: rugalmas készlet maximális tárterületének módosítása</span><span class="sxs-lookup"><span data-stu-id="f9f54-115">Example 2: Modify the max storage of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="f9f54-116">Ez a parancs módosítja a elasticpool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="f9f54-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="f9f54-117">A parancs a maximális tárterületet 2 TB-ra állítja a rugalmas poolban.</span><span class="sxs-lookup"><span data-stu-id="f9f54-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="f9f54-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9f54-118">PARAMETERS</span></span>

### <span data-ttu-id="f9f54-119">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="f9f54-119">-DatabaseDtuMax</span></span>
<span data-ttu-id="f9f54-120">Azt adja meg, hogy a készletben lévő egyetlen adatbázis DTU legfeljebb hány elem használható.</span><span class="sxs-lookup"><span data-stu-id="f9f54-120">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="f9f54-121">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="f9f54-121">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="f9f54-122">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f9f54-122">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="f9f54-123">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="f9f54-123">Basic.</span></span>  <span data-ttu-id="f9f54-124">5 DTU</span><span class="sxs-lookup"><span data-stu-id="f9f54-124">5 DTUs</span></span>
- <span data-ttu-id="f9f54-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="f9f54-125">Standard.</span></span> <span data-ttu-id="f9f54-126">100 DTU</span><span class="sxs-lookup"><span data-stu-id="f9f54-126">100 DTUs</span></span>
- <span data-ttu-id="f9f54-127">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="f9f54-127">Premium.</span></span> <span data-ttu-id="f9f54-128">125 DTU</span><span class="sxs-lookup"><span data-stu-id="f9f54-128">125 DTUs</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f54-129">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="f9f54-129">-DatabaseDtuMin</span></span>
<span data-ttu-id="f9f54-130">Itt adhatja meg, hogy a rugalmas készlet milyen minimális számú DTU a készlet összes adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="f9f54-130">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="f9f54-131">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="f9f54-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="f9f54-132">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="f9f54-132">The default value is zero (0).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f54-133">-Dtu</span><span class="sxs-lookup"><span data-stu-id="f9f54-133">-Dtu</span></span>
<span data-ttu-id="f9f54-134">A rugalmas készlet megosztott DTU teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9f54-134">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="f9f54-135">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="f9f54-135">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="f9f54-136">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f9f54-136">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="f9f54-137">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="f9f54-137">Basic.</span></span> <span data-ttu-id="f9f54-138">100 DTU</span><span class="sxs-lookup"><span data-stu-id="f9f54-138">100 DTUs</span></span>
- <span data-ttu-id="f9f54-139">Standard.</span><span class="sxs-lookup"><span data-stu-id="f9f54-139">Standard.</span></span> <span data-ttu-id="f9f54-140">100 DTU</span><span class="sxs-lookup"><span data-stu-id="f9f54-140">100 DTUs</span></span>
- <span data-ttu-id="f9f54-141">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="f9f54-141">Premium.</span></span> <span data-ttu-id="f9f54-142">125 DTU</span><span class="sxs-lookup"><span data-stu-id="f9f54-142">125 DTUs</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f54-143">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="f9f54-143">-Edition</span></span>
<span data-ttu-id="f9f54-144">A rugalmas készlet Azure SQL-adatbázisának kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9f54-144">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="f9f54-145">A kiadás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="f9f54-145">You cannot change the edition.</span></span> <span data-ttu-id="f9f54-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f9f54-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9f54-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="f9f54-147">None</span></span>
- <span data-ttu-id="f9f54-148">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="f9f54-148">Basic</span></span>
- <span data-ttu-id="f9f54-149">Standard</span><span class="sxs-lookup"><span data-stu-id="f9f54-149">Standard</span></span>
- <span data-ttu-id="f9f54-150">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="f9f54-150">Premium</span></span>
- <span data-ttu-id="f9f54-151">PremiumRS</span><span class="sxs-lookup"><span data-stu-id="f9f54-151">PremiumRS</span></span>
- <span data-ttu-id="f9f54-152">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="f9f54-152">DataWarehouse</span></span>
- <span data-ttu-id="f9f54-153">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="f9f54-153">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f54-154">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f9f54-154">-ElasticPoolName</span></span>
<span data-ttu-id="f9f54-155">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9f54-155">Specifies the name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9f54-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f54-156">-ResourceGroupName</span></span>
<span data-ttu-id="f9f54-157">Annak az erőforráscsoport a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f9f54-157">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="f9f54-158">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f9f54-158">-ServerName</span></span>
<span data-ttu-id="f9f54-159">A rugalmas készletet tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9f54-159">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="f9f54-160">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="f9f54-160">-StorageMB</span></span>
<span data-ttu-id="f9f54-161">A rugalmas készlet tárterületének korlátját adja meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="f9f54-161">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="f9f54-162">További információt az New-AzureRmSqlElasticPool parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="f9f54-162">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f54-163">-Címkék</span><span class="sxs-lookup"><span data-stu-id="f9f54-163">-Tags</span></span>
<span data-ttu-id="f9f54-164">A kulcs-érték párok szótárát adja meg, hogy a parancsmag a rugalmas készletet a kivonatoló táblázat formájában társítja.</span><span class="sxs-lookup"><span data-stu-id="f9f54-164">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="f9f54-165">Példa:</span><span class="sxs-lookup"><span data-stu-id="f9f54-165">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f54-166">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f9f54-166">-Confirm</span></span>
<span data-ttu-id="f9f54-167">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f9f54-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9f54-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f54-168">-WhatIf</span></span>
<span data-ttu-id="f9f54-169">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f9f54-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9f54-170">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9f54-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9f54-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f54-171">-DefaultProfile</span></span>
<span data-ttu-id="f9f54-172">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9f54-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9f54-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f54-173">CommonParameters</span></span>
<span data-ttu-id="f9f54-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9f54-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f54-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9f54-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f54-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9f54-176">INPUTS</span></span>

## <span data-ttu-id="f9f54-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9f54-177">OUTPUTS</span></span>

### <span data-ttu-id="f9f54-178">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="f9f54-178">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="f9f54-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9f54-179">NOTES</span></span>

## <span data-ttu-id="f9f54-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9f54-180">RELATED LINKS</span></span>

[<span data-ttu-id="f9f54-181">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f9f54-181">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f9f54-182">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f9f54-182">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="f9f54-183">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f9f54-183">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="f9f54-184">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f9f54-184">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f9f54-185">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f9f54-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
