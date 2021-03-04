---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: cf74b21d2b07ddf8f92203c43e7005f81cbb2a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928081"
---
# <span data-ttu-id="ae894-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="ae894-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="ae894-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae894-102">SYNOPSIS</span></span>
<span data-ttu-id="ae894-103">CustomRule objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="ae894-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="ae894-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ae894-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae894-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ae894-105">DESCRIPTION</span></span>
<span data-ttu-id="ae894-106">CustomRule objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="ae894-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="ae894-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ae894-107">EXAMPLES</span></span>

### <span data-ttu-id="ae894-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ae894-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="ae894-109">CustomRule-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ae894-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="ae894-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae894-110">PARAMETERS</span></span>

### <span data-ttu-id="ae894-111">-Művelet</span><span class="sxs-lookup"><span data-stu-id="ae894-111">-Action</span></span>
<span data-ttu-id="ae894-112">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="ae894-112">Type of Actions.</span></span>
<span data-ttu-id="ae894-113">Lehetséges értékek: "Megengedve", "Blokk", "Napló"</span><span class="sxs-lookup"><span data-stu-id="ae894-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="ae894-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae894-114">-DefaultProfile</span></span>
<span data-ttu-id="ae894-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae894-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae894-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ae894-116">-EnabledState</span></span>
<span data-ttu-id="ae894-117">Engedélyezett állapot.</span><span class="sxs-lookup"><span data-stu-id="ae894-117">Enabled State.</span></span> <span data-ttu-id="ae894-118">Lehetséges értékek: "Engedélyezve", "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="ae894-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="ae894-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="ae894-119">-MatchCondition</span></span>
<span data-ttu-id="ae894-120">Az egyezések feltételeinek listája.</span><span class="sxs-lookup"><span data-stu-id="ae894-120">List of match conditions.</span></span>

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

### <span data-ttu-id="ae894-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ae894-121">-Name</span></span>
<span data-ttu-id="ae894-122">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="ae894-122">Name of the rule</span></span>

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

### <span data-ttu-id="ae894-123">-Priority</span><span class="sxs-lookup"><span data-stu-id="ae894-123">-Priority</span></span>
<span data-ttu-id="ae894-124">Ismerteti a szabály prioritását.</span><span class="sxs-lookup"><span data-stu-id="ae894-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="ae894-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="ae894-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="ae894-126">Díjkorlát időtartama.</span><span class="sxs-lookup"><span data-stu-id="ae894-126">Rate limit duration.</span></span> <span data-ttu-id="ae894-127">Alapértelmezett – 1 perc</span><span class="sxs-lookup"><span data-stu-id="ae894-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="ae894-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="ae894-128">-RateLimitThreshold</span></span>
<span data-ttu-id="ae894-129">Díjkorlát küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="ae894-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="ae894-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="ae894-130">-RuleType</span></span>
<span data-ttu-id="ae894-131">A szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="ae894-131">Type of the rule.</span></span>
<span data-ttu-id="ae894-132">Lehetséges értékek: "MatchRule", 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="ae894-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="ae894-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae894-133">CommonParameters</span></span>
<span data-ttu-id="ae894-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae894-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae894-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae894-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae894-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae894-136">INPUTS</span></span>

### <span data-ttu-id="ae894-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="ae894-137">None</span></span>

## <span data-ttu-id="ae894-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae894-138">OUTPUTS</span></span>

### <span data-ttu-id="ae894-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="ae894-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="ae894-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ae894-140">NOTES</span></span>

## <span data-ttu-id="ae894-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae894-141">RELATED LINKS</span></span>

<span data-ttu-id="ae894-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="ae894-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
