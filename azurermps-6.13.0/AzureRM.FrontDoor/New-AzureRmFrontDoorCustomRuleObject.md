---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
ms.openlocfilehash: a5a1494bd217147a4e6f4c94a85140313429898f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491924"
---
# <span data-ttu-id="305fb-101">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="305fb-101">New-AzureRmFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="305fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="305fb-102">SYNOPSIS</span></span>
<span data-ttu-id="305fb-103">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="305fb-103">Create CustomRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="305fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="305fb-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="305fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="305fb-105">DESCRIPTION</span></span>
<span data-ttu-id="305fb-106">CustomRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="305fb-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="305fb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="305fb-107">EXAMPLES</span></span>

### <span data-ttu-id="305fb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="305fb-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

RuleType                   : MatchRule
Action                     : Block
MatchConditions            : {Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition}
Priority                   : 2
RateLimitDurationInMinutes : 1
RateLimitThreshold         :
Name                       : Rule1
Etag                       :
Transforms                 :
```

<span data-ttu-id="305fb-109">CustomRule objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="305fb-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="305fb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="305fb-110">PARAMETERS</span></span>

### <span data-ttu-id="305fb-111">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="305fb-111">-Action</span></span>
<span data-ttu-id="305fb-112">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="305fb-112">Type of Actions.</span></span>
<span data-ttu-id="305fb-113">A lehetséges értékek a következők: "Allow", "blokk", "log"</span><span class="sxs-lookup"><span data-stu-id="305fb-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305fb-114">-DefaultProfile</span></span>
<span data-ttu-id="305fb-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="305fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305fb-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="305fb-116">-MatchCondition</span></span>
<span data-ttu-id="305fb-117">A egyeztetési feltételek listája.</span><span class="sxs-lookup"><span data-stu-id="305fb-117">List of match conditions.</span></span>

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

### <span data-ttu-id="305fb-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="305fb-118">-Name</span></span>
<span data-ttu-id="305fb-119">A szabály neve</span><span class="sxs-lookup"><span data-stu-id="305fb-119">Name of the rule</span></span>

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

### <span data-ttu-id="305fb-120">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="305fb-120">-Priority</span></span>
<span data-ttu-id="305fb-121">A szabály prioritását ismerteti.</span><span class="sxs-lookup"><span data-stu-id="305fb-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="305fb-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="305fb-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="305fb-123">A mérték korlátjának időtartama.</span><span class="sxs-lookup"><span data-stu-id="305fb-123">Rate limit duration.</span></span> <span data-ttu-id="305fb-124">Default-1 perc</span><span class="sxs-lookup"><span data-stu-id="305fb-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="305fb-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="305fb-125">-RateLimitThreshold</span></span>
<span data-ttu-id="305fb-126">Ráta limit thresold</span><span class="sxs-lookup"><span data-stu-id="305fb-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="305fb-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="305fb-127">-RuleType</span></span>
<span data-ttu-id="305fb-128">A szabály típusa.</span><span class="sxs-lookup"><span data-stu-id="305fb-128">Type of the rule.</span></span>
<span data-ttu-id="305fb-129">A lehetséges értékek a következők: "MatchRule", "RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="305fb-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="305fb-130">-Transform</span><span class="sxs-lookup"><span data-stu-id="305fb-130">-Transform</span></span>
<span data-ttu-id="305fb-131">Az átalakítások listája</span><span class="sxs-lookup"><span data-stu-id="305fb-131">List of transforms</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="305fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305fb-132">CommonParameters</span></span>
<span data-ttu-id="305fb-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="305fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305fb-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="305fb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305fb-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="305fb-135">INPUTS</span></span>

### <span data-ttu-id="305fb-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="305fb-136">None</span></span>

## <span data-ttu-id="305fb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="305fb-137">OUTPUTS</span></span>

### <span data-ttu-id="305fb-138">Microsoft. Azure. Command. FrontDoor. models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="305fb-138">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="305fb-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="305fb-139">NOTES</span></span>

## <span data-ttu-id="305fb-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="305fb-140">RELATED LINKS</span></span>

<span data-ttu-id="305fb-141">[Új – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="305fb-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span></span>
