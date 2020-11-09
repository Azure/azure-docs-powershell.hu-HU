---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 0222900be337cfe9eab97da31fc9d2dd84744e43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297608"
---
# <span data-ttu-id="2a567-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2a567-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="2a567-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a567-102">SYNOPSIS</span></span>
<span data-ttu-id="2a567-103">Áttelepítési feladatot hoz létre és indít el az Azure adatbázis-áttelepítési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="2a567-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="2a567-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a567-104">SYNTAX</span></span>

### <span data-ttu-id="2a567-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a567-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a567-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a567-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a567-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a567-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a567-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a567-108">DESCRIPTION</span></span>
<span data-ttu-id="2a567-109">Az New-AzDataMigrationTask parancsmag adatáttelepítési feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2a567-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="2a567-110">Ez a parancsmag a feladattípusok enumerálása, az Azure Resource Group, a kapcsolódó Azure-adatbázis áttelepítési szolgáltatásának és a Project adatbevitelének paramétereit veszi figyelembe.</span><span class="sxs-lookup"><span data-stu-id="2a567-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="2a567-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2a567-111">EXAMPLES</span></span>

### <span data-ttu-id="2a567-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2a567-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="2a567-113">Az alábbi példa azt szemlélteti, hogy miként hozhat létre egy MyMigrationTask nevű új adatáttelepítési feladatot a TestService nevű myDMSProject és szolgáltatás nevű projektben.</span><span class="sxs-lookup"><span data-stu-id="2a567-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="2a567-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a567-114">PARAMETERS</span></span>

### <span data-ttu-id="2a567-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a567-115">-DefaultProfile</span></span>
<span data-ttu-id="2a567-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a567-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a567-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a567-117">-InputObject</span></span>
<span data-ttu-id="2a567-118">PSProject objektum</span><span class="sxs-lookup"><span data-stu-id="2a567-118">PSProject Object.</span></span>

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

### <span data-ttu-id="2a567-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2a567-119">-Name</span></span>
<span data-ttu-id="2a567-120">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="2a567-120">The name of the task.</span></span>

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

### <span data-ttu-id="2a567-121">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="2a567-121">-ProjectName</span></span>
<span data-ttu-id="2a567-122">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="2a567-122">The name of the project.</span></span>

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

### <span data-ttu-id="2a567-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a567-123">-ResourceGroupName</span></span>
<span data-ttu-id="2a567-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2a567-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a567-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a567-125">-ResourceId</span></span>
<span data-ttu-id="2a567-126">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="2a567-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="2a567-127">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="2a567-127">-ServiceName</span></span>
<span data-ttu-id="2a567-128">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="2a567-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="2a567-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="2a567-129">-TaskType</span></span>
<span data-ttu-id="2a567-130">Tevékenység típusa</span><span class="sxs-lookup"><span data-stu-id="2a567-130">Task Type.</span></span>

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

### <span data-ttu-id="2a567-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="2a567-131">-MigrationValidation</span></span> 
<span data-ttu-id="2a567-132">Tevékenység-visszajelzési objektum érvényesítési hívással, nem kötelező, de javasolt.</span><span class="sxs-lookup"><span data-stu-id="2a567-132">Task response object by validation call, optional but recommended.</span></span>

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

### <span data-ttu-id="2a567-133">– Várjon</span><span class="sxs-lookup"><span data-stu-id="2a567-133">-Wait</span></span>
<span data-ttu-id="2a567-134">Várjon-e feladatot a tevékenység befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="2a567-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="2a567-135">Ha a jelölő be van állítva, akkor minden egyes másodperc elteltével ellenőrizze a tevékenység befejeződését, és térjen vissza a felhasználóhoz a tevékenység tulajdonságai között, ahol a kimenet vagy a hiba megvizsgálható.</span><span class="sxs-lookup"><span data-stu-id="2a567-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="2a567-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2a567-136">-Confirm</span></span>
<span data-ttu-id="2a567-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a567-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a567-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a567-138">-WhatIf</span></span>
<span data-ttu-id="2a567-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a567-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a567-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a567-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a567-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a567-141">CommonParameters</span></span>
<span data-ttu-id="2a567-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a567-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a567-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a567-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a567-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a567-144">INPUTS</span></span>

### <span data-ttu-id="2a567-145">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="2a567-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="2a567-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2a567-146">System.String</span></span>

## <span data-ttu-id="2a567-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a567-147">OUTPUTS</span></span>

### <span data-ttu-id="2a567-148">Microsoft. Azure. Command. DataMigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="2a567-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="2a567-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a567-149">NOTES</span></span>

## <span data-ttu-id="2a567-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a567-150">RELATED LINKS</span></span>
