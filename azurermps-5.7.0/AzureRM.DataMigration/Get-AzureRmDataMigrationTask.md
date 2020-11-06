---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: 5ca6edfa811a1b73cbdaae59e8d3b0e2f76cc15f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495386"
---
# <span data-ttu-id="13992-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="13992-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="13992-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13992-102">SYNOPSIS</span></span>
<span data-ttu-id="13992-103">Beolvassa az Azure adatbázis-áttelepítési szolgáltatás áttelepítési feladatához társított PSProjectTask-objektumot.</span><span class="sxs-lookup"><span data-stu-id="13992-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13992-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13992-104">SYNTAX</span></span>

### <span data-ttu-id="13992-105">ListByComponent (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13992-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="13992-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="13992-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="13992-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="13992-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="13992-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="13992-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="13992-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="13992-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="13992-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="13992-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="13992-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="13992-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="13992-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="13992-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="13992-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="13992-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="13992-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="13992-114">DESCRIPTION</span></span>
<span data-ttu-id="13992-115">A Get-AzureRmDataMigrationTask parancsmag beolvassa az Azure adatbázis-áttelepítési szolgáltatás áttelepítési feladatához társított tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="13992-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="13992-116">Példák</span><span class="sxs-lookup"><span data-stu-id="13992-116">EXAMPLES</span></span>

### <span data-ttu-id="13992-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13992-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="13992-118">A fenti példa azt szemlélteti, hogy hogyan lehet Get-AzureRmDataMigrationTask parancsmagot használni az Azure-adatbázis áttelepítési szolgáltatás áttelepítési feladatának tulajdonságaihoz bemeneti paraméterként átadott tevékenység neve alapján.</span><span class="sxs-lookup"><span data-stu-id="13992-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="13992-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="13992-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="13992-120">A fenti példa azt szemlélteti, hogy Get-AzureRmDataMigrationTask parancsmag használatával hogyan lehet beolvasni a PSProject objektumhoz a bemeneti paraméterként átadott összes áttelepítési feladatot.</span><span class="sxs-lookup"><span data-stu-id="13992-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="13992-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13992-121">PARAMETERS</span></span>

### <span data-ttu-id="13992-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13992-122">-DefaultProfile</span></span>
<span data-ttu-id="13992-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13992-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13992-124">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="13992-124">-Expand</span></span>
<span data-ttu-id="13992-125">Kimenet kibontása</span><span class="sxs-lookup"><span data-stu-id="13992-125">Expand output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13992-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13992-126">-InputObject</span></span>
<span data-ttu-id="13992-127">PSProject objektum</span><span class="sxs-lookup"><span data-stu-id="13992-127">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13992-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13992-128">-Name</span></span>
<span data-ttu-id="13992-129">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="13992-129">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13992-130">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="13992-130">-ProjectName</span></span>
<span data-ttu-id="13992-131">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="13992-131">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13992-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13992-132">-ResourceGroupName</span></span>
<span data-ttu-id="13992-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="13992-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13992-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13992-134">-ResourceId</span></span>
<span data-ttu-id="13992-135">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="13992-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13992-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="13992-136">-ResultType</span></span>
<span data-ttu-id="13992-137">A megadott eredmény típusú kimenet kibontása</span><span class="sxs-lookup"><span data-stu-id="13992-137">Expand output of given result type.</span></span>

```yaml
Type: ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13992-138">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="13992-138">-ServiceName</span></span>
<span data-ttu-id="13992-139">Az adatáttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="13992-139">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13992-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="13992-140">-TaskType</span></span>
<span data-ttu-id="13992-141">Szűrés TaskType szerint</span><span class="sxs-lookup"><span data-stu-id="13992-141">Filter by TaskType.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="13992-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13992-142">INPUTS</span></span>

### <span data-ttu-id="13992-143">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="13992-143">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="13992-144">System. String</span><span class="sxs-lookup"><span data-stu-id="13992-144">System.String</span></span>

## <span data-ttu-id="13992-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13992-145">OUTPUTS</span></span>

### <span data-ttu-id="13992-146">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. DataMigration. models. PSProjectTask, Microsoft. Azure. commands. DataMigration, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="13992-146">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="13992-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13992-147">NOTES</span></span>

## <span data-ttu-id="13992-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13992-148">RELATED LINKS</span></span>

