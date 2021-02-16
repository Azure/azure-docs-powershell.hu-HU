---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: f45134cae9c77108aca4084470fd7f919fde02a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148082"
---
# <span data-ttu-id="fe14e-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="fe14e-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="fe14e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe14e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe14e-103">Eltávolít egy Azure Database Migration Service-projektet az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="fe14e-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="fe14e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fe14e-104">SYNTAX</span></span>

### <span data-ttu-id="fe14e-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe14e-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe14e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe14e-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe14e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe14e-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe14e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fe14e-108">DESCRIPTION</span></span>
<span data-ttu-id="fe14e-109">A Remove-AzDataMigrationProject parancsmag eltávolítja az Azure Database Migration Service-projektet az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="fe14e-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="fe14e-110">A DeleteRunningTask paraméter megadva eltávolítja az eltávolított projekthez társított Összes Azure-adatbázis-áttelepítési szolgáltatásbeli feladatot.</span><span class="sxs-lookup"><span data-stu-id="fe14e-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="fe14e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fe14e-111">EXAMPLES</span></span>

### <span data-ttu-id="fe14e-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="fe14e-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="fe14e-113">A fenti példa eltávolítja a myDMProject nevű Azure Adatbázis-áttelepítési szolgáltatás projektet az Azure-ból a bemeneti paraméterként megadott név alapján.</span><span class="sxs-lookup"><span data-stu-id="fe14e-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="fe14e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="fe14e-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="fe14e-115">A fenti példa eltávolítja a PSProject objektumon alapuló Azure Database Migration Service projektet bemeneti paraméterként.</span><span class="sxs-lookup"><span data-stu-id="fe14e-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="fe14e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe14e-116">PARAMETERS</span></span>

### <span data-ttu-id="fe14e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe14e-117">-DefaultProfile</span></span>
<span data-ttu-id="fe14e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe14e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe14e-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="fe14e-119">-DeleteRunningTask</span></span>
<span data-ttu-id="fe14e-120">Futó feladat törlése</span><span class="sxs-lookup"><span data-stu-id="fe14e-120">Delete any running task</span></span>

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

### <span data-ttu-id="fe14e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fe14e-121">-Force</span></span>
<span data-ttu-id="fe14e-122">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="fe14e-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fe14e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe14e-123">-InputObject</span></span>
<span data-ttu-id="fe14e-124">PSProject objektum.</span><span class="sxs-lookup"><span data-stu-id="fe14e-124">PSProject Object.</span></span>

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

### <span data-ttu-id="fe14e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fe14e-125">-Name</span></span>
<span data-ttu-id="fe14e-126">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="fe14e-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe14e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe14e-127">-PassThru</span></span>
<span data-ttu-id="fe14e-128">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="fe14e-128">Returns an true/false.</span></span>
<span data-ttu-id="fe14e-129">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fe14e-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe14e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe14e-130">-ResourceGroupName</span></span>
<span data-ttu-id="fe14e-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fe14e-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe14e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe14e-132">-ResourceId</span></span>
<span data-ttu-id="fe14e-133">Projekterőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fe14e-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="fe14e-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fe14e-134">-ServiceName</span></span>
<span data-ttu-id="fe14e-135">Adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="fe14e-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="fe14e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe14e-136">-Confirm</span></span>
<span data-ttu-id="fe14e-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fe14e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe14e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe14e-138">-WhatIf</span></span>
<span data-ttu-id="fe14e-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fe14e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe14e-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe14e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe14e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe14e-141">CommonParameters</span></span>
<span data-ttu-id="fe14e-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe14e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe14e-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe14e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe14e-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe14e-144">INPUTS</span></span>

### <span data-ttu-id="fe14e-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="fe14e-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="fe14e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="fe14e-146">System.String</span></span>

## <span data-ttu-id="fe14e-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe14e-147">OUTPUTS</span></span>

### <span data-ttu-id="fe14e-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fe14e-148">System.Boolean</span></span>

## <span data-ttu-id="fe14e-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fe14e-149">NOTES</span></span>

## <span data-ttu-id="fe14e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe14e-150">RELATED LINKS</span></span>
