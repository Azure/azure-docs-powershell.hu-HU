---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: a27d8c91f7262e83b139b6662a1f5f401f964b56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845182"
---
# <span data-ttu-id="136bf-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="136bf-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="136bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="136bf-102">SYNOPSIS</span></span>
<span data-ttu-id="136bf-103">Rugalmas adatbázis-készletet hoz létre egy SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="136bf-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="136bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="136bf-104">SYNTAX</span></span>

### <span data-ttu-id="136bf-105">DtuBasedPool (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="136bf-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="136bf-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="136bf-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="136bf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="136bf-107">DESCRIPTION</span></span>
<span data-ttu-id="136bf-108">A **New-AzSqlElasticPool** parancsmag létrehoz egy rugalmas adatbázis-készletet egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="136bf-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="136bf-109">Több paraméter ( *-DTU,-DatabaseDtuMin és-DatabaseDtuMax* ) szükséges, hogy a beállítás értéke az adott paraméterhez tartozó érvényes értékek listájából származik.</span><span class="sxs-lookup"><span data-stu-id="136bf-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="136bf-110">A-DatabaseDtuMax 100-as normál-készlethez például csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="136bf-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="136bf-111">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="136bf-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="136bf-112">Példák</span><span class="sxs-lookup"><span data-stu-id="136bf-112">EXAMPLES</span></span>

### <span data-ttu-id="136bf-113">Példa 1: DTU elasztikus Pool létrehozása</span><span class="sxs-lookup"><span data-stu-id="136bf-113">Example 1: Create a DTU elastic pool</span></span>

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

<span data-ttu-id="136bf-114">Ez a parancs egy rugalmas medencét hoz létre a ElasticPool01 nevű standard szolgáltatási rétegben.</span><span class="sxs-lookup"><span data-stu-id="136bf-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="136bf-115">A server01 nevű, ResourceGroup01 nevű Azure-erőforráscsoporthoz rendelt kiszolgáló a rugalmas készletet tárolja.</span><span class="sxs-lookup"><span data-stu-id="136bf-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="136bf-116">A parancs a készlet DTU és a készlet adatbázisainak értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="136bf-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="136bf-117">2. példa: vCore elasztikus Pool létrehozása</span><span class="sxs-lookup"><span data-stu-id="136bf-117">Example 2: Create a vCore elastic pool</span></span>

```
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                :
```

<span data-ttu-id="136bf-118">Ez a parancs egy rugalmas medencét hoz létre a ElasticPool01 nevű GengeralPurpose-szolgáltatási rétegben.</span><span class="sxs-lookup"><span data-stu-id="136bf-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="136bf-119">A server01 nevű, ResourceGroup01 nevű Azure-erőforráscsoporthoz rendelt kiszolgáló a rugalmas készletet tárolja.</span><span class="sxs-lookup"><span data-stu-id="136bf-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="136bf-120">A parancs a készlet vCore és a készlet adatbázisainak értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="136bf-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="136bf-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="136bf-121">PARAMETERS</span></span>

### <span data-ttu-id="136bf-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="136bf-122">-AsJob</span></span>
<span data-ttu-id="136bf-123">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="136bf-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="136bf-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="136bf-124">-ComputeGeneration</span></span>
<span data-ttu-id="136bf-125">A hozzárendelni kívánt számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="136bf-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="136bf-126">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="136bf-126">-DatabaseDtuMax</span></span>
<span data-ttu-id="136bf-127">Megadja, hogy a készletben lévő egyetlen adatbázisból hány adatbázis-átviteli egység (DTU) használható.</span><span class="sxs-lookup"><span data-stu-id="136bf-127">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="136bf-128">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="136bf-128">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="136bf-129">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="136bf-129">Basic.</span></span> <span data-ttu-id="136bf-130">5 DTU</span><span class="sxs-lookup"><span data-stu-id="136bf-130">5 DTUs</span></span>
- <span data-ttu-id="136bf-131">Standard.</span><span class="sxs-lookup"><span data-stu-id="136bf-131">Standard.</span></span> <span data-ttu-id="136bf-132">100 DTU</span><span class="sxs-lookup"><span data-stu-id="136bf-132">100 DTUs</span></span>
- <span data-ttu-id="136bf-133">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="136bf-133">Premium.</span></span> <span data-ttu-id="136bf-134">125 DTU: az érvényes értékek részleteiről az adott méretű medence táblázata [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="136bf-134">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="136bf-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="136bf-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="136bf-136">Itt adhatja meg, hogy a rugalmas készlet milyen minimális számú DTU a készlet összes adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="136bf-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="136bf-137">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="136bf-137">The default value is zero (0).</span></span>
<span data-ttu-id="136bf-138">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="136bf-138">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="136bf-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="136bf-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="136bf-140">A maximális VCore szám: bármely SqlAzure-adatbázis használható a készletben.</span><span class="sxs-lookup"><span data-stu-id="136bf-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="136bf-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="136bf-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="136bf-142">A minimális VCore szám: bármely SqlAzure-adatbázis használható a készletben.</span><span class="sxs-lookup"><span data-stu-id="136bf-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="136bf-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="136bf-143">-DefaultProfile</span></span>
<span data-ttu-id="136bf-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="136bf-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="136bf-145">-Dtu</span><span class="sxs-lookup"><span data-stu-id="136bf-145">-Dtu</span></span>
<span data-ttu-id="136bf-146">A rugalmas készlet megosztott DTU teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="136bf-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="136bf-147">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="136bf-147">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="136bf-148">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="136bf-148">Basic.</span></span>
<span data-ttu-id="136bf-149">100 DTU</span><span class="sxs-lookup"><span data-stu-id="136bf-149">100 DTUs</span></span>
- <span data-ttu-id="136bf-150">Standard.</span><span class="sxs-lookup"><span data-stu-id="136bf-150">Standard.</span></span>
<span data-ttu-id="136bf-151">100 DTU</span><span class="sxs-lookup"><span data-stu-id="136bf-151">100 DTUs</span></span>
- <span data-ttu-id="136bf-152">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="136bf-152">Premium.</span></span>
<span data-ttu-id="136bf-153">125 DTU: az érvényes értékek részleteiről az adott méretű medence táblázata [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="136bf-153">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="136bf-154">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="136bf-154">-Edition</span></span>
<span data-ttu-id="136bf-155">A rugalmas készlethez használt Azure SQL-adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="136bf-155">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="136bf-156">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="136bf-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="136bf-157">Nincs</span><span class="sxs-lookup"><span data-stu-id="136bf-157">None</span></span>
- <span data-ttu-id="136bf-158">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="136bf-158">Basic</span></span>
- <span data-ttu-id="136bf-159">Standard</span><span class="sxs-lookup"><span data-stu-id="136bf-159">Standard</span></span>
- <span data-ttu-id="136bf-160">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="136bf-160">Premium</span></span>
- <span data-ttu-id="136bf-161">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="136bf-161">DataWarehouse</span></span>
- <span data-ttu-id="136bf-162">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="136bf-162">Free</span></span>
- <span data-ttu-id="136bf-163">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="136bf-163">Stretch</span></span>
- <span data-ttu-id="136bf-164">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="136bf-164">GeneralPurpose</span></span>
- <span data-ttu-id="136bf-165">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="136bf-165">BusinessCritical</span></span>

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

### <span data-ttu-id="136bf-166">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="136bf-166">-ElasticPoolName</span></span>
<span data-ttu-id="136bf-167">Annak a rugalmas készletnek a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="136bf-167">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="136bf-168">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="136bf-168">-LicenseType</span></span>
<span data-ttu-id="136bf-169">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="136bf-169">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="136bf-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="136bf-170">-ResourceGroupName</span></span>
<span data-ttu-id="136bf-171">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag a rugalmas készletet rendeli.</span><span class="sxs-lookup"><span data-stu-id="136bf-171">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="136bf-172">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="136bf-172">-ServerName</span></span>
<span data-ttu-id="136bf-173">A rugalmas készletet tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="136bf-173">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="136bf-174">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="136bf-174">-StorageMB</span></span>
<span data-ttu-id="136bf-175">A rugalmas készlet tárterületének korlátját adja meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="136bf-175">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="136bf-176">Ha nem adja meg ezt a paramétert, ez a parancsmag egy olyan értéket számít ki, amely a *DTU* paraméter értékétől függ.</span><span class="sxs-lookup"><span data-stu-id="136bf-176">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="136bf-177">Lásd: a [eDTU és a tárolási korlátozások](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) a lehetséges értékekhez.</span><span class="sxs-lookup"><span data-stu-id="136bf-177">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="136bf-178">-Címkék</span><span class="sxs-lookup"><span data-stu-id="136bf-178">-Tags</span></span>
<span data-ttu-id="136bf-179">A kulcs-érték párok szótárát adja meg egy kivonatoló táblázat formájában, amelyre ez a parancsmag a rugalmas készletet társítja.</span><span class="sxs-lookup"><span data-stu-id="136bf-179">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="136bf-180">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="136bf-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="136bf-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="136bf-181">-VCore</span></span>
<span data-ttu-id="136bf-182">Az SQL Azure rugalmas készlet Vcores megosztott száma összesen.</span><span class="sxs-lookup"><span data-stu-id="136bf-182">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="136bf-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="136bf-183">-ZoneRedundant</span></span>
<span data-ttu-id="136bf-184">A zóna redundancia az Azure SQL rugalmas készlettel való társításhoz</span><span class="sxs-lookup"><span data-stu-id="136bf-184">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="136bf-185">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="136bf-185">-Confirm</span></span>
<span data-ttu-id="136bf-186">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="136bf-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="136bf-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="136bf-187">-WhatIf</span></span>
<span data-ttu-id="136bf-188">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="136bf-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="136bf-189">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="136bf-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="136bf-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136bf-190">CommonParameters</span></span>
<span data-ttu-id="136bf-191">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="136bf-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136bf-192">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="136bf-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136bf-193">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="136bf-193">INPUTS</span></span>

### <span data-ttu-id="136bf-194">System. String</span><span class="sxs-lookup"><span data-stu-id="136bf-194">System.String</span></span>

## <span data-ttu-id="136bf-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="136bf-195">OUTPUTS</span></span>

### <span data-ttu-id="136bf-196">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="136bf-196">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="136bf-197">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="136bf-197">NOTES</span></span>

## <span data-ttu-id="136bf-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="136bf-198">RELATED LINKS</span></span>

[<span data-ttu-id="136bf-199">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="136bf-199">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="136bf-200">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="136bf-200">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="136bf-201">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="136bf-201">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="136bf-202">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="136bf-202">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="136bf-203">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="136bf-203">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="136bf-204">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="136bf-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
