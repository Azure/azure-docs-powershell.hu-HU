---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5a96ea5ac1ded346e289d44f54762909d5f96e31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918713"
---
# <span data-ttu-id="3703c-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="3703c-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="3703c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3703c-102">SYNOPSIS</span></span>
<span data-ttu-id="3703c-103">Új letiltott szabálycsoport-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3703c-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="3703c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3703c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3703c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3703c-105">DESCRIPTION</span></span>
<span data-ttu-id="3703c-106">A **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** parancsmag létrehoz egy új letiltott szabálycsoport-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="3703c-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="3703c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3703c-107">EXAMPLES</span></span>

### <span data-ttu-id="3703c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3703c-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="3703c-109">A parancs létrehoz egy új letiltott szabálycsoport-konfigurációt a REQUEST-942-APPLICATION-ATTACK-SQLI nevű szabálycsoporthoz, a 942130-as és a 942140-es szabály letiltva.</span><span class="sxs-lookup"><span data-stu-id="3703c-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="3703c-110">Az új letiltott szabálycsoport-konfigurációt a $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="3703c-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="3703c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3703c-111">PARAMETERS</span></span>

### <span data-ttu-id="3703c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3703c-112">-DefaultProfile</span></span>
<span data-ttu-id="3703c-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3703c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3703c-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="3703c-114">-RuleGroupName</span></span>
<span data-ttu-id="3703c-115">A letiltott szabálycsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3703c-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="3703c-116">-Rules</span><span class="sxs-lookup"><span data-stu-id="3703c-116">-Rules</span></span>
<span data-ttu-id="3703c-117">A letiltott szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="3703c-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="3703c-118">Null érték esetén a szabálycsoport összes szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="3703c-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3703c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3703c-119">CommonParameters</span></span>
<span data-ttu-id="3703c-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3703c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3703c-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3703c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3703c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3703c-122">INPUTS</span></span>

### <span data-ttu-id="3703c-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="3703c-123">None</span></span>

## <span data-ttu-id="3703c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3703c-124">OUTPUTS</span></span>

### <span data-ttu-id="3703c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="3703c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="3703c-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3703c-126">NOTES</span></span>

## <span data-ttu-id="3703c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3703c-127">RELATED LINKS</span></span>

[<span data-ttu-id="3703c-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3703c-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="3703c-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3703c-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

