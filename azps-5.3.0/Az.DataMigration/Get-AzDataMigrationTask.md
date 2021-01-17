---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465773"
---
# <span data-ttu-id="48d79-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="48d79-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="48d79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48d79-102">SYNOPSIS</span></span>
<span data-ttu-id="48d79-103">Lekéri az Azure Adatbázis-áttelepítési szolgáltatás áttelepítési feladatával társított PSProjectTask objektumot.</span><span class="sxs-lookup"><span data-stu-id="48d79-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="48d79-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48d79-104">SYNTAX</span></span>

### <span data-ttu-id="48d79-105">ListByComponent (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48d79-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d79-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="48d79-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d79-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="48d79-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d79-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="48d79-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d79-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="48d79-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d79-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="48d79-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d79-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="48d79-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d79-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="48d79-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d79-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="48d79-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48d79-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48d79-114">DESCRIPTION</span></span>
<span data-ttu-id="48d79-115">A Get-AzDataMigrationTask parancsmag beolvassa az Azure Adatbázis-áttelepítési szolgáltatás áttelepítési feladatával társított tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="48d79-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="48d79-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48d79-116">EXAMPLES</span></span>

### <span data-ttu-id="48d79-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="48d79-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="48d79-118">A fenti példa egy Get-AzDataMigrationTask parancsmag használatát mutatja be az Azure Adatbázis-áttelepítési szolgáltatás áttelepítési feladatával társított tulajdonságok beolvasásához bemeneti paraméterként átadott feladatnév alapján.</span><span class="sxs-lookup"><span data-stu-id="48d79-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="48d79-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="48d79-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="48d79-120">A fenti példa egy Get-AzDataMigrationTask parancsmag használatával beolvassa a BEMENETI paraméterként átadott PSProject objektummal társított összes áttelepítési feladatot.</span><span class="sxs-lookup"><span data-stu-id="48d79-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="48d79-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48d79-121">PARAMETERS</span></span>

### <span data-ttu-id="48d79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d79-122">-DefaultProfile</span></span>
<span data-ttu-id="48d79-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48d79-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48d79-124">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="48d79-124">-Expand</span></span>
<span data-ttu-id="48d79-125">Kimenet kibontása</span><span class="sxs-lookup"><span data-stu-id="48d79-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d79-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48d79-126">-InputObject</span></span>
<span data-ttu-id="48d79-127">PSProject objektum.</span><span class="sxs-lookup"><span data-stu-id="48d79-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48d79-128">-Name</span><span class="sxs-lookup"><span data-stu-id="48d79-128">-Name</span></span>
<span data-ttu-id="48d79-129">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="48d79-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d79-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="48d79-130">-ProjectName</span></span>
<span data-ttu-id="48d79-131">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="48d79-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d79-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d79-132">-ResourceGroupName</span></span>
<span data-ttu-id="48d79-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="48d79-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d79-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48d79-134">-ResourceId</span></span>
<span data-ttu-id="48d79-135">Projekterőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="48d79-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d79-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="48d79-136">-ResultType</span></span>
<span data-ttu-id="48d79-137">A megadott eredménytípus kimenetének kibontása</span><span class="sxs-lookup"><span data-stu-id="48d79-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d79-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="48d79-138">-ServiceName</span></span>
<span data-ttu-id="48d79-139">Adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="48d79-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d79-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="48d79-140">-TaskType</span></span>
<span data-ttu-id="48d79-141">Szűrés Feladattípus szerint.</span><span class="sxs-lookup"><span data-stu-id="48d79-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48d79-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d79-142">CommonParameters</span></span>
<span data-ttu-id="48d79-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d79-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d79-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d79-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d79-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48d79-145">INPUTS</span></span>

### <span data-ttu-id="48d79-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="48d79-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="48d79-147">System.String</span><span class="sxs-lookup"><span data-stu-id="48d79-147">System.String</span></span>

## <span data-ttu-id="48d79-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48d79-148">OUTPUTS</span></span>

### <span data-ttu-id="48d79-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="48d79-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="48d79-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48d79-150">NOTES</span></span>

## <span data-ttu-id="48d79-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48d79-151">RELATED LINKS</span></span>
