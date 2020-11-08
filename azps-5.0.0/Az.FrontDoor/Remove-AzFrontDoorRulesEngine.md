---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185440"
---
# <span data-ttu-id="db7e6-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="db7e6-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="db7e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="db7e6-103">A szabályok motorjának eltávolítása a bejárati ajtóról</span><span class="sxs-lookup"><span data-stu-id="db7e6-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="db7e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db7e6-104">SYNTAX</span></span>

### <span data-ttu-id="db7e6-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db7e6-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db7e6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db7e6-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db7e6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db7e6-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db7e6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="db7e6-108">DESCRIPTION</span></span>
<span data-ttu-id="db7e6-109">A szabályok motorjának eltávolítása a bejárati ajtóról</span><span class="sxs-lookup"><span data-stu-id="db7e6-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="db7e6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="db7e6-110">EXAMPLES</span></span>

### <span data-ttu-id="db7e6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="db7e6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="db7e6-112">A szabályok motor-konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="db7e6-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="db7e6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="db7e6-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="db7e6-114">A nem létező szabályok motor-konfigurációjának eltávolításakor várható eredmény.</span><span class="sxs-lookup"><span data-stu-id="db7e6-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="db7e6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db7e6-115">PARAMETERS</span></span>

### <span data-ttu-id="db7e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db7e6-116">-DefaultProfile</span></span>
<span data-ttu-id="db7e6-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db7e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db7e6-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="db7e6-118">-FrontDoorName</span></span>
<span data-ttu-id="db7e6-119">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="db7e6-119">Front Door name.</span></span>

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

### <span data-ttu-id="db7e6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db7e6-120">-InputObject</span></span>
<span data-ttu-id="db7e6-121">A Rule Engine objektum frissítése.</span><span class="sxs-lookup"><span data-stu-id="db7e6-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="db7e6-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db7e6-122">-Name</span></span>
<span data-ttu-id="db7e6-123">A szabályok motorjának neve</span><span class="sxs-lookup"><span data-stu-id="db7e6-123">Rules engine name.</span></span>

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

### <span data-ttu-id="db7e6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db7e6-124">-PassThru</span></span>
<span data-ttu-id="db7e6-125">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="db7e6-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="db7e6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db7e6-126">-ResourceGroupName</span></span>
<span data-ttu-id="db7e6-127">Az erőforráscsoport neve, amelybe az első ajtó jön létre.</span><span class="sxs-lookup"><span data-stu-id="db7e6-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="db7e6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db7e6-128">-ResourceId</span></span>
<span data-ttu-id="db7e6-129">A frissítendő RulesEngine erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="db7e6-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="db7e6-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db7e6-130">-Confirm</span></span>
<span data-ttu-id="db7e6-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db7e6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db7e6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db7e6-132">-WhatIf</span></span>
<span data-ttu-id="db7e6-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db7e6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db7e6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db7e6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db7e6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db7e6-135">CommonParameters</span></span>
<span data-ttu-id="db7e6-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db7e6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db7e6-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="db7e6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db7e6-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db7e6-138">INPUTS</span></span>

### <span data-ttu-id="db7e6-139">Microsoft. Azure. Command. FrontDoor. models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="db7e6-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="db7e6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="db7e6-140">System.String</span></span>

## <span data-ttu-id="db7e6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db7e6-141">OUTPUTS</span></span>

### <span data-ttu-id="db7e6-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db7e6-142">System.Boolean</span></span>

## <span data-ttu-id="db7e6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db7e6-143">NOTES</span></span>

## <span data-ttu-id="db7e6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db7e6-144">RELATED LINKS</span></span>