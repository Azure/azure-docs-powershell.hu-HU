---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672649"
---
# <span data-ttu-id="0d0b7-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="0d0b7-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="0d0b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d0b7-103">Áttelepítési feladatot hoz létre és indít el az Azure adatbázis-áttelepítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d0b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d0b7-104">SYNTAX</span></span>

### <span data-ttu-id="0d0b7-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d0b7-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0d0b7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d0b7-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0d0b7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d0b7-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0d0b7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d0b7-108">DESCRIPTION</span></span>
<span data-ttu-id="0d0b7-109">Az New-AzureRmDataMigrationTask parancsmag adatáttelepítési feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="0d0b7-110">Ez a parancsmag a feladattípusok enumerálása, az Azure Resource Group, a kapcsolódó Azure-áttelepítési szolgáltatás és a projekt mint bemenet paramétereit veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Data Migration Service and Project as input.</span></span> 

## <span data-ttu-id="0d0b7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0d0b7-111">EXAMPLES</span></span>

### <span data-ttu-id="0d0b7-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0d0b7-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
<span data-ttu-id="0d0b7-113">Az alábbi példa azt szemlélteti, hogy miként hozhat létre egy MyMigrationTask nevű új adatáttelepítési feladatot a TestService nevű myDMSProject és szolgáltatás nevű projektben.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="0d0b7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d0b7-114">PARAMETERS</span></span>

### <span data-ttu-id="0d0b7-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0d0b7-115">-Confirm</span></span>
<span data-ttu-id="0d0b7-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d0b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d0b7-117">-DefaultProfile</span></span>
<span data-ttu-id="0d0b7-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d0b7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d0b7-119">-InputObject</span></span>
<span data-ttu-id="0d0b7-120">PSProject objektum</span><span class="sxs-lookup"><span data-stu-id="0d0b7-120">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d0b7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0d0b7-121">-Name</span></span>
<span data-ttu-id="0d0b7-122">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-122">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d0b7-123">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="0d0b7-123">-ProjectName</span></span>
<span data-ttu-id="0d0b7-124">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-124">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d0b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d0b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="0d0b7-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d0b7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d0b7-127">-ResourceId</span></span>
<span data-ttu-id="0d0b7-128">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="0d0b7-128">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d0b7-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="0d0b7-129">-ServiceName</span></span>
<span data-ttu-id="0d0b7-130">Az adatáttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-130">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d0b7-131">-TaskType</span><span class="sxs-lookup"><span data-stu-id="0d0b7-131">-TaskType</span></span>
<span data-ttu-id="0d0b7-132">Tevékenység típusa</span><span class="sxs-lookup"><span data-stu-id="0d0b7-132">Task Type.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d0b7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d0b7-133">-WhatIf</span></span>
<span data-ttu-id="0d0b7-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d0b7-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-135">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="0d0b7-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d0b7-136">INPUTS</span></span>

### <span data-ttu-id="0d0b7-137">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="0d0b7-137">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="0d0b7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0d0b7-138">System.String</span></span>


## <span data-ttu-id="0d0b7-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d0b7-139">OUTPUTS</span></span>

### <span data-ttu-id="0d0b7-140">Microsoft. Azure. Command. DataMigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="0d0b7-140">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>


## <span data-ttu-id="0d0b7-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d0b7-141">NOTES</span></span>

## <span data-ttu-id="0d0b7-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d0b7-142">RELATED LINKS</span></span>


