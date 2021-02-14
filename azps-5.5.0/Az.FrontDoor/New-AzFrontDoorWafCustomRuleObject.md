---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147883"
---
# <span data-ttu-id="b17a7-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="b17a7-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="b17a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b17a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b17a7-103">CustomRule objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="b17a7-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b17a7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b17a7-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b17a7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b17a7-105">DESCRIPTION</span></span>
<span data-ttu-id="b17a7-106">CustomRule objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="b17a7-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b17a7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b17a7-107">EXAMPLES</span></span>

### <span data-ttu-id="b17a7-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b17a7-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="b17a7-109">CustomRule-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="b17a7-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="b17a7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b17a7-110">PARAMETERS</span></span>

### <span data-ttu-id="b17a7-111">-Művelet</span><span class="sxs-lookup"><span data-stu-id="b17a7-111">-Action</span></span>
<span data-ttu-id="b17a7-112">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="b17a7-112">Type of Actions.</span></span>
<span data-ttu-id="b17a7-113">Lehetséges értékek: "Megengedve", "Blokk", "Napló"</span><span class="sxs-lookup"><span data-stu-id="b17a7-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="b17a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b17a7-114">-DefaultProfile</span></span>
<span data-ttu-id="b17a7-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b17a7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b17a7-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b17a7-116">-EnabledState</span></span>
<span data-ttu-id="b17a7-117">Engedélyezett állapot.</span><span class="sxs-lookup"><span data-stu-id="b17a7-117">Enabled State.</span></span> <span data-ttu-id="b17a7-118">Lehetséges értékek: "Engedélyezve", "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="b17a7-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="b17a7-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="b17a7-119">-MatchCondition</span></span>
<span data-ttu-id="b17a7-120">Az egyezések feltételeinek listája.</span><span class="sxs-lookup"><span data-stu-id="b17a7-120">List of match conditions.</span></span>

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

### <span data-ttu-id="b17a7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b17a7-121">-Name</span></span>
<span data-ttu-id="b17a7-122">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="b17a7-122">Name of the rule</span></span>

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

### <span data-ttu-id="b17a7-123">-Priority</span><span class="sxs-lookup"><span data-stu-id="b17a7-123">-Priority</span></span>
<span data-ttu-id="b17a7-124">Ismerteti a szabály prioritását.</span><span class="sxs-lookup"><span data-stu-id="b17a7-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="b17a7-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="b17a7-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="b17a7-126">Díjkorlát időtartama.</span><span class="sxs-lookup"><span data-stu-id="b17a7-126">Rate limit duration.</span></span> <span data-ttu-id="b17a7-127">Alapértelmezett – 1 perc</span><span class="sxs-lookup"><span data-stu-id="b17a7-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="b17a7-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="b17a7-128">-RateLimitThreshold</span></span>
<span data-ttu-id="b17a7-129">Díjkorlát küszöbértéke</span><span class="sxs-lookup"><span data-stu-id="b17a7-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="b17a7-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="b17a7-130">-RuleType</span></span>
<span data-ttu-id="b17a7-131">A szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="b17a7-131">Type of the rule.</span></span>
<span data-ttu-id="b17a7-132">Lehetséges értékek: "MatchRule", 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="b17a7-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="b17a7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b17a7-133">CommonParameters</span></span>
<span data-ttu-id="b17a7-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b17a7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b17a7-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b17a7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b17a7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b17a7-136">INPUTS</span></span>

### <span data-ttu-id="b17a7-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="b17a7-137">None</span></span>

## <span data-ttu-id="b17a7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b17a7-138">OUTPUTS</span></span>

### <span data-ttu-id="b17a7-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="b17a7-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="b17a7-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b17a7-140">NOTES</span></span>

## <span data-ttu-id="b17a7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b17a7-141">RELATED LINKS</span></span>

<span data-ttu-id="b17a7-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="b17a7-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
