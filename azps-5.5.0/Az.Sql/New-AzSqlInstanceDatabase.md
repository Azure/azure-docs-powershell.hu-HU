---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164938"
---
# <span data-ttu-id="cd699-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd699-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="cd699-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd699-102">SYNOPSIS</span></span>
<span data-ttu-id="cd699-103">Létrehoz egy Azure SQL Felügyeltpéldány-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="cd699-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="cd699-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd699-104">SYNTAX</span></span>

### <span data-ttu-id="cd699-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="cd699-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd699-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="cd699-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd699-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="cd699-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd699-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd699-108">DESCRIPTION</span></span>
<span data-ttu-id="cd699-109">A **New-AzSqlInstanceDatabase** parancsmag létrehoz egy Azure SQL Felügyelt példány adatbázist.</span><span class="sxs-lookup"><span data-stu-id="cd699-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="cd699-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd699-110">EXAMPLES</span></span>

### <span data-ttu-id="cd699-111">1. példa: Adatbázis létrehozása egy megadott példányon</span><span class="sxs-lookup"><span data-stu-id="cd699-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="cd699-112">Ez a parancs létrehoz egy Database01 nevű példányadatbázist a példány managedInstance1 példányon.</span><span class="sxs-lookup"><span data-stu-id="cd699-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="cd699-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd699-113">PARAMETERS</span></span>

### <span data-ttu-id="cd699-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd699-114">-AsJob</span></span>
<span data-ttu-id="cd699-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cd699-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd699-116">-Collation</span><span class="sxs-lookup"><span data-stu-id="cd699-116">-Collation</span></span>
<span data-ttu-id="cd699-117">A használt Azure SQL Instance Database szétválogatása.</span><span class="sxs-lookup"><span data-stu-id="cd699-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd699-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd699-118">-DefaultProfile</span></span>
<span data-ttu-id="cd699-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd699-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd699-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cd699-120">-InstanceName</span></span>
<span data-ttu-id="cd699-121">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="cd699-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd699-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="cd699-122">-InstanceObject</span></span>
<span data-ttu-id="cd699-123">A példányobjektum</span><span class="sxs-lookup"><span data-stu-id="cd699-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd699-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="cd699-124">-InstanceResourceId</span></span>
<span data-ttu-id="cd699-125">A példány erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cd699-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd699-126">-Name</span><span class="sxs-lookup"><span data-stu-id="cd699-126">-Name</span></span>
<span data-ttu-id="cd699-127">A létrehozni szükséges Azure SQL-példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="cd699-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd699-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd699-128">-ResourceGroupName</span></span>
<span data-ttu-id="cd699-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd699-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd699-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd699-130">-Tag</span></span>
<span data-ttu-id="cd699-131">Az Azure Sql Instance-adatbázissal társítva</span><span class="sxs-lookup"><span data-stu-id="cd699-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd699-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd699-132">-Confirm</span></span>
<span data-ttu-id="cd699-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cd699-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd699-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd699-134">-WhatIf</span></span>
<span data-ttu-id="cd699-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cd699-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd699-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd699-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd699-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd699-137">CommonParameters</span></span>
<span data-ttu-id="cd699-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd699-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd699-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd699-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd699-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd699-140">INPUTS</span></span>

### <span data-ttu-id="cd699-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="cd699-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="cd699-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cd699-142">System.String</span></span>

## <span data-ttu-id="cd699-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd699-143">OUTPUTS</span></span>

### <span data-ttu-id="cd699-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cd699-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="cd699-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd699-145">NOTES</span></span>

## <span data-ttu-id="cd699-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd699-146">RELATED LINKS</span></span>
