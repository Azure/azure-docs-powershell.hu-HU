---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 563cddc1723f0706eb5cdde691e9ab960e871989
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498703"
---
# <span data-ttu-id="43643-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="43643-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="43643-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43643-102">SYNOPSIS</span></span>
<span data-ttu-id="43643-103">Egy rugalmas adatbázis-készlet tulajdonságait módosítja az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="43643-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43643-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43643-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43643-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43643-105">DESCRIPTION</span></span>
<span data-ttu-id="43643-106">A **set-AzureRmSqlElasticPool** parancsmag az Azure SQL-adatbázisban egy rugalmas készlet tulajdonságainak beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="43643-106">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="43643-107">Ez a parancsmag módosíthatja a eDTUs ( *DTU* ), a maximális tárterületet ( *StorageMB* ), a maximális eDTUs az adatbázisokban ( *DatabaseDtuMax* ) és a minimális eDTUs per Database ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="43643-107">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>

<span data-ttu-id="43643-108">Több paraméter ( *-DTU,-DatabaseDtuMin és-DatabaseDtuMax* ) szükséges, hogy a beállítás értéke az adott paraméterhez tartozó érvényes értékek listájából származik.</span><span class="sxs-lookup"><span data-stu-id="43643-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="43643-109">A-DatabaseDtuMax 100-as normál-készlethez például csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="43643-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="43643-110">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="43643-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="43643-111">Példák</span><span class="sxs-lookup"><span data-stu-id="43643-111">EXAMPLES</span></span>

### <span data-ttu-id="43643-112">Példa 1: rugalmas készlet tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="43643-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="43643-113">Ez a parancs módosítja a elasticpool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="43643-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="43643-114">A parancs beállítja a rugalmas készlet DTU számát a 1000-ra, és beállítja a minimális és a maximális DTU.</span><span class="sxs-lookup"><span data-stu-id="43643-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="43643-115">2. példa: rugalmas készlet tárterületének maximális méretét módosítja.</span><span class="sxs-lookup"><span data-stu-id="43643-115">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="43643-116">Ez a parancs módosítja a elasticpool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="43643-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="43643-117">A parancs a maximális tárterületet 2 TB-ra állítja a rugalmas poolban.</span><span class="sxs-lookup"><span data-stu-id="43643-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="43643-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43643-118">PARAMETERS</span></span>

### <span data-ttu-id="43643-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43643-119">-AsJob</span></span>
<span data-ttu-id="43643-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43643-120">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="43643-121">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="43643-121">-DatabaseDtuMax</span></span>
<span data-ttu-id="43643-122">Azt adja meg, hogy a készletben lévő egyetlen adatbázis DTU legfeljebb hány elem használható.</span><span class="sxs-lookup"><span data-stu-id="43643-122">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="43643-123">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="43643-123">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="43643-124">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="43643-124">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="43643-125">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="43643-125">Basic.</span></span>  <span data-ttu-id="43643-126">5 DTU</span><span class="sxs-lookup"><span data-stu-id="43643-126">5 DTUs</span></span>
- <span data-ttu-id="43643-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="43643-127">Standard.</span></span> <span data-ttu-id="43643-128">100 DTU</span><span class="sxs-lookup"><span data-stu-id="43643-128">100 DTUs</span></span>
- <span data-ttu-id="43643-129">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="43643-129">Premium.</span></span> <span data-ttu-id="43643-130">125 DTU</span><span class="sxs-lookup"><span data-stu-id="43643-130">125 DTUs</span></span>


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

### <span data-ttu-id="43643-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="43643-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="43643-132">Itt adhatja meg, hogy a rugalmas készlet milyen minimális számú DTU a készlet összes adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="43643-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="43643-133">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="43643-133">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="43643-134">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="43643-134">The default value is zero (0).</span></span>

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

### <span data-ttu-id="43643-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43643-135">-DefaultProfile</span></span>
<span data-ttu-id="43643-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43643-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43643-137">-Dtu</span><span class="sxs-lookup"><span data-stu-id="43643-137">-Dtu</span></span>
<span data-ttu-id="43643-138">A rugalmas készlet megosztott DTU teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="43643-138">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="43643-139">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="43643-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="43643-140">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="43643-140">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="43643-141">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="43643-141">Basic.</span></span> <span data-ttu-id="43643-142">100 DTU</span><span class="sxs-lookup"><span data-stu-id="43643-142">100 DTUs</span></span>
- <span data-ttu-id="43643-143">Standard.</span><span class="sxs-lookup"><span data-stu-id="43643-143">Standard.</span></span> <span data-ttu-id="43643-144">100 DTU</span><span class="sxs-lookup"><span data-stu-id="43643-144">100 DTUs</span></span>
- <span data-ttu-id="43643-145">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="43643-145">Premium.</span></span> <span data-ttu-id="43643-146">125 DTU</span><span class="sxs-lookup"><span data-stu-id="43643-146">125 DTUs</span></span>

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

### <span data-ttu-id="43643-147">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="43643-147">-Edition</span></span>
<span data-ttu-id="43643-148">A rugalmas készlet Azure SQL-adatbázisának kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="43643-148">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="43643-149">A kiadás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="43643-149">You cannot change the edition.</span></span> <span data-ttu-id="43643-150">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="43643-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43643-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="43643-151">None</span></span>
- <span data-ttu-id="43643-152">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="43643-152">Basic</span></span>
- <span data-ttu-id="43643-153">Standard</span><span class="sxs-lookup"><span data-stu-id="43643-153">Standard</span></span>
- <span data-ttu-id="43643-154">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="43643-154">Premium</span></span>
- <span data-ttu-id="43643-155">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="43643-155">DataWarehouse</span></span>

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

### <span data-ttu-id="43643-156">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="43643-156">-ElasticPoolName</span></span>
<span data-ttu-id="43643-157">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43643-157">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43643-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43643-158">-ResourceGroupName</span></span>
<span data-ttu-id="43643-159">Annak az erőforráscsoport a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="43643-159">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="43643-160">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="43643-160">-ServerName</span></span>
<span data-ttu-id="43643-161">A rugalmas készletet tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43643-161">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="43643-162">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="43643-162">-StorageMB</span></span>
<span data-ttu-id="43643-163">A rugalmas készlet tárterületének korlátját adja meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="43643-163">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="43643-164">További információt az New-AzureRmSqlElasticPool parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="43643-164">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="43643-165">-Címkék</span><span class="sxs-lookup"><span data-stu-id="43643-165">-Tags</span></span>
<span data-ttu-id="43643-166">A kulcs-érték párok szótárát adja meg, hogy a parancsmag a rugalmas készletet a kivonatoló táblázat formájában társítja.</span><span class="sxs-lookup"><span data-stu-id="43643-166">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="43643-167">Példa:</span><span class="sxs-lookup"><span data-stu-id="43643-167">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="43643-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="43643-168">-ZoneRedundant</span></span>
<span data-ttu-id="43643-169">A zóna redundancia az Azure SQL rugalmas készlettel való társításhoz</span><span class="sxs-lookup"><span data-stu-id="43643-169">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="43643-170">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43643-170">-Confirm</span></span>
<span data-ttu-id="43643-171">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43643-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43643-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43643-172">-WhatIf</span></span>
<span data-ttu-id="43643-173">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43643-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43643-174">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43643-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43643-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43643-175">CommonParameters</span></span>
<span data-ttu-id="43643-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43643-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43643-177">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43643-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43643-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43643-178">INPUTS</span></span>

### <span data-ttu-id="43643-179">Nincs</span><span class="sxs-lookup"><span data-stu-id="43643-179">None</span></span>
<span data-ttu-id="43643-180">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="43643-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43643-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43643-181">OUTPUTS</span></span>

### <span data-ttu-id="43643-182">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="43643-182">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="43643-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43643-183">NOTES</span></span>

## <span data-ttu-id="43643-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43643-184">RELATED LINKS</span></span>

[<span data-ttu-id="43643-185">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="43643-185">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="43643-186">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="43643-186">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="43643-187">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="43643-187">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="43643-188">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="43643-188">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="43643-189">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="43643-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
