---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 2ef6ff642d22429ae22186ce01a4a17dad125b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497255"
---
# <span data-ttu-id="019d0-101">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="019d0-101">New-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="019d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="019d0-102">SYNOPSIS</span></span>
<span data-ttu-id="019d0-103">Azure SQL Managed instance-adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="019d0-103">Creates an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="019d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="019d0-104">SYNTAX</span></span>

### <span data-ttu-id="019d0-105">CreateNewInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="019d0-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="019d0-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="019d0-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="019d0-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="019d0-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzureRmSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="019d0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="019d0-108">DESCRIPTION</span></span>
<span data-ttu-id="019d0-109">A **New-AzureRmSqlInstanceDatabase** parancsmag egy Azure SQL Managed instance-adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="019d0-109">The **New-AzureRmSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="019d0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="019d0-110">EXAMPLES</span></span>

### <span data-ttu-id="019d0-111">Példa 1: adatbázis létrehozása megadott példányban</span><span class="sxs-lookup"><span data-stu-id="019d0-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
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

<span data-ttu-id="019d0-112">Ez a parancs létrehoz egy Database01 nevű példány-adatbázist, például a managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="019d0-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="019d0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="019d0-113">PARAMETERS</span></span>

### <span data-ttu-id="019d0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="019d0-114">-AsJob</span></span>
<span data-ttu-id="019d0-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="019d0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="019d0-116">-Szétválogatás</span><span class="sxs-lookup"><span data-stu-id="019d0-116">-Collation</span></span>
<span data-ttu-id="019d0-117">Az Azure SQL-példányok adatbázis-egybevetésének szétválogatása.</span><span class="sxs-lookup"><span data-stu-id="019d0-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="019d0-118">-DefaultProfile</span></span>
<span data-ttu-id="019d0-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="019d0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="019d0-120">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="019d0-120">-InstanceName</span></span>
<span data-ttu-id="019d0-121">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="019d0-121">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019d0-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="019d0-122">-InstanceObject</span></span>
<span data-ttu-id="019d0-123">A instance objektum</span><span class="sxs-lookup"><span data-stu-id="019d0-123">The instance object</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="019d0-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="019d0-124">-InstanceResourceId</span></span>
<span data-ttu-id="019d0-125">A példány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="019d0-125">The instance resource id</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="019d0-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="019d0-126">-Name</span></span>
<span data-ttu-id="019d0-127">A létrehozandó Azure SQL-példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="019d0-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019d0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="019d0-128">-ResourceGroupName</span></span>
<span data-ttu-id="019d0-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="019d0-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019d0-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="019d0-130">-Tag</span></span>
<span data-ttu-id="019d0-131">Az Azure SQL instance adatbázisához társítani kívánt Címkék</span><span class="sxs-lookup"><span data-stu-id="019d0-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019d0-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="019d0-132">-Confirm</span></span>
<span data-ttu-id="019d0-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="019d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="019d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="019d0-134">-WhatIf</span></span>
<span data-ttu-id="019d0-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="019d0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="019d0-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="019d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="019d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="019d0-137">CommonParameters</span></span>
<span data-ttu-id="019d0-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="019d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="019d0-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="019d0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="019d0-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="019d0-140">INPUTS</span></span>

### <span data-ttu-id="019d0-141">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="019d0-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="019d0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="019d0-142">System.String</span></span>

## <span data-ttu-id="019d0-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="019d0-143">OUTPUTS</span></span>

### <span data-ttu-id="019d0-144">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="019d0-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="019d0-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="019d0-145">NOTES</span></span>

## <span data-ttu-id="019d0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="019d0-146">RELATED LINKS</span></span>
