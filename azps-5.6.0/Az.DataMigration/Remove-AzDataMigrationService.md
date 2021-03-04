---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 313748a0d674146ae0442174ee50a7069f55b9b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941889"
---
# <span data-ttu-id="87eb5-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="87eb5-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="87eb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="87eb5-103">Eltávolítja az Azure Adatbázis-áttelepítési szolgáltatás egy példányát az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="87eb5-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="87eb5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87eb5-104">SYNTAX</span></span>

### <span data-ttu-id="87eb5-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87eb5-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87eb5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87eb5-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87eb5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87eb5-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87eb5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87eb5-108">DESCRIPTION</span></span>
<span data-ttu-id="87eb5-109">A Remove-AzDataMigrationService parancsmag eltávolítja az Azure Adatbázis-áttelepítési szolgáltatás egy példányát az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="87eb5-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="87eb5-110">A DeleteRunningTask paraméter megadva eltávolítja az eltávolított szolgáltatáshoz társított összes Azure Adatbázis-áttelepítési szolgáltatásbeli feladatot.</span><span class="sxs-lookup"><span data-stu-id="87eb5-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="87eb5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87eb5-111">EXAMPLES</span></span>

### <span data-ttu-id="87eb5-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="87eb5-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="87eb5-113">A fenti példa eltávolítja a TestService nevű Azure Adatbázis-áttelepítési szolgáltatás egy példányát, amely a MyResourceGroup nevű Azure Resource Group nevű Azure Resource Groupban található.</span><span class="sxs-lookup"><span data-stu-id="87eb5-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="87eb5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87eb5-114">PARAMETERS</span></span>

### <span data-ttu-id="87eb5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87eb5-115">-DefaultProfile</span></span>
<span data-ttu-id="87eb5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87eb5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87eb5-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="87eb5-117">-DeleteRunningTask</span></span>
<span data-ttu-id="87eb5-118">Futó feladat törlése</span><span class="sxs-lookup"><span data-stu-id="87eb5-118">Delete any running task</span></span>

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

### <span data-ttu-id="87eb5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="87eb5-119">-Force</span></span>
<span data-ttu-id="87eb5-120">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="87eb5-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="87eb5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87eb5-121">-InputObject</span></span>
<span data-ttu-id="87eb5-122">PSDataMigrationService objektum.</span><span class="sxs-lookup"><span data-stu-id="87eb5-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87eb5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="87eb5-123">-Name</span></span>
<span data-ttu-id="87eb5-124">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="87eb5-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87eb5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87eb5-125">-PassThru</span></span>
<span data-ttu-id="87eb5-126">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="87eb5-126">Returns an true/false.</span></span>
<span data-ttu-id="87eb5-127">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="87eb5-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="87eb5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87eb5-128">-ResourceGroupName</span></span>
<span data-ttu-id="87eb5-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="87eb5-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="87eb5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87eb5-130">-ResourceId</span></span>
<span data-ttu-id="87eb5-131">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="87eb5-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="87eb5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87eb5-132">-Confirm</span></span>
<span data-ttu-id="87eb5-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="87eb5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87eb5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87eb5-134">-WhatIf</span></span>
<span data-ttu-id="87eb5-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="87eb5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87eb5-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87eb5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87eb5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87eb5-137">CommonParameters</span></span>
<span data-ttu-id="87eb5-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87eb5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87eb5-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87eb5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87eb5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87eb5-140">INPUTS</span></span>

### <span data-ttu-id="87eb5-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="87eb5-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="87eb5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="87eb5-142">System.String</span></span>

## <span data-ttu-id="87eb5-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87eb5-143">OUTPUTS</span></span>

### <span data-ttu-id="87eb5-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="87eb5-144">System.Boolean</span></span>

## <span data-ttu-id="87eb5-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87eb5-145">NOTES</span></span>

## <span data-ttu-id="87eb5-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87eb5-146">RELATED LINKS</span></span>
