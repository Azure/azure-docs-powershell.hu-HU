---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bdfd9cb100b43f58326b9b94c4e15bb24561eadd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841374"
---
# <span data-ttu-id="0d5ba-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d5ba-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="0d5ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5ba-103">WAF-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="0d5ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d5ba-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d5ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d5ba-105">DESCRIPTION</span></span>
<span data-ttu-id="0d5ba-106">A **New-AzApplicationGatewayWebApplicationFirewallConfiguration** parancsmag létrehoz egy webalkalmazás-TŰZFAL (WAF) konfigurációt egy Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="0d5ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0d5ba-107">EXAMPLES</span></span>

### <span data-ttu-id="0d5ba-108">1. példa: webalkalmazások tűzfal-konfigurációjának létrehozása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="0d5ba-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="0d5ba-109">Az első parancs létrehoz egy új, letiltott szabálykészlet-konfigurációt a "Request-942-APPLICATION-ATTACK-SQLI" nevű szabály csoporthoz a 942130 és a 942140-as szabály letiltásával.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="0d5ba-110">A második parancs a "Request-921-protokoll – támadás" nevű szabály csoportjának egy másik letiltott szabály-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="0d5ba-111">A szabályok nincsenek konkrétan átadva, így a szabály csoport minden szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="0d5ba-112">Az utolsó parancs Ezután létrehoz egy WAF-konfigurációt, melyben a tűzfal szabályai le vannak tiltva az $disabledRuleGroup 1 és a $disabledRuleGroup 2 rendszerben.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="0d5ba-113">Az új WAF-konfiguráció a $firewallConfig változóban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="0d5ba-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d5ba-114">PARAMETERS</span></span>

### <span data-ttu-id="0d5ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5ba-115">-DefaultProfile</span></span>
<span data-ttu-id="0d5ba-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d5ba-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="0d5ba-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="0d5ba-118">A letiltott szabályok csoportjai.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="0d5ba-119">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="0d5ba-119">-Enabled</span></span>
<span data-ttu-id="0d5ba-120">Azt jelzi, hogy engedélyezve van-e a WAF.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="0d5ba-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="0d5ba-121">-FirewallMode</span></span>
<span data-ttu-id="0d5ba-122">A webalkalmazás-tűzfal üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="0d5ba-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0d5ba-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d5ba-124">Nyomozás</span><span class="sxs-lookup"><span data-stu-id="0d5ba-124">Detection</span></span>
- <span data-ttu-id="0d5ba-125">Megelőzés</span><span class="sxs-lookup"><span data-stu-id="0d5ba-125">Prevention</span></span>

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

### <span data-ttu-id="0d5ba-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="0d5ba-126">-RuleSetType</span></span>
<span data-ttu-id="0d5ba-127">A webalkalmazás-tűzfal szabálykészlet típusa.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="0d5ba-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0d5ba-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="0d5ba-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="0d5ba-129">OWASP</span></span>

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

### <span data-ttu-id="0d5ba-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="0d5ba-130">-RuleSetVersion</span></span>
<span data-ttu-id="0d5ba-131">A szabálykészlet típusának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-131">The version of the rule set type.</span></span>
<span data-ttu-id="0d5ba-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0d5ba-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="0d5ba-133">3,0</span><span class="sxs-lookup"><span data-stu-id="0d5ba-133">3.0</span></span>
- <span data-ttu-id="0d5ba-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="0d5ba-134">2.2.9</span></span>

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

### <span data-ttu-id="0d5ba-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0d5ba-135">-Confirm</span></span>
<span data-ttu-id="0d5ba-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d5ba-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d5ba-137">-WhatIf</span></span>
<span data-ttu-id="0d5ba-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d5ba-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d5ba-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d5ba-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5ba-140">CommonParameters</span></span>
<span data-ttu-id="0d5ba-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d5ba-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5ba-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5ba-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5ba-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d5ba-143">INPUTS</span></span>

## <span data-ttu-id="0d5ba-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d5ba-144">OUTPUTS</span></span>

### <span data-ttu-id="0d5ba-145">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d5ba-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="0d5ba-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d5ba-146">NOTES</span></span>

## <span data-ttu-id="0d5ba-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d5ba-147">RELATED LINKS</span></span>

[<span data-ttu-id="0d5ba-148">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d5ba-148">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="0d5ba-149">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d5ba-149">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


