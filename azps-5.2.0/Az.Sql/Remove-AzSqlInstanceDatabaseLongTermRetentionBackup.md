---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369611"
---
# <span data-ttu-id="2a1fe-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2a1fe-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="2a1fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="2a1fe-103">Törli a hosszú távú adatmegőrzési biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="2a1fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2a1fe-104">SYNTAX</span></span>

### <span data-ttu-id="2a1fe-105">RemoveBackupDefault (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a1fe-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a1fe-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a1fe-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a1fe-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a1fe-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a1fe-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2a1fe-108">DESCRIPTION</span></span>
<span data-ttu-id="2a1fe-109">A **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** parancsmag törli a megadott biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="2a1fe-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2a1fe-110">EXAMPLES</span></span>

### <span data-ttu-id="2a1fe-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2a1fe-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="2a1fe-112">A 15be823c-7e2c-49d8-819f-a3fdcad92215;1322682505500000000 név törlése</span><span class="sxs-lookup"><span data-stu-id="2a1fe-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="2a1fe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a1fe-113">PARAMETERS</span></span>

### <span data-ttu-id="2a1fe-114">-BackupName</span><span class="sxs-lookup"><span data-stu-id="2a1fe-114">-BackupName</span></span>
<span data-ttu-id="2a1fe-115">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-115">The name of the backup.</span></span>

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

### <span data-ttu-id="2a1fe-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a1fe-116">-DatabaseName</span></span>
<span data-ttu-id="2a1fe-117">Annak a felügyelt adatbázisnak a neve, amelyből a biztonsági másolat jött létre.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-117">The name of the Managed Database the backup is from.</span></span>

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

### <span data-ttu-id="2a1fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a1fe-118">-DefaultProfile</span></span>
<span data-ttu-id="2a1fe-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a1fe-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2a1fe-120">-Force</span></span>
<span data-ttu-id="2a1fe-121">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="2a1fe-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2a1fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a1fe-122">-InputObject</span></span>
<span data-ttu-id="2a1fe-123">Az eltávolítható Adatbázis hosszú távú adatmegőrzési biztonsági másolat objektuma.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-123">The Database Long Term Retention Backup object to remove.</span></span>

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

### <span data-ttu-id="2a1fe-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2a1fe-124">-InstanceName</span></span>
<span data-ttu-id="2a1fe-125">Annak a felügyelt példánynak a neve, amely alatt a biztonsági másolat van.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-125">The name of the Managed Instance the backup is under.</span></span>

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

### <span data-ttu-id="2a1fe-126">-Location</span><span class="sxs-lookup"><span data-stu-id="2a1fe-126">-Location</span></span>
<span data-ttu-id="2a1fe-127">A biztonsági másolatok forrás felügyelt példányának helye.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-127">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="2a1fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a1fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="2a1fe-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a1fe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a1fe-130">-ResourceId</span></span>
<span data-ttu-id="2a1fe-131">Az adatbázis hosszú távú adatmegőrzési biztonsági másolatának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="2a1fe-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a1fe-132">-Confirm</span></span>
<span data-ttu-id="2a1fe-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a1fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a1fe-134">-WhatIf</span></span>
<span data-ttu-id="2a1fe-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a1fe-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a1fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a1fe-137">CommonParameters</span></span>
<span data-ttu-id="2a1fe-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a1fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a1fe-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a1fe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a1fe-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a1fe-140">INPUTS</span></span>

### <span data-ttu-id="2a1fe-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="2a1fe-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="2a1fe-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2a1fe-142">System.String</span></span>

## <span data-ttu-id="2a1fe-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a1fe-143">OUTPUTS</span></span>

### <span data-ttu-id="2a1fe-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="2a1fe-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="2a1fe-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2a1fe-145">NOTES</span></span>

## <span data-ttu-id="2a1fe-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a1fe-146">RELATED LINKS</span></span>

[<span data-ttu-id="2a1fe-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2a1fe-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2a1fe-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2a1fe-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2a1fe-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2a1fe-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2a1fe-150">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2a1fe-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)