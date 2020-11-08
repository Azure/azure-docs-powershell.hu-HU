---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 9408e51cfcdab3cd2c82617ee7f8cb9bc7d3918a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014276"
---
# <span data-ttu-id="fe602-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fe602-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="fe602-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe602-102">SYNOPSIS</span></span>
<span data-ttu-id="fe602-103">Hosszú távú adatmegőrzési biztonsági másolat (oka) t kap.</span><span class="sxs-lookup"><span data-stu-id="fe602-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="fe602-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe602-104">SYNTAX</span></span>

### <span data-ttu-id="fe602-105">Hely (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe602-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe602-106">Példánynév</span><span class="sxs-lookup"><span data-stu-id="fe602-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe602-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe602-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe602-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="fe602-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe602-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe602-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe602-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe602-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe602-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe602-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe602-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe602-112">DESCRIPTION</span></span>
<span data-ttu-id="fe602-113">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="fe602-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="fe602-114">Példák</span><span class="sxs-lookup"><span data-stu-id="fe602-114">EXAMPLES</span></span>

### <span data-ttu-id="fe602-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fe602-115">Example 1</span></span>
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

<span data-ttu-id="fe602-116">Az adott adatbázis hosszú távú adatmegőrzési biztonsági másolatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fe602-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="fe602-117">Az erőforráscsoport nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fe602-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="fe602-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe602-118">PARAMETERS</span></span>

### <span data-ttu-id="fe602-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="fe602-119">-BackupName</span></span>
<span data-ttu-id="fe602-120">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="fe602-120">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe602-121">-DatabaseName</span></span>
<span data-ttu-id="fe602-122">Annak a felügyelt adatbázisnak a neve, amely a biztonsági másolatokat adja.</span><span class="sxs-lookup"><span data-stu-id="fe602-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="fe602-123">-DatabaseState</span></span>
<span data-ttu-id="fe602-124">Annak az adatbázisnak az állapota, amelynek biztonsági másolatait meg szeretné keresni, élve, törölt vagy mindet.</span><span class="sxs-lookup"><span data-stu-id="fe602-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="fe602-125">Alapértékek mind</span><span class="sxs-lookup"><span data-stu-id="fe602-125">Defaults to All</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe602-126">-DefaultProfile</span></span>
<span data-ttu-id="fe602-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe602-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe602-128">-InputObject</span></span>
<span data-ttu-id="fe602-129">Az adatbázis-objektum, amelyhez biztonsági másolatot kap.</span><span class="sxs-lookup"><span data-stu-id="fe602-129">The database object to get backups for.</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-130">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="fe602-130">-InstanceName</span></span>
<span data-ttu-id="fe602-131">Annak a felügyelt példánynak a neve, amelyen a biztonsági másolatok szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="fe602-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="fe602-132">-Location</span></span>
<span data-ttu-id="fe602-133">A biztonsági másolatok forrásként kezelt példányának helye.</span><span class="sxs-lookup"><span data-stu-id="fe602-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="fe602-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="fe602-135">Szeretné-e, hogy csak az adatbázis legújabb biztonsági másolatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fe602-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="fe602-136">Az alapértelmezett érték a false.</span><span class="sxs-lookup"><span data-stu-id="fe602-136">Defaults to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe602-137">-ResourceGroupName</span></span>
<span data-ttu-id="fe602-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fe602-138">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe602-139">-ResourceId</span></span>
<span data-ttu-id="fe602-140">Az adatbázis-erőforrás azonosítója, amellyel biztonsági másolatot kaphat.</span><span class="sxs-lookup"><span data-stu-id="fe602-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe602-141">-Confirm</span></span>
<span data-ttu-id="fe602-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe602-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe602-143">-WhatIf</span></span>
<span data-ttu-id="fe602-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe602-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe602-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe602-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe602-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe602-146">CommonParameters</span></span>
<span data-ttu-id="fe602-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe602-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe602-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fe602-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe602-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe602-149">INPUTS</span></span>

### <span data-ttu-id="fe602-150">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fe602-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="fe602-151">System. String</span><span class="sxs-lookup"><span data-stu-id="fe602-151">System.String</span></span>

## <span data-ttu-id="fe602-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe602-152">OUTPUTS</span></span>

### <span data-ttu-id="fe602-153">Microsoft. Azure. Command. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="fe602-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="fe602-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe602-154">NOTES</span></span>

## <span data-ttu-id="fe602-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe602-155">RELATED LINKS</span></span>

[<span data-ttu-id="fe602-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fe602-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="fe602-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe602-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fe602-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe602-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fe602-159">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="fe602-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)