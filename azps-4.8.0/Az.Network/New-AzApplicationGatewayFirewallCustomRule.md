---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: b25c25b642f8c912f62f75788e69e96c3ebdc73c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180533"
---
# <span data-ttu-id="6e26a-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="6e26a-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="6e26a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e26a-102">SYNOPSIS</span></span>
<span data-ttu-id="6e26a-103">Új egyéni szabály létrehozása az alkalmazás-átjáró tűzfal-házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="6e26a-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="6e26a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e26a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e26a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e26a-105">DESCRIPTION</span></span>
<span data-ttu-id="6e26a-106">A **New-AzApplicationGatewayFirewallCustomRule** létrehoz egy egyéni szabályt a tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="6e26a-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="6e26a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6e26a-107">EXAMPLES</span></span>

### <span data-ttu-id="6e26a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6e26a-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="6e26a-109">A parancs létrehoz egy új egyéni szabályt, amelyben szerepel a példa-szabály, az 1-es prioritás és a MatchRule a feltétel változóban definiált feltételekkel, a művelet az Allow (Engedélyezés) értéket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="6e26a-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="6e26a-110">Az új egyeztetési egyéni szabály a $customRule-ban lesz mentve.</span><span class="sxs-lookup"><span data-stu-id="6e26a-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="6e26a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e26a-111">PARAMETERS</span></span>

### <span data-ttu-id="6e26a-112">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="6e26a-112">-Action</span></span>
<span data-ttu-id="6e26a-113">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="6e26a-113">Type of Actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e26a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e26a-114">-DefaultProfile</span></span>
<span data-ttu-id="6e26a-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e26a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e26a-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="6e26a-116">-MatchCondition</span></span>
<span data-ttu-id="6e26a-117">A egyeztetési feltételek listája.</span><span class="sxs-lookup"><span data-stu-id="6e26a-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e26a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e26a-118">-Name</span></span>
<span data-ttu-id="6e26a-119">A szabály neve.</span><span class="sxs-lookup"><span data-stu-id="6e26a-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="6e26a-120">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="6e26a-120">-Priority</span></span>
<span data-ttu-id="6e26a-121">A szabály prioritását ismerteti.</span><span class="sxs-lookup"><span data-stu-id="6e26a-121">Describes priority of the rule.</span></span>
<span data-ttu-id="6e26a-122">Az alacsonyabb értéket tartalmazó szabályokat a program a magasabb értékű szabályok előtt értékeli ki.</span><span class="sxs-lookup"><span data-stu-id="6e26a-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="6e26a-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="6e26a-123">-RuleType</span></span>
<span data-ttu-id="6e26a-124">A szabály típusának ismertetése.</span><span class="sxs-lookup"><span data-stu-id="6e26a-124">Describes type of rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e26a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e26a-125">CommonParameters</span></span>
<span data-ttu-id="6e26a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e26a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e26a-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e26a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e26a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e26a-128">INPUTS</span></span>

### <span data-ttu-id="6e26a-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="6e26a-129">None</span></span>

## <span data-ttu-id="6e26a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e26a-130">OUTPUTS</span></span>

### <span data-ttu-id="6e26a-131">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="6e26a-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="6e26a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e26a-132">NOTES</span></span>

## <span data-ttu-id="6e26a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e26a-133">RELATED LINKS</span></span>
