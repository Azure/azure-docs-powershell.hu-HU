---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194506"
---
# <span data-ttu-id="3315c-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3315c-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="3315c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3315c-102">SYNOPSIS</span></span>
<span data-ttu-id="3315c-103">Egy rugalmas adatbázis-készlet tulajdonságait módosítja az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="3315c-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="3315c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3315c-104">SYNTAX</span></span>

### <span data-ttu-id="3315c-105">DtuBasedPool (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3315c-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3315c-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="3315c-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3315c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3315c-107">DESCRIPTION</span></span>
<span data-ttu-id="3315c-108">A **set-AzSqlElasticPool** parancsmag az Azure SQL-adatbázisban egy rugalmas készlet tulajdonságainak beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3315c-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="3315c-109">Ez a parancsmag módosíthatja a eDTUs ( *DTU* ), a maximális tárterületet ( *StorageMB* ), a maximális eDTUs az adatbázisokban ( *DatabaseDtuMax* ) és a minimális eDTUs per Database ( *DatabaseDtuMin* ).</span><span class="sxs-lookup"><span data-stu-id="3315c-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="3315c-110">Több paraméter ( *-DTU,-DatabaseDtuMin és-DatabaseDtuMax* ) szükséges, hogy a beállítás értéke az adott paraméterhez tartozó érvényes értékek listájából származik.</span><span class="sxs-lookup"><span data-stu-id="3315c-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="3315c-111">A-DatabaseDtuMax 100-as normál-készlethez például csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="3315c-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="3315c-112">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3315c-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="3315c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="3315c-113">EXAMPLES</span></span>

### <span data-ttu-id="3315c-114">Példa 1: rugalmas készlet tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="3315c-114">Example 1: Modify properties for an elastic pool</span></span>
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

<span data-ttu-id="3315c-115">Ez a parancs módosítja a elasticpool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="3315c-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="3315c-116">A parancs beállítja a rugalmas készlet DTU számát a 1000-ra, és beállítja a minimális és a maximális DTU.</span><span class="sxs-lookup"><span data-stu-id="3315c-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="3315c-117">2. példa: rugalmas készlet tárterületének maximális méretét módosítja.</span><span class="sxs-lookup"><span data-stu-id="3315c-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

<span data-ttu-id="3315c-118">Ez a parancs módosítja a elasticpool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="3315c-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="3315c-119">A parancs a maximális tárterületet 2 TB-ra állítja a rugalmas poolban.</span><span class="sxs-lookup"><span data-stu-id="3315c-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="3315c-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="3315c-120">Example 3</span></span>

<span data-ttu-id="3315c-121">Egy rugalmas adatbázis-készlet tulajdonságait módosítja az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="3315c-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="3315c-122">autogenerated</span><span class="sxs-lookup"><span data-stu-id="3315c-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="3315c-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3315c-123">PARAMETERS</span></span>

### <span data-ttu-id="3315c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3315c-124">-AsJob</span></span>
<span data-ttu-id="3315c-125">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3315c-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3315c-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3315c-126">-ComputeGeneration</span></span>
<span data-ttu-id="3315c-127">A hozzárendelni kívánt számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="3315c-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="3315c-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="3315c-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="3315c-129">Azt adja meg, hogy a készletben lévő egyetlen adatbázis DTU legfeljebb hány elem használható.</span><span class="sxs-lookup"><span data-stu-id="3315c-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="3315c-130">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3315c-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="3315c-131">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3315c-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="3315c-132">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="3315c-132">Basic.</span></span>  <span data-ttu-id="3315c-133">5 DTU</span><span class="sxs-lookup"><span data-stu-id="3315c-133">5 DTUs</span></span>
- <span data-ttu-id="3315c-134">Standard.</span><span class="sxs-lookup"><span data-stu-id="3315c-134">Standard.</span></span> <span data-ttu-id="3315c-135">100 DTU</span><span class="sxs-lookup"><span data-stu-id="3315c-135">100 DTUs</span></span>
- <span data-ttu-id="3315c-136">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="3315c-136">Premium.</span></span> <span data-ttu-id="3315c-137">125 DTU</span><span class="sxs-lookup"><span data-stu-id="3315c-137">125 DTUs</span></span>

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

### <span data-ttu-id="3315c-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="3315c-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="3315c-139">Itt adhatja meg, hogy a rugalmas készlet milyen minimális számú DTU a készlet összes adatbázisához.</span><span class="sxs-lookup"><span data-stu-id="3315c-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="3315c-140">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3315c-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="3315c-141">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="3315c-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="3315c-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="3315c-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="3315c-143">A maximális VCore szám: bármely SqlAzure-adatbázis használható a készletben.</span><span class="sxs-lookup"><span data-stu-id="3315c-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="3315c-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="3315c-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="3315c-145">A minimális VCore szám: bármely SqlAzure-adatbázis használható a készletben.</span><span class="sxs-lookup"><span data-stu-id="3315c-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="3315c-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3315c-146">-DefaultProfile</span></span>
<span data-ttu-id="3315c-147">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3315c-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3315c-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="3315c-148">-Dtu</span></span>
<span data-ttu-id="3315c-149">A rugalmas készlet megosztott DTU teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3315c-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="3315c-150">Ha meg szeretné tudni, hogy mely értékek érvényesek, tekintse át az adott méretű készlet táblázatát a [rugalmas medencékben](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span><span class="sxs-lookup"><span data-stu-id="3315c-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="3315c-151">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3315c-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="3315c-152">Egyszerű.</span><span class="sxs-lookup"><span data-stu-id="3315c-152">Basic.</span></span> <span data-ttu-id="3315c-153">100 DTU</span><span class="sxs-lookup"><span data-stu-id="3315c-153">100 DTUs</span></span>
- <span data-ttu-id="3315c-154">Standard.</span><span class="sxs-lookup"><span data-stu-id="3315c-154">Standard.</span></span> <span data-ttu-id="3315c-155">100 DTU</span><span class="sxs-lookup"><span data-stu-id="3315c-155">100 DTUs</span></span>
- <span data-ttu-id="3315c-156">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="3315c-156">Premium.</span></span> <span data-ttu-id="3315c-157">125 DTU</span><span class="sxs-lookup"><span data-stu-id="3315c-157">125 DTUs</span></span>

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

### <span data-ttu-id="3315c-158">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="3315c-158">-Edition</span></span>
<span data-ttu-id="3315c-159">A rugalmas készlet Azure SQL-adatbázisának kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3315c-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="3315c-160">A kiadás nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="3315c-160">You cannot change the edition.</span></span> <span data-ttu-id="3315c-161">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3315c-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3315c-162">Nincs</span><span class="sxs-lookup"><span data-stu-id="3315c-162">None</span></span>
- <span data-ttu-id="3315c-163">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="3315c-163">Basic</span></span>
- <span data-ttu-id="3315c-164">Standard</span><span class="sxs-lookup"><span data-stu-id="3315c-164">Standard</span></span>
- <span data-ttu-id="3315c-165">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="3315c-165">Premium</span></span>
- <span data-ttu-id="3315c-166">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="3315c-166">DataWarehouse</span></span>
- <span data-ttu-id="3315c-167">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="3315c-167">Free</span></span>
- <span data-ttu-id="3315c-168">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="3315c-168">Stretch</span></span>
- <span data-ttu-id="3315c-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="3315c-169">GeneralPurpose</span></span>
- <span data-ttu-id="3315c-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="3315c-170">BusinessCritical</span></span>

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

### <span data-ttu-id="3315c-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3315c-171">-ElasticPoolName</span></span>
<span data-ttu-id="3315c-172">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3315c-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="3315c-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3315c-173">-LicenseType</span></span>
<span data-ttu-id="3315c-174">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="3315c-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="3315c-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3315c-175">-ResourceGroupName</span></span>
<span data-ttu-id="3315c-176">Annak az erőforráscsoport a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="3315c-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="3315c-177">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3315c-177">-ServerName</span></span>
<span data-ttu-id="3315c-178">A rugalmas készletet tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3315c-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="3315c-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="3315c-179">-StorageMB</span></span>
<span data-ttu-id="3315c-180">A rugalmas készlet tárterületének korlátját adja meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="3315c-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="3315c-181">További információt az New-AzSqlElasticPool parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="3315c-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="3315c-182">-Címkék</span><span class="sxs-lookup"><span data-stu-id="3315c-182">-Tags</span></span>
<span data-ttu-id="3315c-183">A kulcs-érték párok szótárát adja meg, hogy a parancsmag a rugalmas készletet a kivonatoló táblázat formájában társítja.</span><span class="sxs-lookup"><span data-stu-id="3315c-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="3315c-184">Példa: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="3315c-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="3315c-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="3315c-185">-VCore</span></span>
<span data-ttu-id="3315c-186">Az SQL Azure rugalmas készlet vcore megosztott száma összesen.</span><span class="sxs-lookup"><span data-stu-id="3315c-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="3315c-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="3315c-187">-ZoneRedundant</span></span>
<span data-ttu-id="3315c-188">A zóna redundancia az Azure SQL rugalmas készlettel való társításhoz</span><span class="sxs-lookup"><span data-stu-id="3315c-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="3315c-189">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3315c-189">-Confirm</span></span>
<span data-ttu-id="3315c-190">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3315c-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3315c-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3315c-191">-WhatIf</span></span>
<span data-ttu-id="3315c-192">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3315c-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3315c-193">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3315c-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3315c-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3315c-194">CommonParameters</span></span>
<span data-ttu-id="3315c-195">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3315c-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3315c-196">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3315c-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3315c-197">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3315c-197">INPUTS</span></span>

### <span data-ttu-id="3315c-198">System. String</span><span class="sxs-lookup"><span data-stu-id="3315c-198">System.String</span></span>

## <span data-ttu-id="3315c-199">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3315c-199">OUTPUTS</span></span>

### <span data-ttu-id="3315c-200">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="3315c-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="3315c-201">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3315c-201">NOTES</span></span>

## <span data-ttu-id="3315c-202">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3315c-202">RELATED LINKS</span></span>

[<span data-ttu-id="3315c-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3315c-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="3315c-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="3315c-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="3315c-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="3315c-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="3315c-206">Új – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3315c-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="3315c-207">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3315c-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
