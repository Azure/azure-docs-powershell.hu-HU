---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 9fd01fdf63a0c58599c00a6a6739802efb5304d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837244"
---
# <span data-ttu-id="af05d-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="af05d-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="af05d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af05d-102">SYNOPSIS</span></span>
<span data-ttu-id="af05d-103">Új letiltott szabály-konfiguráció létrehozása.</span><span class="sxs-lookup"><span data-stu-id="af05d-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="af05d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af05d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af05d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af05d-105">DESCRIPTION</span></span>
<span data-ttu-id="af05d-106">A **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** parancsmag új letiltott szabály-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="af05d-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="af05d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af05d-107">EXAMPLES</span></span>

### <span data-ttu-id="af05d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="af05d-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="af05d-109">A parancs új, letiltott szabály-konfigurációt hoz létre a "Request-942-APPLICATION-ATTACK-SQLI" nevű szabály csoportjának a 942130 és a 942140-as szabály letiltásával.</span><span class="sxs-lookup"><span data-stu-id="af05d-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="af05d-110">Az új letiltott szabály csoport konfigurációját a program az 1 $disabledRuleGroup menti.</span><span class="sxs-lookup"><span data-stu-id="af05d-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="af05d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af05d-111">PARAMETERS</span></span>

### <span data-ttu-id="af05d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af05d-112">-DefaultProfile</span></span>
<span data-ttu-id="af05d-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af05d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af05d-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="af05d-114">-RuleGroupName</span></span>
<span data-ttu-id="af05d-115">Annak a szabálynak a neve, amely le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="af05d-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="af05d-116">-Szabályok</span><span class="sxs-lookup"><span data-stu-id="af05d-116">-Rules</span></span>
<span data-ttu-id="af05d-117">A letiltani kívánt szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="af05d-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="af05d-118">Ha NULL, a szabály csoport minden szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="af05d-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="af05d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af05d-119">CommonParameters</span></span>
<span data-ttu-id="af05d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af05d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af05d-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af05d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af05d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af05d-122">INPUTS</span></span>

### <span data-ttu-id="af05d-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="af05d-123">None</span></span>

## <span data-ttu-id="af05d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af05d-124">OUTPUTS</span></span>

### <span data-ttu-id="af05d-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="af05d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="af05d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af05d-126">NOTES</span></span>

## <span data-ttu-id="af05d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af05d-127">RELATED LINKS</span></span>

[<span data-ttu-id="af05d-128">Új – AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="af05d-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="af05d-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="af05d-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

