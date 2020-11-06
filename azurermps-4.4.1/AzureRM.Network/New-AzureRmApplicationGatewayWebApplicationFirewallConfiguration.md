---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 281a4a0d935d73777f7fdd693f3d32982b2da47a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495542"
---
# <span data-ttu-id="87617-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="87617-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="87617-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87617-102">SYNOPSIS</span></span>
<span data-ttu-id="87617-103">WAF-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="87617-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87617-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87617-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87617-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87617-105">DESCRIPTION</span></span>
<span data-ttu-id="87617-106">A **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** parancsmag létrehoz egy webalkalmazás-TŰZFAL (WAF) konfigurációt egy Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="87617-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="87617-107">Példák</span><span class="sxs-lookup"><span data-stu-id="87617-107">EXAMPLES</span></span>

### <span data-ttu-id="87617-108">1. példa: webalkalmazások tűzfal-konfigurációjának létrehozása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="87617-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="87617-109">Az első parancs létrehoz egy új, letiltott szabálykészlet-konfigurációt a "Request-942-APPLICATION-ATTACK-SQLI" nevű szabály csoporthoz a 942130 és a 942140-as szabály letiltásával.</span><span class="sxs-lookup"><span data-stu-id="87617-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="87617-110">A második parancs a "Request-921-protokoll – támadás" nevű szabály csoportjának egy másik letiltott szabály-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="87617-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="87617-111">A szabályok nincsenek konkrétan átadva, így a szabály csoport minden szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="87617-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="87617-112">Az utolsó parancs Ezután létrehoz egy WAF-konfigurációt, melyben a tűzfal szabályai le vannak tiltva az $disabledRuleGroup 1 és a $disabledRuleGroup 2 rendszerben.</span><span class="sxs-lookup"><span data-stu-id="87617-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="87617-113">Az új WAF-konfiguráció a $firewallConfig változóban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="87617-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="87617-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87617-114">PARAMETERS</span></span>

### <span data-ttu-id="87617-115">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="87617-115">-DisabledRuleGroups</span></span>
<span data-ttu-id="87617-116">A letiltott szabályok csoportjai.</span><span class="sxs-lookup"><span data-stu-id="87617-116">The disabled rule groups.</span></span>

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

### <span data-ttu-id="87617-117">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="87617-117">-Enabled</span></span>
<span data-ttu-id="87617-118">Azt jelzi, hogy engedélyezve van-e a WAF.</span><span class="sxs-lookup"><span data-stu-id="87617-118">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87617-119">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="87617-119">-FirewallMode</span></span>
<span data-ttu-id="87617-120">A webalkalmazás-tűzfal üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="87617-120">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="87617-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="87617-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87617-122">Nyomozás</span><span class="sxs-lookup"><span data-stu-id="87617-122">Detection</span></span>
- <span data-ttu-id="87617-123">Megelőzés</span><span class="sxs-lookup"><span data-stu-id="87617-123">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87617-124">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="87617-124">-RuleSetType</span></span>
<span data-ttu-id="87617-125">A webalkalmazás-tűzfal szabálykészlet típusa.</span><span class="sxs-lookup"><span data-stu-id="87617-125">The type of the web application firewall rule set.</span></span> <span data-ttu-id="87617-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="87617-126">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="87617-127">OWASP</span><span class="sxs-lookup"><span data-stu-id="87617-127">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87617-128">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="87617-128">-RuleSetVersion</span></span>
<span data-ttu-id="87617-129">A szabálykészlet típusának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="87617-129">The version of the rule set type.</span></span>
<span data-ttu-id="87617-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="87617-130">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="87617-131">3,0</span><span class="sxs-lookup"><span data-stu-id="87617-131">3.0</span></span>
- <span data-ttu-id="87617-132">2.2.9</span><span class="sxs-lookup"><span data-stu-id="87617-132">2.2.9</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87617-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87617-133">-Confirm</span></span>
<span data-ttu-id="87617-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87617-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87617-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87617-135">-WhatIf</span></span>
<span data-ttu-id="87617-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87617-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87617-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87617-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87617-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87617-138">-DefaultProfile</span></span>
<span data-ttu-id="87617-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87617-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87617-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87617-140">CommonParameters</span></span>
<span data-ttu-id="87617-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87617-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87617-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87617-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87617-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87617-143">INPUTS</span></span>

## <span data-ttu-id="87617-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87617-144">OUTPUTS</span></span>

### <span data-ttu-id="87617-145">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="87617-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="87617-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87617-146">NOTES</span></span>

## <span data-ttu-id="87617-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87617-147">RELATED LINKS</span></span>

[<span data-ttu-id="87617-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="87617-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="87617-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="87617-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


