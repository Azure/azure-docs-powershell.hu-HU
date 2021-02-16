---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153155"
---
# <span data-ttu-id="aaef4-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="aaef4-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="aaef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaef4-102">SYNOPSIS</span></span>
<span data-ttu-id="aaef4-103">A Szabálymotor eltávolítása az előtérből</span><span class="sxs-lookup"><span data-stu-id="aaef4-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="aaef4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aaef4-104">SYNTAX</span></span>

### <span data-ttu-id="aaef4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aaef4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaef4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaef4-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaef4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaef4-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaef4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aaef4-108">DESCRIPTION</span></span>
<span data-ttu-id="aaef4-109">A Szabálymotor eltávolítása az előtérből</span><span class="sxs-lookup"><span data-stu-id="aaef4-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="aaef4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aaef4-110">EXAMPLES</span></span>

### <span data-ttu-id="aaef4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="aaef4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="aaef4-112">A szabálymotor konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aaef4-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="aaef4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="aaef4-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="aaef4-114">Várt eredmény nem létező szabálymotor-konfiguráció eltávolításakor.</span><span class="sxs-lookup"><span data-stu-id="aaef4-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="aaef4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaef4-115">PARAMETERS</span></span>

### <span data-ttu-id="aaef4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaef4-116">-DefaultProfile</span></span>
<span data-ttu-id="aaef4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aaef4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaef4-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="aaef4-118">-FrontDoorName</span></span>
<span data-ttu-id="aaef4-119">Front Door name.</span><span class="sxs-lookup"><span data-stu-id="aaef4-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaef4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaef4-120">-InputObject</span></span>
<span data-ttu-id="aaef4-121">Frissítenünk kell a Szabálymotor objektumot.</span><span class="sxs-lookup"><span data-stu-id="aaef4-121">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaef4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aaef4-122">-Name</span></span>
<span data-ttu-id="aaef4-123">A szabálymotor neve.</span><span class="sxs-lookup"><span data-stu-id="aaef4-123">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaef4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aaef4-124">-PassThru</span></span>
<span data-ttu-id="aaef4-125">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="aaef4-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="aaef4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaef4-126">-ResourceGroupName</span></span>
<span data-ttu-id="aaef4-127">Az erőforráscsoport neve, amelybe a front door nevet fogja létrehozni.</span><span class="sxs-lookup"><span data-stu-id="aaef4-127">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaef4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaef4-128">-ResourceId</span></span>
<span data-ttu-id="aaef4-129">Frissítend kell a RulesEngine erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="aaef4-129">Resource Id of the RulesEngine to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaef4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaef4-130">-Confirm</span></span>
<span data-ttu-id="aaef4-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aaef4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaef4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaef4-132">-WhatIf</span></span>
<span data-ttu-id="aaef4-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aaef4-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaef4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aaef4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaef4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaef4-135">CommonParameters</span></span>
<span data-ttu-id="aaef4-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaef4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaef4-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aaef4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaef4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaef4-138">INPUTS</span></span>

### <span data-ttu-id="aaef4-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="aaef4-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="aaef4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="aaef4-140">System.String</span></span>

## <span data-ttu-id="aaef4-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaef4-141">OUTPUTS</span></span>

### <span data-ttu-id="aaef4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aaef4-142">System.Boolean</span></span>

## <span data-ttu-id="aaef4-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aaef4-143">NOTES</span></span>

## <span data-ttu-id="aaef4-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aaef4-144">RELATED LINKS</span></span>
