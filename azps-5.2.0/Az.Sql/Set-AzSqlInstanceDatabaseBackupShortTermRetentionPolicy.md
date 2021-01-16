---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 93c4c5c1fa269414b80001f9fd24f1a79c5ed4de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332057"
---
# <span data-ttu-id="3e825-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3e825-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="3e825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e825-102">SYNOPSIS</span></span>
<span data-ttu-id="3e825-103">Biztonsági másolatot készít rövid távú adatmegőrzési házirendről.</span><span class="sxs-lookup"><span data-stu-id="3e825-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="3e825-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e825-104">SYNTAX</span></span>

### <span data-ttu-id="3e825-105">PolicyByResourceInstanceDatabaseSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e825-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e825-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3e825-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e825-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3e825-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e825-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e825-108">DESCRIPTION</span></span>
<span data-ttu-id="3e825-109">A **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** parancsmag megkapja az adatbázishoz regisztrált rövid távú adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="3e825-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="3e825-110">A házirend az időkorrekciós biztonsági másolatok megőrzési ideje napokban.</span><span class="sxs-lookup"><span data-stu-id="3e825-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="3e825-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e825-111">EXAMPLES</span></span>

### <span data-ttu-id="3e825-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3e825-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="3e825-113">Ez a parancs 35 napra állítja be az adatbázis01 rövid távú adatmegőrzési házirendját.</span><span class="sxs-lookup"><span data-stu-id="3e825-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="3e825-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3e825-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="3e825-115">Ez a parancs egy adatbázis-objektum pipázásával 35 napra állítja be az adatbázis01 rövid távú adatmegőrzési házirendét.</span><span class="sxs-lookup"><span data-stu-id="3e825-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="3e825-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="3e825-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="3e825-117">Ez a parancs beállítja a rövid távú adatmegőrzési házirendet minden DB1 nevű törölt adatbázisra egy törölt adatbázis-objektum pipázásával.</span><span class="sxs-lookup"><span data-stu-id="3e825-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="3e825-118">Megjegyzés: A törölt adatbázisok adatmegőrzési ideje csak csökkenthető.</span><span class="sxs-lookup"><span data-stu-id="3e825-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="3e825-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e825-119">PARAMETERS</span></span>

### <span data-ttu-id="3e825-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e825-120">-DatabaseName</span></span>
<span data-ttu-id="3e825-121">Annak az Azure SQL Instance Databasenek a neve, amelyről a biztonsági másolatok lekérhetők.</span><span class="sxs-lookup"><span data-stu-id="3e825-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e825-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e825-122">-DefaultProfile</span></span>
<span data-ttu-id="3e825-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e825-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e825-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="3e825-124">-DeletionDate</span></span>
<span data-ttu-id="3e825-125">Az Azure SQL Instance Database törlési dátuma a biztonsági másolatok beolvasásához ezredmásodperc pontossággal (például 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="3e825-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e825-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e825-126">-InputObject</span></span>
<span data-ttu-id="3e825-127">Az élő vagy törölt adatbázis-objektum, amelyhez be kell szerezni/be kell állítani a házirendet.</span><span class="sxs-lookup"><span data-stu-id="3e825-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e825-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3e825-128">-InstanceName</span></span>
<span data-ttu-id="3e825-129">Annak az Azure SQL Felügyelt példánynak a neve, amelyben az adatbázis van.</span><span class="sxs-lookup"><span data-stu-id="3e825-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e825-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e825-130">-ResourceGroupName</span></span>
<span data-ttu-id="3e825-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e825-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e825-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e825-132">-ResourceId</span></span>
<span data-ttu-id="3e825-133">A rövid távú adatmegőrzési házirend erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3e825-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e825-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="3e825-134">-RetentionDays</span></span>
<span data-ttu-id="3e825-135">Több nap biztonsági mentés.</span><span class="sxs-lookup"><span data-stu-id="3e825-135">Days of backup retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e825-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e825-136">-Confirm</span></span>
<span data-ttu-id="3e825-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3e825-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e825-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e825-138">-WhatIf</span></span>
<span data-ttu-id="3e825-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3e825-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e825-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e825-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e825-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e825-141">CommonParameters</span></span>
<span data-ttu-id="3e825-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e825-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e825-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e825-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e825-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e825-144">INPUTS</span></span>

### <span data-ttu-id="3e825-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3e825-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="3e825-146">System.String</span><span class="sxs-lookup"><span data-stu-id="3e825-146">System.String</span></span>

## <span data-ttu-id="3e825-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e825-147">OUTPUTS</span></span>

### <span data-ttu-id="3e825-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3e825-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="3e825-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e825-149">NOTES</span></span>

## <span data-ttu-id="3e825-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e825-150">RELATED LINKS</span></span>
