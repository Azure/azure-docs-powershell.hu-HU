---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: f92af476c7a9cf642512f3aa338069ab37b1c840
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469961"
---
# <span data-ttu-id="26fa9-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26fa9-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="26fa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="26fa9-103">Létrehoz egy adatbázist vagy egy rugalmas adatbázist.</span><span class="sxs-lookup"><span data-stu-id="26fa9-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="26fa9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26fa9-104">SYNTAX</span></span>

### <span data-ttu-id="26fa9-105">DtuBasedDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26fa9-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26fa9-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="26fa9-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26fa9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26fa9-107">DESCRIPTION</span></span>
<span data-ttu-id="26fa9-108">A **New-AzSqlDatabase** parancsmag létrehoz egy Azure SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="26fa9-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="26fa9-109">Rugalmas adatbázist úgy is létrehozhat, hogy a *RugalmasságPoolName* paramétert egy meglévő rugalmas készletre uszodában hozza létre.</span><span class="sxs-lookup"><span data-stu-id="26fa9-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="26fa9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26fa9-110">EXAMPLES</span></span>

### <span data-ttu-id="26fa9-111">1. példa: Adatbázis létrehozása egy megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="26fa9-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="26fa9-112">Ez a parancs létrehoz egy Database01 nevű adatbázist a kiszolgáló Server01 kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="26fa9-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="26fa9-113">2. példa: Rugalmas adatbázis létrehozása egy adott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="26fa9-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="26fa9-114">Ez a parancs létrehoz egy Database02 nevű adatbázist a Kiszolgáló01 kiszolgálón található RugalmasPool01 nevű rugalmas készletben.</span><span class="sxs-lookup"><span data-stu-id="26fa9-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="26fa9-115">3. példa: Vcore-adatbázis létrehozása egy adott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="26fa9-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="26fa9-116">Ez a parancs létrehoz egy Database03 nevű Vcore-adatbázist a server Server01 kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="26fa9-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="26fa9-117">4. példa: Kiszolgáló nélküli adatbázis létrehozása a megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="26fa9-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="26fa9-118">Ez a parancs létrehoz egy Database04 nevű kiszolgáló nélküli adatbázist a server Server01 kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="26fa9-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="26fa9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26fa9-119">PARAMETERS</span></span>

### <span data-ttu-id="26fa9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26fa9-120">-AsJob</span></span>
<span data-ttu-id="26fa9-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="26fa9-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26fa9-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="26fa9-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="26fa9-123">Az adatbázis (csak kiszolgáló nélküli) automatikus szüneteltetési késleltetése percben, -1 a letiltáshoz</span><span class="sxs-lookup"><span data-stu-id="26fa9-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="26fa9-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="26fa9-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="26fa9-125">Az SQL-adatbázis biztonsági másolatai tárolásához használt biztonsági mentési tárterület-redundancia.</span><span class="sxs-lookup"><span data-stu-id="26fa9-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="26fa9-126">A beállítások a helyi, a zóna és a földrajzi hely.</span><span class="sxs-lookup"><span data-stu-id="26fa9-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="26fa9-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="26fa9-127">-CatalogCollation</span></span>
<span data-ttu-id="26fa9-128">Az SQL-adatbáziskatalógus szétválogatásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26fa9-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="26fa9-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="26fa9-129">-CollationName</span></span>
<span data-ttu-id="26fa9-130">Az SQL-adatbázis szétválogatásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26fa9-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="26fa9-131">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="26fa9-131">-ComputeGeneration</span></span>
<span data-ttu-id="26fa9-132">A hozzárendelni megfelelő számítási generálás.</span><span class="sxs-lookup"><span data-stu-id="26fa9-132">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="26fa9-133">-ComputeModel</span></span>
<span data-ttu-id="26fa9-134">Az Azure Sql-adatbázis számítási modellje.</span><span class="sxs-lookup"><span data-stu-id="26fa9-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="26fa9-135">Kiszolgáló nélküli vagy kiépítve</span><span class="sxs-lookup"><span data-stu-id="26fa9-135">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26fa9-136">-DatabaseName</span></span>
<span data-ttu-id="26fa9-137">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26fa9-137">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fa9-138">-DefaultProfile</span></span>
<span data-ttu-id="26fa9-139">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="26fa9-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26fa9-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="26fa9-140">-Edition</span></span>
<span data-ttu-id="26fa9-141">Az adatbázishoz hozzárendelni megfelelő kiadás.</span><span class="sxs-lookup"><span data-stu-id="26fa9-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="26fa9-142">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="26fa9-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26fa9-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="26fa9-143">None</span></span>
- <span data-ttu-id="26fa9-144">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="26fa9-144">Basic</span></span>
- <span data-ttu-id="26fa9-145">Normál</span><span class="sxs-lookup"><span data-stu-id="26fa9-145">Standard</span></span>
- <span data-ttu-id="26fa9-146">Prémium</span><span class="sxs-lookup"><span data-stu-id="26fa9-146">Premium</span></span>
- <span data-ttu-id="26fa9-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="26fa9-147">DataWarehouse</span></span>
- <span data-ttu-id="26fa9-148">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="26fa9-148">Free</span></span>
- <span data-ttu-id="26fa9-149">Nyújtás</span><span class="sxs-lookup"><span data-stu-id="26fa9-149">Stretch</span></span>
- <span data-ttu-id="26fa9-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="26fa9-150">GeneralPurpose</span></span>
- <span data-ttu-id="26fa9-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="26fa9-151">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="26fa9-152">-ElasticPoolName</span></span>
<span data-ttu-id="26fa9-153">Annak a rugalmas készletnek a neve, amelybe az adatbázist be kell tenni.</span><span class="sxs-lookup"><span data-stu-id="26fa9-153">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-154">-Force</span><span class="sxs-lookup"><span data-stu-id="26fa9-154">-Force</span></span>
<span data-ttu-id="26fa9-155">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="26fa9-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="26fa9-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="26fa9-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="26fa9-157">Annak az adatbázisnak az olvasásien másodlagos másolatai száma, amelyekhez az olvasási alkalmazás-leképezés kapcsolatok irányíthatók.</span><span class="sxs-lookup"><span data-stu-id="26fa9-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="26fa9-158">Ez a tulajdonság csak hiperskála kiadású adatbázisokhoz van beállítva.</span><span class="sxs-lookup"><span data-stu-id="26fa9-158">This property is only settable for Hyperscale edition databases.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="26fa9-159">-LicenseType</span></span>
<span data-ttu-id="26fa9-160">Az Azure Sql-adatbázis licenctípusa.</span><span class="sxs-lookup"><span data-stu-id="26fa9-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="26fa9-161">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="26fa9-161">Possible values are:</span></span>
- <span data-ttu-id="26fa9-162">BasePrice – Azure Hybrid Benefit (AHB) kedvezményes árazás érvényes a meglévő SQL Server-licenctulajdonosokra.</span><span class="sxs-lookup"><span data-stu-id="26fa9-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="26fa9-163">Az adatbázis ára leszámítoljuk a meglévő SQL Server-licenctulajdonosok számára.</span><span class="sxs-lookup"><span data-stu-id="26fa9-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="26fa9-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discounting for existing SQL Server license owners is not applied.</span><span class="sxs-lookup"><span data-stu-id="26fa9-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="26fa9-165">Az adatbázis ára új SQL Server-licencköltségeket fog tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="26fa9-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="26fa9-166">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="26fa9-166">-MaxSizeBytes</span></span>
<span data-ttu-id="26fa9-167">Az adatbázis maximális méretét adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="26fa9-167">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-168">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="26fa9-168">-MinimumCapacity</span></span>
<span data-ttu-id="26fa9-169">Az a minimális kapacitás, amit az adatbázis kioszt, ha nincs szüneteltetve.</span><span class="sxs-lookup"><span data-stu-id="26fa9-169">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="26fa9-170">Csak kiszolgáló nélküli Azure Sql-adatbázisok esetén.</span><span class="sxs-lookup"><span data-stu-id="26fa9-170">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="26fa9-171">-ReadScale</span></span>
<span data-ttu-id="26fa9-172">Ha engedélyezve van, akkor azok a kapcsolatok, amelyek kapcsolati karakterláncában az alkalmazás szándékosan csak olvashatóan van beállítva, egy olvasható másodlagos másolatba irányíthatók.</span><span class="sxs-lookup"><span data-stu-id="26fa9-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="26fa9-173">Ez a tulajdonság csak prémium és üzleti kritikus adatbázisokhoz van beállítva.</span><span class="sxs-lookup"><span data-stu-id="26fa9-173">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="26fa9-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="26fa9-175">Az adatbázishoz hozzárendelni szükséges szolgáltatás-célkiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26fa9-175">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26fa9-176">-ResourceGroupName</span></span>
<span data-ttu-id="26fa9-177">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="26fa9-177">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="26fa9-178">-SampleName</span><span class="sxs-lookup"><span data-stu-id="26fa9-178">-SampleName</span></span>
<span data-ttu-id="26fa9-179">Az adatbázis létrehozásakor alkalmazandó mintaséma neve.</span><span class="sxs-lookup"><span data-stu-id="26fa9-179">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-180">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="26fa9-180">-SecondaryType</span></span>
<span data-ttu-id="26fa9-181">Az adatbázis másodlagos típusa, ha az másodlagos.</span><span class="sxs-lookup"><span data-stu-id="26fa9-181">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="26fa9-182">Érvényes értékek: Földrajzi név és Név.</span><span class="sxs-lookup"><span data-stu-id="26fa9-182">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="26fa9-183">-ServerName</span><span class="sxs-lookup"><span data-stu-id="26fa9-183">-ServerName</span></span>
<span data-ttu-id="26fa9-184">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26fa9-184">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="26fa9-185">-Címkék</span><span class="sxs-lookup"><span data-stu-id="26fa9-185">-Tags</span></span>
<span data-ttu-id="26fa9-186">Egy olyan kulcsérték-párok szótárát adja meg kivonattábla formájában, amely a parancsmag az új adatbázishoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="26fa9-186">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="26fa9-187">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="26fa9-187">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="26fa9-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="26fa9-188">-VCore</span></span>
<span data-ttu-id="26fa9-189">Az Azure Sql-adatbázis Vcore-száma</span><span class="sxs-lookup"><span data-stu-id="26fa9-189">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26fa9-190">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="26fa9-190">-ZoneRedundant</span></span>
<span data-ttu-id="26fa9-191">Az Azure Sql-adatbázissal társítva található zónaredundáns</span><span class="sxs-lookup"><span data-stu-id="26fa9-191">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="26fa9-192">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26fa9-192">-Confirm</span></span>
<span data-ttu-id="26fa9-193">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="26fa9-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26fa9-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26fa9-194">-WhatIf</span></span>
<span data-ttu-id="26fa9-195">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="26fa9-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26fa9-196">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26fa9-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26fa9-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fa9-197">CommonParameters</span></span>
<span data-ttu-id="26fa9-198">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26fa9-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fa9-199">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26fa9-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fa9-200">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26fa9-200">INPUTS</span></span>

### <span data-ttu-id="26fa9-201">System.String</span><span class="sxs-lookup"><span data-stu-id="26fa9-201">System.String</span></span>

## <span data-ttu-id="26fa9-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26fa9-202">OUTPUTS</span></span>

### <span data-ttu-id="26fa9-203">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="26fa9-203">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="26fa9-204">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26fa9-204">NOTES</span></span>

## <span data-ttu-id="26fa9-205">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26fa9-205">RELATED LINKS</span></span>

[<span data-ttu-id="26fa9-206">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26fa9-206">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="26fa9-207">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="26fa9-207">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="26fa9-208">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="26fa9-208">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="26fa9-209">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26fa9-209">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="26fa9-210">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26fa9-210">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="26fa9-211">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26fa9-211">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="26fa9-212">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26fa9-212">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="26fa9-213">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="26fa9-213">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

