---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184527"
---
# <span data-ttu-id="8827e-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="8827e-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="8827e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8827e-102">SYNOPSIS</span></span>
<span data-ttu-id="8827e-103">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="8827e-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="8827e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8827e-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8827e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8827e-105">DESCRIPTION</span></span>
<span data-ttu-id="8827e-106">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="8827e-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="8827e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8827e-107">EXAMPLES</span></span>

### <span data-ttu-id="8827e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8827e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="8827e-109">CustomRule objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="8827e-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="8827e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8827e-110">PARAMETERS</span></span>

### <span data-ttu-id="8827e-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="8827e-111">-Action</span></span>
<span data-ttu-id="8827e-112">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="8827e-112">Type of Actions.</span></span>
<span data-ttu-id="8827e-113">A lehetséges értékek a következők: "Allow", "blokk", "log"</span><span class="sxs-lookup"><span data-stu-id="8827e-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="8827e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8827e-114">-DefaultProfile</span></span>
<span data-ttu-id="8827e-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8827e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8827e-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8827e-116">-EnabledState</span></span>
<span data-ttu-id="8827e-117">Engedélyezett állapot</span><span class="sxs-lookup"><span data-stu-id="8827e-117">Enabled State.</span></span> <span data-ttu-id="8827e-118">A lehetséges értékek a következők: "engedélyezve", "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="8827e-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="8827e-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="8827e-119">-MatchCondition</span></span>
<span data-ttu-id="8827e-120">A egyeztetési feltételek listája.</span><span class="sxs-lookup"><span data-stu-id="8827e-120">List of match conditions.</span></span>

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

### <span data-ttu-id="8827e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8827e-121">-Name</span></span>
<span data-ttu-id="8827e-122">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="8827e-122">Name of the rule</span></span>

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

### <span data-ttu-id="8827e-123">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="8827e-123">-Priority</span></span>
<span data-ttu-id="8827e-124">A szabály prioritását ismerteti.</span><span class="sxs-lookup"><span data-stu-id="8827e-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="8827e-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="8827e-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="8827e-126">A mérték korlátjának időtartama.</span><span class="sxs-lookup"><span data-stu-id="8827e-126">Rate limit duration.</span></span> <span data-ttu-id="8827e-127">Default-1 perc</span><span class="sxs-lookup"><span data-stu-id="8827e-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="8827e-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="8827e-128">-RateLimitThreshold</span></span>
<span data-ttu-id="8827e-129">Ráta korlátozási küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="8827e-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="8827e-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="8827e-130">-RuleType</span></span>
<span data-ttu-id="8827e-131">A szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="8827e-131">Type of the rule.</span></span>
<span data-ttu-id="8827e-132">A lehetséges értékek a következők: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="8827e-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="8827e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8827e-133">CommonParameters</span></span>
<span data-ttu-id="8827e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8827e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8827e-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8827e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8827e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8827e-136">INPUTS</span></span>

### <span data-ttu-id="8827e-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="8827e-137">None</span></span>

## <span data-ttu-id="8827e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8827e-138">OUTPUTS</span></span>

### <span data-ttu-id="8827e-139">Microsoft. Azure. Command. FrontDoor. models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="8827e-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="8827e-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8827e-140">NOTES</span></span>

## <span data-ttu-id="8827e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8827e-141">RELATED LINKS</span></span>

<span data-ttu-id="8827e-142">[Új – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="8827e-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
