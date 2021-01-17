---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 0222900be337cfe9eab97da31fc9d2dd84744e43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357669"
---
# <span data-ttu-id="4e994-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="4e994-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="4e994-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e994-102">SYNOPSIS</span></span>
<span data-ttu-id="4e994-103">Adatáttelepítési feladatot hoz létre és kezd el az Azure Adatbázis-áttelepítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="4e994-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="4e994-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4e994-104">SYNTAX</span></span>

### <span data-ttu-id="4e994-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e994-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e994-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e994-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e994-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e994-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e994-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4e994-108">DESCRIPTION</span></span>
<span data-ttu-id="4e994-109">A New-AzDataMigrationTask parancsmag adatáttelepítési feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4e994-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="4e994-110">Ez a parancsmag beveszi a tevékenységtípus-számláló, az Azure Resource Group, a kapcsolódó Azure-adatbázis-áttelepítési szolgáltatás és a Project paramétereit bemenetként.</span><span class="sxs-lookup"><span data-stu-id="4e994-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="4e994-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4e994-111">EXAMPLES</span></span>

### <span data-ttu-id="4e994-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="4e994-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="4e994-113">Ez a példa parancsfájl bemutatja, hogy miként hozhat létre egy MyMigrationTask nevű új adatáttelepítési feladatot a myDMSProject és a TestService nevű projektben.</span><span class="sxs-lookup"><span data-stu-id="4e994-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="4e994-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e994-114">PARAMETERS</span></span>

### <span data-ttu-id="4e994-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e994-115">-DefaultProfile</span></span>
<span data-ttu-id="4e994-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e994-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e994-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e994-117">-InputObject</span></span>
<span data-ttu-id="4e994-118">PSProject objektum.</span><span class="sxs-lookup"><span data-stu-id="4e994-118">PSProject Object.</span></span>

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

### <span data-ttu-id="4e994-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4e994-119">-Name</span></span>
<span data-ttu-id="4e994-120">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="4e994-120">The name of the task.</span></span>

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

### <span data-ttu-id="4e994-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="4e994-121">-ProjectName</span></span>
<span data-ttu-id="4e994-122">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="4e994-122">The name of the project.</span></span>

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

### <span data-ttu-id="4e994-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e994-123">-ResourceGroupName</span></span>
<span data-ttu-id="4e994-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4e994-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e994-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e994-125">-ResourceId</span></span>
<span data-ttu-id="4e994-126">Projekterőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4e994-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="4e994-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4e994-127">-ServiceName</span></span>
<span data-ttu-id="4e994-128">Adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="4e994-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="4e994-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="4e994-129">-TaskType</span></span>
<span data-ttu-id="4e994-130">Tevékenység típusa.</span><span class="sxs-lookup"><span data-stu-id="4e994-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e994-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="4e994-131">-MigrationValidation</span></span> 
<span data-ttu-id="4e994-132">Feladat válaszobjektuma érvényesítési hívásokkal, nem kötelező, de ajánlott.</span><span class="sxs-lookup"><span data-stu-id="4e994-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e994-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="4e994-133">-Wait</span></span>
<span data-ttu-id="4e994-134">Hogy várni kell-e a tevékenység befejezésére.</span><span class="sxs-lookup"><span data-stu-id="4e994-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="4e994-135">Ha a jelölő be van állítva, minden másodpercben ellenőrzi, hogy befejeződik-e a feladat, és visszaadja a felhasználónak a feladat tulajdonságait, ahol meg lehet vizsgálni a kimenetet vagy a hibát.</span><span class="sxs-lookup"><span data-stu-id="4e994-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="4e994-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e994-136">-Confirm</span></span>
<span data-ttu-id="4e994-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4e994-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e994-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e994-138">-WhatIf</span></span>
<span data-ttu-id="4e994-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4e994-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e994-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e994-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e994-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e994-141">CommonParameters</span></span>
<span data-ttu-id="4e994-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e994-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e994-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e994-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e994-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e994-144">INPUTS</span></span>

### <span data-ttu-id="4e994-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="4e994-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="4e994-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4e994-146">System.String</span></span>

## <span data-ttu-id="4e994-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e994-147">OUTPUTS</span></span>

### <span data-ttu-id="4e994-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="4e994-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="4e994-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4e994-149">NOTES</span></span>

## <span data-ttu-id="4e994-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e994-150">RELATED LINKS</span></span>
