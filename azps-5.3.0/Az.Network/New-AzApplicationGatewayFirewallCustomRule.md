---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: b25c25b642f8c912f62f75788e69e96c3ebdc73c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379496"
---
# <span data-ttu-id="ab822-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="ab822-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="ab822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab822-102">SYNOPSIS</span></span>
<span data-ttu-id="ab822-103">Létrehoz egy új egyéni szabályt az alkalmazás átjáró tűzfalszabályához.</span><span class="sxs-lookup"><span data-stu-id="ab822-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="ab822-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab822-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab822-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab822-105">DESCRIPTION</span></span>
<span data-ttu-id="ab822-106">A **New-AzApplicationGatewayFirewallCustomRule** létrehoz egy egyéni szabályt a tűzfal házirendhez.</span><span class="sxs-lookup"><span data-stu-id="ab822-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="ab822-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab822-107">EXAMPLES</span></span>

### <span data-ttu-id="ab822-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ab822-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="ab822-109">A parancs létrehoz egy új egyéni szabályt a példaszabály nevével, az 1-es prioritást, a szabálytípus pedig a Feltételváltozóban definiált feltételt, a művelet pedig az engedélyezőt fogja adni.</span><span class="sxs-lookup"><span data-stu-id="ab822-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="ab822-110">Az új egyezés egyéni szabály mentése a $customRule.</span><span class="sxs-lookup"><span data-stu-id="ab822-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="ab822-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab822-111">PARAMETERS</span></span>

### <span data-ttu-id="ab822-112">-Művelet</span><span class="sxs-lookup"><span data-stu-id="ab822-112">-Action</span></span>
<span data-ttu-id="ab822-113">A műveletek típusa.</span><span class="sxs-lookup"><span data-stu-id="ab822-113">Type of Actions.</span></span>

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

### <span data-ttu-id="ab822-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab822-114">-DefaultProfile</span></span>
<span data-ttu-id="ab822-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab822-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab822-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="ab822-116">-MatchCondition</span></span>
<span data-ttu-id="ab822-117">Az egyezések feltételeinek listája.</span><span class="sxs-lookup"><span data-stu-id="ab822-117">List of match conditions.</span></span>

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

### <span data-ttu-id="ab822-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ab822-118">-Name</span></span>
<span data-ttu-id="ab822-119">A szabály neve.</span><span class="sxs-lookup"><span data-stu-id="ab822-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="ab822-120">-Priority</span><span class="sxs-lookup"><span data-stu-id="ab822-120">-Priority</span></span>
<span data-ttu-id="ab822-121">Ismerteti a szabály prioritását.</span><span class="sxs-lookup"><span data-stu-id="ab822-121">Describes priority of the rule.</span></span>
<span data-ttu-id="ab822-122">Az alacsonyabb értékű szabályokat a program a magasabb értékű szabályok előtt értékeli ki.</span><span class="sxs-lookup"><span data-stu-id="ab822-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="ab822-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="ab822-123">-RuleType</span></span>
<span data-ttu-id="ab822-124">A szabály típusát ismerteti.</span><span class="sxs-lookup"><span data-stu-id="ab822-124">Describes type of rule.</span></span>

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

### <span data-ttu-id="ab822-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab822-125">CommonParameters</span></span>
<span data-ttu-id="ab822-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab822-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab822-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab822-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab822-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab822-128">INPUTS</span></span>

### <span data-ttu-id="ab822-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="ab822-129">None</span></span>

## <span data-ttu-id="ab822-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab822-130">OUTPUTS</span></span>

### <span data-ttu-id="ab822-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="ab822-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="ab822-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab822-132">NOTES</span></span>

## <span data-ttu-id="ab822-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab822-133">RELATED LINKS</span></span>
