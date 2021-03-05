---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd66238627c96d2b3b1a8aaa2ebc7e2505515d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999462"
---
# <span data-ttu-id="d7c44-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="d7c44-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="d7c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7c44-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c44-103">Az Azure SQL Felügyelt példány adatbázis redundáns biztonsági másolatának adatait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d7c44-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="d7c44-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7c44-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7c44-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7c44-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c44-106">A **Get-AzSqlInstanceDatabaseGeoBackup** parancsmag egy vagy több Azure SQL-adatbázisból redundáns biztonsági másolatot kap egy Azure SQL-adatbázis felügyelt példányából.</span><span class="sxs-lookup"><span data-stu-id="d7c44-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="d7c44-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7c44-107">EXAMPLES</span></span>

### <span data-ttu-id="d7c44-108">1. példa: Az összes adatbázis redundáns biztonsági mentése egy példányon</span><span class="sxs-lookup"><span data-stu-id="d7c44-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="d7c44-109">Ez a parancs az összes adatbázis redundáns biztonsági másolatát lekérte a managedInstance1 nevű példányról.</span><span class="sxs-lookup"><span data-stu-id="d7c44-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="d7c44-110">2. példa: Adatbázis redundáns biztonsági mentése név szerint felügyelt példányon</span><span class="sxs-lookup"><span data-stu-id="d7c44-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="d7c44-111">Ez a parancs egy felügyeltAdatbázis1 nevű adatbázis-redundáns biztonsági másolatot kap egy managedInstance1 nevű példányból.</span><span class="sxs-lookup"><span data-stu-id="d7c44-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="d7c44-112">3. példa: Az összes adatbázis redundáns biztonsági mentése egy példányon szűréssel</span><span class="sxs-lookup"><span data-stu-id="d7c44-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="d7c44-113">Ez a parancs minden olyan adatbázis-redundáns biztonsági másolatot kap a managedInstance1 példányról, amely a "managedDatabase" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="d7c44-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="d7c44-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7c44-114">PARAMETERS</span></span>

### <span data-ttu-id="d7c44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c44-115">-DefaultProfile</span></span>
<span data-ttu-id="d7c44-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7c44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7c44-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d7c44-117">-InstanceName</span></span>
<span data-ttu-id="d7c44-118">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="d7c44-118">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c44-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d7c44-119">-Name</span></span>
<span data-ttu-id="d7c44-120">A visszakeresni megfelelő példányadatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d7c44-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c44-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7c44-121">-ResourceGroupName</span></span>
<span data-ttu-id="d7c44-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d7c44-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c44-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c44-123">CommonParameters</span></span>
<span data-ttu-id="d7c44-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7c44-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c44-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7c44-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c44-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7c44-126">INPUTS</span></span>

### <span data-ttu-id="d7c44-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7c44-127">None</span></span>

## <span data-ttu-id="d7c44-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7c44-128">OUTPUTS</span></span>

### <span data-ttu-id="d7c44-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d7c44-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="d7c44-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7c44-130">NOTES</span></span>

## <span data-ttu-id="d7c44-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7c44-131">RELATED LINKS</span></span>
