---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: b25c25b642f8c912f62f75788e69e96c3ebdc73c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340313"
---
# <span data-ttu-id="1a644-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="1a644-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="1a644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a644-102">SYNOPSIS</span></span>
<span data-ttu-id="1a644-103">Létrehoz egy új egyéni szabályt az alkalmazás átjáró tűzfal házirendhez.</span><span class="sxs-lookup"><span data-stu-id="1a644-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="1a644-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1a644-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a644-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1a644-105">DESCRIPTION</span></span>
<span data-ttu-id="1a644-106">A **New-AzApplicationGatewayFirewallCustomRule** létrehoz egy egyéni szabályt a tűzfal házirendhez.</span><span class="sxs-lookup"><span data-stu-id="1a644-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="1a644-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1a644-107">EXAMPLES</span></span>

### <span data-ttu-id="1a644-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1a644-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="1a644-109">A parancs létrehoz egy új egyéni szabályt a példaszabály nevével, az 1-es prioritást, a szabálytípus pedig a Feltételváltozóban definiált feltételt, a művelet pedig az engedélyezőt fogja adni.</span><span class="sxs-lookup"><span data-stu-id="1a644-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="1a644-110">Az új egyezés egyéni szabály mentése a $customRule.</span><span class="sxs-lookup"><span data-stu-id="1a644-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="1a644-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a644-111">PARAMETERS</span></span>

### <span data-ttu-id="1a644-112">-Művelet</span><span class="sxs-lookup"><span data-stu-id="1a644-112">-Action</span></span>
<span data-ttu-id="1a644-113">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="1a644-113">Type of Actions.</span></span>

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

### <span data-ttu-id="1a644-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a644-114">-DefaultProfile</span></span>
<span data-ttu-id="1a644-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a644-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a644-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="1a644-116">-MatchCondition</span></span>
<span data-ttu-id="1a644-117">Az egyezések feltételeinek listája.</span><span class="sxs-lookup"><span data-stu-id="1a644-117">List of match conditions.</span></span>

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

### <span data-ttu-id="1a644-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1a644-118">-Name</span></span>
<span data-ttu-id="1a644-119">A szabály neve.</span><span class="sxs-lookup"><span data-stu-id="1a644-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="1a644-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="1a644-120">-Priority</span></span>
<span data-ttu-id="1a644-121">Ismerteti a szabály prioritását.</span><span class="sxs-lookup"><span data-stu-id="1a644-121">Describes priority of the rule.</span></span>
<span data-ttu-id="1a644-122">Az alacsonyabb értékű szabályokat a program a magasabb értékű szabályok előtt értékeli ki.</span><span class="sxs-lookup"><span data-stu-id="1a644-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="1a644-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="1a644-123">-RuleType</span></span>
<span data-ttu-id="1a644-124">A szabály típusát ismerteti.</span><span class="sxs-lookup"><span data-stu-id="1a644-124">Describes type of rule.</span></span>

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

### <span data-ttu-id="1a644-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a644-125">CommonParameters</span></span>
<span data-ttu-id="1a644-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a644-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a644-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a644-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a644-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a644-128">INPUTS</span></span>

### <span data-ttu-id="1a644-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="1a644-129">None</span></span>

## <span data-ttu-id="1a644-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a644-130">OUTPUTS</span></span>

### <span data-ttu-id="1a644-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="1a644-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="1a644-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1a644-132">NOTES</span></span>

## <span data-ttu-id="1a644-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a644-133">RELATED LINKS</span></span>
