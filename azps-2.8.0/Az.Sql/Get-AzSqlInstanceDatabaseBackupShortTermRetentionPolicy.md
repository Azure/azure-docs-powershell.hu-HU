---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: b93f9a4ffe0e77d464b1913207d0fd3bf7691699
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839190"
---
# <span data-ttu-id="9f145-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9f145-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="9f145-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f145-102">SYNOPSIS</span></span>
<span data-ttu-id="9f145-103">Rövid távú adatmegőrzési házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="9f145-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="9f145-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f145-104">SYNTAX</span></span>

### <span data-ttu-id="9f145-105">PolicyByResourceInstanceDatabaseSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f145-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f145-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9f145-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f145-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9f145-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f145-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f145-108">DESCRIPTION</span></span>
<span data-ttu-id="9f145-109">A **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** parancsmag az adatbázishoz regisztrált rövid távú adatmegőrzési házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9f145-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="9f145-110">A házirend az adatmegőrzési időszak napokban, a visszaadott időpontos biztonsági másolatok esetében.</span><span class="sxs-lookup"><span data-stu-id="9f145-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="9f145-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9f145-111">EXAMPLES</span></span>

### <span data-ttu-id="9f145-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9f145-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="9f145-113">Ez a parancs a database01 rövid távú adatmegőrzési házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9f145-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="9f145-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9f145-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="9f145-115">Ez a parancs beolvassa a database01 rövid távú adatmegőrzési házirendjét egy adatbázis-objektum csővezetékeken keresztül.</span><span class="sxs-lookup"><span data-stu-id="9f145-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="9f145-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="9f145-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="9f145-117">Ez a parancs beolvassa a rövid távú adatmegőrzési házirendet a database01-ban nevű törölt adatbázisokban egy törölt adatbázis-objektumon keresztül.</span><span class="sxs-lookup"><span data-stu-id="9f145-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="9f145-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f145-118">PARAMETERS</span></span>

### <span data-ttu-id="9f145-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9f145-119">-DatabaseName</span></span>
<span data-ttu-id="9f145-120">Az Azure SQL-példány adatbázisának neve a biztonsági másolatok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="9f145-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="9f145-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f145-121">-DefaultProfile</span></span>
<span data-ttu-id="9f145-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f145-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f145-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="9f145-123">-DeletionDate</span></span>
<span data-ttu-id="9f145-124">Az Azure SQL-példány adatbázisának törlési dátuma a biztonsági másolatok (például 2016-02-23T00:22.847 Z) beolvasásához</span><span class="sxs-lookup"><span data-stu-id="9f145-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="9f145-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f145-125">-InputObject</span></span>
<span data-ttu-id="9f145-126">Az aktív vagy törölt adatbázis-objektum a házirend beolvasásához vagy beállításához.</span><span class="sxs-lookup"><span data-stu-id="9f145-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f145-127">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="9f145-127">-InstanceName</span></span>
<span data-ttu-id="9f145-128">Az adatbázisnak az Azure SQL-alapú felügyelt példányának neve.</span><span class="sxs-lookup"><span data-stu-id="9f145-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="9f145-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f145-129">-ResourceGroupName</span></span>
<span data-ttu-id="9f145-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9f145-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f145-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f145-131">-ResourceId</span></span>
<span data-ttu-id="9f145-132">A rövid távú adatmegőrzési házirend erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9f145-132">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f145-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f145-133">CommonParameters</span></span>
<span data-ttu-id="9f145-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f145-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f145-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9f145-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f145-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f145-136">INPUTS</span></span>

### <span data-ttu-id="9f145-137">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="9f145-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="9f145-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9f145-138">System.String</span></span>

## <span data-ttu-id="9f145-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f145-139">OUTPUTS</span></span>

### <span data-ttu-id="9f145-140">Microsoft. Azure. Command. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9f145-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="9f145-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f145-141">NOTES</span></span>

## <span data-ttu-id="9f145-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f145-142">RELATED LINKS</span></span>
