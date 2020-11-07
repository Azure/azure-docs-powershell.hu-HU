---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 62823ec87758142b34490f24d3e1b24e0c434f85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668807"
---
# <span data-ttu-id="fdea0-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fdea0-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="fdea0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdea0-102">SYNOPSIS</span></span>
<span data-ttu-id="fdea0-103">Beállítja az adatbázis tulajdonságait, vagy áthelyezi egy meglévő adatbázist egy rugalmas készletbe.</span><span class="sxs-lookup"><span data-stu-id="fdea0-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="fdea0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdea0-104">SYNTAX</span></span>

### <span data-ttu-id="fdea0-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fdea0-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdea0-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="fdea0-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdea0-107">Átnevezése</span><span class="sxs-lookup"><span data-stu-id="fdea0-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdea0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdea0-108">DESCRIPTION</span></span>
<span data-ttu-id="fdea0-109">A **set-AzSqlDatabase** parancsmag az Azure SQL-adatbázisban tárolt adatbázis tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="fdea0-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="fdea0-110">Ez a parancsmag módosíthatja a Service Tier ( *kiadás* ), a teljesítményszint ( *RequestedServiceObjectiveName* ) és az adatbázis tárterületének maximális méretét ( *MaxSizeBytes* ).</span><span class="sxs-lookup"><span data-stu-id="fdea0-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="fdea0-111">Emellett megadhatja, hogy az *ElasticPoolName* paraméter az adatbázis rugalmas készletéből való áthelyezését is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="fdea0-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="fdea0-112">Ha egy adatbázis már egy rugalmas készletben van, akkor a *RequestedServiceObjectiveName* paraméterrel az adatbázist rugalmas készletből és egyetlen adatbázis teljesítmény szintjére helyezheti.</span><span class="sxs-lookup"><span data-stu-id="fdea0-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="fdea0-113">Példák</span><span class="sxs-lookup"><span data-stu-id="fdea0-113">EXAMPLES</span></span>

### <span data-ttu-id="fdea0-114">1. példa: adatbázis frissítése normál S0-adatbázisba</span><span class="sxs-lookup"><span data-stu-id="fdea0-114">Example 1: Update a database to a Standard S0 database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S0"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="fdea0-115">Ez a parancs frissíti a Database01 nevű adatbázist egy szabványos S0-adatbázishoz egy Server01 nevű kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="fdea0-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="fdea0-116">2. példa: adatbázis felvétele elasztikus poolba</span><span class="sxs-lookup"><span data-stu-id="fdea0-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="fdea0-117">A parancs hozzáadja a Database01 nevű adatbázist a Server01 nevű ElasticPool01 nevű rugalmas készlethez.</span><span class="sxs-lookup"><span data-stu-id="fdea0-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="fdea0-118">3. példa: az adatbázis tárterületének maximális méretének módosítása</span><span class="sxs-lookup"><span data-stu-id="fdea0-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="fdea0-119">Ez a parancs frissíti a Database01 nevű adatbázist a maximális méret 1 TB értékre állításával.</span><span class="sxs-lookup"><span data-stu-id="fdea0-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="fdea0-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdea0-120">PARAMETERS</span></span>

### <span data-ttu-id="fdea0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdea0-121">-AsJob</span></span>
<span data-ttu-id="fdea0-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fdea0-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdea0-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="fdea0-123">-ComputeGeneration</span></span>
<span data-ttu-id="fdea0-124">A hozzárendelni kívánt számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="fdea0-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fdea0-125">-DatabaseName</span></span>
<span data-ttu-id="fdea0-126">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdea0-126">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="fdea0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdea0-127">-DefaultProfile</span></span>
<span data-ttu-id="fdea0-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fdea0-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdea0-129">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="fdea0-129">-Edition</span></span>
<span data-ttu-id="fdea0-130">Az adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdea0-130">Specifies the edition for the database.</span></span>
<span data-ttu-id="fdea0-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fdea0-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fdea0-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="fdea0-132">None</span></span>
- <span data-ttu-id="fdea0-133">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="fdea0-133">Basic</span></span>
- <span data-ttu-id="fdea0-134">Standard</span><span class="sxs-lookup"><span data-stu-id="fdea0-134">Standard</span></span>
- <span data-ttu-id="fdea0-135">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="fdea0-135">Premium</span></span>
- <span data-ttu-id="fdea0-136">Adattárházi</span><span class="sxs-lookup"><span data-stu-id="fdea0-136">DataWarehouse</span></span>
- <span data-ttu-id="fdea0-137">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="fdea0-137">Free</span></span>
- <span data-ttu-id="fdea0-138">Nyúlik</span><span class="sxs-lookup"><span data-stu-id="fdea0-138">Stretch</span></span>
- <span data-ttu-id="fdea0-139">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="fdea0-139">GeneralPurpose</span></span>
- <span data-ttu-id="fdea0-140">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="fdea0-140">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-141">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fdea0-141">-ElasticPoolName</span></span>
<span data-ttu-id="fdea0-142">Annak a rugalmas készletnek a nevét adja meg, amelybe az adatbázist át szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="fdea0-142">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fdea0-143">-LicenseType</span></span>
<span data-ttu-id="fdea0-144">Az Azure SQL-adatbázis licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="fdea0-144">The license type for the Azure Sql database.</span></span> <span data-ttu-id="fdea0-145">A lehetséges értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="fdea0-145">Possible values are:</span></span>
- <span data-ttu-id="fdea0-146">BasePrice – Azure hibrid haszon (AHB) a meglévő SQL Server-licenccel rendelkező tulajdonosok kedvezményes árait alkalmazzák.</span><span class="sxs-lookup"><span data-stu-id="fdea0-146">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="fdea0-147">Az adatbázis ára a meglévő SQL Server-licenccel rendelkező tulajdonosok számára diszkontálva lesz.</span><span class="sxs-lookup"><span data-stu-id="fdea0-147">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="fdea0-148">A LicenseIncluded-Azure Hybrid haszon (AHB) árengedménye nem érvényes a meglévő SQL Server-licenccel rendelkező tulajdonosok esetében.</span><span class="sxs-lookup"><span data-stu-id="fdea0-148">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="fdea0-149">Az adatbázis ára tartalmazni fogja az új SQL Server-licencek költségeit.</span><span class="sxs-lookup"><span data-stu-id="fdea0-149">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-150">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="fdea0-150">-MaxSizeBytes</span></span>
<span data-ttu-id="fdea0-151">Az Azure SQL-adatbázis maximális mérete bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="fdea0-151">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-152">-NewName</span><span class="sxs-lookup"><span data-stu-id="fdea0-152">-NewName</span></span>
<span data-ttu-id="fdea0-153">Az új név az adatbázis átnevezéséhez.</span><span class="sxs-lookup"><span data-stu-id="fdea0-153">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-154">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="fdea0-154">-ReadScale</span></span>
<span data-ttu-id="fdea0-155">Az Azure SQL-adatbázishoz rendelt olvasási méretarány beállítás. (Engedélyezve/letiltva)</span><span class="sxs-lookup"><span data-stu-id="fdea0-155">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-156">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="fdea0-156">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="fdea0-157">Az adatbázishoz hozzárendelni kívánt szolgáltatási cél nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdea0-157">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="fdea0-158">A szolgáltatási célkitűzésekről további információt az [Azure SQL Database Service Tiers és a teljesítmény szintje](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) a Microsoft Developer Network műsortárában című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="fdea0-158">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdea0-159">-ResourceGroupName</span></span>
<span data-ttu-id="fdea0-160">Annak a csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="fdea0-160">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fdea0-161">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fdea0-161">-ServerName</span></span>
<span data-ttu-id="fdea0-162">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdea0-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="fdea0-163">-Címkék</span><span class="sxs-lookup"><span data-stu-id="fdea0-163">-Tags</span></span>
<span data-ttu-id="fdea0-164">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="fdea0-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fdea0-165">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="fdea0-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="fdea0-166">-VCore</span></span>
<span data-ttu-id="fdea0-167">Az Azure SQL-adatbázis vcore száma</span><span class="sxs-lookup"><span data-stu-id="fdea0-167">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="fdea0-168">-ZoneRedundant</span></span>
<span data-ttu-id="fdea0-169">A zóna redundancia az Azure SQL-adatbázishoz való társításhoz</span><span class="sxs-lookup"><span data-stu-id="fdea0-169">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdea0-170">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fdea0-170">-Confirm</span></span>
<span data-ttu-id="fdea0-171">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fdea0-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdea0-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdea0-172">-WhatIf</span></span>
<span data-ttu-id="fdea0-173">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fdea0-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdea0-174">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fdea0-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdea0-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdea0-175">CommonParameters</span></span>
<span data-ttu-id="fdea0-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdea0-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdea0-177">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fdea0-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdea0-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdea0-178">INPUTS</span></span>

### <span data-ttu-id="fdea0-179">System. String</span><span class="sxs-lookup"><span data-stu-id="fdea0-179">System.String</span></span>

## <span data-ttu-id="fdea0-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdea0-180">OUTPUTS</span></span>

### <span data-ttu-id="fdea0-181">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fdea0-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fdea0-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdea0-182">NOTES</span></span>

## <span data-ttu-id="fdea0-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdea0-183">RELATED LINKS</span></span>

[<span data-ttu-id="fdea0-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fdea0-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="fdea0-185">Új – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fdea0-185">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="fdea0-186">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fdea0-186">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="fdea0-187">Önéletrajz – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fdea0-187">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="fdea0-188">Felfüggesztés – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fdea0-188">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="fdea0-189">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fdea0-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
