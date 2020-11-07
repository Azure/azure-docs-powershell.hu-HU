---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: 3db29e4ab0f2ab4afc9a3c29ef8ea0335ed5d528
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839472"
---
# <span data-ttu-id="ee614-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ee614-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="ee614-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee614-102">SYNOPSIS</span></span>
<span data-ttu-id="ee614-103">Információt ad az Azure SQL Managed instance Database redundáns biztonsági másolatról.</span><span class="sxs-lookup"><span data-stu-id="ee614-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="ee614-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee614-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee614-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee614-105">DESCRIPTION</span></span>
<span data-ttu-id="ee614-106">A **Get-AzSqlInstanceDatabaseGeoBackup** parancsmag egy vagy több Azure SQL-adatbázisból redundáns biztonsági mentést kap egy Azure SQL-adatbázisból felügyelt példányról.</span><span class="sxs-lookup"><span data-stu-id="ee614-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="ee614-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee614-107">EXAMPLES</span></span>

### <span data-ttu-id="ee614-108">Példa 1: az adatbázis redundáns biztonsági mentése példányban</span><span class="sxs-lookup"><span data-stu-id="ee614-108">Example 1: Get all database redundant backups on a instance</span></span>
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

<span data-ttu-id="ee614-109">Ez a parancs a managedInstance1 nevű példányban minden redundáns biztonsági mentést kap.</span><span class="sxs-lookup"><span data-stu-id="ee614-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="ee614-110">2. példa: az adatbázis redundáns biztonsági másolatának beszerzése név alapján egy felügyelt példányon</span><span class="sxs-lookup"><span data-stu-id="ee614-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="ee614-111">Ez a parancs a managedDatabase1 nevű adatbázis redundáns biztonsági másolatát egy managedInstance1 nevű példányból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ee614-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="ee614-112">3. példa: az adatbázis redundáns biztonsági másolatának beszerzése szűréssel</span><span class="sxs-lookup"><span data-stu-id="ee614-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
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

<span data-ttu-id="ee614-113">Ez a parancs minden olyan redundáns biztonsági másolatot kap, amely a managedInstance1 nevű példányban a "managedDatabase" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="ee614-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="ee614-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee614-114">PARAMETERS</span></span>

### <span data-ttu-id="ee614-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee614-115">-DefaultProfile</span></span>
<span data-ttu-id="ee614-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee614-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee614-117">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="ee614-117">-InstanceName</span></span>
<span data-ttu-id="ee614-118">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="ee614-118">The name of the instance.</span></span>

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

### <span data-ttu-id="ee614-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee614-119">-Name</span></span>
<span data-ttu-id="ee614-120">A lekérdezni kívánt példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ee614-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ee614-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee614-121">-ResourceGroupName</span></span>
<span data-ttu-id="ee614-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee614-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ee614-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee614-123">CommonParameters</span></span>
<span data-ttu-id="ee614-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee614-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee614-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ee614-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee614-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee614-126">INPUTS</span></span>

### <span data-ttu-id="ee614-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee614-127">None</span></span>

## <span data-ttu-id="ee614-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee614-128">OUTPUTS</span></span>

### <span data-ttu-id="ee614-129">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ee614-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="ee614-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee614-130">NOTES</span></span>

## <span data-ttu-id="ee614-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee614-131">RELATED LINKS</span></span>
