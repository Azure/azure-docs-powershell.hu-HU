---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 464334aa67be554a20c7d1b15e7d591a25979809
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929761"
---
# <span data-ttu-id="fc0c6-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fc0c6-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="fc0c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0c6-103">Hosszú távú adatmegőrzési biztonsági mentést kap.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="fc0c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc0c6-104">SYNTAX</span></span>

### <span data-ttu-id="fc0c6-105">Hely (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc0c6-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc0c6-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="fc0c6-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc0c6-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc0c6-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc0c6-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="fc0c6-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc0c6-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc0c6-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc0c6-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc0c6-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc0c6-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc0c6-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc0c6-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc0c6-112">DESCRIPTION</span></span>
<span data-ttu-id="fc0c6-113">{{ Töltse ki a leírás }}</span><span class="sxs-lookup"><span data-stu-id="fc0c6-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="fc0c6-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc0c6-114">EXAMPLES</span></span>

### <span data-ttu-id="fc0c6-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="fc0c6-115">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


BackupExpirationTime : 3/10/2020 1:10:45 PM
BackupName           : 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
BackupTime           : 2/22/2020 6:04:15 AM
DatabaseName         : test
DatabaseDeletionTime : 2/24/2020 2:56:44 PM
Location             : southeastasia
ResourceId           : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManaged
                       Instances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
ManagedInstanceName  : testInstance
InstanceCreateTime   : 10/17/2019 4:52:10 PM
ResourceGroupName    : testResourceGroup
```

<span data-ttu-id="fc0c6-116">Egy adott adatbázis összes hosszú távú adatmegőrzési biztonsági másolatát beveszi.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="fc0c6-117">Az erőforráscsoport megadása nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="fc0c6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc0c6-118">PARAMETERS</span></span>

### <span data-ttu-id="fc0c6-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="fc0c6-119">-BackupName</span></span>
<span data-ttu-id="fc0c6-120">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-120">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc0c6-121">-DatabaseName</span></span>
<span data-ttu-id="fc0c6-122">Annak a felügyelt adatbázisnak a neve, amely alatt a biztonsági másolatok vannak.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="fc0c6-123">-DatabaseState</span></span>
<span data-ttu-id="fc0c6-124">Annak az adatbázisnak az állapota, amelynek biztonsági másolatát meg szeretné találni: "Élő", "Törölt" vagy "Mind".</span><span class="sxs-lookup"><span data-stu-id="fc0c6-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="fc0c6-125">Alapértékek az összeshez</span><span class="sxs-lookup"><span data-stu-id="fc0c6-125">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0c6-126">-DefaultProfile</span></span>
<span data-ttu-id="fc0c6-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc0c6-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc0c6-128">-InputObject</span></span>
<span data-ttu-id="fc0c6-129">Az adatbázis-objektum, amelyről biztonsági másolatot készít.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-129">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fc0c6-130">-InstanceName</span></span>
<span data-ttu-id="fc0c6-131">Annak a felügyelt példánynak a neve, amely alatt a biztonsági másolatok vannak.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-132">-Location</span><span class="sxs-lookup"><span data-stu-id="fc0c6-132">-Location</span></span>
<span data-ttu-id="fc0c6-133">A biztonsági másolatok forrás felügyelt példányának helye.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="fc0c6-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="fc0c6-135">Függetlenül attól, hogy adatbázisonként a legújabb biztonsági másolatot kell-e készíteni.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="fc0c6-136">Alapértelmezés szerint hamis.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-136">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc0c6-137">-ResourceGroupName</span></span>
<span data-ttu-id="fc0c6-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc0c6-139">-ResourceId</span></span>
<span data-ttu-id="fc0c6-140">Az adatbázis erőforrás-azonosítója, amelyről biztonsági másolatot készít.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc0c6-141">-Confirm</span></span>
<span data-ttu-id="fc0c6-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc0c6-143">-WhatIf</span></span>
<span data-ttu-id="fc0c6-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc0c6-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc0c6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0c6-146">CommonParameters</span></span>
<span data-ttu-id="fc0c6-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc0c6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0c6-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc0c6-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0c6-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc0c6-149">INPUTS</span></span>

### <span data-ttu-id="fc0c6-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fc0c6-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="fc0c6-151">System.String</span><span class="sxs-lookup"><span data-stu-id="fc0c6-151">System.String</span></span>

## <span data-ttu-id="fc0c6-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc0c6-152">OUTPUTS</span></span>

### <span data-ttu-id="fc0c6-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="fc0c6-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="fc0c6-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc0c6-154">NOTES</span></span>

## <span data-ttu-id="fc0c6-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc0c6-155">RELATED LINKS</span></span>

[<span data-ttu-id="fc0c6-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fc0c6-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="fc0c6-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fc0c6-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fc0c6-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fc0c6-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fc0c6-159">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fc0c6-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)