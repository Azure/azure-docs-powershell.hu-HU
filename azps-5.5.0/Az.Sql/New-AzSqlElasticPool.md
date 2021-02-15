---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 64234421f7507bb77511f136efe60657f439228f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158243"
---
# <span data-ttu-id="46142-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46142-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="46142-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46142-102">SYNOPSIS</span></span>
<span data-ttu-id="46142-103">Rugalmas adatbáziskészletet hoz létre egy SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="46142-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="46142-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="46142-104">SYNTAX</span></span>

### <span data-ttu-id="46142-105">DtuBasedPool (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46142-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46142-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="46142-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46142-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="46142-107">DESCRIPTION</span></span>
<span data-ttu-id="46142-108">A **New-AzSqlElasticPool** parancsmag rugalmas adatbáziskészletet hoz létre egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="46142-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="46142-109">Számos paraméter (*-Dtu, -DatabaseDtuMin és -DatabaseDtuMax*) esetén a beállított érték szerepel az adott paraméter érvényes értékeinek listájában.</span><span class="sxs-lookup"><span data-stu-id="46142-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="46142-110">Egy normál 100 eDTU-készlet esetén például a -DatabaseDtuMax érték csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="46142-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="46142-111">Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="46142-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="46142-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="46142-112">EXAMPLES</span></span>

### <span data-ttu-id="46142-113">1. példa: DTU rugalmas készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="46142-113">Example 1: Create a DTU elastic pool</span></span>

```powershell
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

<span data-ttu-id="46142-114">Ez a parancs rugalmas készletet hoz létre az RugalmasságPool01 nevű standard szolgáltatásszinten.</span><span class="sxs-lookup"><span data-stu-id="46142-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="46142-115">Az Erőforráscsoport01 nevű Azure-erőforráscsoporthoz rendelt kiszolgáló a kiszolgáló01 nevű rugalmas készletet használja.</span><span class="sxs-lookup"><span data-stu-id="46142-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="46142-116">A parancs megadja a készlet és a készlet adatbázisai DTU tulajdonságértékét.</span><span class="sxs-lookup"><span data-stu-id="46142-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="46142-117">2. példa: Rugalmas vCore-készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="46142-117">Example 2: Create a vCore elastic pool</span></span>

```powershell
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

<span data-ttu-id="46142-118">Ez a parancs egy rugalmassági készletet hoz létre a GengeralPurpose service tierjében, az RugalmasságPool01 nevű rétegben.</span><span class="sxs-lookup"><span data-stu-id="46142-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="46142-119">Az Erőforráscsoport01 nevű Azure-erőforráscsoporthoz rendelt kiszolgáló a kiszolgáló01 nevű rugalmas készletet használja.</span><span class="sxs-lookup"><span data-stu-id="46142-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="46142-120">A parancs megadja a készlet és a készletben található adatbázisok vCore tulajdonságértékét.</span><span class="sxs-lookup"><span data-stu-id="46142-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="46142-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="46142-121">Example 3</span></span>

<span data-ttu-id="46142-122">Rugalmas adatbáziskészletet hoz létre egy SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="46142-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="46142-123">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="46142-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="46142-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46142-124">PARAMETERS</span></span>

### <span data-ttu-id="46142-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46142-125">-AsJob</span></span>
<span data-ttu-id="46142-126">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="46142-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46142-127">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="46142-127">-ComputeGeneration</span></span>
<span data-ttu-id="46142-128">A hozzárendelni megfelelő számítási generáció.</span><span class="sxs-lookup"><span data-stu-id="46142-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="46142-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="46142-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="46142-130">Azt adja meg, hogy a készlet bármelyik adatbázisa legfeljebb hány adatbázist tud felhasználtan.</span><span class="sxs-lookup"><span data-stu-id="46142-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="46142-131">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="46142-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="46142-132">Alapszintű.</span><span class="sxs-lookup"><span data-stu-id="46142-132">Basic.</span></span> <span data-ttu-id="46142-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="46142-133">5 DTUs</span></span>
- <span data-ttu-id="46142-134">Normál.</span><span class="sxs-lookup"><span data-stu-id="46142-134">Standard.</span></span> <span data-ttu-id="46142-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="46142-135">100 DTUs</span></span>
- <span data-ttu-id="46142-136">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="46142-136">Premium.</span></span> <span data-ttu-id="46142-137">125 DTUs Az értékek érvényességének részleteit az adott méretkészlet rugalmas készletekben található táblázatában [láthatja.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="46142-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="46142-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="46142-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="46142-139">Megadja, hogy a rugalmas készlet hány DTUs-t garantál a készlet összes adatbázisának.</span><span class="sxs-lookup"><span data-stu-id="46142-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="46142-140">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="46142-140">The default value is zero (0).</span></span>
<span data-ttu-id="46142-141">Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="46142-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="46142-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="46142-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="46142-143">Az SqlAzure-adatbázis által a készletben megengedett maximális VCore-szám.</span><span class="sxs-lookup"><span data-stu-id="46142-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="46142-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="46142-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="46142-145">Az SqlAzure-adatbázis által a készletben felhasznált minimális VCore-szám.</span><span class="sxs-lookup"><span data-stu-id="46142-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="46142-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46142-146">-DefaultProfile</span></span>
<span data-ttu-id="46142-147">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="46142-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46142-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="46142-148">-Dtu</span></span>
<span data-ttu-id="46142-149">A rugalmas készlet megosztott DTUS-inak teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="46142-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="46142-150">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="46142-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="46142-151">Alapszintű.</span><span class="sxs-lookup"><span data-stu-id="46142-151">Basic.</span></span>
<span data-ttu-id="46142-152">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="46142-152">100 DTUs</span></span>
- <span data-ttu-id="46142-153">Normál.</span><span class="sxs-lookup"><span data-stu-id="46142-153">Standard.</span></span>
<span data-ttu-id="46142-154">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="46142-154">100 DTUs</span></span>
- <span data-ttu-id="46142-155">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="46142-155">Premium.</span></span>
<span data-ttu-id="46142-156">125 DTUs Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="46142-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="46142-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="46142-157">-Edition</span></span>
<span data-ttu-id="46142-158">A rugalmas készlethez használt Azure SQL-adatbázis kiadását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="46142-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="46142-159">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="46142-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46142-160">Nincs</span><span class="sxs-lookup"><span data-stu-id="46142-160">None</span></span>
- <span data-ttu-id="46142-161">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="46142-161">Basic</span></span>
- <span data-ttu-id="46142-162">Normál</span><span class="sxs-lookup"><span data-stu-id="46142-162">Standard</span></span>
- <span data-ttu-id="46142-163">Prémium</span><span class="sxs-lookup"><span data-stu-id="46142-163">Premium</span></span>
- <span data-ttu-id="46142-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="46142-164">DataWarehouse</span></span>
- <span data-ttu-id="46142-165">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="46142-165">Free</span></span>
- <span data-ttu-id="46142-166">Nyújtás</span><span class="sxs-lookup"><span data-stu-id="46142-166">Stretch</span></span>
- <span data-ttu-id="46142-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="46142-167">GeneralPurpose</span></span>
- <span data-ttu-id="46142-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="46142-168">BusinessCritical</span></span>

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

### <span data-ttu-id="46142-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="46142-169">-ElasticPoolName</span></span>
<span data-ttu-id="46142-170">A parancsmag által létrehozott rugalmas készlet neve.</span><span class="sxs-lookup"><span data-stu-id="46142-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="46142-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="46142-171">-LicenseType</span></span>
<span data-ttu-id="46142-172">Az Azure Sql-adatbázis licenctípusa.</span><span class="sxs-lookup"><span data-stu-id="46142-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="46142-173">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="46142-173">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="46142-174">Az SQL rugalmassági készlet karbantartási konfigurációs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="46142-174">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="46142-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46142-175">-ResourceGroupName</span></span>
<span data-ttu-id="46142-176">Annak az erőforráscsoportnak a neve, amelyhez a parancsmag hozzárendeli a rugalmas készletet.</span><span class="sxs-lookup"><span data-stu-id="46142-176">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="46142-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="46142-177">-ServerName</span></span>
<span data-ttu-id="46142-178">A rugalmas készletet tartalmazó kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="46142-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="46142-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="46142-179">-StorageMB</span></span>
<span data-ttu-id="46142-180">A rugalmas készlet tárterületkorlátját határozza meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="46142-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="46142-181">Ha nem adja meg ezt a paramétert, ez a parancsmag a Dtu paraméter *értékétől* függ.</span><span class="sxs-lookup"><span data-stu-id="46142-181">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="46142-182">A [lehetséges értékekre vonatkozó eDTU](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) és tárterületkorlátok.</span><span class="sxs-lookup"><span data-stu-id="46142-182">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="46142-183">-Címkék</span><span class="sxs-lookup"><span data-stu-id="46142-183">-Tags</span></span>
<span data-ttu-id="46142-184">Egy olyan kulcsérték-párok szótárát adja meg kivonattábla formájában, amely a parancsmag a rugalmas készlethez van társítva.</span><span class="sxs-lookup"><span data-stu-id="46142-184">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="46142-185">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="46142-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="46142-186">-VCore</span><span class="sxs-lookup"><span data-stu-id="46142-186">-VCore</span></span>
<span data-ttu-id="46142-187">Az Sql Azure rugalmassági készletre vonatkozó vcore-ek összesített megosztott száma.</span><span class="sxs-lookup"><span data-stu-id="46142-187">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="46142-188">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="46142-188">-ZoneRedundant</span></span>
<span data-ttu-id="46142-189">The zone redundancy to associate with the Azure Sql Elastic Pool</span><span class="sxs-lookup"><span data-stu-id="46142-189">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="46142-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46142-190">-Confirm</span></span>
<span data-ttu-id="46142-191">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="46142-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46142-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46142-192">-WhatIf</span></span>
<span data-ttu-id="46142-193">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="46142-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46142-194">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46142-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46142-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46142-195">CommonParameters</span></span>
<span data-ttu-id="46142-196">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46142-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46142-197">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46142-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46142-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46142-198">INPUTS</span></span>

### <span data-ttu-id="46142-199">System.String</span><span class="sxs-lookup"><span data-stu-id="46142-199">System.String</span></span>

## <span data-ttu-id="46142-200">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46142-200">OUTPUTS</span></span>

### <span data-ttu-id="46142-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="46142-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="46142-202">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="46142-202">NOTES</span></span>

## <span data-ttu-id="46142-203">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46142-203">RELATED LINKS</span></span>

[<span data-ttu-id="46142-204">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46142-204">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="46142-205">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="46142-205">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="46142-206">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="46142-206">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="46142-207">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46142-207">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="46142-208">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46142-208">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="46142-209">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="46142-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
