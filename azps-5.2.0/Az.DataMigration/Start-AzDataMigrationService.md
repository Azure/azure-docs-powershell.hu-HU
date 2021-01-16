---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328981"
---
# <span data-ttu-id="669fe-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="669fe-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="669fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="669fe-102">SYNOPSIS</span></span>
<span data-ttu-id="669fe-103">Leállítva elindítja az Azure Adatbázis-áttelepítési szolgáltatás egy példányát.</span><span class="sxs-lookup"><span data-stu-id="669fe-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="669fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="669fe-104">SYNTAX</span></span>

### <span data-ttu-id="669fe-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="669fe-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669fe-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="669fe-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669fe-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="669fe-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="669fe-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="669fe-108">DESCRIPTION</span></span>
<span data-ttu-id="669fe-109">A Start-AzDataMigrationService parancsmag leállítva elindítja az Azure Adatbázis-áttelepítési szolgáltatás egy példányát.</span><span class="sxs-lookup"><span data-stu-id="669fe-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="669fe-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="669fe-110">EXAMPLES</span></span>

### <span data-ttu-id="669fe-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="669fe-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="669fe-112">A fenti példa elindít egy Tesztszolgáltatás nevű Azure Database Migration Service-példányt egy leállítva állapotban, a bemenetként átadott szolgáltatásnév alapján.</span><span class="sxs-lookup"><span data-stu-id="669fe-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="669fe-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="669fe-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="669fe-114">A fenti példa elindít egy Azure Database Migration Service példányt a BEMENETI paraméterként átadott PSDataMigrationService alapján.</span><span class="sxs-lookup"><span data-stu-id="669fe-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="669fe-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="669fe-115">PARAMETERS</span></span>

### <span data-ttu-id="669fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669fe-116">-DefaultProfile</span></span>
<span data-ttu-id="669fe-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="669fe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="669fe-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="669fe-118">-InputObject</span></span>
<span data-ttu-id="669fe-119">PSDataMigrationService objektum.</span><span class="sxs-lookup"><span data-stu-id="669fe-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="669fe-120">-Name</span><span class="sxs-lookup"><span data-stu-id="669fe-120">-Name</span></span>
<span data-ttu-id="669fe-121">Adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="669fe-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="669fe-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="669fe-122">-PassThru</span></span>
<span data-ttu-id="669fe-123">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="669fe-123">Returns an true/false.</span></span>
<span data-ttu-id="669fe-124">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="669fe-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="669fe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="669fe-125">-ResourceGroupName</span></span>
<span data-ttu-id="669fe-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="669fe-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="669fe-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="669fe-127">-ResourceId</span></span>
<span data-ttu-id="669fe-128">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="669fe-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="669fe-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="669fe-129">-Confirm</span></span>
<span data-ttu-id="669fe-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="669fe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="669fe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="669fe-131">-WhatIf</span></span>
<span data-ttu-id="669fe-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="669fe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="669fe-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="669fe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="669fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669fe-134">CommonParameters</span></span>
<span data-ttu-id="669fe-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="669fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669fe-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="669fe-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669fe-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="669fe-137">INPUTS</span></span>

### <span data-ttu-id="669fe-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="669fe-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="669fe-139">System.String</span><span class="sxs-lookup"><span data-stu-id="669fe-139">System.String</span></span>

## <span data-ttu-id="669fe-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="669fe-140">OUTPUTS</span></span>

### <span data-ttu-id="669fe-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="669fe-141">System.Boolean</span></span>

## <span data-ttu-id="669fe-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="669fe-142">NOTES</span></span>

## <span data-ttu-id="669fe-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="669fe-143">RELATED LINKS</span></span>
