---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 5b1901ef5d06d24e6561861dca3c8e1d89185d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495588"
---
# <span data-ttu-id="a9c36-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a9c36-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="a9c36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9c36-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c36-103">Rugalmas adatbázis-készletet hoz létre egy SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="a9c36-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9c36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9c36-104">SYNTAX</span></span>

### <span data-ttu-id="a9c36-105">DtuBasedPool (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9c36-105">DtuBasedPool (Default)</span></span>
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9c36-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="a9c36-106">VcoreBasedPool</span></span>
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9c36-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9c36-107">DESCRIPTION</span></span>
<span data-ttu-id="a9c36-108">A **New-AzureRmSqlElasticPool** parancsmag létrehoz egy rugalmas adatbázis-készletet egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="a9c36-108">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="a9c36-109">Több paraméter ( *-DTU,-DatabaseDtuMin és-DatabaseDtuMax* ) szükséges, hogy a beállítás értéke az adott paraméterhez tartozó érvényes értékek listájából származik.</span><span class="sxs-lookup"><span data-stu-id="a9c36-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="a9c36-110">A-DatabaseDtuMax 100-as normál-készlethez például csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="a9c36-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="a9c36-111">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="a9c36-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="a9c36-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a9c36-112">EXAMPLES</span></span>

### <span data-ttu-id="a9c36-113">1. példa: rugalmas készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="a9c36-113">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="a9c36-114">Ez a parancs egy rugalmas medencét hoz létre a ElasticPool01 nevű standard szolgáltatási rétegben.</span><span class="sxs-lookup"><span data-stu-id="a9c36-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="a9c36-115">A server01 nevű, ResourceGroup01 nevű Azure-erőforráscsoporthoz rendelt kiszolgáló a rugalmas készletet tárolja.</span><span class="sxs-lookup"><span data-stu-id="a9c36-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="a9c36-116">A parancs a készlet DTU és a készlet adatbázisainak értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9c36-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="a9c36-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9c36-117">PARAMETERS</span></span>

### <span data-ttu-id="a9c36-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9c36-118">-AsJob</span></span>
<span data-ttu-id="a9c36-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a9c36-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9c36-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a9c36-120">-ComputeGeneration</span></span>
<span data-ttu-id="a9c36-121">A hozzárendelni kívánt számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="a9c36-121">The compute generation to assign.</span></span>

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

### <span data-ttu-id="a9c36-122">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="a9c36-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="a9c36-123">Megadja, hogy a készletben lévő egyetlen adatbázisból hány adatbázis-átviteli egység (DTU) használható.</span><span class="sxs-lookup"><span data-stu-id="a9c36-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="a9c36-124">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a9c36-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="a9c36-125">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="a9c36-125">Basic.</span></span> <span data-ttu-id="a9c36-126">5 DTU</span><span class="sxs-lookup"><span data-stu-id="a9c36-126">5 DTUs</span></span>
- <span data-ttu-id="a9c36-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="a9c36-127">Standard.</span></span> <span data-ttu-id="a9c36-128">100 DTU</span><span class="sxs-lookup"><span data-stu-id="a9c36-128">100 DTUs</span></span>
- <span data-ttu-id="a9c36-129">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="a9c36-129">Premium.</span></span> <span data-ttu-id="a9c36-130">125 DTU: az érvényes értékek részleteiről az adott méretű medence táblázata [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a9c36-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="a9c36-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="a9c36-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="a9c36-132">Itt adhatja meg, hogy a rugalmas készlet milyen minimális számú DTU a készlet összes adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="a9c36-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="a9c36-133">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="a9c36-133">The default value is zero (0).</span></span>
<span data-ttu-id="a9c36-134">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="a9c36-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="a9c36-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="a9c36-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="a9c36-136">A Maxmium VCore megadhatja, hogy az SqlAzure-adatbázisok a készletben is használhatók legyenek.</span><span class="sxs-lookup"><span data-stu-id="a9c36-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="a9c36-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="a9c36-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="a9c36-138">A minimális VCore szám: bármely SqlAzure-adatbázis használható a készletben.</span><span class="sxs-lookup"><span data-stu-id="a9c36-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="a9c36-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c36-139">-DefaultProfile</span></span>
<span data-ttu-id="a9c36-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a9c36-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9c36-141">-Dtu</span><span class="sxs-lookup"><span data-stu-id="a9c36-141">-Dtu</span></span>
<span data-ttu-id="a9c36-142">A rugalmas készlet megosztott DTU teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9c36-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="a9c36-143">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a9c36-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="a9c36-144">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="a9c36-144">Basic.</span></span>
<span data-ttu-id="a9c36-145">100 DTU</span><span class="sxs-lookup"><span data-stu-id="a9c36-145">100 DTUs</span></span>
- <span data-ttu-id="a9c36-146">Standard.</span><span class="sxs-lookup"><span data-stu-id="a9c36-146">Standard.</span></span>
<span data-ttu-id="a9c36-147">100 DTU</span><span class="sxs-lookup"><span data-stu-id="a9c36-147">100 DTUs</span></span>
- <span data-ttu-id="a9c36-148">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="a9c36-148">Premium.</span></span>
<span data-ttu-id="a9c36-149">125 DTU: az érvényes értékek részleteiről az adott méretű medence táblázata [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a9c36-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="a9c36-150">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="a9c36-150">-Edition</span></span>
<span data-ttu-id="a9c36-151">A rugalmas készlethez használt Azure SQL-adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9c36-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="a9c36-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a9c36-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9c36-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="a9c36-153">None</span></span>
- <span data-ttu-id="a9c36-154">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="a9c36-154">Basic</span></span>
- <span data-ttu-id="a9c36-155">Standard</span><span class="sxs-lookup"><span data-stu-id="a9c36-155">Standard</span></span>
- <span data-ttu-id="a9c36-156">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="a9c36-156">Premium</span></span>
- <span data-ttu-id="a9c36-157">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="a9c36-157">DataWarehouse</span></span>
- <span data-ttu-id="a9c36-158">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="a9c36-158">Free</span></span>
- <span data-ttu-id="a9c36-159">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="a9c36-159">Stretch</span></span>
- <span data-ttu-id="a9c36-160">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="a9c36-160">GeneralPurpose</span></span>
- <span data-ttu-id="a9c36-161">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="a9c36-161">BusinessCritical</span></span>

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

### <span data-ttu-id="a9c36-162">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a9c36-162">-ElasticPoolName</span></span>
<span data-ttu-id="a9c36-163">Annak a rugalmas készletnek a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a9c36-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a9c36-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a9c36-164">-LicenseType</span></span>
<span data-ttu-id="a9c36-165">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="a9c36-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="a9c36-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c36-166">-ResourceGroupName</span></span>
<span data-ttu-id="a9c36-167">Annak az erőforrás-csoportnak a nevét adja meg, amelyre a parancsmag a rugalmas készletet rendeli.</span><span class="sxs-lookup"><span data-stu-id="a9c36-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="a9c36-168">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a9c36-168">-ServerName</span></span>
<span data-ttu-id="a9c36-169">A rugalmas készletet tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9c36-169">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="a9c36-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="a9c36-170">-StorageMB</span></span>
<span data-ttu-id="a9c36-171">A rugalmas készlet tárterületének korlátját adja meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="a9c36-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="a9c36-172">Ha nem adja meg ezt a paramétert, ez a parancsmag egy olyan értéket számít ki, amely a *DTU* paraméter értékétől függ.</span><span class="sxs-lookup"><span data-stu-id="a9c36-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="a9c36-173">Lásd: a [eDTU és a tárolási korlátozások](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) a lehetséges értékekhez.</span><span class="sxs-lookup"><span data-stu-id="a9c36-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="a9c36-174">-Címkék</span><span class="sxs-lookup"><span data-stu-id="a9c36-174">-Tags</span></span>
<span data-ttu-id="a9c36-175">A kulcs-érték párok szótárát adja meg egy kivonatoló táblázat formájában, amelyre ez a parancsmag a rugalmas készletet társítja.</span><span class="sxs-lookup"><span data-stu-id="a9c36-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="a9c36-176">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="a9c36-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a9c36-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="a9c36-177">-VCore</span></span>
<span data-ttu-id="a9c36-178">Az SQL Azure rugalmas készlet Vcores megosztott száma összesen.</span><span class="sxs-lookup"><span data-stu-id="a9c36-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="a9c36-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a9c36-179">-ZoneRedundant</span></span>
<span data-ttu-id="a9c36-180">A zóna redundancia az Azure SQL rugalmas készlettel való társításhoz</span><span class="sxs-lookup"><span data-stu-id="a9c36-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="a9c36-181">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a9c36-181">-Confirm</span></span>
<span data-ttu-id="a9c36-182">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a9c36-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c36-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c36-183">-WhatIf</span></span>
<span data-ttu-id="a9c36-184">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a9c36-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9c36-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9c36-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c36-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c36-186">CommonParameters</span></span>
<span data-ttu-id="a9c36-187">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9c36-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c36-188">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9c36-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c36-189">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9c36-189">INPUTS</span></span>

### <span data-ttu-id="a9c36-190">System. String</span><span class="sxs-lookup"><span data-stu-id="a9c36-190">System.String</span></span>

## <span data-ttu-id="a9c36-191">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9c36-191">OUTPUTS</span></span>

### <span data-ttu-id="a9c36-192">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="a9c36-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="a9c36-193">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9c36-193">NOTES</span></span>

## <span data-ttu-id="a9c36-194">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9c36-194">RELATED LINKS</span></span>

[<span data-ttu-id="a9c36-195">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a9c36-195">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a9c36-196">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="a9c36-196">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="a9c36-197">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="a9c36-197">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="a9c36-198">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a9c36-198">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a9c36-199">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a9c36-199">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a9c36-200">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="a9c36-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
