---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 7f24d7a7fc027e8d4411b12a3f04d24121af5354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927185"
---
# <span data-ttu-id="7863c-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="7863c-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="7863c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7863c-102">SYNOPSIS</span></span>
<span data-ttu-id="7863c-103">Szabálymotor frissítése</span><span class="sxs-lookup"><span data-stu-id="7863c-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="7863c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7863c-104">SYNTAX</span></span>

### <span data-ttu-id="7863c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7863c-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7863c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7863c-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7863c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7863c-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7863c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7863c-108">DESCRIPTION</span></span>
<span data-ttu-id="7863c-109">Szabálymotor frissítése</span><span class="sxs-lookup"><span data-stu-id="7863c-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="7863c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7863c-110">EXAMPLES</span></span>

### <span data-ttu-id="7863c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7863c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}

PS C:\> $rulesEngineRule2 = New-AzFrontDoorRulesEngineRuleObject -Name rules2 -Priority 3 -Action $rulesEngineAction
PS C:\AFD\azure-powershell\artifacts\Debug\Az.FrontDoor> Set-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1, $rulesEngineRule2

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1, rules2}
```

<span data-ttu-id="7863c-112">Szerezze be a meglévő szabálymotor konfigurációját, és vegyen fel hozzá egy másik szabálymotorszabályt.</span><span class="sxs-lookup"><span data-stu-id="7863c-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="7863c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7863c-113">PARAMETERS</span></span>

### <span data-ttu-id="7863c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7863c-114">-DefaultProfile</span></span>
<span data-ttu-id="7863c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7863c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7863c-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="7863c-116">-FrontDoorName</span></span>
<span data-ttu-id="7863c-117">Front Door name.</span><span class="sxs-lookup"><span data-stu-id="7863c-117">Front Door name.</span></span>

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

### <span data-ttu-id="7863c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7863c-118">-InputObject</span></span>
<span data-ttu-id="7863c-119">Frissítenünk kell a Szabálymotor objektumot.</span><span class="sxs-lookup"><span data-stu-id="7863c-119">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="7863c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7863c-120">-Name</span></span>
<span data-ttu-id="7863c-121">A szabálymotor neve.</span><span class="sxs-lookup"><span data-stu-id="7863c-121">Rules engine name.</span></span>

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

### <span data-ttu-id="7863c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7863c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7863c-123">Az erőforráscsoport neve, amelyből a front door lesz létrehozva.</span><span class="sxs-lookup"><span data-stu-id="7863c-123">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="7863c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7863c-124">-ResourceId</span></span>
<span data-ttu-id="7863c-125">Frissítend kell a RulesEngine erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7863c-125">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="7863c-126">-Rule</span><span class="sxs-lookup"><span data-stu-id="7863c-126">-Rule</span></span>
<span data-ttu-id="7863c-127">Egy adott szabálymotor-konfigurációt definiáló szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="7863c-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7863c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7863c-128">-Confirm</span></span>
<span data-ttu-id="7863c-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7863c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7863c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7863c-130">-WhatIf</span></span>
<span data-ttu-id="7863c-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7863c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7863c-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7863c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7863c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7863c-133">CommonParameters</span></span>
<span data-ttu-id="7863c-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7863c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7863c-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7863c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7863c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7863c-136">INPUTS</span></span>

### <span data-ttu-id="7863c-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="7863c-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="7863c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7863c-138">System.String</span></span>

## <span data-ttu-id="7863c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7863c-139">OUTPUTS</span></span>

### <span data-ttu-id="7863c-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="7863c-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="7863c-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7863c-141">NOTES</span></span>

## <span data-ttu-id="7863c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7863c-142">RELATED LINKS</span></span>
