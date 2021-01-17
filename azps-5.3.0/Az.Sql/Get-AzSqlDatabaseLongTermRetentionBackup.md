---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e97143f282bc01bbdd9c5d6186f0ccb5532b1df1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374946"
---
# <span data-ttu-id="71d60-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="71d60-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="71d60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71d60-102">SYNOPSIS</span></span>
<span data-ttu-id="71d60-103">Egy vagy több hosszú távú adatmegőrzési biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="71d60-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="71d60-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71d60-104">SYNTAX</span></span>

### <span data-ttu-id="71d60-105">Hely (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71d60-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d60-106">ServerName</span><span class="sxs-lookup"><span data-stu-id="71d60-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d60-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="71d60-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d60-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="71d60-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d60-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="71d60-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d60-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="71d60-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d60-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="71d60-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71d60-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71d60-112">DESCRIPTION</span></span>
<span data-ttu-id="71d60-113">A **Get-AzSqlDatabaseLongTermRetentionBackup** parancsmag hosszú távú adatmegőrzési biztonsági másolatokat kap egy helyről, kiszolgálóról vagy adatbázisról, illetve egy adott hosszú távú adatmegőrzésről.</span><span class="sxs-lookup"><span data-stu-id="71d60-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="71d60-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71d60-114">EXAMPLES</span></span>

### <span data-ttu-id="71d60-115">1. példa: Az összes biztonsági mentés lekérte egy helyre</span><span class="sxs-lookup"><span data-stu-id="71d60-115">Example 1: Get all backups for a location</span></span>
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

<span data-ttu-id="71d60-116">Ez a parancs a northeurope-ban található összes (esetleg élő vagy törölt) adatbázisra vonatkozó hosszú távú adatmegőrzési biztonsági másolatot kap, az erőforráscsoport csak akkor lesz beállítva, ha a kiszolgáló élő.</span><span class="sxs-lookup"><span data-stu-id="71d60-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="71d60-117">2. példa: Erőforráscsoport alatti hely összes biztonsági másolatának be szerezze</span><span class="sxs-lookup"><span data-stu-id="71d60-117">Example 2: Get all backups for a location under a resource group</span></span>
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

<span data-ttu-id="71d60-118">Ez a parancs minden hosszú távú adatmegőrzési biztonsági másolatot kap az északeurope-i erőforráscsoportokban található (esetleg élő vagy törölt) adatbázisokról.</span><span class="sxs-lookup"><span data-stu-id="71d60-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="71d60-119">3. példa: Adott hosszú távú adatmegőrzési biztonsági másolat készítése</span><span class="sxs-lookup"><span data-stu-id="71d60-119">Example 3: Get a specific long term retention backup</span></span>
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

<span data-ttu-id="71d60-120">Ez a parancs a 601061b7-d10b-46e0-bf77-a2bfb16a6add;13165566550000000 nevet kapja</span><span class="sxs-lookup"><span data-stu-id="71d60-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="71d60-121">4. példa: Az adatbázis összes hosszú távú adatmegőrzési biztonsági mentése</span><span class="sxs-lookup"><span data-stu-id="71d60-121">Example 4: Get all long term retention backups for a database</span></span>
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

<span data-ttu-id="71d60-122">Ez a parancs hosszú távú adatmegőrzési biztonsági másolatokat kap az adatbázis01-hez</span><span class="sxs-lookup"><span data-stu-id="71d60-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="71d60-123">5. példa: Hosszú távú adatmegőrzési biztonsági másolatok készítése szűréssel</span><span class="sxs-lookup"><span data-stu-id="71d60-123">Example 5: Get long term retention backups using filtering</span></span>
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

<span data-ttu-id="71d60-124">Ez a parancs minden biztonsági mentést a "601061b7" névvel kezdődik</span><span class="sxs-lookup"><span data-stu-id="71d60-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="71d60-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71d60-125">PARAMETERS</span></span>

### <span data-ttu-id="71d60-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="71d60-126">-BackupName</span></span>
<span data-ttu-id="71d60-127">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="71d60-127">The name of the backup.</span></span>

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

### <span data-ttu-id="71d60-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71d60-128">-DatabaseName</span></span>
<span data-ttu-id="71d60-129">Annak az Azure SQL-adatbázisnak a neve, amelyből a biztonsági másolat jött létre.</span><span class="sxs-lookup"><span data-stu-id="71d60-129">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="71d60-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="71d60-130">-DatabaseState</span></span>
<span data-ttu-id="71d60-131">Annak az adatbázisnak az állapota, amelynek biztonsági másolatát meg szeretné találni: "Élő", "Törölt" vagy "Mind".</span><span class="sxs-lookup"><span data-stu-id="71d60-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="71d60-132">Alapértékek az összeshez</span><span class="sxs-lookup"><span data-stu-id="71d60-132">Defaults to All</span></span>

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

### <span data-ttu-id="71d60-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d60-133">-DefaultProfile</span></span>
<span data-ttu-id="71d60-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71d60-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71d60-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71d60-135">-InputObject</span></span>
<span data-ttu-id="71d60-136">Az adatbázis-objektum, amelyről biztonsági másolatot kell készíteni.</span><span class="sxs-lookup"><span data-stu-id="71d60-136">The database object to get backups for.</span></span>

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

### <span data-ttu-id="71d60-137">-Location</span><span class="sxs-lookup"><span data-stu-id="71d60-137">-Location</span></span>
<span data-ttu-id="71d60-138">A biztonsági másolatok forráskiszolgálójának helye.</span><span class="sxs-lookup"><span data-stu-id="71d60-138">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="71d60-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="71d60-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="71d60-140">Függetlenül attól, hogy adatbázisonként a legújabb biztonsági másolatot kell-e készíteni.</span><span class="sxs-lookup"><span data-stu-id="71d60-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="71d60-141">Alapértelmezés szerint hamis.</span><span class="sxs-lookup"><span data-stu-id="71d60-141">Defaults to false.</span></span>

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

### <span data-ttu-id="71d60-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d60-142">-ResourceGroupName</span></span>
<span data-ttu-id="71d60-143">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71d60-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="71d60-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71d60-144">-ResourceId</span></span>
<span data-ttu-id="71d60-145">Az adatbázis erőforrás-azonosítója, amelyről biztonsági másolatot készít.</span><span class="sxs-lookup"><span data-stu-id="71d60-145">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="71d60-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71d60-146">-ServerName</span></span>
<span data-ttu-id="71d60-147">Annak az Azure SQL Servernek a neve, amely alatt a biztonsági másolatok vannak.</span><span class="sxs-lookup"><span data-stu-id="71d60-147">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="71d60-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71d60-148">-Confirm</span></span>
<span data-ttu-id="71d60-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="71d60-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71d60-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71d60-150">-WhatIf</span></span>
<span data-ttu-id="71d60-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="71d60-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71d60-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71d60-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71d60-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d60-153">CommonParameters</span></span>
<span data-ttu-id="71d60-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d60-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d60-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71d60-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d60-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71d60-156">INPUTS</span></span>

### <span data-ttu-id="71d60-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="71d60-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="71d60-158">System.String</span><span class="sxs-lookup"><span data-stu-id="71d60-158">System.String</span></span>

## <span data-ttu-id="71d60-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71d60-159">OUTPUTS</span></span>

### <span data-ttu-id="71d60-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="71d60-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="71d60-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71d60-161">NOTES</span></span>

## <span data-ttu-id="71d60-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71d60-162">RELATED LINKS</span></span>

[<span data-ttu-id="71d60-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="71d60-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="71d60-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71d60-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="71d60-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71d60-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="71d60-166">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="71d60-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)