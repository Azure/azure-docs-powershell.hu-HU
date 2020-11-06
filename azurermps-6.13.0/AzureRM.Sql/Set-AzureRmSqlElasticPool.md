---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 6b059905cdc1e9474ce455f78fac88f282b5ce10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497224"
---
# <span data-ttu-id="33736-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33736-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="33736-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33736-102">SYNOPSIS</span></span>
<span data-ttu-id="33736-103">Egy rugalmas adatbázis-készlet tulajdonságait módosítja az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="33736-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33736-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33736-104">SYNTAX</span></span>

### <span data-ttu-id="33736-105">DtuBasedPool (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33736-105">DtuBasedPool (Default)</span></span>
```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33736-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="33736-106">VcoreBasedPool</span></span>
```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33736-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="33736-107">DESCRIPTION</span></span>
<span data-ttu-id="33736-108">A **set-AzureRmSqlElasticPool** parancsmag az Azure SQL-adatbázisban egy rugalmas készlet tulajdonságainak beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="33736-108">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="33736-109">Ez a parancsmag módosíthatja a eDTUs ( *DTU* ), a maximális tárterületet ( *StorageMB* ), a maximális eDTUs az adatbázisokban ( *DatabaseDtuMax* ) és a minimális eDTUs per Database ( *DatqabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="33736-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>
<span data-ttu-id="33736-110">Több paraméter ( *-DTU,-DatabaseDtuMin és-DatabaseDtuMax* ) szükséges, hogy a beállítás értéke az adott paraméterhez tartozó érvényes értékek listájából származik.</span><span class="sxs-lookup"><span data-stu-id="33736-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="33736-111">A-DatabaseDtuMax 100-as normál-készlethez például csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="33736-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="33736-112">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="33736-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="33736-113">Példák</span><span class="sxs-lookup"><span data-stu-id="33736-113">EXAMPLES</span></span>

### <span data-ttu-id="33736-114">Példa 1: rugalmas készlet tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="33736-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="33736-115">Ez a parancs módosítja a elasticpool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="33736-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="33736-116">A parancs beállítja a rugalmas készlet DTU számát a 1000-ra, és beállítja a minimális és a maximális DTU.</span><span class="sxs-lookup"><span data-stu-id="33736-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="33736-117">2. példa: rugalmas készlet tárterületének maximális méretét módosítja.</span><span class="sxs-lookup"><span data-stu-id="33736-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="33736-118">Ez a parancs módosítja a elasticpool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="33736-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="33736-119">A parancs a maximális tárterületet 2 TB-ra állítja a rugalmas poolban.</span><span class="sxs-lookup"><span data-stu-id="33736-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="33736-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33736-120">PARAMETERS</span></span>

### <span data-ttu-id="33736-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33736-121">-AsJob</span></span>
<span data-ttu-id="33736-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="33736-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="33736-123">-ComputeGeneration</span></span>
<span data-ttu-id="33736-124">A hozzárendelni kívánt számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="33736-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="33736-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="33736-126">Azt adja meg, hogy a készletben lévő egyetlen adatbázis DTU legfeljebb hány elem használható.</span><span class="sxs-lookup"><span data-stu-id="33736-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="33736-127">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="33736-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="33736-128">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="33736-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="33736-129">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="33736-129">Basic.</span></span>  <span data-ttu-id="33736-130">5 DTU</span><span class="sxs-lookup"><span data-stu-id="33736-130">5 DTUs</span></span>
- <span data-ttu-id="33736-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="33736-131">Standard.</span></span> <span data-ttu-id="33736-132">100 DTU</span><span class="sxs-lookup"><span data-stu-id="33736-132">100 DTUs</span></span>
- <span data-ttu-id="33736-133">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="33736-133">Premium.</span></span> <span data-ttu-id="33736-134">125 DTU</span><span class="sxs-lookup"><span data-stu-id="33736-134">125 DTUs</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="33736-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="33736-136">Itt adhatja meg, hogy a rugalmas készlet milyen minimális számú DTU a készlet összes adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="33736-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="33736-137">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="33736-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="33736-138">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="33736-138">The default value is zero (0).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="33736-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="33736-140">A Maxmium VCore megadhatja, hogy az SqlAzure-adatbázisok a készletben is használhatók legyenek.</span><span class="sxs-lookup"><span data-stu-id="33736-140">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="33736-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="33736-142">A minimális VCore szám: bármely SqlAzure-adatbázis használható a készletben.</span><span class="sxs-lookup"><span data-stu-id="33736-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33736-143">-DefaultProfile</span></span>
<span data-ttu-id="33736-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="33736-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33736-145">-Dtu</span><span class="sxs-lookup"><span data-stu-id="33736-145">-Dtu</span></span>
<span data-ttu-id="33736-146">A rugalmas készlet megosztott DTU teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="33736-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="33736-147">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="33736-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="33736-148">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="33736-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="33736-149">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="33736-149">Basic.</span></span> <span data-ttu-id="33736-150">100 DTU</span><span class="sxs-lookup"><span data-stu-id="33736-150">100 DTUs</span></span>
- <span data-ttu-id="33736-151">Standard.</span><span class="sxs-lookup"><span data-stu-id="33736-151">Standard.</span></span> <span data-ttu-id="33736-152">100 DTU</span><span class="sxs-lookup"><span data-stu-id="33736-152">100 DTUs</span></span>
- <span data-ttu-id="33736-153">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="33736-153">Premium.</span></span> <span data-ttu-id="33736-154">125 DTU</span><span class="sxs-lookup"><span data-stu-id="33736-154">125 DTUs</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-155">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="33736-155">-Edition</span></span>
<span data-ttu-id="33736-156">A rugalmas készlet Azure SQL-adatbázisának kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="33736-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="33736-157">A kiadás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="33736-157">You cannot change the edition.</span></span> <span data-ttu-id="33736-158">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="33736-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="33736-159">Nincs</span><span class="sxs-lookup"><span data-stu-id="33736-159">None</span></span>
- <span data-ttu-id="33736-160">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="33736-160">Basic</span></span>
- <span data-ttu-id="33736-161">Standard</span><span class="sxs-lookup"><span data-stu-id="33736-161">Standard</span></span>
- <span data-ttu-id="33736-162">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="33736-162">Premium</span></span>
- <span data-ttu-id="33736-163">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="33736-163">DataWarehouse</span></span>
- <span data-ttu-id="33736-164">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="33736-164">Free</span></span>
- <span data-ttu-id="33736-165">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="33736-165">Stretch</span></span>
- <span data-ttu-id="33736-166">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="33736-166">GeneralPurpose</span></span>
- <span data-ttu-id="33736-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="33736-167">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="33736-168">-ElasticPoolName</span></span>
<span data-ttu-id="33736-169">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33736-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="33736-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="33736-170">-LicenseType</span></span>
<span data-ttu-id="33736-171">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="33736-171">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33736-172">-ResourceGroupName</span></span>
<span data-ttu-id="33736-173">Annak az erőforráscsoport a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="33736-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="33736-174">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="33736-174">-ServerName</span></span>
<span data-ttu-id="33736-175">A rugalmas készletet tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="33736-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="33736-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="33736-176">-StorageMB</span></span>
<span data-ttu-id="33736-177">A rugalmas készlet tárterületének korlátját adja meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="33736-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="33736-178">További információt az New-AzureRmSqlElasticPool parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="33736-178">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="33736-179">-Címkék</span><span class="sxs-lookup"><span data-stu-id="33736-179">-Tags</span></span>
<span data-ttu-id="33736-180">A kulcs-érték párok szótárát adja meg, hogy a parancsmag a rugalmas készletet a kivonatoló táblázat formájában társítja.</span><span class="sxs-lookup"><span data-stu-id="33736-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="33736-181">Példa: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="33736-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="33736-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="33736-182">-VCore</span></span>
<span data-ttu-id="33736-183">Az SQL Azure rugalmas készlet vcore megosztott száma összesen.</span><span class="sxs-lookup"><span data-stu-id="33736-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="33736-184">-ZoneRedundant</span></span>
<span data-ttu-id="33736-185">A zóna redundancia az Azure SQL rugalmas készlettel való társításhoz</span><span class="sxs-lookup"><span data-stu-id="33736-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33736-186">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="33736-186">-Confirm</span></span>
<span data-ttu-id="33736-187">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="33736-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33736-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33736-188">-WhatIf</span></span>
<span data-ttu-id="33736-189">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="33736-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33736-190">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="33736-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33736-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33736-191">CommonParameters</span></span>
<span data-ttu-id="33736-192">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33736-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33736-193">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33736-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33736-194">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33736-194">INPUTS</span></span>

### <span data-ttu-id="33736-195">System. String</span><span class="sxs-lookup"><span data-stu-id="33736-195">System.String</span></span>

## <span data-ttu-id="33736-196">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33736-196">OUTPUTS</span></span>

### <span data-ttu-id="33736-197">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="33736-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="33736-198">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33736-198">NOTES</span></span>

## <span data-ttu-id="33736-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33736-199">RELATED LINKS</span></span>

[<span data-ttu-id="33736-200">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33736-200">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="33736-201">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="33736-201">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="33736-202">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="33736-202">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="33736-203">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33736-203">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="33736-204">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="33736-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
