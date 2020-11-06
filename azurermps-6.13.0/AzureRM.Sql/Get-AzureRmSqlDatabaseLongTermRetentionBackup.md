---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 6ae416cd9ac49bc4d7f54289cd9c5b43a377d20b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495631"
---
# <span data-ttu-id="87ca3-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="87ca3-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="87ca3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="87ca3-103">Egy vagy több hosszú távú adatmegőrzési biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="87ca3-103">Gets one or more long term retention backups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87ca3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87ca3-104">SYNTAX</span></span>

### <span data-ttu-id="87ca3-105">Hely (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87ca3-105">Location (Default)</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ca3-106">Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="87ca3-106">ServerName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ca3-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="87ca3-107">BackupName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 -DatabaseName <String> [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87ca3-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="87ca3-108">GetBackupByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ca3-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="87ca3-109">GetBackupsByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ca3-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="87ca3-110">GetBackupByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ca3-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="87ca3-111">GetBackupsByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87ca3-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="87ca3-112">DESCRIPTION</span></span>
<span data-ttu-id="87ca3-113">A **Get-AzureRmSqlDatabaseLongTermRetentionBackup** parancsmag minden hosszú távú adatmegőrzési biztonsági másolatot kap egy hely, egy kiszolgáló vagy egy adatbázis esetében, vagy egy bizonyos hosszú távú adatmegőrzési biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="87ca3-113">The **Get-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="87ca3-114">Példák</span><span class="sxs-lookup"><span data-stu-id="87ca3-114">EXAMPLES</span></span>

### <span data-ttu-id="87ca3-115">Példa 1: a hely minden biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="87ca3-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="87ca3-116">Ez a parancs minden hosszú távú adatmegőrzési biztonsági másolatot kap minden adatbázishoz (amely lehet, hogy életben vagy törölt) az northeurope-ban.</span><span class="sxs-lookup"><span data-stu-id="87ca3-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="87ca3-117">2. példa: adott hosszú távú adatmegőrzési biztonsági másolat beszerzése</span><span class="sxs-lookup"><span data-stu-id="87ca3-117">Example 2: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="87ca3-118">Ez a parancs a biztonsági másolatot a név 601061b7-d10b-46e0-bf77-a2bfb16a6add kapja; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="87ca3-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="87ca3-119">3. példa: az adatbázis hosszú távú adatmegőrzési biztonsági másolatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="87ca3-119">Example 3: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzureRmSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="87ca3-120">Ez a parancs minden hosszú távú adatmegőrzési biztonsági másolatot kap a database01-hoz</span><span class="sxs-lookup"><span data-stu-id="87ca3-120">This command gets all long term retention backups for database01</span></span>

## <span data-ttu-id="87ca3-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87ca3-121">PARAMETERS</span></span>

### <span data-ttu-id="87ca3-122">-BackupName</span><span class="sxs-lookup"><span data-stu-id="87ca3-122">-BackupName</span></span>
<span data-ttu-id="87ca3-123">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="87ca3-123">The name of the backup.</span></span>

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

### <span data-ttu-id="87ca3-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="87ca3-124">-DatabaseName</span></span>
<span data-ttu-id="87ca3-125">Annak az Azure SQL-adatbázisnak a neve, amelyből a biztonsági másolat származik.</span><span class="sxs-lookup"><span data-stu-id="87ca3-125">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="87ca3-126">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="87ca3-126">-DatabaseState</span></span>
<span data-ttu-id="87ca3-127">Annak az adatbázisnak az állapota, amelynek biztonsági másolatait meg szeretné keresni, élve, törölt vagy mindet.</span><span class="sxs-lookup"><span data-stu-id="87ca3-127">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="87ca3-128">Alapértékek mind</span><span class="sxs-lookup"><span data-stu-id="87ca3-128">Defaults to All</span></span>

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

### <span data-ttu-id="87ca3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ca3-129">-DefaultProfile</span></span>
<span data-ttu-id="87ca3-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87ca3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87ca3-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87ca3-131">-InputObject</span></span>
<span data-ttu-id="87ca3-132">Az adatbázis-objektum, amelyhez biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="87ca3-132">The database object to get backups for.</span></span>

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

### <span data-ttu-id="87ca3-133">-Hely</span><span class="sxs-lookup"><span data-stu-id="87ca3-133">-Location</span></span>
<span data-ttu-id="87ca3-134">A biztonsági másolatok forrása kiszolgálójának helye.</span><span class="sxs-lookup"><span data-stu-id="87ca3-134">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="87ca3-135">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="87ca3-135">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="87ca3-136">Szeretné-e, hogy csak az adatbázis legújabb biztonsági másolatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="87ca3-136">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="87ca3-137">Az alapértelmezett érték a false.</span><span class="sxs-lookup"><span data-stu-id="87ca3-137">Defaults to false.</span></span>

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

### <span data-ttu-id="87ca3-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87ca3-138">-ResourceId</span></span>
<span data-ttu-id="87ca3-139">Az adatbázis-erőforrás azonosítója, amellyel biztonsági másolatot kaphat.</span><span class="sxs-lookup"><span data-stu-id="87ca3-139">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="87ca3-140">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="87ca3-140">-ServerName</span></span>
<span data-ttu-id="87ca3-141">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a biztonsági másolatok találhatók.</span><span class="sxs-lookup"><span data-stu-id="87ca3-141">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="87ca3-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87ca3-142">-Confirm</span></span>
<span data-ttu-id="87ca3-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87ca3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87ca3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87ca3-144">-WhatIf</span></span>
<span data-ttu-id="87ca3-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87ca3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87ca3-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87ca3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87ca3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ca3-147">CommonParameters</span></span>
<span data-ttu-id="87ca3-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87ca3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ca3-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87ca3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ca3-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87ca3-150">INPUTS</span></span>

### <span data-ttu-id="87ca3-151">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="87ca3-151">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>
<span data-ttu-id="87ca3-152">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="87ca3-152">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="87ca3-153">System. String</span><span class="sxs-lookup"><span data-stu-id="87ca3-153">System.String</span></span>

## <span data-ttu-id="87ca3-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87ca3-154">OUTPUTS</span></span>

### <span data-ttu-id="87ca3-155">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="87ca3-155">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="87ca3-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87ca3-156">NOTES</span></span>

## <span data-ttu-id="87ca3-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87ca3-157">RELATED LINKS</span></span>

[<span data-ttu-id="87ca3-158">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="87ca3-158">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="87ca3-159">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="87ca3-159">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="87ca3-160">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="87ca3-160">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="87ca3-161">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="87ca3-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
