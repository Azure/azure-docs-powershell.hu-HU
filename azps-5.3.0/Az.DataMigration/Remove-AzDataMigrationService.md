---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377606"
---
# <span data-ttu-id="da9b4-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="da9b4-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="da9b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="da9b4-103">Eltávolítja az Azure Adatbázis-áttelepítési szolgáltatás egy példányát az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="da9b4-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="da9b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da9b4-104">SYNTAX</span></span>

### <span data-ttu-id="da9b4-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da9b4-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da9b4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da9b4-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da9b4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da9b4-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da9b4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da9b4-108">DESCRIPTION</span></span>
<span data-ttu-id="da9b4-109">A Remove-AzDataMigrationService parancsmag eltávolítja az Azure Adatbázis-áttelepítési szolgáltatás egy példányát az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="da9b4-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="da9b4-110">A DeleteRunningTask paraméter megadva eltávolítja az eltávolított szolgáltatáshoz társított összes Azure Adatbázis-áttelepítési szolgáltatásbeli feladatot.</span><span class="sxs-lookup"><span data-stu-id="da9b4-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="da9b4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da9b4-111">EXAMPLES</span></span>

### <span data-ttu-id="da9b4-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="da9b4-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="da9b4-113">A fenti példa eltávolítja a TestService nevű Azure Adatbázis-áttelepítési szolgáltatás egy példányát, amely a MyResourceGroup nevű Azure Resource Group nevű Azure Resource Groupban található.</span><span class="sxs-lookup"><span data-stu-id="da9b4-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="da9b4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da9b4-114">PARAMETERS</span></span>

### <span data-ttu-id="da9b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9b4-115">-DefaultProfile</span></span>
<span data-ttu-id="da9b4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da9b4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da9b4-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="da9b4-117">-DeleteRunningTask</span></span>
<span data-ttu-id="da9b4-118">Futó feladat törlése</span><span class="sxs-lookup"><span data-stu-id="da9b4-118">Delete any running task</span></span>

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

### <span data-ttu-id="da9b4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="da9b4-119">-Force</span></span>
<span data-ttu-id="da9b4-120">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="da9b4-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="da9b4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da9b4-121">-InputObject</span></span>
<span data-ttu-id="da9b4-122">PSDataMigrationService objektum.</span><span class="sxs-lookup"><span data-stu-id="da9b4-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="da9b4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="da9b4-123">-Name</span></span>
<span data-ttu-id="da9b4-124">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="da9b4-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="da9b4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da9b4-125">-PassThru</span></span>
<span data-ttu-id="da9b4-126">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="da9b4-126">Returns an true/false.</span></span>
<span data-ttu-id="da9b4-127">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="da9b4-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da9b4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da9b4-128">-ResourceGroupName</span></span>
<span data-ttu-id="da9b4-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="da9b4-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="da9b4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da9b4-130">-ResourceId</span></span>
<span data-ttu-id="da9b4-131">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="da9b4-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="da9b4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da9b4-132">-Confirm</span></span>
<span data-ttu-id="da9b4-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="da9b4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da9b4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da9b4-134">-WhatIf</span></span>
<span data-ttu-id="da9b4-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="da9b4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da9b4-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da9b4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da9b4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9b4-137">CommonParameters</span></span>
<span data-ttu-id="da9b4-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da9b4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9b4-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da9b4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9b4-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da9b4-140">INPUTS</span></span>

### <span data-ttu-id="da9b4-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="da9b4-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="da9b4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="da9b4-142">System.String</span></span>

## <span data-ttu-id="da9b4-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da9b4-143">OUTPUTS</span></span>

### <span data-ttu-id="da9b4-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da9b4-144">System.Boolean</span></span>

## <span data-ttu-id="da9b4-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da9b4-145">NOTES</span></span>

## <span data-ttu-id="da9b4-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da9b4-146">RELATED LINKS</span></span>
