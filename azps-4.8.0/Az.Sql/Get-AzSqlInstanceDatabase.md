---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183254"
---
# <span data-ttu-id="12705-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="12705-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="12705-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12705-102">SYNOPSIS</span></span>
<span data-ttu-id="12705-103">Információt ad az Azure SQL Managed instance adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="12705-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="12705-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12705-104">SYNTAX</span></span>

### <span data-ttu-id="12705-105">GetInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12705-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12705-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="12705-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12705-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="12705-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12705-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="12705-108">DESCRIPTION</span></span>
<span data-ttu-id="12705-109">A **Get-AzSqlInstanceDatabase** parancsmag egy vagy több Azure SQL-adatbázisból áll egy Azure SQL-adatbázis felügyelt példányával.</span><span class="sxs-lookup"><span data-stu-id="12705-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="12705-110">Példák</span><span class="sxs-lookup"><span data-stu-id="12705-110">EXAMPLES</span></span>

### <span data-ttu-id="12705-111">Példa 1: a példány minden adatbázisának beolvasása</span><span class="sxs-lookup"><span data-stu-id="12705-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="12705-112">Ez a parancs a managedInstance1 nevű példány minden adatbázisát bekapja.</span><span class="sxs-lookup"><span data-stu-id="12705-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="12705-113">2. példa: adatbázis beszerzése névvel egy felügyelt példányban</span><span class="sxs-lookup"><span data-stu-id="12705-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="12705-114">Ez a parancs a managedDatabase1 nevű adatbázist egy managedInstance1 nevű példányból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="12705-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="12705-115">3. példa: az összes adatbázis beolvasása szűréssel</span><span class="sxs-lookup"><span data-stu-id="12705-115">Example 3: Get all databases on a instance using filtering</span></span>
```
PS C:\> Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="12705-116">Ez a parancs a managedInstance1 nevű példány minden adatbázisát beolvassa, amely a "managedDatabase" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="12705-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="12705-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12705-117">PARAMETERS</span></span>

### <span data-ttu-id="12705-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12705-118">-DefaultProfile</span></span>
<span data-ttu-id="12705-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12705-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12705-120">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="12705-120">-InstanceName</span></span>
<span data-ttu-id="12705-121">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="12705-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12705-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="12705-122">-InstanceObject</span></span>
<span data-ttu-id="12705-123">A példány-adatbázis beszerzéséhez használandó objektum</span><span class="sxs-lookup"><span data-stu-id="12705-123">The instance object to use for getting instance database</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12705-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="12705-124">-InstanceResourceId</span></span>
<span data-ttu-id="12705-125">A beolvasott példány-objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="12705-125">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12705-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12705-126">-Name</span></span>
<span data-ttu-id="12705-127">A lekérdezni kívánt Azure SQL-példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="12705-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12705-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12705-128">-ResourceGroupName</span></span>
<span data-ttu-id="12705-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="12705-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12705-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12705-130">CommonParameters</span></span>
<span data-ttu-id="12705-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12705-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12705-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="12705-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12705-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12705-133">INPUTS</span></span>

### <span data-ttu-id="12705-134">System. String</span><span class="sxs-lookup"><span data-stu-id="12705-134">System.String</span></span>

### <span data-ttu-id="12705-135">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="12705-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="12705-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12705-136">OUTPUTS</span></span>

### <span data-ttu-id="12705-137">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="12705-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="12705-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12705-138">NOTES</span></span>

## <span data-ttu-id="12705-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12705-139">RELATED LINKS</span></span>
