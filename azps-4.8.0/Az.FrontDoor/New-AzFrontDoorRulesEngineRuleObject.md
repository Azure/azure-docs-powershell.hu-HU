---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017755"
---
# <span data-ttu-id="cf9f8-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="cf9f8-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="cf9f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf9f8-102">SYNOPSIS</span></span>
<span data-ttu-id="cf9f8-103">PSRulesEngineRule objektum létrehozása szabályok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="cf9f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf9f8-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf9f8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf9f8-105">DESCRIPTION</span></span>
<span data-ttu-id="cf9f8-106">PSRulesEngineRule objektum létrehozása szabályok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="cf9f8-107">A parancsmag "New-AzFrontDoorRulesEngineActionObject" (parancsmag "New-") segítségével hozzon létre PSRulesEngineAction objektumot a "-műveletek" paraméterre való átlépéshez.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="cf9f8-108">A parancsmag "New-AzFrontDoorRulesEngineMatchConditionObject" paranccsal PSRulesEngineMatchCondition objektumot hozhat létre a "-MatchCondition" paraméterre való átlépéshez.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="cf9f8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cf9f8-109">EXAMPLES</span></span>

### <span data-ttu-id="cf9f8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf9f8-110">Example 1</span></span>
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

<span data-ttu-id="cf9f8-111">Új PSRulesEngineRule objektum létrehozása és az almezők megjelenítésének bemutatása</span><span class="sxs-lookup"><span data-stu-id="cf9f8-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="cf9f8-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="cf9f8-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="cf9f8-113">A kimenet várható értéke érvénytelen prioritású érték elküldésekor.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="cf9f8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf9f8-114">PARAMETERS</span></span>

### <span data-ttu-id="cf9f8-115">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="cf9f8-115">-Action</span></span>
<span data-ttu-id="cf9f8-116">A kérésen és válaszon végrehajtandó műveletek, ha az összes egyezési feltétel teljesül.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

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

### <span data-ttu-id="cf9f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf9f8-117">-DefaultProfile</span></span>
<span data-ttu-id="cf9f8-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf9f8-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="cf9f8-119">-MatchCondition</span></span>
<span data-ttu-id="cf9f8-120">Azoknak a feltételeknek a listája, amelyeknek meg kell felelnie ahhoz, hogy az adott szabály futása végrehajtható legyen.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="cf9f8-121">Ha nincs egyezési feltétel, a művelet mindig futni fog.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-121">Having no match conditions means the actions will always run.</span></span>

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

### <span data-ttu-id="cf9f8-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="cf9f8-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="cf9f8-123">Ha ez a szabály a megfelelő, akkor a szabályok motorja továbbra is futtatja a fennmaradó szabályokat, vagy leáll.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="cf9f8-124">A lehetséges értékek folytatódnak és megállnak.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="cf9f8-125">Ha nincs megadva, az alapértelmezett érték a folytatáshoz.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-125">If not present, defaults to Continue.</span></span>

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

### <span data-ttu-id="cf9f8-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf9f8-126">-Name</span></span>
<span data-ttu-id="cf9f8-127">Az adott szabályra hivatkozó név.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="cf9f8-128">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="cf9f8-128">-Priority</span></span>
<span data-ttu-id="cf9f8-129">A szabályhoz hozzárendelt prioritás.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="cf9f8-130">Nem lehet negatív.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-130">Cannot be negative.</span></span>

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

### <span data-ttu-id="cf9f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf9f8-131">CommonParameters</span></span>
<span data-ttu-id="cf9f8-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf9f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf9f8-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cf9f8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf9f8-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf9f8-134">INPUTS</span></span>

### <span data-ttu-id="cf9f8-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="cf9f8-135">None</span></span>

## <span data-ttu-id="cf9f8-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf9f8-136">OUTPUTS</span></span>

### <span data-ttu-id="cf9f8-137">Microsoft. Azure. Command. FrontDoor. models. PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="cf9f8-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="cf9f8-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf9f8-138">NOTES</span></span>

## <span data-ttu-id="cf9f8-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf9f8-139">RELATED LINKS</span></span>
