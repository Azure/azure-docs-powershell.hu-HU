---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187404"
---
# <span data-ttu-id="aa9b9-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="aa9b9-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="aa9b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9b9-103">Felügyelt szabály-kizárási objektum létrehozása a felügyelt WAF, csoportoknak vagy szabályoknak.</span><span class="sxs-lookup"><span data-stu-id="aa9b9-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="aa9b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa9b9-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa9b9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa9b9-105">DESCRIPTION</span></span>
<span data-ttu-id="aa9b9-106">Felügyelt szabály-kizárási objektum létrehozása a felügyelt WAF, csoportoknak vagy szabályoknak.</span><span class="sxs-lookup"><span data-stu-id="aa9b9-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="aa9b9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa9b9-107">EXAMPLES</span></span>

### <span data-ttu-id="aa9b9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aa9b9-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="aa9b9-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa9b9-109">PARAMETERS</span></span>

### <span data-ttu-id="aa9b9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa9b9-110">-DefaultProfile</span></span>
<span data-ttu-id="aa9b9-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa9b9-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa9b9-112">-Operátor</span><span class="sxs-lookup"><span data-stu-id="aa9b9-112">-Operator</span></span>
<span data-ttu-id="aa9b9-113">Az operátor, amely a kijelölő párosításakor használatos, a EqualsAny azt jelenti, hogy nincs kiválasztó (a megadott típus minden egyezési változója)</span><span class="sxs-lookup"><span data-stu-id="aa9b9-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="aa9b9-114">-Választó</span><span class="sxs-lookup"><span data-stu-id="aa9b9-114">-Selector</span></span>
<span data-ttu-id="aa9b9-115">Kiválasztó minta az operátor használatával való egyeztetéshez (ha az operátor nem EqualsAny)</span><span class="sxs-lookup"><span data-stu-id="aa9b9-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="aa9b9-116">-Változó</span><span class="sxs-lookup"><span data-stu-id="aa9b9-116">-Variable</span></span>
<span data-ttu-id="aa9b9-117">Egyezés változó</span><span class="sxs-lookup"><span data-stu-id="aa9b9-117">Match variable.</span></span> <span data-ttu-id="aa9b9-118">Lehetséges értékek: RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="aa9b9-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="aa9b9-119">A QueryStringArgNames például nem számítja ki a megadott operátorral a szelektorhoz illő paramétereket.</span><span class="sxs-lookup"><span data-stu-id="aa9b9-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="aa9b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9b9-120">CommonParameters</span></span>
<span data-ttu-id="aa9b9-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa9b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9b9-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aa9b9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9b9-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa9b9-123">INPUTS</span></span>

### <span data-ttu-id="aa9b9-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="aa9b9-124">None</span></span>

## <span data-ttu-id="aa9b9-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa9b9-125">OUTPUTS</span></span>

### <span data-ttu-id="aa9b9-126">Microsoft. Azure. Command. FrontDoor. models. PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="aa9b9-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="aa9b9-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa9b9-127">NOTES</span></span>

## <span data-ttu-id="aa9b9-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa9b9-128">RELATED LINKS</span></span>

<span data-ttu-id="aa9b9-129">[Új – AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [Új – AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [Új – AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="aa9b9-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
