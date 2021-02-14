---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147867"
---
# <span data-ttu-id="e8b78-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="e8b78-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="e8b78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8b78-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b78-103">Felügyelt szabálykizárási objektum létrehozása a waf felügyelt szabálykészletek, -csoportok és -szabályok számára.</span><span class="sxs-lookup"><span data-stu-id="e8b78-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="e8b78-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e8b78-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8b78-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e8b78-105">DESCRIPTION</span></span>
<span data-ttu-id="e8b78-106">Felügyelt szabálykizárási objektum létrehozása a waf felügyelt szabálykészletek, -csoportok és -szabályok számára.</span><span class="sxs-lookup"><span data-stu-id="e8b78-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="e8b78-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e8b78-107">EXAMPLES</span></span>

### <span data-ttu-id="e8b78-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e8b78-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="e8b78-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8b78-109">PARAMETERS</span></span>

### <span data-ttu-id="e8b78-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b78-110">-DefaultProfile</span></span>
<span data-ttu-id="e8b78-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8b78-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8b78-112">-Operátor</span><span class="sxs-lookup"><span data-stu-id="e8b78-112">-Operator</span></span>
<span data-ttu-id="e8b78-113">Operátor, amely a választó egyeztetésekor használható, az EqualsAny azt jelenti, hogy nincs kiválasztó (a megadott típusú összes egyező változó)</span><span class="sxs-lookup"><span data-stu-id="e8b78-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="e8b78-114">-Választó</span><span class="sxs-lookup"><span data-stu-id="e8b78-114">-Selector</span></span>
<span data-ttu-id="e8b78-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span><span class="sxs-lookup"><span data-stu-id="e8b78-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b78-116">-Variable</span><span class="sxs-lookup"><span data-stu-id="e8b78-116">-Variable</span></span>
<span data-ttu-id="e8b78-117">Változó egyeztetése</span><span class="sxs-lookup"><span data-stu-id="e8b78-117">Match variable.</span></span> <span data-ttu-id="e8b78-118">Lehetséges értékek: RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestNamePostArgNames.</span><span class="sxs-lookup"><span data-stu-id="e8b78-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="e8b78-119">A QueryStringArgNames például kivételt ad a választónak a megadott operátorral egyező GET paraméterekből.</span><span class="sxs-lookup"><span data-stu-id="e8b78-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="e8b78-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b78-120">CommonParameters</span></span>
<span data-ttu-id="e8b78-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8b78-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b78-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8b78-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b78-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8b78-123">INPUTS</span></span>

### <span data-ttu-id="e8b78-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="e8b78-124">None</span></span>

## <span data-ttu-id="e8b78-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8b78-125">OUTPUTS</span></span>

### <span data-ttu-id="e8b78-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="e8b78-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="e8b78-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e8b78-127">NOTES</span></span>

## <span data-ttu-id="e8b78-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8b78-128">RELATED LINKS</span></span>

<span data-ttu-id="e8b78-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="e8b78-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
