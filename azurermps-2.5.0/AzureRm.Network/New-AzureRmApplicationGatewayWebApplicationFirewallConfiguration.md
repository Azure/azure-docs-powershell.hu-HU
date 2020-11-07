---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: f0117a7fa89f5e392009a9df814996ee66cc8bcd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848421"
---
# <span data-ttu-id="44ab1-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="44ab1-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="44ab1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="44ab1-103">WAF-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="44ab1-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44ab1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44ab1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44ab1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="44ab1-105">DESCRIPTION</span></span>
<span data-ttu-id="44ab1-106">A **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** parancsmag létrehoz egy webalkalmazás-TŰZFAL (WAF) konfigurációt egy Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="44ab1-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="44ab1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="44ab1-107">EXAMPLES</span></span>

### <span data-ttu-id="44ab1-108">1. példa: webalkalmazások tűzfal-konfigurációjának létrehozása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="44ab1-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="44ab1-109">Az első parancs létrehoz egy új, letiltott szabálykészlet-konfigurációt a "Request-942-APPLICATION-ATTACK-SQLI" nevű szabály csoporthoz a 942130 és a 942140-as szabály letiltásával.</span><span class="sxs-lookup"><span data-stu-id="44ab1-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="44ab1-110">A második parancs a "Request-921-protokoll – támadás" nevű szabály csoportjának egy másik letiltott szabály-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="44ab1-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="44ab1-111">A szabályok nincsenek konkrétan átadva, így a szabály csoport minden szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="44ab1-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="44ab1-112">Az utolsó parancs Ezután létrehoz egy WAF-konfigurációt, melyben a tűzfal szabályai le vannak tiltva az $disabledRuleGroup 1 és a $disabledRuleGroup 2 rendszerben.</span><span class="sxs-lookup"><span data-stu-id="44ab1-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="44ab1-113">Az új WAF-konfiguráció a $firewallConfig változóban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="44ab1-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="44ab1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44ab1-114">PARAMETERS</span></span>

### <span data-ttu-id="44ab1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ab1-115">-DefaultProfile</span></span>
<span data-ttu-id="44ab1-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44ab1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ab1-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="44ab1-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="44ab1-118">A letiltott szabályok csoportjai.</span><span class="sxs-lookup"><span data-stu-id="44ab1-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ab1-119">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="44ab1-119">-Enabled</span></span>
<span data-ttu-id="44ab1-120">Azt jelzi, hogy engedélyezve van-e a WAF.</span><span class="sxs-lookup"><span data-stu-id="44ab1-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ab1-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="44ab1-121">-FirewallMode</span></span>
<span data-ttu-id="44ab1-122">A webalkalmazás-tűzfal üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="44ab1-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="44ab1-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="44ab1-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44ab1-124">Nyomozás</span><span class="sxs-lookup"><span data-stu-id="44ab1-124">Detection</span></span>
- <span data-ttu-id="44ab1-125">Megelőzés</span><span class="sxs-lookup"><span data-stu-id="44ab1-125">Prevention</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ab1-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="44ab1-126">-RuleSetType</span></span>
<span data-ttu-id="44ab1-127">A webalkalmazás-tűzfal szabálykészlet típusa.</span><span class="sxs-lookup"><span data-stu-id="44ab1-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="44ab1-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="44ab1-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="44ab1-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="44ab1-129">OWASP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ab1-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="44ab1-130">-RuleSetVersion</span></span>
<span data-ttu-id="44ab1-131">A szabálykészlet típusának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="44ab1-131">The version of the rule set type.</span></span>
<span data-ttu-id="44ab1-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="44ab1-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="44ab1-133">3,0</span><span class="sxs-lookup"><span data-stu-id="44ab1-133">3.0</span></span>
- <span data-ttu-id="44ab1-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="44ab1-134">2.2.9</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ab1-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="44ab1-135">-Confirm</span></span>
<span data-ttu-id="44ab1-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="44ab1-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ab1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44ab1-137">-WhatIf</span></span>
<span data-ttu-id="44ab1-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="44ab1-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44ab1-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44ab1-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ab1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ab1-140">CommonParameters</span></span>
<span data-ttu-id="44ab1-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44ab1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ab1-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ab1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ab1-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44ab1-143">INPUTS</span></span>

## <span data-ttu-id="44ab1-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44ab1-144">OUTPUTS</span></span>

### <span data-ttu-id="44ab1-145">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="44ab1-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="44ab1-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44ab1-146">NOTES</span></span>

## <span data-ttu-id="44ab1-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44ab1-147">RELATED LINKS</span></span>

[<span data-ttu-id="44ab1-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="44ab1-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="44ab1-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="44ab1-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

