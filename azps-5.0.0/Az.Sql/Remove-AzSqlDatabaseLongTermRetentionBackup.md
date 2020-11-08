---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: be2e9342407cea6ba3da0bf239ee73e7b726dd82
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185824"
---
# <span data-ttu-id="3a660-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3a660-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="3a660-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a660-102">SYNOPSIS</span></span>
<span data-ttu-id="3a660-103">Hosszú távú adatmegőrzési biztonsági másolat törlése</span><span class="sxs-lookup"><span data-stu-id="3a660-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="3a660-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a660-104">SYNTAX</span></span>

### <span data-ttu-id="3a660-105">RemoveBackupDefault (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a660-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a660-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="3a660-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a660-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="3a660-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a660-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a660-108">DESCRIPTION</span></span>
<span data-ttu-id="3a660-109">A **Remove-AzSqlDatabaseLongTermRetentionBackup** parancsmag törli a megadott biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="3a660-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="3a660-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3a660-110">EXAMPLES</span></span>

### <span data-ttu-id="3a660-111">Példa 1: egyetlen biztonsági másolat törlése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="3a660-111">Example 1: Delete a single backup with resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000" -ResourceGrouName resourcegroup01


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

<span data-ttu-id="3a660-112">Törli a biztonsági másolatot a név 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="3a660-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="3a660-113">2. példa: egyetlen biztonsági másolat törlése erőforráscsoport nélkül</span><span class="sxs-lookup"><span data-stu-id="3a660-113">Example 2: Delete a single backup without resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server02 -DatabaseName database02 -BackupName "55970792-164c-4a4a-88e5-7158d092d503;131656309980000000"


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

<span data-ttu-id="3a660-114">Törli a biztonsági másolatot a név 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="3a660-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="3a660-115">3. példa: egy hely minden biztonsági mentésének törlése</span><span class="sxs-lookup"><span data-stu-id="3a660-115">Example 3: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="3a660-116">Ez a parancs törli a hosszú távú adatmegőrzési biztonsági mentéseket a northeurope helyéhez.</span><span class="sxs-lookup"><span data-stu-id="3a660-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="3a660-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a660-117">PARAMETERS</span></span>

### <span data-ttu-id="3a660-118">-BackupName</span><span class="sxs-lookup"><span data-stu-id="3a660-118">-BackupName</span></span>
<span data-ttu-id="3a660-119">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="3a660-119">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a660-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a660-120">-DatabaseName</span></span>
<span data-ttu-id="3a660-121">Annak az Azure SQL-adatbázisnak a neve, amelyből a biztonsági másolat származik.</span><span class="sxs-lookup"><span data-stu-id="3a660-121">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a660-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a660-122">-DefaultProfile</span></span>
<span data-ttu-id="3a660-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a660-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a660-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3a660-124">-Force</span></span>
<span data-ttu-id="3a660-125">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="3a660-125">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a660-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a660-126">-InputObject</span></span>
<span data-ttu-id="3a660-127">Az adatbázis hosszú távú adatmegőrzési objektuma eltávolításra készül.</span><span class="sxs-lookup"><span data-stu-id="3a660-127">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a660-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="3a660-128">-Location</span></span>
<span data-ttu-id="3a660-129">A biztonsági másolatok forrása kiszolgálójának helye.</span><span class="sxs-lookup"><span data-stu-id="3a660-129">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a660-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a660-130">-ResourceGroupName</span></span>
<span data-ttu-id="3a660-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3a660-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a660-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a660-132">-ResourceId</span></span>
<span data-ttu-id="3a660-133">Az adatbázis hosszú távú adatmegőrzési biztonsági másolatának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3a660-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a660-134">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3a660-134">-ServerName</span></span>
<span data-ttu-id="3a660-135">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a biztonsági másolat található.</span><span class="sxs-lookup"><span data-stu-id="3a660-135">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a660-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3a660-136">-Confirm</span></span>
<span data-ttu-id="3a660-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3a660-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a660-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a660-138">-WhatIf</span></span>
<span data-ttu-id="3a660-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3a660-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a660-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a660-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a660-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a660-141">CommonParameters</span></span>
<span data-ttu-id="3a660-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a660-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a660-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a660-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a660-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a660-144">INPUTS</span></span>

### <span data-ttu-id="3a660-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3a660-145">System.String</span></span>

## <span data-ttu-id="3a660-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a660-146">OUTPUTS</span></span>

### <span data-ttu-id="3a660-147">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="3a660-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="3a660-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a660-148">NOTES</span></span>

## <span data-ttu-id="3a660-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a660-149">RELATED LINKS</span></span>

[<span data-ttu-id="3a660-150">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3a660-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3a660-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a660-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3a660-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a660-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3a660-153">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3a660-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)