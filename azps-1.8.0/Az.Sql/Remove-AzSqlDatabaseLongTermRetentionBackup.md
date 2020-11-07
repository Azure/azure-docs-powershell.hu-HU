---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 8fd76e227951afefcbb8f7b04cf4ae3616ef5ef7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668858"
---
# <span data-ttu-id="d3f6c-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d3f6c-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="d3f6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f6c-103">Hosszú távú adatmegőrzési biztonsági másolat törlése</span><span class="sxs-lookup"><span data-stu-id="d3f6c-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="d3f6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3f6c-104">SYNTAX</span></span>

### <span data-ttu-id="d3f6c-105">RemoveBackupDefault (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3f6c-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f6c-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="d3f6c-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f6c-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f6c-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f6c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3f6c-108">DESCRIPTION</span></span>
<span data-ttu-id="d3f6c-109">A **Remove-AzSqlDatabaseLongTermRetentionBackup** parancsmag törli a megadott biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="d3f6c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d3f6c-110">EXAMPLES</span></span>

### <span data-ttu-id="d3f6c-111">Példa 1: egyetlen biztonsági másolat törlése</span><span class="sxs-lookup"><span data-stu-id="d3f6c-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="d3f6c-112">Törli a biztonsági másolatot a név 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="d3f6c-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="d3f6c-113">2. példa: egy hely minden biztonsági mentésének törlése</span><span class="sxs-lookup"><span data-stu-id="d3f6c-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="d3f6c-114">Ez a parancs törli a hosszú távú adatmegőrzési biztonsági mentéseket a northeurope helyéhez.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="d3f6c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3f6c-115">PARAMETERS</span></span>

### <span data-ttu-id="d3f6c-116">-BackupName</span><span class="sxs-lookup"><span data-stu-id="d3f6c-116">-BackupName</span></span>
<span data-ttu-id="d3f6c-117">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-117">The name of the backup.</span></span>

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

### <span data-ttu-id="d3f6c-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3f6c-118">-DatabaseName</span></span>
<span data-ttu-id="d3f6c-119">Annak az Azure SQL-adatbázisnak a neve, amelyből a biztonsági másolat származik.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-119">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="d3f6c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f6c-120">-DefaultProfile</span></span>
<span data-ttu-id="d3f6c-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3f6c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d3f6c-122">-Force</span></span>
<span data-ttu-id="d3f6c-123">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="d3f6c-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d3f6c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3f6c-124">-InputObject</span></span>
<span data-ttu-id="d3f6c-125">Az adatbázis hosszú távú adatmegőrzési objektuma eltávolításra készül.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f6c-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="d3f6c-126">-Location</span></span>
<span data-ttu-id="d3f6c-127">A biztonsági másolatok forrása kiszolgálójának helye.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-127">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="d3f6c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f6c-128">-ResourceId</span></span>
<span data-ttu-id="d3f6c-129">Az adatbázis hosszú távú adatmegőrzési biztonsági másolatának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="d3f6c-130">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d3f6c-130">-ServerName</span></span>
<span data-ttu-id="d3f6c-131">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a biztonsági másolat található.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-131">The name of the Azure SQL Server the backup is under.</span></span>

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

### <span data-ttu-id="d3f6c-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d3f6c-132">-Confirm</span></span>
<span data-ttu-id="d3f6c-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f6c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f6c-134">-WhatIf</span></span>
<span data-ttu-id="d3f6c-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f6c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f6c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f6c-137">CommonParameters</span></span>
<span data-ttu-id="d3f6c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3f6c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f6c-139">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3f6c-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f6c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3f6c-140">INPUTS</span></span>

### <span data-ttu-id="d3f6c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f6c-141">System.String</span></span>

## <span data-ttu-id="d3f6c-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3f6c-142">OUTPUTS</span></span>

### <span data-ttu-id="d3f6c-143">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="d3f6c-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="d3f6c-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3f6c-144">NOTES</span></span>

## <span data-ttu-id="d3f6c-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3f6c-145">RELATED LINKS</span></span>

[<span data-ttu-id="d3f6c-146">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d3f6c-146">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d3f6c-147">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d3f6c-147">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d3f6c-148">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d3f6c-148">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d3f6c-149">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d3f6c-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)