---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 6c40a54dd230bc4c7e45f97b4fa6f969940e1673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666416"
---
# <span data-ttu-id="6be69-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="6be69-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="6be69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6be69-102">SYNOPSIS</span></span>
<span data-ttu-id="6be69-103">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="6be69-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="6be69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6be69-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6be69-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6be69-105">DESCRIPTION</span></span>
<span data-ttu-id="6be69-106">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="6be69-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="6be69-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6be69-107">EXAMPLES</span></span>

### <span data-ttu-id="6be69-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6be69-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="6be69-109">CustomRule objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="6be69-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="6be69-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6be69-110">PARAMETERS</span></span>

### <span data-ttu-id="6be69-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="6be69-111">-Action</span></span>
<span data-ttu-id="6be69-112">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="6be69-112">Type of Actions.</span></span>
<span data-ttu-id="6be69-113">A lehetséges értékek a következők: "Allow", "blokk", "log"</span><span class="sxs-lookup"><span data-stu-id="6be69-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="6be69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be69-114">-DefaultProfile</span></span>
<span data-ttu-id="6be69-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6be69-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6be69-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="6be69-116">-MatchCondition</span></span>
<span data-ttu-id="6be69-117">A egyeztetési feltételek listája.</span><span class="sxs-lookup"><span data-stu-id="6be69-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6be69-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6be69-118">-Name</span></span>
<span data-ttu-id="6be69-119">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="6be69-119">Name of the rule</span></span>

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

### <span data-ttu-id="6be69-120">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="6be69-120">-Priority</span></span>
<span data-ttu-id="6be69-121">A szabály prioritását ismerteti.</span><span class="sxs-lookup"><span data-stu-id="6be69-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="6be69-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="6be69-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="6be69-123">A mérték korlátjának időtartama.</span><span class="sxs-lookup"><span data-stu-id="6be69-123">Rate limit duration.</span></span> <span data-ttu-id="6be69-124">Default-1 perc</span><span class="sxs-lookup"><span data-stu-id="6be69-124">Default - 1 minute</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6be69-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="6be69-125">-RateLimitThreshold</span></span>
<span data-ttu-id="6be69-126">Ráta korlátozási küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="6be69-126">Rate limit threshold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6be69-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6be69-127">-RuleType</span></span>
<span data-ttu-id="6be69-128">A szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="6be69-128">Type of the rule.</span></span>
<span data-ttu-id="6be69-129">A lehetséges értékek a következők: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="6be69-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="6be69-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be69-130">CommonParameters</span></span>
<span data-ttu-id="6be69-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6be69-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be69-132">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6be69-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be69-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6be69-133">INPUTS</span></span>

### <span data-ttu-id="6be69-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="6be69-134">None</span></span>

## <span data-ttu-id="6be69-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6be69-135">OUTPUTS</span></span>

### <span data-ttu-id="6be69-136">Microsoft. Azure. Command. FrontDoor. models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="6be69-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="6be69-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6be69-137">NOTES</span></span>

## <span data-ttu-id="6be69-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6be69-138">RELATED LINKS</span></span>

<span data-ttu-id="6be69-139">[Új – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="6be69-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
