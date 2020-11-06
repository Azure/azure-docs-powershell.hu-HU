---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 8352f7a63e40986e27c4b521dca58aaf003679bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502948"
---
# <span data-ttu-id="83650-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="83650-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="83650-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83650-102">SYNOPSIS</span></span>
<span data-ttu-id="83650-103">Áttelepítési feladatot hoz létre és indít el az Azure adatbázis-áttelepítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="83650-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83650-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83650-104">SYNTAX</span></span>

### <span data-ttu-id="83650-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83650-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83650-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83650-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83650-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83650-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83650-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="83650-108">DESCRIPTION</span></span>
<span data-ttu-id="83650-109">Az New-AzureRmDataMigrationTask parancsmag adatáttelepítési feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="83650-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="83650-110">Ez a parancsmag a feladattípusok enumerálása, az Azure Resource Group, a kapcsolódó Azure-adatbázis áttelepítési szolgáltatásának és a Project adatbevitelének paramétereit veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="83650-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="83650-111">Példák</span><span class="sxs-lookup"><span data-stu-id="83650-111">EXAMPLES</span></span>

### <span data-ttu-id="83650-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="83650-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```

<span data-ttu-id="83650-113">Az alábbi példa azt szemlélteti, hogy miként hozhat létre egy MyMigrationTask nevű új adatáttelepítési feladatot a TestService nevű myDMSProject és szolgáltatás nevű projektben.</span><span class="sxs-lookup"><span data-stu-id="83650-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="83650-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83650-114">PARAMETERS</span></span>

### <span data-ttu-id="83650-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83650-115">-DefaultProfile</span></span>
<span data-ttu-id="83650-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83650-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83650-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83650-117">-InputObject</span></span>
<span data-ttu-id="83650-118">PSProject objektum</span><span class="sxs-lookup"><span data-stu-id="83650-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83650-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83650-119">-Name</span></span>
<span data-ttu-id="83650-120">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="83650-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83650-121">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="83650-121">-ProjectName</span></span>
<span data-ttu-id="83650-122">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="83650-122">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83650-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83650-123">-ResourceGroupName</span></span>
<span data-ttu-id="83650-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="83650-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83650-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83650-125">-ResourceId</span></span>
<span data-ttu-id="83650-126">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="83650-126">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83650-127">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="83650-127">-ServiceName</span></span>
<span data-ttu-id="83650-128">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="83650-128">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83650-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="83650-129">-TaskType</span></span>
<span data-ttu-id="83650-130">Tevékenység típusa</span><span class="sxs-lookup"><span data-stu-id="83650-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83650-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83650-131">-Confirm</span></span>
<span data-ttu-id="83650-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83650-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83650-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83650-133">-WhatIf</span></span>
<span data-ttu-id="83650-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83650-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83650-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83650-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83650-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83650-136">CommonParameters</span></span>
<span data-ttu-id="83650-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83650-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83650-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83650-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83650-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83650-139">INPUTS</span></span>

### <span data-ttu-id="83650-140">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="83650-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="83650-141">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="83650-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="83650-142">System. String</span><span class="sxs-lookup"><span data-stu-id="83650-142">System.String</span></span>

## <span data-ttu-id="83650-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83650-143">OUTPUTS</span></span>

### <span data-ttu-id="83650-144">Microsoft. Azure. Command. DataMigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="83650-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="83650-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83650-145">NOTES</span></span>

## <span data-ttu-id="83650-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83650-146">RELATED LINKS</span></span>
