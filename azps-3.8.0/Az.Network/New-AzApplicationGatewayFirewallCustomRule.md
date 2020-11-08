---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: d8e22f5eb0e504757bd94fa5235d07ad3e3db998
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014830"
---
# <span data-ttu-id="9eae7-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="9eae7-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="9eae7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9eae7-102">SYNOPSIS</span></span>
<span data-ttu-id="9eae7-103">Új egyéni szabály létrehozása az alkalmazás-átjáró tűzfal-házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="9eae7-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="9eae7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9eae7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eae7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9eae7-105">DESCRIPTION</span></span>
<span data-ttu-id="9eae7-106">A **New-AzApplicationGatewayFirewallCustomRule** létrehoz egy egyéni szabályt a tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="9eae7-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="9eae7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9eae7-107">EXAMPLES</span></span>

### <span data-ttu-id="9eae7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9eae7-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -matchConditons $condtion -Action Allow
```

<span data-ttu-id="9eae7-109">A parancs létrehoz egy új egyéni szabályt, amelyben szerepel a példa-szabály, az 1-es prioritás és a MatchRule a feltétel változóban definiált feltételekkel, a művelet az Allow (Engedélyezés) értéket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="9eae7-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="9eae7-110">Az új egyeztetési egyéni szabály a $customRule-ban lesz mentve.</span><span class="sxs-lookup"><span data-stu-id="9eae7-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="9eae7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9eae7-111">PARAMETERS</span></span>

### <span data-ttu-id="9eae7-112">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="9eae7-112">-Action</span></span>
<span data-ttu-id="9eae7-113">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="9eae7-113">Type of Actions.</span></span>

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

### <span data-ttu-id="9eae7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eae7-114">-DefaultProfile</span></span>
<span data-ttu-id="9eae7-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9eae7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eae7-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="9eae7-116">-MatchCondition</span></span>
<span data-ttu-id="9eae7-117">A egyeztetési feltételek listája.</span><span class="sxs-lookup"><span data-stu-id="9eae7-117">List of match conditions.</span></span>

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

### <span data-ttu-id="9eae7-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9eae7-118">-Name</span></span>
<span data-ttu-id="9eae7-119">A szabály neve.</span><span class="sxs-lookup"><span data-stu-id="9eae7-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="9eae7-120">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="9eae7-120">-Priority</span></span>
<span data-ttu-id="9eae7-121">A szabály prioritását ismerteti.</span><span class="sxs-lookup"><span data-stu-id="9eae7-121">Describes priority of the rule.</span></span>
<span data-ttu-id="9eae7-122">Az alacsonyabb értéket tartalmazó szabályokat a program a magasabb értékű szabályok előtt értékeli ki.</span><span class="sxs-lookup"><span data-stu-id="9eae7-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="9eae7-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="9eae7-123">-RuleType</span></span>
<span data-ttu-id="9eae7-124">A szabály típusának ismertetése.</span><span class="sxs-lookup"><span data-stu-id="9eae7-124">Describes type of rule.</span></span>

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

### <span data-ttu-id="9eae7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eae7-125">CommonParameters</span></span>
<span data-ttu-id="9eae7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9eae7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eae7-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eae7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eae7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eae7-128">INPUTS</span></span>

### <span data-ttu-id="9eae7-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="9eae7-129">None</span></span>

## <span data-ttu-id="9eae7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eae7-130">OUTPUTS</span></span>

### <span data-ttu-id="9eae7-131">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="9eae7-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="9eae7-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9eae7-132">NOTES</span></span>

## <span data-ttu-id="9eae7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9eae7-133">RELATED LINKS</span></span>
