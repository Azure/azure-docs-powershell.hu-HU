---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337206"
---
# <span data-ttu-id="b7450-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7450-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="b7450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7450-102">SYNOPSIS</span></span>
<span data-ttu-id="b7450-103">Módosítja egy rugalmas adatbáziskészlet tulajdonságait az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="b7450-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="b7450-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7450-104">SYNTAX</span></span>

### <span data-ttu-id="b7450-105">DtuBasedPool (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7450-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7450-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="b7450-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7450-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7450-107">DESCRIPTION</span></span>
<span data-ttu-id="b7450-108">A **Set-AzSqlElasticPool** parancsmag beállítja egy rugalmas készlet tulajdonságait az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="b7450-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="b7450-109">Ez a parancsmag képes módosítani a készletenkénti eDTUsokat *(Dtu),* a tárterület maximális méretét készletenként *(StorageMB),* adatbázisonkénti maximális eDTUs értékeket *(DatabaseDtuMax)* és adatbázisonkénti minimális eDTUs-értékeket *(DatabaseDtuMin*).</span><span class="sxs-lookup"><span data-stu-id="b7450-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="b7450-110">Számos paraméter (*-Dtu, -DatabaseDtuMin és -DatabaseDtuMax*) esetén a beállított érték szerepel az adott paraméter érvényes értékeinek listájában.</span><span class="sxs-lookup"><span data-stu-id="b7450-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="b7450-111">Egy normál 100 eDTU-készlet esetén például a -DatabaseDtuMax érték csak 10, 20, 50 vagy 100 lehet.</span><span class="sxs-lookup"><span data-stu-id="b7450-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="b7450-112">Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b7450-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="b7450-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7450-113">EXAMPLES</span></span>

### <span data-ttu-id="b7450-114">1. példa: Rugalmas készlet tulajdonságainak módosítása</span><span class="sxs-lookup"><span data-stu-id="b7450-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="b7450-115">Ez a parancs módosítja egy rugalmasságipool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b7450-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="b7450-116">A parancs 1000-re állítja a rugalmas készlet DTUs-ját, és beállítja a minimális és a maximális DTUs-t.</span><span class="sxs-lookup"><span data-stu-id="b7450-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="b7450-117">2. példa: Rugalmas készlet maximális tárterületméretének módosítása</span><span class="sxs-lookup"><span data-stu-id="b7450-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="b7450-118">Ez a parancs módosítja egy rugalmasságipool01 nevű rugalmas készlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b7450-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="b7450-119">A parancs egy rugalmas készlet maximális tárterületét 2 TB-osra állítja.</span><span class="sxs-lookup"><span data-stu-id="b7450-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="b7450-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="b7450-120">Example 3</span></span>

<span data-ttu-id="b7450-121">Módosítja egy rugalmas adatbáziskészlet tulajdonságait az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="b7450-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="b7450-122">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="b7450-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="b7450-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7450-123">PARAMETERS</span></span>

### <span data-ttu-id="b7450-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7450-124">-AsJob</span></span>
<span data-ttu-id="b7450-125">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b7450-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7450-126">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="b7450-126">-ComputeGeneration</span></span>
<span data-ttu-id="b7450-127">A hozzárendelni megfelelő számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="b7450-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="b7450-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="b7450-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="b7450-129">Azt adja meg, hogy a készlet bármelyik adatbázisa legfeljebb hány DTUs-t képes igénybeni.</span><span class="sxs-lookup"><span data-stu-id="b7450-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="b7450-130">Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b7450-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="b7450-131">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b7450-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="b7450-132">Alapszintű.</span><span class="sxs-lookup"><span data-stu-id="b7450-132">Basic.</span></span>  <span data-ttu-id="b7450-133">5 DTUs</span><span class="sxs-lookup"><span data-stu-id="b7450-133">5 DTUs</span></span>
- <span data-ttu-id="b7450-134">Normál.</span><span class="sxs-lookup"><span data-stu-id="b7450-134">Standard.</span></span> <span data-ttu-id="b7450-135">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="b7450-135">100 DTUs</span></span>
- <span data-ttu-id="b7450-136">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="b7450-136">Premium.</span></span> <span data-ttu-id="b7450-137">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="b7450-137">125 DTUs</span></span>

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

### <span data-ttu-id="b7450-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="b7450-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="b7450-139">Megadja, hogy a rugalmas készlet hány DTUs-t garantál a készlet összes adatbázisának.</span><span class="sxs-lookup"><span data-stu-id="b7450-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="b7450-140">Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b7450-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="b7450-141">Az alapértelmezett érték nulla (0).</span><span class="sxs-lookup"><span data-stu-id="b7450-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="b7450-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="b7450-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="b7450-143">Az SqlAzure-adatbázis által a készletben megengedett maximális VCore-szám.</span><span class="sxs-lookup"><span data-stu-id="b7450-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="b7450-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="b7450-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="b7450-145">Az SqlAzure-adatbázis által a készletben felhasznált minimális VCore-szám.</span><span class="sxs-lookup"><span data-stu-id="b7450-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="b7450-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7450-146">-DefaultProfile</span></span>
<span data-ttu-id="b7450-147">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b7450-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7450-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="b7450-148">-Dtu</span></span>
<span data-ttu-id="b7450-149">A rugalmas készlet megosztott DTUS-inak teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7450-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="b7450-150">Az érvényes értékekről a rugalmas készletekben található adott méretkészlet táblázatában [olvashat részletesen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="b7450-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="b7450-151">A különböző kiadások alapértelmezett értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b7450-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="b7450-152">Alapszintű.</span><span class="sxs-lookup"><span data-stu-id="b7450-152">Basic.</span></span> <span data-ttu-id="b7450-153">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="b7450-153">100 DTUs</span></span>
- <span data-ttu-id="b7450-154">Normál.</span><span class="sxs-lookup"><span data-stu-id="b7450-154">Standard.</span></span> <span data-ttu-id="b7450-155">100 DTUs</span><span class="sxs-lookup"><span data-stu-id="b7450-155">100 DTUs</span></span>
- <span data-ttu-id="b7450-156">Prémium verzió.</span><span class="sxs-lookup"><span data-stu-id="b7450-156">Premium.</span></span> <span data-ttu-id="b7450-157">125 DTUs</span><span class="sxs-lookup"><span data-stu-id="b7450-157">125 DTUs</span></span>

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

### <span data-ttu-id="b7450-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="b7450-158">-Edition</span></span>
<span data-ttu-id="b7450-159">A rugalmas készlet Azure SQL-adatbázisának kiadását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b7450-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="b7450-160">A kiadás nem változtatható meg.</span><span class="sxs-lookup"><span data-stu-id="b7450-160">You cannot change the edition.</span></span> <span data-ttu-id="b7450-161">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="b7450-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7450-162">Nincs</span><span class="sxs-lookup"><span data-stu-id="b7450-162">None</span></span>
- <span data-ttu-id="b7450-163">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="b7450-163">Basic</span></span>
- <span data-ttu-id="b7450-164">Normál</span><span class="sxs-lookup"><span data-stu-id="b7450-164">Standard</span></span>
- <span data-ttu-id="b7450-165">Prémium</span><span class="sxs-lookup"><span data-stu-id="b7450-165">Premium</span></span>
- <span data-ttu-id="b7450-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="b7450-166">DataWarehouse</span></span>
- <span data-ttu-id="b7450-167">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="b7450-167">Free</span></span>
- <span data-ttu-id="b7450-168">Nyújtás</span><span class="sxs-lookup"><span data-stu-id="b7450-168">Stretch</span></span>
- <span data-ttu-id="b7450-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="b7450-169">GeneralPurpose</span></span>
- <span data-ttu-id="b7450-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="b7450-170">BusinessCritical</span></span>

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

### <span data-ttu-id="b7450-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b7450-171">-ElasticPoolName</span></span>
<span data-ttu-id="b7450-172">A rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7450-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="b7450-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b7450-173">-LicenseType</span></span>
<span data-ttu-id="b7450-174">Az Azure Sql-adatbázis licenctípusa.</span><span class="sxs-lookup"><span data-stu-id="b7450-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="b7450-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7450-175">-ResourceGroupName</span></span>
<span data-ttu-id="b7450-176">Annak az erőforráscsoportnak a neve, amelyhez a rugalmas készlet hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b7450-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="b7450-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7450-177">-ServerName</span></span>
<span data-ttu-id="b7450-178">A rugalmas készletet tartalmazó kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="b7450-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="b7450-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="b7450-179">-StorageMB</span></span>
<span data-ttu-id="b7450-180">A rugalmas készlet tárterületkorlátját határozza meg megabájtban.</span><span class="sxs-lookup"><span data-stu-id="b7450-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="b7450-181">További információért lásd a New-AzSqlElasticPool parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b7450-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="b7450-182">-Címkék</span><span class="sxs-lookup"><span data-stu-id="b7450-182">-Tags</span></span>
<span data-ttu-id="b7450-183">Egy olyan kulcsérték-párok szótárát adja meg, amelyekhez a parancsmag hash táblázat formájában társítja a rugalmas készletet.</span><span class="sxs-lookup"><span data-stu-id="b7450-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="b7450-184">Például: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="b7450-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="b7450-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="b7450-185">-VCore</span></span>
<span data-ttu-id="b7450-186">A Vcore teljes megosztott száma az Sql Azure Rugalmas készlethez.</span><span class="sxs-lookup"><span data-stu-id="b7450-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="b7450-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="b7450-187">-ZoneRedundant</span></span>
<span data-ttu-id="b7450-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span><span class="sxs-lookup"><span data-stu-id="b7450-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="b7450-189">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7450-189">-Confirm</span></span>
<span data-ttu-id="b7450-190">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b7450-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7450-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7450-191">-WhatIf</span></span>
<span data-ttu-id="b7450-192">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b7450-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7450-193">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7450-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7450-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7450-194">CommonParameters</span></span>
<span data-ttu-id="b7450-195">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7450-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7450-196">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7450-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7450-197">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7450-197">INPUTS</span></span>

### <span data-ttu-id="b7450-198">System.String</span><span class="sxs-lookup"><span data-stu-id="b7450-198">System.String</span></span>

## <span data-ttu-id="b7450-199">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7450-199">OUTPUTS</span></span>

### <span data-ttu-id="b7450-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="b7450-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="b7450-201">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7450-201">NOTES</span></span>

## <span data-ttu-id="b7450-202">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7450-202">RELATED LINKS</span></span>

[<span data-ttu-id="b7450-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7450-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="b7450-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="b7450-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="b7450-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="b7450-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="b7450-206">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b7450-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="b7450-207">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b7450-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
