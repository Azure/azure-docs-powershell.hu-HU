---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: acb7e9b453b94381f4f5a2a0edf49e32258809ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941881"
---
# <span data-ttu-id="83d7d-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="83d7d-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="83d7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="83d7d-103">Eltávolít egy Azure Database Migration Service-feladatot az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="83d7d-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="83d7d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83d7d-104">SYNTAX</span></span>

### <span data-ttu-id="83d7d-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83d7d-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83d7d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83d7d-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83d7d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83d7d-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d7d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83d7d-108">DESCRIPTION</span></span>
<span data-ttu-id="83d7d-109">A Remove-AzDataMigrationTask parancsmag eltávolítja az Azure Adatbázis-áttelepítési szolgáltatás egyik feladatát az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="83d7d-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="83d7d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83d7d-110">EXAMPLES</span></span>

### <span data-ttu-id="83d7d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="83d7d-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="83d7d-112">Az előző példa eltávolít egy TestTask nevű Azure-adatbázis-áttelepítési szolgáltatást az Azure-ból a feladatnév paramétere alapján.</span><span class="sxs-lookup"><span data-stu-id="83d7d-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="83d7d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="83d7d-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="83d7d-114">Az előző példa eltávolít egy, a PSProjectTask objektumon alapuló Azure Database Migration Service-feladatot.</span><span class="sxs-lookup"><span data-stu-id="83d7d-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="83d7d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83d7d-115">PARAMETERS</span></span>

### <span data-ttu-id="83d7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d7d-116">-DefaultProfile</span></span>
<span data-ttu-id="83d7d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83d7d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83d7d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="83d7d-118">-Force</span></span>
<span data-ttu-id="83d7d-119">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="83d7d-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="83d7d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83d7d-120">-InputObject</span></span>
<span data-ttu-id="83d7d-121">PSProjectTask objektum.</span><span class="sxs-lookup"><span data-stu-id="83d7d-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83d7d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="83d7d-122">-Name</span></span>
<span data-ttu-id="83d7d-123">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="83d7d-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d7d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83d7d-124">-PassThru</span></span>
<span data-ttu-id="83d7d-125">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="83d7d-125">Returns an true/false.</span></span>
<span data-ttu-id="83d7d-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="83d7d-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83d7d-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="83d7d-127">-ProjectName</span></span>
<span data-ttu-id="83d7d-128">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="83d7d-128">The name of the project.</span></span>

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

### <span data-ttu-id="83d7d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d7d-129">-ResourceGroupName</span></span>
<span data-ttu-id="83d7d-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="83d7d-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="83d7d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83d7d-131">-ResourceId</span></span>
<span data-ttu-id="83d7d-132">Projekterőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="83d7d-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="83d7d-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="83d7d-133">-ServiceName</span></span>
<span data-ttu-id="83d7d-134">Adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="83d7d-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="83d7d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83d7d-135">-Confirm</span></span>
<span data-ttu-id="83d7d-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="83d7d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d7d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d7d-137">-WhatIf</span></span>
<span data-ttu-id="83d7d-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="83d7d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d7d-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83d7d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d7d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d7d-140">CommonParameters</span></span>
<span data-ttu-id="83d7d-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d7d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d7d-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d7d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d7d-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83d7d-143">INPUTS</span></span>

### <span data-ttu-id="83d7d-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="83d7d-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="83d7d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="83d7d-145">System.String</span></span>

## <span data-ttu-id="83d7d-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83d7d-146">OUTPUTS</span></span>

### <span data-ttu-id="83d7d-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83d7d-147">System.Boolean</span></span>

## <span data-ttu-id="83d7d-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83d7d-148">NOTES</span></span>

## <span data-ttu-id="83d7d-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83d7d-149">RELATED LINKS</span></span>
