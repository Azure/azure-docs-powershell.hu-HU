---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468090"
---
# <span data-ttu-id="86659-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="86659-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="86659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86659-102">SYNOPSIS</span></span>
<span data-ttu-id="86659-103">Módosítja egy rugalmas adatbáziskészlet tulajdonságait az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="86659-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="86659-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86659-104">SYNTAX</span></span>

### <span data-ttu-id="86659-105">DtuBasedPool (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86659-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86659-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="86659-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86659-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86659-107">DESCRIPTION</span></span>
<span data-ttu-id="86659-108">A **Set-AzSqlElasticPool** parancsmag beállítja egy rugalmas készlet tulajdonságait az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="86659-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="86659-109">Ez a parancsmag képes módosítani a készletenkénti eDTUsokat *(Dtu),* a tárterület maximális méretét készletenként *(StorageMB),* adatbázisonkénti maximális eDTUs értékeket *(DatabaseDtuMax)* és adatbázisonkénti minimális eDTUs-értékeket *(DatabaseDtuMin*).</span><span class="sxs-lookup"><span data-stu-id="86659-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="86659-110">Számos paraméter (*-Dtu, -DatabaseDtuMin és -DatabaseDtuMax*) esetén a beállított érték szerepel az adott paraméter érvényes értékeinek listájában.</span><span class="sxs-lookup"><span data-stu-id="86659-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="86659-111">Egy normál 100 eDTU-készlet esetén például a -DatabaseDtuMax érték csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="86659-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="86659-112">Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="86659-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="86659-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86659-113">EXAMPLES</span></span>

### <span data-ttu-id="86659-114">1. példa: Rugalmas készlet tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="86659-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="86659-115">Ez a parancs módosítja egy rugalmasságipool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="86659-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="86659-116">A parancs 1000-re állítja a rugalmas készlet DTUs-ját, és beállítja a minimális és a maximális DTUs-t.</span><span class="sxs-lookup"><span data-stu-id="86659-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="86659-117">2. példa: Rugalmas készlet maximális tárterületméretének módosítása</span><span class="sxs-lookup"><span data-stu-id="86659-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="86659-118">Ez a parancs módosítja egy rugalmasságipool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="86659-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="86659-119">A parancs egy rugalmas készlet maximális tárterületét 2 TB-osra állítja.</span><span class="sxs-lookup"><span data-stu-id="86659-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="86659-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="86659-120">Example 3</span></span>

<span data-ttu-id="86659-121">Módosítja egy rugalmas adatbáziskészlet tulajdonságait az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="86659-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="86659-122">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="86659-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="86659-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86659-123">PARAMETERS</span></span>

### <span data-ttu-id="86659-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86659-124">-AsJob</span></span>
<span data-ttu-id="86659-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="86659-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86659-126">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="86659-126">-ComputeGeneration</span></span>
<span data-ttu-id="86659-127">A hozzárendelni megfelelő számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="86659-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="86659-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="86659-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="86659-129">Azt adja meg, hogy a készlet bármelyik adatbázisa legfeljebb hány DTUs-t képes igénybeni.</span><span class="sxs-lookup"><span data-stu-id="86659-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="86659-130">Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="86659-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="86659-131">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="86659-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="86659-132">Alapszintű.</span><span class="sxs-lookup"><span data-stu-id="86659-132">Basic.</span></span>  <span data-ttu-id="86659-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="86659-133">5 DTUs</span></span>
- <span data-ttu-id="86659-134">Normál.</span><span class="sxs-lookup"><span data-stu-id="86659-134">Standard.</span></span> <span data-ttu-id="86659-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="86659-135">100 DTUs</span></span>
- <span data-ttu-id="86659-136">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="86659-136">Premium.</span></span> <span data-ttu-id="86659-137">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="86659-137">125 DTUs</span></span>

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

### <span data-ttu-id="86659-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="86659-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="86659-139">Megadja, hogy a rugalmas készlet hány DTUs-t garantál a készlet összes adatbázisának.</span><span class="sxs-lookup"><span data-stu-id="86659-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="86659-140">Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="86659-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="86659-141">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="86659-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="86659-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="86659-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="86659-143">Az SqlAzure-adatbázis által a készletben megengedett maximális VCore-szám.</span><span class="sxs-lookup"><span data-stu-id="86659-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="86659-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="86659-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="86659-145">Az SqlAzure-adatbázis által a készletben felhasznált minimális VCore-szám.</span><span class="sxs-lookup"><span data-stu-id="86659-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="86659-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86659-146">-DefaultProfile</span></span>
<span data-ttu-id="86659-147">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="86659-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86659-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="86659-148">-Dtu</span></span>
<span data-ttu-id="86659-149">A rugalmas készlet megosztott DTUS-inak teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="86659-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="86659-150">Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="86659-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="86659-151">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="86659-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="86659-152">Alapszintű.</span><span class="sxs-lookup"><span data-stu-id="86659-152">Basic.</span></span> <span data-ttu-id="86659-153">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="86659-153">100 DTUs</span></span>
- <span data-ttu-id="86659-154">Normál.</span><span class="sxs-lookup"><span data-stu-id="86659-154">Standard.</span></span> <span data-ttu-id="86659-155">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="86659-155">100 DTUs</span></span>
- <span data-ttu-id="86659-156">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="86659-156">Premium.</span></span> <span data-ttu-id="86659-157">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="86659-157">125 DTUs</span></span>

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

### <span data-ttu-id="86659-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="86659-158">-Edition</span></span>
<span data-ttu-id="86659-159">A rugalmas készlet Azure SQL-adatbázisának kiadását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="86659-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="86659-160">A kiadás nem változtatható meg.</span><span class="sxs-lookup"><span data-stu-id="86659-160">You cannot change the edition.</span></span> <span data-ttu-id="86659-161">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="86659-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="86659-162">Nincs</span><span class="sxs-lookup"><span data-stu-id="86659-162">None</span></span>
- <span data-ttu-id="86659-163">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="86659-163">Basic</span></span>
- <span data-ttu-id="86659-164">Normál</span><span class="sxs-lookup"><span data-stu-id="86659-164">Standard</span></span>
- <span data-ttu-id="86659-165">Prémium</span><span class="sxs-lookup"><span data-stu-id="86659-165">Premium</span></span>
- <span data-ttu-id="86659-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="86659-166">DataWarehouse</span></span>
- <span data-ttu-id="86659-167">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="86659-167">Free</span></span>
- <span data-ttu-id="86659-168">Nyújtás</span><span class="sxs-lookup"><span data-stu-id="86659-168">Stretch</span></span>
- <span data-ttu-id="86659-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="86659-169">GeneralPurpose</span></span>
- <span data-ttu-id="86659-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="86659-170">BusinessCritical</span></span>

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

### <span data-ttu-id="86659-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="86659-171">-ElasticPoolName</span></span>
<span data-ttu-id="86659-172">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86659-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="86659-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="86659-173">-LicenseType</span></span>
<span data-ttu-id="86659-174">Az Azure Sql-adatbázis licenctípusa.</span><span class="sxs-lookup"><span data-stu-id="86659-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="86659-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86659-175">-ResourceGroupName</span></span>
<span data-ttu-id="86659-176">Annak az erőforráscsoportnak a neve, amelyhez a rugalmas készlet hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="86659-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="86659-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="86659-177">-ServerName</span></span>
<span data-ttu-id="86659-178">A rugalmas készletet tartalmazó kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="86659-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="86659-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="86659-179">-StorageMB</span></span>
<span data-ttu-id="86659-180">A rugalmas készlet tárterületkorlátját határozza meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="86659-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="86659-181">További információért lásd a New-AzSqlElasticPool parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="86659-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="86659-182">-Címkék</span><span class="sxs-lookup"><span data-stu-id="86659-182">-Tags</span></span>
<span data-ttu-id="86659-183">Egy olyan kulcsérték-párok szótárát adja meg, amelyekhez a parancsmag hash táblázat formájában társítja a rugalmas készletet.</span><span class="sxs-lookup"><span data-stu-id="86659-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="86659-184">Például: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="86659-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="86659-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="86659-185">-VCore</span></span>
<span data-ttu-id="86659-186">A Vcore teljes megosztott száma az Sql Azure Rugalmas készlethez.</span><span class="sxs-lookup"><span data-stu-id="86659-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="86659-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="86659-187">-ZoneRedundant</span></span>
<span data-ttu-id="86659-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span><span class="sxs-lookup"><span data-stu-id="86659-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="86659-189">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86659-189">-Confirm</span></span>
<span data-ttu-id="86659-190">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="86659-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86659-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86659-191">-WhatIf</span></span>
<span data-ttu-id="86659-192">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="86659-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86659-193">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86659-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86659-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86659-194">CommonParameters</span></span>
<span data-ttu-id="86659-195">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86659-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86659-196">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86659-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86659-197">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86659-197">INPUTS</span></span>

### <span data-ttu-id="86659-198">System.String</span><span class="sxs-lookup"><span data-stu-id="86659-198">System.String</span></span>

## <span data-ttu-id="86659-199">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86659-199">OUTPUTS</span></span>

### <span data-ttu-id="86659-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="86659-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="86659-201">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86659-201">NOTES</span></span>

## <span data-ttu-id="86659-202">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86659-202">RELATED LINKS</span></span>

[<span data-ttu-id="86659-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="86659-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="86659-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="86659-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="86659-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="86659-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="86659-206">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="86659-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="86659-207">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="86659-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
