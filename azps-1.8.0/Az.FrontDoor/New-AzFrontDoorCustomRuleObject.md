---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 19f8215f8feaa1765da871f0fa38cc0120d842ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836170"
---
# <span data-ttu-id="64a0d-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="64a0d-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="64a0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="64a0d-103">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="64a0d-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="64a0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64a0d-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64a0d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64a0d-105">DESCRIPTION</span></span>
<span data-ttu-id="64a0d-106">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="64a0d-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="64a0d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64a0d-107">EXAMPLES</span></span>

### <span data-ttu-id="64a0d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="64a0d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="64a0d-109">CustomRule objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="64a0d-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="64a0d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64a0d-110">PARAMETERS</span></span>

### <span data-ttu-id="64a0d-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="64a0d-111">-Action</span></span>
<span data-ttu-id="64a0d-112">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="64a0d-112">Type of Actions.</span></span>
<span data-ttu-id="64a0d-113">A lehetséges értékek a következők: "Allow", "blokk", "log"</span><span class="sxs-lookup"><span data-stu-id="64a0d-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="64a0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a0d-114">-DefaultProfile</span></span>
<span data-ttu-id="64a0d-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64a0d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a0d-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="64a0d-116">-MatchCondition</span></span>
<span data-ttu-id="64a0d-117">A egyeztetési feltételek listája.</span><span class="sxs-lookup"><span data-stu-id="64a0d-117">List of match conditions.</span></span>

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

### <span data-ttu-id="64a0d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64a0d-118">-Name</span></span>
<span data-ttu-id="64a0d-119">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="64a0d-119">Name of the rule</span></span>

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

### <span data-ttu-id="64a0d-120">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="64a0d-120">-Priority</span></span>
<span data-ttu-id="64a0d-121">A szabály prioritását ismerteti.</span><span class="sxs-lookup"><span data-stu-id="64a0d-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="64a0d-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="64a0d-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="64a0d-123">A mérték korlátjának időtartama.</span><span class="sxs-lookup"><span data-stu-id="64a0d-123">Rate limit duration.</span></span> <span data-ttu-id="64a0d-124">Default-1 perc</span><span class="sxs-lookup"><span data-stu-id="64a0d-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="64a0d-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="64a0d-125">-RateLimitThreshold</span></span>
<span data-ttu-id="64a0d-126">Ráta limit thresold</span><span class="sxs-lookup"><span data-stu-id="64a0d-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="64a0d-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="64a0d-127">-RuleType</span></span>
<span data-ttu-id="64a0d-128">A szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="64a0d-128">Type of the rule.</span></span>
<span data-ttu-id="64a0d-129">A lehetséges értékek a következők: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="64a0d-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="64a0d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a0d-130">CommonParameters</span></span>
<span data-ttu-id="64a0d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64a0d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a0d-132">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="64a0d-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a0d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64a0d-133">INPUTS</span></span>

### <span data-ttu-id="64a0d-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="64a0d-134">None</span></span>

## <span data-ttu-id="64a0d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64a0d-135">OUTPUTS</span></span>

### <span data-ttu-id="64a0d-136">Microsoft. Azure. Command. FrontDoor. models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="64a0d-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="64a0d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64a0d-137">NOTES</span></span>

## <span data-ttu-id="64a0d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64a0d-138">RELATED LINKS</span></span>

<span data-ttu-id="64a0d-139">[Új – AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="64a0d-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span></span>
