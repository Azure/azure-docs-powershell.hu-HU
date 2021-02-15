---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 8602bd4636e3e6034552f48a6f6514a453b816a0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400671"
---
# <span data-ttu-id="e3950-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="e3950-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="e3950-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3950-102">SYNOPSIS</span></span>
<span data-ttu-id="e3950-103">CustomRule objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="e3950-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="e3950-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3950-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3950-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3950-105">DESCRIPTION</span></span>
<span data-ttu-id="e3950-106">Create CustomRule Object for WAF policy creation</span><span class="sxs-lookup"><span data-stu-id="e3950-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="e3950-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3950-107">EXAMPLES</span></span>

### <span data-ttu-id="e3950-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e3950-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="e3950-109">CustomRule-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="e3950-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="e3950-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3950-110">PARAMETERS</span></span>

### <span data-ttu-id="e3950-111">-Action</span><span class="sxs-lookup"><span data-stu-id="e3950-111">-Action</span></span>
<span data-ttu-id="e3950-112">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="e3950-112">Type of Actions.</span></span>
<span data-ttu-id="e3950-113">Lehetséges értékek: "Megengedve", "Blokk", "Napló"</span><span class="sxs-lookup"><span data-stu-id="e3950-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3950-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3950-114">-DefaultProfile</span></span>
<span data-ttu-id="e3950-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3950-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3950-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="e3950-116">-MatchCondition</span></span>
<span data-ttu-id="e3950-117">Az egyezések feltételeinek listája.</span><span class="sxs-lookup"><span data-stu-id="e3950-117">List of match conditions.</span></span>

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

### <span data-ttu-id="e3950-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e3950-118">-Name</span></span>
<span data-ttu-id="e3950-119">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="e3950-119">Name of the rule</span></span>

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

### <span data-ttu-id="e3950-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="e3950-120">-Priority</span></span>
<span data-ttu-id="e3950-121">Ismerteti a szabály prioritását.</span><span class="sxs-lookup"><span data-stu-id="e3950-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="e3950-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="e3950-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="e3950-123">Díjkorlát időtartama.</span><span class="sxs-lookup"><span data-stu-id="e3950-123">Rate limit duration.</span></span> <span data-ttu-id="e3950-124">Alapértelmezett – 1 perc</span><span class="sxs-lookup"><span data-stu-id="e3950-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="e3950-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="e3950-125">-RateLimitThreshold</span></span>
<span data-ttu-id="e3950-126">Rátakorlát</span><span class="sxs-lookup"><span data-stu-id="e3950-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="e3950-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e3950-127">-RuleType</span></span>
<span data-ttu-id="e3950-128">A szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="e3950-128">Type of the rule.</span></span>
<span data-ttu-id="e3950-129">Lehetséges értékek: "MatchRule", 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="e3950-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3950-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3950-130">CommonParameters</span></span>
<span data-ttu-id="e3950-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3950-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3950-132">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3950-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3950-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3950-133">INPUTS</span></span>

### <span data-ttu-id="e3950-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="e3950-134">None</span></span>

## <span data-ttu-id="e3950-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3950-135">OUTPUTS</span></span>

### <span data-ttu-id="e3950-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="e3950-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="e3950-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3950-137">NOTES</span></span>

## <span data-ttu-id="e3950-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3950-138">RELATED LINKS</span></span>

<span data-ttu-id="e3950-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="e3950-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span></span>
