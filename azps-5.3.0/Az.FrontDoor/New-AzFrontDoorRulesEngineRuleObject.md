---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466115"
---
# <span data-ttu-id="29277-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="29277-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="29277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29277-102">SYNOPSIS</span></span>
<span data-ttu-id="29277-103">PSRulesEngineRule-objektumot hozhat létre a Szabálymotor létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="29277-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="29277-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="29277-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29277-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="29277-105">DESCRIPTION</span></span>
<span data-ttu-id="29277-106">PSRulesEngineRule-objektumot hozhat létre a Szabálymotor létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="29277-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="29277-107">A "New-AzFrontDoorRulesEngineActionObject" parancsmag használatával hozzon létre PSRulesEngineAction objektumot, és adja át a "-Action" paraméternek.</span><span class="sxs-lookup"><span data-stu-id="29277-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="29277-108">A "New-AzFrontDoorRulesEngineMatchConditionObject" parancsmag használatával hozzon létre PSRulesEngineMatchCondition objektumot a "-MatchCondition" paraméterbe való áthaladáshoz.</span><span class="sxs-lookup"><span data-stu-id="29277-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="29277-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="29277-109">EXAMPLES</span></span>

### <span data-ttu-id="29277-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="29277-110">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority 0 -Action $rulesEngineAction -MatchProcessingBehavior Stop -MatchCondition $rulesEngineMatchCondition

Name                    : rules1
Priority                : 0
MatchProcessingBehavior : Stop
MatchCondition          : {Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition}
Action                  : Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction


PS C:\> $rulesEngineRule1.Action

RequestHeaderActions           ResponseHeaderActions RouteConfigurationOverride
--------------------           --------------------- --------------------------
{headeraction1, headeraction2} {}                    Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineRule1.MatchCondition[0]

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transforms               : {Lowercase, Uppercase}
```

<span data-ttu-id="29277-111">Hozzon létre új PSRulesEngineRule objektumot, és mutassa be, hogyan láthatja az almezőket.</span><span class="sxs-lookup"><span data-stu-id="29277-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="29277-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="29277-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="29277-113">Kimenet elvárása érvénytelen prioritású érték esetén.</span><span class="sxs-lookup"><span data-stu-id="29277-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="29277-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29277-114">PARAMETERS</span></span>

### <span data-ttu-id="29277-115">-Művelet</span><span class="sxs-lookup"><span data-stu-id="29277-115">-Action</span></span>
<span data-ttu-id="29277-116">A kérelem és a válasz végrehajtásához szükséges műveletek, ha az összes egyezés feltétel teljesül.</span><span class="sxs-lookup"><span data-stu-id="29277-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29277-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29277-117">-DefaultProfile</span></span>
<span data-ttu-id="29277-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29277-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29277-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="29277-119">-MatchCondition</span></span>
<span data-ttu-id="29277-120">Az egyező feltételek listája, amelyeknek meg kell felelnie a szabályműveletek futtatásához.</span><span class="sxs-lookup"><span data-stu-id="29277-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="29277-121">Ha nem teljesülnek a feltételek, a műveletek mindig futni fognak.</span><span class="sxs-lookup"><span data-stu-id="29277-121">Having no match conditions means the actions will always run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29277-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="29277-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="29277-123">Ha ez a szabály egyezés, akkor a szabálymotor továbbra is futtatja a hátralévő szabályokat, vagy leáll.</span><span class="sxs-lookup"><span data-stu-id="29277-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="29277-124">Lehetséges értékek: Folytatás és Leállítás.</span><span class="sxs-lookup"><span data-stu-id="29277-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="29277-125">Ha nincs jelen, az alapértelmezett beállítás a Folytatás.</span><span class="sxs-lookup"><span data-stu-id="29277-125">If not present, defaults to Continue.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchProcessingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: Continue, Stop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29277-126">-Name</span><span class="sxs-lookup"><span data-stu-id="29277-126">-Name</span></span>
<span data-ttu-id="29277-127">Az adott szabályra hivatkozó név.</span><span class="sxs-lookup"><span data-stu-id="29277-127">A name to refer to this specific rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29277-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="29277-128">-Priority</span></span>
<span data-ttu-id="29277-129">A szabályhoz rendelt prioritás.</span><span class="sxs-lookup"><span data-stu-id="29277-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="29277-130">Nem lehet negatív.</span><span class="sxs-lookup"><span data-stu-id="29277-130">Cannot be negative.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29277-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29277-131">CommonParameters</span></span>
<span data-ttu-id="29277-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29277-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29277-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29277-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29277-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29277-134">INPUTS</span></span>

### <span data-ttu-id="29277-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="29277-135">None</span></span>

## <span data-ttu-id="29277-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29277-136">OUTPUTS</span></span>

### <span data-ttu-id="29277-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="29277-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="29277-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="29277-138">NOTES</span></span>

## <span data-ttu-id="29277-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29277-139">RELATED LINKS</span></span>
