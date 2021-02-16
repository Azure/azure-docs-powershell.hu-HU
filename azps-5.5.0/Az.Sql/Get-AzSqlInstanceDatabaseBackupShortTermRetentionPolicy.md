---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165802"
---
# <span data-ttu-id="77cc9-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="77cc9-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="77cc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="77cc9-103">Biztonsági másolatot kap rövid távú adatmegőrzési házirendről.</span><span class="sxs-lookup"><span data-stu-id="77cc9-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="77cc9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77cc9-104">SYNTAX</span></span>

### <span data-ttu-id="77cc9-105">PolicyByResourceInstanceDatabaseSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77cc9-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77cc9-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="77cc9-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77cc9-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="77cc9-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77cc9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77cc9-108">DESCRIPTION</span></span>
<span data-ttu-id="77cc9-109">A **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy parancsmag** megkapja az adatbázishoz regisztrált rövid távú adatmegőrzési házirendet.</span><span class="sxs-lookup"><span data-stu-id="77cc9-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="77cc9-110">A házirend az időkorrekciós biztonsági másolatok megőrzési ideje napokban.</span><span class="sxs-lookup"><span data-stu-id="77cc9-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="77cc9-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77cc9-111">EXAMPLES</span></span>

### <span data-ttu-id="77cc9-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="77cc9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="77cc9-113">Ez a parancs az adatbázis01 rövid távú adatmegőrzési házirendje.</span><span class="sxs-lookup"><span data-stu-id="77cc9-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="77cc9-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="77cc9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="77cc9-115">Ez a parancs az adatbázis01 rövid távú adatmegőrzési házirendét kapja meg egy adatbázis-objektum pipázásával.</span><span class="sxs-lookup"><span data-stu-id="77cc9-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="77cc9-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="77cc9-116">Example 3</span></span>
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

<span data-ttu-id="77cc9-117">Ez a parancs az adatbázis01 nevű törölt adatbázisokra vonatkozó rövid távú adatmegőrzési házirendet egy törölt adatbázis-objektum pipázásával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="77cc9-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="77cc9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77cc9-118">PARAMETERS</span></span>

### <span data-ttu-id="77cc9-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="77cc9-119">-DatabaseName</span></span>
<span data-ttu-id="77cc9-120">Annak az Azure SQL Instance Databasenek a neve, amelyről lekérhető a biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="77cc9-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="77cc9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77cc9-121">-DefaultProfile</span></span>
<span data-ttu-id="77cc9-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77cc9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77cc9-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="77cc9-123">-DeletionDate</span></span>
<span data-ttu-id="77cc9-124">Az Azure SQL Instance Database törlési dátuma a biztonsági másolatok beolvasásához ezredmásodperc pontossággal (például 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="77cc9-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="77cc9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77cc9-125">-InputObject</span></span>
<span data-ttu-id="77cc9-126">Az élő vagy törölt adatbázis-objektum, amelyhez be kell szerezni/be kell állítani a házirendet.</span><span class="sxs-lookup"><span data-stu-id="77cc9-126">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="77cc9-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="77cc9-127">-InstanceName</span></span>
<span data-ttu-id="77cc9-128">Annak az Azure SQL Managed Instance-példánynak a neve, amelyben az adatbázis van.</span><span class="sxs-lookup"><span data-stu-id="77cc9-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="77cc9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77cc9-129">-ResourceGroupName</span></span>
<span data-ttu-id="77cc9-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="77cc9-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="77cc9-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77cc9-131">-ResourceId</span></span>
<span data-ttu-id="77cc9-132">A rövid távú adatmegőrzési házirend erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="77cc9-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="77cc9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77cc9-133">CommonParameters</span></span>
<span data-ttu-id="77cc9-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77cc9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77cc9-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77cc9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77cc9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77cc9-136">INPUTS</span></span>

### <span data-ttu-id="77cc9-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="77cc9-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="77cc9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="77cc9-138">System.String</span></span>

## <span data-ttu-id="77cc9-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77cc9-139">OUTPUTS</span></span>

### <span data-ttu-id="77cc9-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="77cc9-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="77cc9-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77cc9-141">NOTES</span></span>

## <span data-ttu-id="77cc9-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77cc9-142">RELATED LINKS</span></span>
