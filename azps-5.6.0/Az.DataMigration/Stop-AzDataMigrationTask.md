---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: 33bc407c5585017bfe98591649a0c30e46adfea4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920585"
---
# <span data-ttu-id="9a7c6-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="9a7c6-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="9a7c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a7c6-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7c6-103">Leállít egy futó állapotban futó Azure Database Migration Service-feladatot.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="9a7c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a7c6-104">SYNTAX</span></span>

### <span data-ttu-id="9a7c6-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a7c6-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7c6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a7c6-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7c6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a7c6-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a7c6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a7c6-108">DESCRIPTION</span></span>
<span data-ttu-id="9a7c6-109">Stop-AzDataMigrationTask parancsmag futási állapotban leállítja az adatbázis-áttelepítési tevékenységet.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="9a7c6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a7c6-110">EXAMPLES</span></span>

### <span data-ttu-id="9a7c6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9a7c6-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="9a7c6-112">A fenti példa leállítja a MyDMSTask nevű Azure Database Migration Service-feladatot, amely a MyDMSProject és a TestService nevű Azure Database Migration Service példányhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="9a7c6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="9a7c6-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="9a7c6-114">A fenti példa leállítja a PSProjectTask bemeneti paraméterként átadott Azure Database Migration Service-feladatot</span><span class="sxs-lookup"><span data-stu-id="9a7c6-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="9a7c6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a7c6-115">PARAMETERS</span></span>

### <span data-ttu-id="9a7c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a7c6-116">-DefaultProfile</span></span>
<span data-ttu-id="9a7c6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a7c6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a7c6-118">-InputObject</span></span>
<span data-ttu-id="9a7c6-119">PSProjectTask objektum.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="9a7c6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9a7c6-120">-Name</span></span>
<span data-ttu-id="9a7c6-121">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-121">The name of the task.</span></span>

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

### <span data-ttu-id="9a7c6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a7c6-122">-PassThru</span></span>
<span data-ttu-id="9a7c6-123">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-123">Returns an true/false.</span></span>
<span data-ttu-id="9a7c6-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a7c6-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="9a7c6-125">-ProjectName</span></span>
<span data-ttu-id="9a7c6-126">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-126">The name of the project.</span></span>

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

### <span data-ttu-id="9a7c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a7c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="9a7c6-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="9a7c6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a7c6-129">-ResourceId</span></span>
<span data-ttu-id="9a7c6-130">ProjectTask Resource Id.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="9a7c6-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9a7c6-131">-ServiceName</span></span>
<span data-ttu-id="9a7c6-132">Adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="9a7c6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a7c6-133">-Confirm</span></span>
<span data-ttu-id="9a7c6-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a7c6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a7c6-135">-WhatIf</span></span>
<span data-ttu-id="9a7c6-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a7c6-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a7c6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7c6-138">CommonParameters</span></span>
<span data-ttu-id="9a7c6-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7c6-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a7c6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7c6-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a7c6-141">INPUTS</span></span>

### <span data-ttu-id="9a7c6-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="9a7c6-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="9a7c6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9a7c6-143">System.String</span></span>

## <span data-ttu-id="9a7c6-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a7c6-144">OUTPUTS</span></span>

### <span data-ttu-id="9a7c6-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a7c6-145">System.Boolean</span></span>

## <span data-ttu-id="9a7c6-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a7c6-146">NOTES</span></span>

## <span data-ttu-id="9a7c6-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a7c6-147">RELATED LINKS</span></span>
