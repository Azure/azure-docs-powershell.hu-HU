---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155323"
---
# <span data-ttu-id="7797b-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7797b-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="7797b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7797b-102">SYNOPSIS</span></span>
<span data-ttu-id="7797b-103">Információkat ad vissza az Azure SQL Managed Instance adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="7797b-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="7797b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7797b-104">SYNTAX</span></span>

### <span data-ttu-id="7797b-105">GetInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7797b-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7797b-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="7797b-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7797b-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="7797b-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7797b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7797b-108">DESCRIPTION</span></span>
<span data-ttu-id="7797b-109">A **Get-AzSqlInstanceDatabase** parancsmag egy vagy több Azure SQL-adatbázist kap egy Azure SQL-adatbázis felügyelt példányából.</span><span class="sxs-lookup"><span data-stu-id="7797b-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="7797b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7797b-110">EXAMPLES</span></span>

### <span data-ttu-id="7797b-111">1. példa: Az összes adatbázis lekérte egy példányon</span><span class="sxs-lookup"><span data-stu-id="7797b-111">Example 1: Get all databases on a instance</span></span>
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

<span data-ttu-id="7797b-112">Ez a parancs a managedInstance1 nevű példány összes adatbázisát beveszi.</span><span class="sxs-lookup"><span data-stu-id="7797b-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="7797b-113">2. példa: Adatbázis lekérte név szerint felügyelt példányon</span><span class="sxs-lookup"><span data-stu-id="7797b-113">Example 2: Get a database by name on a Managed instance</span></span>
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

<span data-ttu-id="7797b-114">Ez a parancs egy managedDatabase1 nevű adatbázist kap a managedInstance1 nevű példányból.</span><span class="sxs-lookup"><span data-stu-id="7797b-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="7797b-115">3. példa: Egy példány összes adatbázisának be szereznie szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="7797b-115">Example 3: Get all databases on a instance using filtering</span></span>
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

<span data-ttu-id="7797b-116">Ez a parancs a managedInstance1 példányon a "managedDatabase" kezdetű összes adatbázist lekérte.</span><span class="sxs-lookup"><span data-stu-id="7797b-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="7797b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7797b-117">PARAMETERS</span></span>

### <span data-ttu-id="7797b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7797b-118">-DefaultProfile</span></span>
<span data-ttu-id="7797b-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7797b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7797b-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7797b-120">-InstanceName</span></span>
<span data-ttu-id="7797b-121">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="7797b-121">The instance name.</span></span>

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

### <span data-ttu-id="7797b-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="7797b-122">-InstanceObject</span></span>
<span data-ttu-id="7797b-123">A példányadatbázis beszerzéshez használt példányobjektum</span><span class="sxs-lookup"><span data-stu-id="7797b-123">The instance object to use for getting instance database</span></span>

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

### <span data-ttu-id="7797b-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="7797b-124">-InstanceResourceId</span></span>
<span data-ttu-id="7797b-125">A lekért példányobjektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7797b-125">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="7797b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7797b-126">-Name</span></span>
<span data-ttu-id="7797b-127">A lekérni megfelelő Azure SQL-példány adatbázisának neve.</span><span class="sxs-lookup"><span data-stu-id="7797b-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

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

### <span data-ttu-id="7797b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7797b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7797b-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7797b-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="7797b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7797b-130">CommonParameters</span></span>
<span data-ttu-id="7797b-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7797b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7797b-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7797b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7797b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7797b-133">INPUTS</span></span>

### <span data-ttu-id="7797b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7797b-134">System.String</span></span>

### <span data-ttu-id="7797b-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7797b-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="7797b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7797b-136">OUTPUTS</span></span>

### <span data-ttu-id="7797b-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7797b-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="7797b-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7797b-138">NOTES</span></span>

## <span data-ttu-id="7797b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7797b-139">RELATED LINKS</span></span>
