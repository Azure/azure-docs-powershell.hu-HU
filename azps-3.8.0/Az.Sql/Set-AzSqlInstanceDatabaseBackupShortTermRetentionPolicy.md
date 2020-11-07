---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 1673bd38b3b7694a1eef362da86da9e7e016d135
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846574"
---
# <span data-ttu-id="af4e6-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="af4e6-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="af4e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af4e6-102">SYNOPSIS</span></span>
<span data-ttu-id="af4e6-103">Biztonsági rövid távú adatmegőrzési házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="af4e6-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="af4e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af4e6-104">SYNTAX</span></span>

### <span data-ttu-id="af4e6-105">PolicyByResourceInstanceDatabaseSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af4e6-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af4e6-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="af4e6-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af4e6-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="af4e6-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af4e6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="af4e6-108">DESCRIPTION</span></span>
<span data-ttu-id="af4e6-109">A **set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** parancsmag az adatbázishoz regisztrált rövid távú adatmegőrzési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="af4e6-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="af4e6-110">A házirend az adatmegőrzési időszak napokban, a visszaadott időpontos biztonsági másolatok esetében.</span><span class="sxs-lookup"><span data-stu-id="af4e6-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="af4e6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="af4e6-111">EXAMPLES</span></span>

### <span data-ttu-id="af4e6-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="af4e6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="af4e6-113">Ez a parancs a database01 rövid távú adatmegőrzési házirendjét állítja be a 35 napokra.</span><span class="sxs-lookup"><span data-stu-id="af4e6-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="af4e6-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="af4e6-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="af4e6-115">Ez a parancs a database01 rövid távú adatmegőrzési házirendjét állítja be egy adatbázis-objektumon keresztül az 35-ös napokra.</span><span class="sxs-lookup"><span data-stu-id="af4e6-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="af4e6-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="af4e6-116">Example 3</span></span>
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

<span data-ttu-id="af4e6-117">Ez a parancs a D1 keresztül egy törölt adatbázis-objektumban lévő összes törölt adatbázis rövid távú adatmegőrzési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="af4e6-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="af4e6-118">Megjegyzés: az adatmegőrzési időszakot csak a törölt adatbázisokban lehet csökkenteni.</span><span class="sxs-lookup"><span data-stu-id="af4e6-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="af4e6-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af4e6-119">PARAMETERS</span></span>

### <span data-ttu-id="af4e6-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af4e6-120">-DatabaseName</span></span>
<span data-ttu-id="af4e6-121">Az Azure SQL-példány adatbázisának neve a biztonsági másolatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="af4e6-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="af4e6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4e6-122">-DefaultProfile</span></span>
<span data-ttu-id="af4e6-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af4e6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af4e6-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="af4e6-124">-DeletionDate</span></span>
<span data-ttu-id="af4e6-125">Az Azure SQL-példány adatbázisának törlési dátuma a biztonsági másolatok (például 2016-02-23T00:22.847 Z) beolvasásához</span><span class="sxs-lookup"><span data-stu-id="af4e6-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="af4e6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af4e6-126">-InputObject</span></span>
<span data-ttu-id="af4e6-127">Az aktív vagy törölt adatbázis-objektum a házirend beolvasásához vagy beállításához.</span><span class="sxs-lookup"><span data-stu-id="af4e6-127">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="af4e6-128">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="af4e6-128">-InstanceName</span></span>
<span data-ttu-id="af4e6-129">Az adatbázisnak az Azure SQL-alapú felügyelt példányának neve.</span><span class="sxs-lookup"><span data-stu-id="af4e6-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="af4e6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4e6-130">-ResourceGroupName</span></span>
<span data-ttu-id="af4e6-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="af4e6-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="af4e6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af4e6-132">-ResourceId</span></span>
<span data-ttu-id="af4e6-133">A rövid távú adatmegőrzési házirend erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="af4e6-133">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="af4e6-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="af4e6-134">-RetentionDays</span></span>
<span data-ttu-id="af4e6-135">A biztonságimásolat-adatmegőrzési napok száma.</span><span class="sxs-lookup"><span data-stu-id="af4e6-135">Days of backup retention.</span></span>

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

### <span data-ttu-id="af4e6-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af4e6-136">-Confirm</span></span>
<span data-ttu-id="af4e6-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af4e6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af4e6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af4e6-138">-WhatIf</span></span>
<span data-ttu-id="af4e6-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af4e6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af4e6-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af4e6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af4e6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4e6-141">CommonParameters</span></span>
<span data-ttu-id="af4e6-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af4e6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4e6-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="af4e6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4e6-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af4e6-144">INPUTS</span></span>

### <span data-ttu-id="af4e6-145">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="af4e6-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="af4e6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="af4e6-146">System.String</span></span>

## <span data-ttu-id="af4e6-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af4e6-147">OUTPUTS</span></span>

### <span data-ttu-id="af4e6-148">Microsoft. Azure. Command. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="af4e6-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="af4e6-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af4e6-149">NOTES</span></span>

## <span data-ttu-id="af4e6-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af4e6-150">RELATED LINKS</span></span>
