---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e97143f282bc01bbdd9c5d6186f0ccb5532b1df1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011540"
---
# <span data-ttu-id="4e9fa-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4e9fa-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="4e9fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9fa-103">Egy vagy több hosszú távú adatmegőrzési biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="4e9fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e9fa-104">SYNTAX</span></span>

### <span data-ttu-id="4e9fa-105">Hely (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e9fa-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e9fa-106">Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4e9fa-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e9fa-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="4e9fa-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e9fa-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e9fa-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e9fa-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e9fa-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e9fa-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="4e9fa-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e9fa-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="4e9fa-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e9fa-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e9fa-112">DESCRIPTION</span></span>
<span data-ttu-id="4e9fa-113">A **Get-AzSqlDatabaseLongTermRetentionBackup** parancsmag minden hosszú távú adatmegőrzési biztonsági másolatot kap egy hely, egy kiszolgáló vagy egy adatbázis esetében, vagy egy bizonyos hosszú távú adatmegőrzési biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="4e9fa-114">Példák</span><span class="sxs-lookup"><span data-stu-id="4e9fa-114">EXAMPLES</span></span>

### <span data-ttu-id="4e9fa-115">Példa 1: a hely minden biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4e9fa-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="4e9fa-116">Ez a parancs minden hosszú távú adatmegőrzési biztonsági másolatot kap minden adatbázishoz (amely lehet, hogy életben vagy törölve van) az northeurope-ban, az erőforráscsoport csak akkor lesz beállítva, ha a kiszolgáló él.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="4e9fa-117">2. példa: a biztonsági másolatok beolvasása az erőforráscsoport alatti helyekre</span><span class="sxs-lookup"><span data-stu-id="4e9fa-117">Example 2: Get all backups for a location under a resource group</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ResourceGroup resourceGroup01


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="4e9fa-118">Ez a parancs minden hosszú távú adatmegőrzési biztonsági másolatot kap minden adatbázishoz (amely lehet élve vagy törölve) a northeurope.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="4e9fa-119">3. példa: adott hosszú távú adatmegőrzési biztonsági másolat beszerzése</span><span class="sxs-lookup"><span data-stu-id="4e9fa-119">Example 3: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="4e9fa-120">Ez a parancs a biztonsági másolatot a név 601061b7-d10b-46e0-bf77-a2bfb16a6add kapja; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="4e9fa-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="4e9fa-121">4. példa: az adatbázis hosszú távú adatmegőrzési biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4e9fa-121">Example 4: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="4e9fa-122">Ez a parancs minden hosszú távú adatmegőrzési biztonsági másolatot kap a database01-hoz</span><span class="sxs-lookup"><span data-stu-id="4e9fa-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="4e9fa-123">Példa 5: a hosszú távú adatmegőrzési biztonsági másolatok beszerzése szűréssel</span><span class="sxs-lookup"><span data-stu-id="4e9fa-123">Example 5: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server01
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="4e9fa-124">Ez a parancs minden olyan biztonsági mentést kap, amely a "601061b7" kezdetű névvel kezdődik</span><span class="sxs-lookup"><span data-stu-id="4e9fa-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="4e9fa-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e9fa-125">PARAMETERS</span></span>

### <span data-ttu-id="4e9fa-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="4e9fa-126">-BackupName</span></span>
<span data-ttu-id="4e9fa-127">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-127">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9fa-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e9fa-128">-DatabaseName</span></span>
<span data-ttu-id="4e9fa-129">Annak az Azure SQL-adatbázisnak a neve, amelyből a biztonsági másolat származik.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-129">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BackupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9fa-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="4e9fa-130">-DatabaseState</span></span>
<span data-ttu-id="4e9fa-131">Annak az adatbázisnak az állapota, amelynek biztonsági másolatait meg szeretné keresni, élve, törölt vagy mindet.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="4e9fa-132">Alapértékek mind</span><span class="sxs-lookup"><span data-stu-id="4e9fa-132">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9fa-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e9fa-133">-DefaultProfile</span></span>
<span data-ttu-id="4e9fa-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e9fa-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e9fa-135">-InputObject</span></span>
<span data-ttu-id="4e9fa-136">Az adatbázis-objektum, amelyhez biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-136">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9fa-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="4e9fa-137">-Location</span></span>
<span data-ttu-id="4e9fa-138">A biztonsági másolatok forrása kiszolgálójának helye.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-138">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9fa-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="4e9fa-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="4e9fa-140">Szeretné-e, hogy csak az adatbázis legújabb biztonsági másolatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="4e9fa-141">Az alapértelmezett érték a false.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-141">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9fa-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e9fa-142">-ResourceGroupName</span></span>
<span data-ttu-id="4e9fa-143">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9fa-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e9fa-144">-ResourceId</span></span>
<span data-ttu-id="4e9fa-145">Az adatbázis-erőforrás azonosítója, amellyel biztonsági másolatot kaphat.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-145">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9fa-146">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="4e9fa-146">-ServerName</span></span>
<span data-ttu-id="4e9fa-147">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a biztonsági másolatok találhatók.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-147">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9fa-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e9fa-148">-Confirm</span></span>
<span data-ttu-id="4e9fa-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e9fa-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e9fa-150">-WhatIf</span></span>
<span data-ttu-id="4e9fa-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e9fa-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e9fa-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e9fa-153">CommonParameters</span></span>
<span data-ttu-id="4e9fa-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e9fa-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e9fa-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4e9fa-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e9fa-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e9fa-156">INPUTS</span></span>

### <span data-ttu-id="4e9fa-157">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4e9fa-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="4e9fa-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4e9fa-158">System.String</span></span>

## <span data-ttu-id="4e9fa-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e9fa-159">OUTPUTS</span></span>

### <span data-ttu-id="4e9fa-160">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="4e9fa-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="4e9fa-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e9fa-161">NOTES</span></span>

## <span data-ttu-id="4e9fa-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e9fa-162">RELATED LINKS</span></span>

[<span data-ttu-id="4e9fa-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4e9fa-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="4e9fa-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4e9fa-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="4e9fa-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4e9fa-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="4e9fa-166">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="4e9fa-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)