---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184522"
---
# <span data-ttu-id="0159c-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="0159c-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="0159c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0159c-102">SYNOPSIS</span></span>
<span data-ttu-id="0159c-103">Felügyelt szabály-kizárási objektum létrehozása a felügyelt WAF, csoportoknak vagy szabályoknak.</span><span class="sxs-lookup"><span data-stu-id="0159c-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="0159c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0159c-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0159c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0159c-105">DESCRIPTION</span></span>
<span data-ttu-id="0159c-106">Felügyelt szabály-kizárási objektum létrehozása a felügyelt WAF, csoportoknak vagy szabályoknak.</span><span class="sxs-lookup"><span data-stu-id="0159c-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="0159c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0159c-107">EXAMPLES</span></span>

### <span data-ttu-id="0159c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0159c-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="0159c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0159c-109">PARAMETERS</span></span>

### <span data-ttu-id="0159c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0159c-110">-DefaultProfile</span></span>
<span data-ttu-id="0159c-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0159c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0159c-112">-Operátor</span><span class="sxs-lookup"><span data-stu-id="0159c-112">-Operator</span></span>
<span data-ttu-id="0159c-113">Az operátor, amely a kijelölő párosításakor használatos, a EqualsAny azt jelenti, hogy nincs kiválasztó (a megadott típus minden egyezési változója)</span><span class="sxs-lookup"><span data-stu-id="0159c-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="0159c-114">-Választó</span><span class="sxs-lookup"><span data-stu-id="0159c-114">-Selector</span></span>
<span data-ttu-id="0159c-115">Kiválasztó minta az operátor használatával való egyeztetéshez (ha az operátor nem EqualsAny)</span><span class="sxs-lookup"><span data-stu-id="0159c-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="0159c-116">-Változó</span><span class="sxs-lookup"><span data-stu-id="0159c-116">-Variable</span></span>
<span data-ttu-id="0159c-117">Egyezés változó</span><span class="sxs-lookup"><span data-stu-id="0159c-117">Match variable.</span></span> <span data-ttu-id="0159c-118">Lehetséges értékek: RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="0159c-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="0159c-119">A QueryStringArgNames például nem számítja ki a megadott operátorral a szelektorhoz illő paramétereket.</span><span class="sxs-lookup"><span data-stu-id="0159c-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="0159c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0159c-120">CommonParameters</span></span>
<span data-ttu-id="0159c-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0159c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0159c-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0159c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0159c-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0159c-123">INPUTS</span></span>

### <span data-ttu-id="0159c-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="0159c-124">None</span></span>

## <span data-ttu-id="0159c-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0159c-125">OUTPUTS</span></span>

### <span data-ttu-id="0159c-126">Microsoft. Azure. Command. FrontDoor. models. PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="0159c-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="0159c-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0159c-127">NOTES</span></span>

## <span data-ttu-id="0159c-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0159c-128">RELATED LINKS</span></span>

<span data-ttu-id="0159c-129">[Új – AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [Új – AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [Új – AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="0159c-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
