---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182295"
---
# <span data-ttu-id="730b7-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="730b7-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="730b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="730b7-102">SYNOPSIS</span></span>
<span data-ttu-id="730b7-103">Beolvassa az Azure adatbázis-áttelepítési szolgáltatás áttelepítési feladatához társított PSProjectTask-objektumot.</span><span class="sxs-lookup"><span data-stu-id="730b7-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="730b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="730b7-104">SYNTAX</span></span>

### <span data-ttu-id="730b7-105">ListByComponent (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="730b7-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="730b7-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="730b7-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="730b7-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="730b7-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="730b7-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="730b7-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="730b7-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="730b7-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="730b7-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="730b7-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="730b7-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="730b7-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="730b7-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="730b7-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="730b7-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="730b7-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="730b7-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="730b7-114">DESCRIPTION</span></span>
<span data-ttu-id="730b7-115">A Get-AzDataMigrationTask parancsmag beolvassa az Azure adatbázis-áttelepítési szolgáltatás áttelepítési feladatához társított tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="730b7-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="730b7-116">Példák</span><span class="sxs-lookup"><span data-stu-id="730b7-116">EXAMPLES</span></span>

### <span data-ttu-id="730b7-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="730b7-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="730b7-118">A fenti példa azt szemlélteti, hogy hogyan lehet Get-AzDataMigrationTask parancsmagot használni az Azure-adatbázis áttelepítési szolgáltatás áttelepítési feladatának tulajdonságaihoz bemeneti paraméterként átadott tevékenység neve alapján.</span><span class="sxs-lookup"><span data-stu-id="730b7-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="730b7-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="730b7-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="730b7-120">A fenti példa azt szemlélteti, hogy Get-AzDataMigrationTask parancsmag használatával hogyan lehet beolvasni a PSProject objektumhoz a bemeneti paraméterként átadott összes áttelepítési feladatot.</span><span class="sxs-lookup"><span data-stu-id="730b7-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="730b7-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="730b7-121">PARAMETERS</span></span>

### <span data-ttu-id="730b7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="730b7-122">-DefaultProfile</span></span>
<span data-ttu-id="730b7-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="730b7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="730b7-124">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="730b7-124">-Expand</span></span>
<span data-ttu-id="730b7-125">Kimenet kibontása</span><span class="sxs-lookup"><span data-stu-id="730b7-125">Expand output</span></span>

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

### <span data-ttu-id="730b7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="730b7-126">-InputObject</span></span>
<span data-ttu-id="730b7-127">PSProject objektum</span><span class="sxs-lookup"><span data-stu-id="730b7-127">PSProject Object.</span></span>

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

### <span data-ttu-id="730b7-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="730b7-128">-Name</span></span>
<span data-ttu-id="730b7-129">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="730b7-129">The name of the task.</span></span>

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

### <span data-ttu-id="730b7-130">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="730b7-130">-ProjectName</span></span>
<span data-ttu-id="730b7-131">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="730b7-131">The name of the project.</span></span>

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

### <span data-ttu-id="730b7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="730b7-132">-ResourceGroupName</span></span>
<span data-ttu-id="730b7-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="730b7-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="730b7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="730b7-134">-ResourceId</span></span>
<span data-ttu-id="730b7-135">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="730b7-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="730b7-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="730b7-136">-ResultType</span></span>
<span data-ttu-id="730b7-137">A megadott eredmény típusú kimenet kibontása</span><span class="sxs-lookup"><span data-stu-id="730b7-137">Expand output of given result type.</span></span>

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

### <span data-ttu-id="730b7-138">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="730b7-138">-ServiceName</span></span>
<span data-ttu-id="730b7-139">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="730b7-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="730b7-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="730b7-140">-TaskType</span></span>
<span data-ttu-id="730b7-141">Szűrés TaskType szerint</span><span class="sxs-lookup"><span data-stu-id="730b7-141">Filter by TaskType.</span></span>

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

### <span data-ttu-id="730b7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="730b7-142">CommonParameters</span></span>
<span data-ttu-id="730b7-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="730b7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="730b7-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="730b7-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="730b7-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="730b7-145">INPUTS</span></span>

### <span data-ttu-id="730b7-146">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="730b7-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="730b7-147">System. String</span><span class="sxs-lookup"><span data-stu-id="730b7-147">System.String</span></span>

## <span data-ttu-id="730b7-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="730b7-148">OUTPUTS</span></span>

### <span data-ttu-id="730b7-149">Microsoft. Azure. Command. DataMigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="730b7-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="730b7-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="730b7-150">NOTES</span></span>

## <span data-ttu-id="730b7-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="730b7-151">RELATED LINKS</span></span>
