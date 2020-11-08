---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd57b5d6e4301b1ab22b041367388d37986a946e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188165"
---
# <span data-ttu-id="26755-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="26755-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="26755-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26755-102">SYNOPSIS</span></span>
<span data-ttu-id="26755-103">Információt ad az Azure SQL Managed instance Database redundáns biztonsági másolatról.</span><span class="sxs-lookup"><span data-stu-id="26755-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="26755-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26755-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26755-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26755-105">DESCRIPTION</span></span>
<span data-ttu-id="26755-106">A **Get-AzSqlInstanceDatabaseGeoBackup** parancsmag egy vagy több Azure SQL-adatbázisból redundáns biztonsági mentést kap egy Azure SQL-adatbázisból felügyelt példányról.</span><span class="sxs-lookup"><span data-stu-id="26755-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="26755-107">Példák</span><span class="sxs-lookup"><span data-stu-id="26755-107">EXAMPLES</span></span>

### <span data-ttu-id="26755-108">Példa 1: az adatbázis redundáns biztonsági mentése példányban</span><span class="sxs-lookup"><span data-stu-id="26755-108">Example 1: Get all database redundant backups on a instance</span></span>
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

<span data-ttu-id="26755-109">Ez a parancs a managedInstance1 nevű példányban minden redundáns biztonsági mentést kap.</span><span class="sxs-lookup"><span data-stu-id="26755-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="26755-110">2. példa: az adatbázis redundáns biztonsági másolatának beszerzése név alapján egy felügyelt példányon</span><span class="sxs-lookup"><span data-stu-id="26755-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="26755-111">Ez a parancs a managedDatabase1 nevű adatbázis redundáns biztonsági másolatát egy managedInstance1 nevű példányból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="26755-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="26755-112">3. példa: az adatbázis redundáns biztonsági másolatának beszerzése szűréssel</span><span class="sxs-lookup"><span data-stu-id="26755-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
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

<span data-ttu-id="26755-113">Ez a parancs minden olyan redundáns biztonsági másolatot kap, amely a managedInstance1 nevű példányban a "managedDatabase" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="26755-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="26755-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26755-114">PARAMETERS</span></span>

### <span data-ttu-id="26755-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26755-115">-DefaultProfile</span></span>
<span data-ttu-id="26755-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26755-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26755-117">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="26755-117">-InstanceName</span></span>
<span data-ttu-id="26755-118">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="26755-118">The name of the instance.</span></span>

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

### <span data-ttu-id="26755-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26755-119">-Name</span></span>
<span data-ttu-id="26755-120">A lekérdezni kívánt példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="26755-120">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="26755-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26755-121">-ResourceGroupName</span></span>
<span data-ttu-id="26755-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="26755-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="26755-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26755-123">CommonParameters</span></span>
<span data-ttu-id="26755-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26755-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26755-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="26755-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26755-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26755-126">INPUTS</span></span>

### <span data-ttu-id="26755-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="26755-127">None</span></span>

## <span data-ttu-id="26755-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26755-128">OUTPUTS</span></span>

### <span data-ttu-id="26755-129">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="26755-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="26755-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26755-130">NOTES</span></span>

## <span data-ttu-id="26755-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26755-131">RELATED LINKS</span></span>
