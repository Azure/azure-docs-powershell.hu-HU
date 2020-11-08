---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181313"
---
# <span data-ttu-id="d7be2-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d7be2-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="d7be2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7be2-102">SYNOPSIS</span></span>
<span data-ttu-id="d7be2-103">Hosszú távú adatmegőrzési biztonsági másolat törlése</span><span class="sxs-lookup"><span data-stu-id="d7be2-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="d7be2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7be2-104">SYNTAX</span></span>

### <span data-ttu-id="d7be2-105">RemoveBackupDefault (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7be2-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7be2-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7be2-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7be2-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7be2-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7be2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7be2-108">DESCRIPTION</span></span>
<span data-ttu-id="d7be2-109">A **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** parancsmag törli a megadott biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="d7be2-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="d7be2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d7be2-110">EXAMPLES</span></span>

### <span data-ttu-id="d7be2-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d7be2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="d7be2-112">Törli a biztonsági másolatot a név 15be823c-7e2c-49d8-819f-a3fdcad92215; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="d7be2-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="d7be2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7be2-113">PARAMETERS</span></span>

### <span data-ttu-id="d7be2-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="d7be2-114">-BackupName</span></span>
<span data-ttu-id="d7be2-115">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="d7be2-115">The name of the backup.</span></span>

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

### <span data-ttu-id="d7be2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7be2-116">-DatabaseName</span></span>
<span data-ttu-id="d7be2-117">Annak a felügyelt adatbázisnak a neve, amelyből a biztonsági másolat származik.</span><span class="sxs-lookup"><span data-stu-id="d7be2-117">The name of the Managed Database the backup is from.</span></span>

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

### <span data-ttu-id="d7be2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7be2-118">-DefaultProfile</span></span>
<span data-ttu-id="d7be2-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7be2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7be2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d7be2-120">-Force</span></span>
<span data-ttu-id="d7be2-121">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="d7be2-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d7be2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7be2-122">-InputObject</span></span>
<span data-ttu-id="d7be2-123">Az adatbázis hosszú távú adatmegőrzési objektuma eltávolításra készül.</span><span class="sxs-lookup"><span data-stu-id="d7be2-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7be2-124">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="d7be2-124">-InstanceName</span></span>
<span data-ttu-id="d7be2-125">Annak a felügyelt példánynak a neve, amelyben a biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="d7be2-125">The name of the Managed Instance the backup is under.</span></span>

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

### <span data-ttu-id="d7be2-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="d7be2-126">-Location</span></span>
<span data-ttu-id="d7be2-127">A biztonsági másolatok forrásként kezelt példányának helye.</span><span class="sxs-lookup"><span data-stu-id="d7be2-127">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="d7be2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7be2-128">-ResourceGroupName</span></span>
<span data-ttu-id="d7be2-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d7be2-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7be2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7be2-130">-ResourceId</span></span>
<span data-ttu-id="d7be2-131">Az adatbázis hosszú távú adatmegőrzési biztonsági másolatának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d7be2-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="d7be2-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7be2-132">-Confirm</span></span>
<span data-ttu-id="d7be2-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7be2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7be2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7be2-134">-WhatIf</span></span>
<span data-ttu-id="d7be2-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7be2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7be2-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7be2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7be2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7be2-137">CommonParameters</span></span>
<span data-ttu-id="d7be2-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7be2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7be2-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d7be2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7be2-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7be2-140">INPUTS</span></span>

### <span data-ttu-id="d7be2-141">Microsoft. Azure. Command. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="d7be2-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="d7be2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d7be2-142">System.String</span></span>

## <span data-ttu-id="d7be2-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7be2-143">OUTPUTS</span></span>

### <span data-ttu-id="d7be2-144">Microsoft. Azure. Command. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="d7be2-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="d7be2-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7be2-145">NOTES</span></span>

## <span data-ttu-id="d7be2-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7be2-146">RELATED LINKS</span></span>

[<span data-ttu-id="d7be2-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d7be2-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d7be2-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d7be2-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d7be2-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d7be2-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d7be2-150">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d7be2-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)