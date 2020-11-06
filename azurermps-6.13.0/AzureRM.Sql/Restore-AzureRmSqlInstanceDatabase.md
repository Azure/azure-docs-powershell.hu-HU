---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 61fe76eba8d1f8faf0ab45d0a24f56a8dabf3641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504264"
---
# <span data-ttu-id="e5668-101">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e5668-101">Restore-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="e5668-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5668-102">SYNOPSIS</span></span>
<span data-ttu-id="e5668-103">Visszaállít egy Azure SQL Managed instance-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="e5668-103">Restores an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5668-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5668-104">SYNTAX</span></span>

### <span data-ttu-id="e5668-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5668-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5668-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e5668-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5668-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e5668-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5668-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="e5668-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5668-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e5668-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5668-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e5668-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5668-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5668-111">DESCRIPTION</span></span>
<span data-ttu-id="e5668-112">A **Restore-AzureRmSqlInstanceDatabase** parancsmag egy példány adatbázisát egy időben visszaállítja egy aktív adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="e5668-112">The **Restore-AzureRmSqlInstanceDatabase** cmdlet restores an instance database from a point in time in a live database.</span></span>
<span data-ttu-id="e5668-113">A helyreállított adatbázis új példány adatbázisként jön létre.</span><span class="sxs-lookup"><span data-stu-id="e5668-113">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="e5668-114">Példák</span><span class="sxs-lookup"><span data-stu-id="e5668-114">EXAMPLES</span></span>

### <span data-ttu-id="e5668-115">Példa 1: példány adatbázisának visszaállítása időpontból</span><span class="sxs-lookup"><span data-stu-id="e5668-115">Example 1: Restore a instance database from a point in time</span></span>
```
PS C:\> Restore-AzureRmSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="e5668-116">A parancs visszaállítja a példány-adatbázis Database01 a megadott időpontos biztonsági másolatból az Database01_restored nevű adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="e5668-116">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="e5668-117">2. példa: a példányok adatbázisának visszaállítása az időpontból a különböző erőforráscsoport egy másik példányával</span><span class="sxs-lookup"><span data-stu-id="e5668-117">Example 2: Restore a instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="e5668-118">A parancs visszaállítja a példány-adatbázis Database01 a példány managedInstance1 az erőforráscsoport ResourceGroup01, a megadott időpontos biztonsági másolatról a példány-adatbázisra, amelyet az Database01_restored példánya nevű adatbázishoz (például managedInstance2 az erőforráscsoport ResourceGroup02).</span><span class="sxs-lookup"><span data-stu-id="e5668-118">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

## <span data-ttu-id="e5668-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5668-119">PARAMETERS</span></span>

### <span data-ttu-id="e5668-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5668-120">-AsJob</span></span>
<span data-ttu-id="e5668-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e5668-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5668-122">-DefaultProfile</span></span>
<span data-ttu-id="e5668-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5668-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-124">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="e5668-124">-FromPointInTimeBackup</span></span>
<span data-ttu-id="e5668-125">Visszaállítás egy időpontos biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="e5668-125">Restore from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5668-126">-InputObject</span></span>
<span data-ttu-id="e5668-127">A példány adatbázis-objektum visszaállítása</span><span class="sxs-lookup"><span data-stu-id="e5668-127">The Instance Database object to restore</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-128">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="e5668-128">-InstanceName</span></span>
<span data-ttu-id="e5668-129">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="e5668-129">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5668-130">-Name</span></span>
<span data-ttu-id="e5668-131">A példány adatbázisának neve a visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="e5668-131">The instance database name to restore.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="e5668-132">-PointInTime</span></span>
<span data-ttu-id="e5668-133">A pontos idő az adatbázis visszaállításához.</span><span class="sxs-lookup"><span data-stu-id="e5668-133">The point in time to restore the database to.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5668-134">-ResourceGroupName</span></span>
<span data-ttu-id="e5668-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e5668-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5668-136">-ResourceId</span></span>
<span data-ttu-id="e5668-137">A Restore példány adatbázis-objektumának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e5668-137">The resource id of Instance Database object to restore</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-138">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e5668-138">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="e5668-139">Annak a célnak az adatbázisnak a neve, amelyet vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="e5668-139">The name of the target instance database to restore to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-140">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="e5668-140">-TargetInstanceName</span></span>
<span data-ttu-id="e5668-141">Annak a TARGET-példánynak a neve, amelybe vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="e5668-141">The name of the target instance to restore to.</span></span>
<span data-ttu-id="e5668-142">Ha nincs megadva, a cél példány megegyezik a forrás példánytal.</span><span class="sxs-lookup"><span data-stu-id="e5668-142">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-143">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5668-143">-TargetResourceGroupName</span></span>
<span data-ttu-id="e5668-144">Annak a cél erőforrás-csoportnak a neve, amelybe vissza szeretne állítani.</span><span class="sxs-lookup"><span data-stu-id="e5668-144">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="e5668-145">Ha nem adja meg, a cél erőforráscsoport megegyezik a forrás erőforrás csoporttal.</span><span class="sxs-lookup"><span data-stu-id="e5668-145">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5668-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5668-146">-Confirm</span></span>
<span data-ttu-id="e5668-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5668-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5668-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5668-148">-WhatIf</span></span>
<span data-ttu-id="e5668-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5668-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5668-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5668-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5668-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5668-151">CommonParameters</span></span>
<span data-ttu-id="e5668-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5668-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5668-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5668-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5668-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5668-154">INPUTS</span></span>

### <span data-ttu-id="e5668-155">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e5668-155">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="e5668-156">System. String</span><span class="sxs-lookup"><span data-stu-id="e5668-156">System.String</span></span>

## <span data-ttu-id="e5668-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5668-157">OUTPUTS</span></span>

### <span data-ttu-id="e5668-158">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e5668-158">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e5668-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5668-159">NOTES</span></span>

## <span data-ttu-id="e5668-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5668-160">RELATED LINKS</span></span>
