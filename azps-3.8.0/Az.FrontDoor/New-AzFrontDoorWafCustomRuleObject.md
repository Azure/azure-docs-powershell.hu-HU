---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: d352f70d28b9bfafae46697fb6d69dc50c739b19
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013838"
---
# <span data-ttu-id="6e582-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="6e582-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="6e582-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e582-102">SYNOPSIS</span></span>
<span data-ttu-id="6e582-103">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="6e582-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="6e582-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e582-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e582-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e582-105">DESCRIPTION</span></span>
<span data-ttu-id="6e582-106">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="6e582-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="6e582-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6e582-107">EXAMPLES</span></span>

### <span data-ttu-id="6e582-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6e582-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="6e582-109">CustomRule objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="6e582-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="6e582-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e582-110">PARAMETERS</span></span>

### <span data-ttu-id="6e582-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="6e582-111">-Action</span></span>
<span data-ttu-id="6e582-112">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="6e582-112">Type of Actions.</span></span>
<span data-ttu-id="6e582-113">A lehetséges értékek a következők: "Allow", "blokk", "log"</span><span class="sxs-lookup"><span data-stu-id="6e582-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="6e582-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e582-114">-DefaultProfile</span></span>
<span data-ttu-id="6e582-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e582-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e582-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="6e582-116">-EnabledState</span></span>
<span data-ttu-id="6e582-117">Engedélyezett állapot</span><span class="sxs-lookup"><span data-stu-id="6e582-117">Enabled State.</span></span> <span data-ttu-id="6e582-118">A lehetséges értékek a következők: "engedélyezve", "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="6e582-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="6e582-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="6e582-119">-MatchCondition</span></span>
<span data-ttu-id="6e582-120">A egyeztetési feltételek listája.</span><span class="sxs-lookup"><span data-stu-id="6e582-120">List of match conditions.</span></span>

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

### <span data-ttu-id="6e582-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e582-121">-Name</span></span>
<span data-ttu-id="6e582-122">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="6e582-122">Name of the rule</span></span>

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

### <span data-ttu-id="6e582-123">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="6e582-123">-Priority</span></span>
<span data-ttu-id="6e582-124">A szabály prioritását ismerteti.</span><span class="sxs-lookup"><span data-stu-id="6e582-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="6e582-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="6e582-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="6e582-126">A mérték korlátjának időtartama.</span><span class="sxs-lookup"><span data-stu-id="6e582-126">Rate limit duration.</span></span> <span data-ttu-id="6e582-127">Default-1 perc</span><span class="sxs-lookup"><span data-stu-id="6e582-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="6e582-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="6e582-128">-RateLimitThreshold</span></span>
<span data-ttu-id="6e582-129">Ráta korlátozási küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="6e582-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="6e582-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6e582-130">-RuleType</span></span>
<span data-ttu-id="6e582-131">A szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="6e582-131">Type of the rule.</span></span>
<span data-ttu-id="6e582-132">A lehetséges értékek a következők: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="6e582-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="6e582-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e582-133">CommonParameters</span></span>
<span data-ttu-id="6e582-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e582-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e582-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6e582-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e582-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e582-136">INPUTS</span></span>

### <span data-ttu-id="6e582-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="6e582-137">None</span></span>

## <span data-ttu-id="6e582-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e582-138">OUTPUTS</span></span>

### <span data-ttu-id="6e582-139">Microsoft. Azure. Command. FrontDoor. models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="6e582-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="6e582-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e582-140">NOTES</span></span>

## <span data-ttu-id="6e582-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e582-141">RELATED LINKS</span></span>

<span data-ttu-id="6e582-142">[Új – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="6e582-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
