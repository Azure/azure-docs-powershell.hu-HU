---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fbc0d1e1ac32906c081c5a9714c8420e0f1292e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668892"
---
# <span data-ttu-id="391a1-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="391a1-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="391a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="391a1-102">SYNOPSIS</span></span>
<span data-ttu-id="391a1-103">Rugalmas adatbázis-készletet hoz létre egy SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="391a1-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="391a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="391a1-104">SYNTAX</span></span>

### <span data-ttu-id="391a1-105">DtuBasedPool (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="391a1-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="391a1-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="391a1-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="391a1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="391a1-107">DESCRIPTION</span></span>
<span data-ttu-id="391a1-108">A **New-AzSqlElasticPool** parancsmag létrehoz egy rugalmas adatbázis-készletet egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="391a1-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="391a1-109">Több paraméter ( *-DTU,-DatabaseDtuMin és-DatabaseDtuMax* ) szükséges, hogy a beállítás értéke az adott paraméterhez tartozó érvényes értékek listájából származik.</span><span class="sxs-lookup"><span data-stu-id="391a1-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="391a1-110">A-DatabaseDtuMax 100-as normál-készlethez például csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="391a1-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="391a1-111">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="391a1-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="391a1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="391a1-112">EXAMPLES</span></span>

### <span data-ttu-id="391a1-113">1. példa: rugalmas készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="391a1-113">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="391a1-114">Ez a parancs egy rugalmas medencét hoz létre a ElasticPool01 nevű standard szolgáltatási rétegben.</span><span class="sxs-lookup"><span data-stu-id="391a1-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="391a1-115">A server01 nevű, ResourceGroup01 nevű Azure-erőforráscsoporthoz rendelt kiszolgáló a rugalmas készletet tárolja.</span><span class="sxs-lookup"><span data-stu-id="391a1-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="391a1-116">A parancs a készlet DTU és a készlet adatbázisainak értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="391a1-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="391a1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="391a1-117">PARAMETERS</span></span>

### <span data-ttu-id="391a1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="391a1-118">-AsJob</span></span>
<span data-ttu-id="391a1-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="391a1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="391a1-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="391a1-120">-ComputeGeneration</span></span>
<span data-ttu-id="391a1-121">A hozzárendelni kívánt számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="391a1-121">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391a1-122">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="391a1-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="391a1-123">Megadja, hogy a készletben lévő egyetlen adatbázisból hány adatbázis-átviteli egység (DTU) használható.</span><span class="sxs-lookup"><span data-stu-id="391a1-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="391a1-124">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="391a1-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="391a1-125">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="391a1-125">Basic.</span></span> <span data-ttu-id="391a1-126">5 DTU</span><span class="sxs-lookup"><span data-stu-id="391a1-126">5 DTUs</span></span>
- <span data-ttu-id="391a1-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="391a1-127">Standard.</span></span> <span data-ttu-id="391a1-128">100 DTU</span><span class="sxs-lookup"><span data-stu-id="391a1-128">100 DTUs</span></span>
- <span data-ttu-id="391a1-129">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="391a1-129">Premium.</span></span> <span data-ttu-id="391a1-130">125 DTU: az érvényes értékek részleteiről az adott méretű medence táblázata [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="391a1-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="391a1-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="391a1-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="391a1-132">Itt adhatja meg, hogy a rugalmas készlet milyen minimális számú DTU a készlet összes adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="391a1-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="391a1-133">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="391a1-133">The default value is zero (0).</span></span>
<span data-ttu-id="391a1-134">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="391a1-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="391a1-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="391a1-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="391a1-136">A Maxmium VCore megadhatja, hogy az SqlAzure-adatbázisok a készletben is használhatók legyenek.</span><span class="sxs-lookup"><span data-stu-id="391a1-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="391a1-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="391a1-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="391a1-138">A minimális VCore szám: bármely SqlAzure-adatbázis használható a készletben.</span><span class="sxs-lookup"><span data-stu-id="391a1-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="391a1-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="391a1-139">-DefaultProfile</span></span>
<span data-ttu-id="391a1-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="391a1-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="391a1-141">-Dtu</span><span class="sxs-lookup"><span data-stu-id="391a1-141">-Dtu</span></span>
<span data-ttu-id="391a1-142">A rugalmas készlet megosztott DTU teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="391a1-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="391a1-143">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="391a1-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="391a1-144">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="391a1-144">Basic.</span></span>
<span data-ttu-id="391a1-145">100 DTU</span><span class="sxs-lookup"><span data-stu-id="391a1-145">100 DTUs</span></span>
- <span data-ttu-id="391a1-146">Standard.</span><span class="sxs-lookup"><span data-stu-id="391a1-146">Standard.</span></span>
<span data-ttu-id="391a1-147">100 DTU</span><span class="sxs-lookup"><span data-stu-id="391a1-147">100 DTUs</span></span>
- <span data-ttu-id="391a1-148">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="391a1-148">Premium.</span></span>
<span data-ttu-id="391a1-149">125 DTU: az érvényes értékek részleteiről az adott méretű medence táblázata [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="391a1-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="391a1-150">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="391a1-150">-Edition</span></span>
<span data-ttu-id="391a1-151">A rugalmas készlethez használt Azure SQL-adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="391a1-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="391a1-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="391a1-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="391a1-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="391a1-153">None</span></span>
- <span data-ttu-id="391a1-154">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="391a1-154">Basic</span></span>
- <span data-ttu-id="391a1-155">Standard</span><span class="sxs-lookup"><span data-stu-id="391a1-155">Standard</span></span>
- <span data-ttu-id="391a1-156">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="391a1-156">Premium</span></span>
- <span data-ttu-id="391a1-157">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="391a1-157">DataWarehouse</span></span>
- <span data-ttu-id="391a1-158">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="391a1-158">Free</span></span>
- <span data-ttu-id="391a1-159">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="391a1-159">Stretch</span></span>
- <span data-ttu-id="391a1-160">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="391a1-160">GeneralPurpose</span></span>
- <span data-ttu-id="391a1-161">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="391a1-161">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391a1-162">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="391a1-162">-ElasticPoolName</span></span>
<span data-ttu-id="391a1-163">Annak a rugalmas készletnek a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="391a1-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391a1-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="391a1-164">-LicenseType</span></span>
<span data-ttu-id="391a1-165">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="391a1-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="391a1-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="391a1-166">-ResourceGroupName</span></span>
<span data-ttu-id="391a1-167">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag a rugalmas készletet rendeli.</span><span class="sxs-lookup"><span data-stu-id="391a1-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="391a1-168">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="391a1-168">-ServerName</span></span>
<span data-ttu-id="391a1-169">A rugalmas készletet tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="391a1-169">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="391a1-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="391a1-170">-StorageMB</span></span>
<span data-ttu-id="391a1-171">A rugalmas készlet tárterületének korlátját adja meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="391a1-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="391a1-172">Ha nem adja meg ezt a paramétert, ez a parancsmag egy olyan értéket számít ki, amely a *DTU* paraméter értékétől függ.</span><span class="sxs-lookup"><span data-stu-id="391a1-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="391a1-173">Lásd: a [eDTU és a tárolási korlátozások](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) a lehetséges értékekhez.</span><span class="sxs-lookup"><span data-stu-id="391a1-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="391a1-174">-Címkék</span><span class="sxs-lookup"><span data-stu-id="391a1-174">-Tags</span></span>
<span data-ttu-id="391a1-175">A kulcs-érték párok szótárát adja meg egy kivonatoló táblázat formájában, amelyre ez a parancsmag a rugalmas készletet társítja.</span><span class="sxs-lookup"><span data-stu-id="391a1-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="391a1-176">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="391a1-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="391a1-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="391a1-177">-VCore</span></span>
<span data-ttu-id="391a1-178">Az SQL Azure rugalmas készlet Vcores megosztott száma összesen.</span><span class="sxs-lookup"><span data-stu-id="391a1-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391a1-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="391a1-179">-ZoneRedundant</span></span>
<span data-ttu-id="391a1-180">A zóna redundancia az Azure SQL rugalmas készlettel való társításhoz</span><span class="sxs-lookup"><span data-stu-id="391a1-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="391a1-181">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="391a1-181">-Confirm</span></span>
<span data-ttu-id="391a1-182">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="391a1-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="391a1-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="391a1-183">-WhatIf</span></span>
<span data-ttu-id="391a1-184">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="391a1-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="391a1-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="391a1-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="391a1-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="391a1-186">CommonParameters</span></span>
<span data-ttu-id="391a1-187">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="391a1-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="391a1-188">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="391a1-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="391a1-189">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="391a1-189">INPUTS</span></span>

### <span data-ttu-id="391a1-190">System. String</span><span class="sxs-lookup"><span data-stu-id="391a1-190">System.String</span></span>

## <span data-ttu-id="391a1-191">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="391a1-191">OUTPUTS</span></span>

### <span data-ttu-id="391a1-192">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="391a1-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="391a1-193">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="391a1-193">NOTES</span></span>

## <span data-ttu-id="391a1-194">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="391a1-194">RELATED LINKS</span></span>

[<span data-ttu-id="391a1-195">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="391a1-195">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="391a1-196">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="391a1-196">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="391a1-197">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="391a1-197">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="391a1-198">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="391a1-198">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="391a1-199">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="391a1-199">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="391a1-200">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="391a1-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
