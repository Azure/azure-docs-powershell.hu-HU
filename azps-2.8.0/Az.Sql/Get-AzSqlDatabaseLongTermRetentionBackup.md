---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: fc6c6c2756ecb1c4174fc1255c175a49f66360cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839243"
---
# <span data-ttu-id="fe0eb-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fe0eb-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="fe0eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe0eb-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0eb-103">Egy vagy több hosszú távú adatmegőrzési biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="fe0eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe0eb-104">SYNTAX</span></span>

### <span data-ttu-id="fe0eb-105">Hely (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe0eb-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [[-ResourceGroupName] <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0eb-106">Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fe0eb-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [[-ResourceGroupName] <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0eb-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="fe0eb-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0eb-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe0eb-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0eb-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe0eb-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0eb-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe0eb-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe0eb-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe0eb-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe0eb-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe0eb-112">DESCRIPTION</span></span>
<span data-ttu-id="fe0eb-113">A **Get-AzSqlDatabaseLongTermRetentionBackup** parancsmag minden hosszú távú adatmegőrzési biztonsági másolatot kap egy hely, egy kiszolgáló vagy egy adatbázis esetében, vagy egy bizonyos hosszú távú adatmegőrzési biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="fe0eb-114">Példák</span><span class="sxs-lookup"><span data-stu-id="fe0eb-114">EXAMPLES</span></span>

### <span data-ttu-id="fe0eb-115">Példa 1: a hely minden biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="fe0eb-115">Example 1: Get all backups for a location</span></span>
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

<span data-ttu-id="fe0eb-116">Ez a parancs minden hosszú távú adatmegőrzési biztonsági másolatot kap minden adatbázishoz (amely lehet, hogy életben vagy törölve van) az northeurope-ban, az erőforráscsoport csak akkor lesz beállítva, ha a kiszolgáló él.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="fe0eb-117">2. példa: a biztonsági másolatok beolvasása az erőforráscsoport alatti helyekre</span><span class="sxs-lookup"><span data-stu-id="fe0eb-117">Example 2: Get all backups for a location under a resource group</span></span>
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

<span data-ttu-id="fe0eb-118">Ez a parancs minden hosszú távú adatmegőrzési biztonsági másolatot kap minden adatbázishoz (amely lehet élve vagy törölve) a northeurope.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="fe0eb-119">3. példa: adott hosszú távú adatmegőrzési biztonsági másolat beszerzése</span><span class="sxs-lookup"><span data-stu-id="fe0eb-119">Example 3: Get a specific long term retention backup</span></span>
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

<span data-ttu-id="fe0eb-120">Ez a parancs a biztonsági másolatot a név 601061b7-d10b-46e0-bf77-a2bfb16a6add kapja; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="fe0eb-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="fe0eb-121">4. példa: az adatbázis hosszú távú adatmegőrzési biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="fe0eb-121">Example 4: Get all long term retention backups for a database</span></span>
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

<span data-ttu-id="fe0eb-122">Ez a parancs minden hosszú távú adatmegőrzési biztonsági másolatot kap a database01-hoz</span><span class="sxs-lookup"><span data-stu-id="fe0eb-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="fe0eb-123">Példa 5: a hosszú távú adatmegőrzési biztonsági másolatok beszerzése szűréssel</span><span class="sxs-lookup"><span data-stu-id="fe0eb-123">Example 5: Get long term retention backups using filtering</span></span>
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

<span data-ttu-id="fe0eb-124">Ez a parancs minden olyan biztonsági mentést kap, amely a "601061b7" kezdetű névvel kezdődik</span><span class="sxs-lookup"><span data-stu-id="fe0eb-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="fe0eb-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe0eb-125">PARAMETERS</span></span>

### <span data-ttu-id="fe0eb-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="fe0eb-126">-BackupName</span></span>
<span data-ttu-id="fe0eb-127">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-127">The name of the backup.</span></span>

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

### <span data-ttu-id="fe0eb-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe0eb-128">-DatabaseName</span></span>
<span data-ttu-id="fe0eb-129">Annak az Azure SQL-adatbázisnak a neve, amelyből a biztonsági másolat származik.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-129">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="fe0eb-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="fe0eb-130">-DatabaseState</span></span>
<span data-ttu-id="fe0eb-131">Annak az adatbázisnak az állapota, amelynek biztonsági másolatait meg szeretné keresni, élve, törölt vagy mindet.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="fe0eb-132">Alapértékek mind</span><span class="sxs-lookup"><span data-stu-id="fe0eb-132">Defaults to All</span></span>

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

### <span data-ttu-id="fe0eb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0eb-133">-DefaultProfile</span></span>
<span data-ttu-id="fe0eb-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe0eb-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe0eb-135">-InputObject</span></span>
<span data-ttu-id="fe0eb-136">Az adatbázis-objektum, amelyhez biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-136">The database object to get backups for.</span></span>

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

### <span data-ttu-id="fe0eb-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="fe0eb-137">-Location</span></span>
<span data-ttu-id="fe0eb-138">A biztonsági másolatok forrása kiszolgálójának helye.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-138">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="fe0eb-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="fe0eb-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="fe0eb-140">Szeretné-e, hogy csak az adatbázis legújabb biztonsági másolatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="fe0eb-141">Az alapértelmezett érték a false.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-141">Defaults to false.</span></span>

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

### <span data-ttu-id="fe0eb-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0eb-142">-ResourceGroupName</span></span>
<span data-ttu-id="fe0eb-143">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe0eb-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe0eb-144">-ResourceId</span></span>
<span data-ttu-id="fe0eb-145">Az adatbázis-erőforrás azonosítója, amellyel biztonsági másolatot kaphat.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-145">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="fe0eb-146">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fe0eb-146">-ServerName</span></span>
<span data-ttu-id="fe0eb-147">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a biztonsági másolatok találhatók.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-147">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="fe0eb-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe0eb-148">-Confirm</span></span>
<span data-ttu-id="fe0eb-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe0eb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe0eb-150">-WhatIf</span></span>
<span data-ttu-id="fe0eb-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe0eb-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe0eb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0eb-153">CommonParameters</span></span>
<span data-ttu-id="fe0eb-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe0eb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0eb-155">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fe0eb-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0eb-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe0eb-156">INPUTS</span></span>

### <span data-ttu-id="fe0eb-157">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fe0eb-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="fe0eb-158">System. String</span><span class="sxs-lookup"><span data-stu-id="fe0eb-158">System.String</span></span>

## <span data-ttu-id="fe0eb-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe0eb-159">OUTPUTS</span></span>

### <span data-ttu-id="fe0eb-160">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="fe0eb-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="fe0eb-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe0eb-161">NOTES</span></span>

## <span data-ttu-id="fe0eb-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe0eb-162">RELATED LINKS</span></span>

[<span data-ttu-id="fe0eb-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fe0eb-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="fe0eb-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe0eb-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fe0eb-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe0eb-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fe0eb-166">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fe0eb-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)