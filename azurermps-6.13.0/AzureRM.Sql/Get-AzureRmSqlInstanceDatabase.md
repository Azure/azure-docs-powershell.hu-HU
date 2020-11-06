---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: fe6779c64a3cbc5a484dd4a3ee3662bcdaf59059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495619"
---
# <span data-ttu-id="213e5-101">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="213e5-101">Get-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="213e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="213e5-102">SYNOPSIS</span></span>
<span data-ttu-id="213e5-103">Információt ad az Azure SQL Managed instance adatbázisról.</span><span class="sxs-lookup"><span data-stu-id="213e5-103">Returns information about Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="213e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="213e5-104">SYNTAX</span></span>

### <span data-ttu-id="213e5-105">GetInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="213e5-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="213e5-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="213e5-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="213e5-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="213e5-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="213e5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="213e5-108">DESCRIPTION</span></span>
<span data-ttu-id="213e5-109">A **Get-AzureRmSqlInstanceDatabase** parancsmag egy vagy több Azure SQL-adatbázisból áll egy Azure SQL-adatbázis felügyelt példányával.</span><span class="sxs-lookup"><span data-stu-id="213e5-109">The **Get-AzureRmSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="213e5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="213e5-110">EXAMPLES</span></span>

### <span data-ttu-id="213e5-111">Példa 1: a példány minden adatbázisának beolvasása</span><span class="sxs-lookup"><span data-stu-id="213e5-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
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

<span data-ttu-id="213e5-112">Ez a parancs a managedInstance1 nevű példány minden adatbázisát bekapja.</span><span class="sxs-lookup"><span data-stu-id="213e5-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="213e5-113">2. példa: adatbázis beszerzése névvel egy felügyelt példányban</span><span class="sxs-lookup"><span data-stu-id="213e5-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="213e5-114">Ez a parancs a managedDatabase1 nevű adatbázist egy managedInstance1 nevű példányból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="213e5-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

## <span data-ttu-id="213e5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="213e5-115">PARAMETERS</span></span>

### <span data-ttu-id="213e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213e5-116">-DefaultProfile</span></span>
<span data-ttu-id="213e5-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="213e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="213e5-118">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="213e5-118">-InstanceName</span></span>
<span data-ttu-id="213e5-119">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="213e5-119">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213e5-120">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="213e5-120">-InstanceObject</span></span>
<span data-ttu-id="213e5-121">A példány-adatbázis beszerzéséhez használandó objektum</span><span class="sxs-lookup"><span data-stu-id="213e5-121">The instance object to use for getting instance database</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="213e5-122">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="213e5-122">-InstanceResourceId</span></span>
<span data-ttu-id="213e5-123">A beolvasott példány-objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="213e5-123">The resource id of instance object to get</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="213e5-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="213e5-124">-Name</span></span>
<span data-ttu-id="213e5-125">A lekérdezni kívánt Azure SQL-példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="213e5-125">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="213e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="213e5-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="213e5-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="213e5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213e5-128">CommonParameters</span></span>
<span data-ttu-id="213e5-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="213e5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213e5-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="213e5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213e5-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="213e5-131">INPUTS</span></span>

### <span data-ttu-id="213e5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="213e5-132">System.String</span></span>
<span data-ttu-id="213e5-133">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="213e5-133">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="213e5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="213e5-134">OUTPUTS</span></span>

### <span data-ttu-id="213e5-135">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="213e5-135">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="213e5-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="213e5-136">NOTES</span></span>

## <span data-ttu-id="213e5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="213e5-137">RELATED LINKS</span></span>
