---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: caab43824c63e73e7011c0377d0bd7665befe5dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499547"
---
# <span data-ttu-id="c1e39-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="c1e39-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="c1e39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1e39-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e39-103">Beolvassa az Azure adatbázis-áttelepítési szolgáltatás áttelepítési feladatához társított PSProjectTask-objektumot.</span><span class="sxs-lookup"><span data-stu-id="c1e39-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1e39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1e39-104">SYNTAX</span></span>

### <span data-ttu-id="c1e39-105">ListByComponent (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1e39-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e39-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="c1e39-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e39-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c1e39-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e39-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="c1e39-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e39-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e39-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e39-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e39-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e39-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="c1e39-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e39-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="c1e39-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1e39-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="c1e39-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1e39-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1e39-114">DESCRIPTION</span></span>
<span data-ttu-id="c1e39-115">A Get-AzureRmDataMigrationTask parancsmag beolvassa az Azure adatbázis-áttelepítési szolgáltatás áttelepítési feladatához társított tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c1e39-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="c1e39-116">Példák</span><span class="sxs-lookup"><span data-stu-id="c1e39-116">EXAMPLES</span></span>

### <span data-ttu-id="c1e39-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c1e39-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="c1e39-118">A fenti példa azt szemlélteti, hogy hogyan lehet Get-AzureRmDataMigrationTask parancsmagot használni az Azure-adatbázis áttelepítési szolgáltatás áttelepítési feladatának tulajdonságaihoz bemeneti paraméterként átadott tevékenység neve alapján.</span><span class="sxs-lookup"><span data-stu-id="c1e39-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="c1e39-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="c1e39-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="c1e39-120">A fenti példa azt szemlélteti, hogy Get-AzureRmDataMigrationTask parancsmag használatával hogyan lehet beolvasni a PSProject objektumhoz a bemeneti paraméterként átadott összes áttelepítési feladatot.</span><span class="sxs-lookup"><span data-stu-id="c1e39-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="c1e39-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1e39-121">PARAMETERS</span></span>

### <span data-ttu-id="c1e39-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e39-122">-DefaultProfile</span></span>
<span data-ttu-id="c1e39-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1e39-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e39-124">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="c1e39-124">-Expand</span></span>
<span data-ttu-id="c1e39-125">Kimenet kibontása</span><span class="sxs-lookup"><span data-stu-id="c1e39-125">Expand output</span></span>

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

### <span data-ttu-id="c1e39-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1e39-126">-InputObject</span></span>
<span data-ttu-id="c1e39-127">PSProject objektum</span><span class="sxs-lookup"><span data-stu-id="c1e39-127">PSProject Object.</span></span>

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

### <span data-ttu-id="c1e39-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1e39-128">-Name</span></span>
<span data-ttu-id="c1e39-129">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="c1e39-129">The name of the task.</span></span>

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

### <span data-ttu-id="c1e39-130">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="c1e39-130">-ProjectName</span></span>
<span data-ttu-id="c1e39-131">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="c1e39-131">The name of the project.</span></span>

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

### <span data-ttu-id="c1e39-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e39-132">-ResourceGroupName</span></span>
<span data-ttu-id="c1e39-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c1e39-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="c1e39-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e39-134">-ResourceId</span></span>
<span data-ttu-id="c1e39-135">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="c1e39-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="c1e39-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="c1e39-136">-ResultType</span></span>
<span data-ttu-id="c1e39-137">A megadott eredmény típusú kimenet kibontása</span><span class="sxs-lookup"><span data-stu-id="c1e39-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e39-138">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="c1e39-138">-ServiceName</span></span>
<span data-ttu-id="c1e39-139">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="c1e39-139">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c1e39-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="c1e39-140">-TaskType</span></span>
<span data-ttu-id="c1e39-141">Szűrés TaskType szerint</span><span class="sxs-lookup"><span data-stu-id="c1e39-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e39-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e39-142">CommonParameters</span></span>
<span data-ttu-id="c1e39-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1e39-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e39-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1e39-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e39-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1e39-145">INPUTS</span></span>

### <span data-ttu-id="c1e39-146">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="c1e39-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="c1e39-147">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c1e39-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c1e39-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c1e39-148">System.String</span></span>

## <span data-ttu-id="c1e39-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1e39-149">OUTPUTS</span></span>

### <span data-ttu-id="c1e39-150">Microsoft. Azure. Command. DataMigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="c1e39-150">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="c1e39-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1e39-151">NOTES</span></span>

## <span data-ttu-id="c1e39-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1e39-152">RELATED LINKS</span></span>
