---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 15f9aee8e278a1b33330508a10487e3847820891
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341550"
---
# <span data-ttu-id="8c728-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8c728-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="8c728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c728-102">SYNOPSIS</span></span>
<span data-ttu-id="8c728-103">Beállítja egy adatbázis tulajdonságait, vagy egy meglévő adatbázist rugalmas készletbe áthelyez.</span><span class="sxs-lookup"><span data-stu-id="8c728-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="8c728-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c728-104">SYNTAX</span></span>

### <span data-ttu-id="8c728-105">Frissítés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c728-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c728-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="8c728-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c728-107">Átnevezés</span><span class="sxs-lookup"><span data-stu-id="8c728-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c728-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c728-108">DESCRIPTION</span></span>
<span data-ttu-id="8c728-109">A **Set-AzSqlDatabase** parancsmag beállítja egy adatbázis tulajdonságait az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="8c728-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="8c728-110">Ez a parancsmag módosíthatja az adatbázis szolgáltatási rétegét *(Edition),* a teljesítményszintet *(RequestedServiceObjectiveName)* és a tárterület maximális méretét *(MaxSizeBytes).*</span><span class="sxs-lookup"><span data-stu-id="8c728-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="8c728-111">Emellett megadhatja a *RugalmasságPoolName* paramétert is, hogy az adatbázis rugalmas készletbe helyezze át az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="8c728-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="8c728-112">Ha egy adatbázis már egy rugalmas készletben található, a *RequestedServiceObjectiveName* paraméterrel áthelyezheti az adatbázist egy rugalmas készletből, és egy teljesítményszintre egyetlen adatbázis esetén.</span><span class="sxs-lookup"><span data-stu-id="8c728-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="8c728-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c728-113">EXAMPLES</span></span>

### <span data-ttu-id="8c728-114">1. példa: Adatbázis frissítése Standard S0 adatbázisra</span><span class="sxs-lookup"><span data-stu-id="8c728-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="8c728-115">Ez a parancs frissíti az Adatbázis01 nevű adatbázist egy Server01 nevű kiszolgálón található Standard S0 adatbázisra.</span><span class="sxs-lookup"><span data-stu-id="8c728-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="8c728-116">2. példa: Adatbázis hozzáadása rugalmas készlethez</span><span class="sxs-lookup"><span data-stu-id="8c728-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="8c728-117">Ez a parancs hozzáad egy Database01 nevű adatbázist a Kiszolgáló01 nevű kiszolgálón üzemeltetett RugalmasPool01 nevű rugalmas készlethez.</span><span class="sxs-lookup"><span data-stu-id="8c728-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="8c728-118">3. példa: Adatbázis maximális tárterületméretének módosítása</span><span class="sxs-lookup"><span data-stu-id="8c728-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="8c728-119">Ezzel a paranccsal a Database01 nevű adatbázist 1 TB-ra állíthatja.</span><span class="sxs-lookup"><span data-stu-id="8c728-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="8c728-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c728-120">PARAMETERS</span></span>

### <span data-ttu-id="8c728-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c728-121">-AsJob</span></span>
<span data-ttu-id="8c728-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8c728-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c728-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="8c728-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="8c728-124">Az adatbázis (csak kiszolgáló nélküli) automatikus szüneteltetési késleltetése percben, -1 a letiltáshoz</span><span class="sxs-lookup"><span data-stu-id="8c728-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c728-125">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="8c728-125">-BackupStorageRedundancy</span></span>
<span data-ttu-id="8c728-126">Az SQL-adatbázis biztonsági másolatai tárolásához használt biztonsági mentési tárterület-redundancia.</span><span class="sxs-lookup"><span data-stu-id="8c728-126">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="8c728-127">A beállítások a helyi, a zóna és a földrajzi hely.</span><span class="sxs-lookup"><span data-stu-id="8c728-127">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c728-128">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="8c728-128">-ComputeGeneration</span></span>
<span data-ttu-id="8c728-129">A hozzárendelni megfelelő számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="8c728-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="8c728-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="8c728-130">-ComputeModel</span></span>
<span data-ttu-id="8c728-131">Az Azure Sql-adatbázis számított modellje.</span><span class="sxs-lookup"><span data-stu-id="8c728-131">Computed model of Azure Sql database.</span></span> <span data-ttu-id="8c728-132">Kiszolgáló nélküli vagy kiépítve</span><span class="sxs-lookup"><span data-stu-id="8c728-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="8c728-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8c728-133">-DatabaseName</span></span>
<span data-ttu-id="8c728-134">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c728-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="8c728-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c728-135">-DefaultProfile</span></span>
<span data-ttu-id="8c728-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8c728-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c728-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="8c728-137">-Edition</span></span>
<span data-ttu-id="8c728-138">Az adatbázis kiadását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8c728-138">Specifies the edition for the database.</span></span>
<span data-ttu-id="8c728-139">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="8c728-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8c728-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="8c728-140">None</span></span>
- <span data-ttu-id="8c728-141">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="8c728-141">Basic</span></span>
- <span data-ttu-id="8c728-142">Normál</span><span class="sxs-lookup"><span data-stu-id="8c728-142">Standard</span></span>
- <span data-ttu-id="8c728-143">Prémium</span><span class="sxs-lookup"><span data-stu-id="8c728-143">Premium</span></span>
- <span data-ttu-id="8c728-144">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="8c728-144">DataWarehouse</span></span>
- <span data-ttu-id="8c728-145">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="8c728-145">Free</span></span>
- <span data-ttu-id="8c728-146">Nyújtás</span><span class="sxs-lookup"><span data-stu-id="8c728-146">Stretch</span></span>
- <span data-ttu-id="8c728-147">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="8c728-147">GeneralPurpose</span></span>
- <span data-ttu-id="8c728-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="8c728-148">BusinessCritical</span></span>

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

### <span data-ttu-id="8c728-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8c728-149">-ElasticPoolName</span></span>
<span data-ttu-id="8c728-150">Annak a rugalmas készletnek a nevét adja meg, amelybe át kell áthelyezni az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="8c728-150">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="8c728-151">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="8c728-151">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="8c728-152">Az adatbázishoz társított, csak olvasható másodlagos másolatok száma.</span><span class="sxs-lookup"><span data-stu-id="8c728-152">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="8c728-153">Csak Hiperskála kiadás esetén.</span><span class="sxs-lookup"><span data-stu-id="8c728-153">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c728-154">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8c728-154">-LicenseType</span></span>
<span data-ttu-id="8c728-155">Az Azure Sql-adatbázis licenctípusa.</span><span class="sxs-lookup"><span data-stu-id="8c728-155">The license type for the Azure Sql database.</span></span> <span data-ttu-id="8c728-156">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="8c728-156">Possible values are:</span></span>
- <span data-ttu-id="8c728-157">BasePrice – Azure Hybrid Benefit (AHB) kedvezményes árazás érvényes a meglévő SQL Server-licenctulajdonosokra.</span><span class="sxs-lookup"><span data-stu-id="8c728-157">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="8c728-158">Az adatbázis ára leszámítoljuk a meglévő SQL Server-licenctulajdonosok számára.</span><span class="sxs-lookup"><span data-stu-id="8c728-158">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="8c728-159">LicenseIncluded - Azure Hybrid Benefit (AHB) discounting for existing SQL Server license owners is not applied.</span><span class="sxs-lookup"><span data-stu-id="8c728-159">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="8c728-160">Az adatbázis ára új SQL Server-licencköltségeket fog tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="8c728-160">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="8c728-161">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="8c728-161">-MaxSizeBytes</span></span>
<span data-ttu-id="8c728-162">Az Azure SQL-adatbázis maximális mérete bájtban.</span><span class="sxs-lookup"><span data-stu-id="8c728-162">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="8c728-163">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="8c728-163">-MinimumCapacity</span></span>
<span data-ttu-id="8c728-164">Az a minimális kapacitás, amit az adatbázis kioszt, ha nincs szüneteltetve.</span><span class="sxs-lookup"><span data-stu-id="8c728-164">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="8c728-165">Csak kiszolgáló nélküli Azure Sql-adatbázisok esetén.</span><span class="sxs-lookup"><span data-stu-id="8c728-165">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c728-166">-NewName</span><span class="sxs-lookup"><span data-stu-id="8c728-166">-NewName</span></span>
<span data-ttu-id="8c728-167">Az új név, amelyre az adatbázist át kell nevezni.</span><span class="sxs-lookup"><span data-stu-id="8c728-167">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="8c728-168">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="8c728-168">-ReadScale</span></span>
<span data-ttu-id="8c728-169">Ha engedélyezve van, akkor azok a kapcsolatok, amelyek kapcsolati karakterláncában az alkalmazás szándékosan csak olvashatóan van beállítva, egy olvasható másodlagos másolatba irányíthatók.</span><span class="sxs-lookup"><span data-stu-id="8c728-169">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="8c728-170">Ez a tulajdonság csak prémium és üzleti kritikus adatbázisokhoz van beállítva.</span><span class="sxs-lookup"><span data-stu-id="8c728-170">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="8c728-171">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="8c728-171">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="8c728-172">Az adatbázishoz hozzárendelni szükséges szolgáltatás-célkiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c728-172">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="8c728-173">A szolgáltatás célkitűzéseiről az [Azure SQL adatbázis-szolgáltatási](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) rétegei és teljesítményszintjei című cikk nyújt tájékoztatást a Microsoft Developer Network Könyvtárban.</span><span class="sxs-lookup"><span data-stu-id="8c728-173">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="8c728-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c728-174">-ResourceGroupName</span></span>
<span data-ttu-id="8c728-175">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8c728-175">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8c728-176">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="8c728-176">-SecondaryType</span></span>
<span data-ttu-id="8c728-177">Az adatbázis másodlagos típusa, ha az másodlagos.</span><span class="sxs-lookup"><span data-stu-id="8c728-177">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="8c728-178">Érvényes értékek: Földrajzi név és Név.</span><span class="sxs-lookup"><span data-stu-id="8c728-178">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c728-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8c728-179">-ServerName</span></span>
<span data-ttu-id="8c728-180">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c728-180">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="8c728-181">-Címkék</span><span class="sxs-lookup"><span data-stu-id="8c728-181">-Tags</span></span>
<span data-ttu-id="8c728-182">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="8c728-182">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8c728-183">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="8c728-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8c728-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="8c728-184">-VCore</span></span>
<span data-ttu-id="8c728-185">Az Azure Sql-adatbázis Vcore-száma</span><span class="sxs-lookup"><span data-stu-id="8c728-185">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c728-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="8c728-186">-ZoneRedundant</span></span>
<span data-ttu-id="8c728-187">Az Azure Sql-adatbázissal társítva található zónaredundáns</span><span class="sxs-lookup"><span data-stu-id="8c728-187">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="8c728-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c728-188">-Confirm</span></span>
<span data-ttu-id="8c728-189">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c728-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c728-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c728-190">-WhatIf</span></span>
<span data-ttu-id="8c728-191">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c728-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c728-192">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c728-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c728-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c728-193">CommonParameters</span></span>
<span data-ttu-id="8c728-194">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c728-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c728-195">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c728-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c728-196">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c728-196">INPUTS</span></span>

### <span data-ttu-id="8c728-197">System.String</span><span class="sxs-lookup"><span data-stu-id="8c728-197">System.String</span></span>

## <span data-ttu-id="8c728-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c728-198">OUTPUTS</span></span>

### <span data-ttu-id="8c728-199">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8c728-199">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8c728-200">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c728-200">NOTES</span></span>

## <span data-ttu-id="8c728-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c728-201">RELATED LINKS</span></span>

[<span data-ttu-id="8c728-202">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8c728-202">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="8c728-203">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8c728-203">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="8c728-204">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8c728-204">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="8c728-205">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8c728-205">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="8c728-206">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8c728-206">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="8c728-207">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="8c728-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
