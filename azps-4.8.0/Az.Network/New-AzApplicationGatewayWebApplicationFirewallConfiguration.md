---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 0f186de1ad548be0c566c6fac2b8d1505885bfe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184865"
---
# <span data-ttu-id="7045d-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7045d-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="7045d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7045d-102">SYNOPSIS</span></span>
<span data-ttu-id="7045d-103">WAF-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7045d-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="7045d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7045d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7045d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7045d-105">DESCRIPTION</span></span>
<span data-ttu-id="7045d-106">A **New-AzApplicationGatewayWebApplicationFirewallConfiguration** parancsmag létrehoz egy webalkalmazás-TŰZFAL (WAF) konfigurációt egy Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="7045d-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="7045d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7045d-107">EXAMPLES</span></span>

### <span data-ttu-id="7045d-108">1. példa: webalkalmazások tűzfal-konfigurációjának létrehozása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="7045d-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="7045d-109">Az első parancs létrehoz egy új, letiltott szabálykészlet-konfigurációt a "Request-942-APPLICATION-ATTACK-SQLI" nevű szabály csoporthoz a 942130 és a 942140-as szabály letiltásával.</span><span class="sxs-lookup"><span data-stu-id="7045d-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="7045d-110">A második parancs a "Request-921-protokoll – támadás" nevű szabály csoportjának egy másik letiltott szabály-konfigurációját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7045d-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="7045d-111">A szabályok nincsenek konkrétan átadva, így a szabály csoport minden szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="7045d-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="7045d-112">Az utolsó parancs Ezután létrehoz egy WAF-konfigurációt, melyben a tűzfal szabályai le vannak tiltva az $disabledRuleGroup 1 és a $disabledRuleGroup 2 rendszerben.</span><span class="sxs-lookup"><span data-stu-id="7045d-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="7045d-113">Az új WAF-konfiguráció a $firewallConfig változóban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="7045d-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="7045d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7045d-114">PARAMETERS</span></span>

### <span data-ttu-id="7045d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7045d-115">-DefaultProfile</span></span>
<span data-ttu-id="7045d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7045d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7045d-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="7045d-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="7045d-118">A letiltott szabályok csoportjai.</span><span class="sxs-lookup"><span data-stu-id="7045d-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7045d-119">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="7045d-119">-Enabled</span></span>
<span data-ttu-id="7045d-120">Azt jelzi, hogy engedélyezve van-e a WAF.</span><span class="sxs-lookup"><span data-stu-id="7045d-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="7045d-121">– Kizárás</span><span class="sxs-lookup"><span data-stu-id="7045d-121">-Exclusion</span></span>
<span data-ttu-id="7045d-122">A kizárási listák.</span><span class="sxs-lookup"><span data-stu-id="7045d-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7045d-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="7045d-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="7045d-124">Maximális feltöltési korlát MB-ban</span><span class="sxs-lookup"><span data-stu-id="7045d-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="7045d-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="7045d-125">-FirewallMode</span></span>
<span data-ttu-id="7045d-126">A webalkalmazás-tűzfal üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7045d-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="7045d-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7045d-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7045d-128">Nyomozás</span><span class="sxs-lookup"><span data-stu-id="7045d-128">Detection</span></span>
- <span data-ttu-id="7045d-129">Megelőzés</span><span class="sxs-lookup"><span data-stu-id="7045d-129">Prevention</span></span>

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

### <span data-ttu-id="7045d-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="7045d-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="7045d-131">Maximális kérés: a szövegtörzs mérete KB-ban</span><span class="sxs-lookup"><span data-stu-id="7045d-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="7045d-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="7045d-132">-RequestBodyCheck</span></span>
<span data-ttu-id="7045d-133">Azt, hogy a kérési törzs be van-e jelölve vagy sem.</span><span class="sxs-lookup"><span data-stu-id="7045d-133">Whether request body is checked or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7045d-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="7045d-134">-RuleSetType</span></span>
<span data-ttu-id="7045d-135">A webalkalmazás-tűzfal szabálykészlet típusa.</span><span class="sxs-lookup"><span data-stu-id="7045d-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="7045d-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7045d-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="7045d-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="7045d-137">OWASP</span></span>

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

### <span data-ttu-id="7045d-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="7045d-138">-RuleSetVersion</span></span>
<span data-ttu-id="7045d-139">A szabálykészlet típusának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="7045d-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7045d-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7045d-140">-Confirm</span></span>
<span data-ttu-id="7045d-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7045d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7045d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7045d-142">-WhatIf</span></span>
<span data-ttu-id="7045d-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7045d-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7045d-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7045d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7045d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7045d-145">CommonParameters</span></span>
<span data-ttu-id="7045d-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7045d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7045d-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7045d-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7045d-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7045d-148">INPUTS</span></span>

### <span data-ttu-id="7045d-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="7045d-149">None</span></span>

## <span data-ttu-id="7045d-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7045d-150">OUTPUTS</span></span>

### <span data-ttu-id="7045d-151">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7045d-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="7045d-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7045d-152">NOTES</span></span>

## <span data-ttu-id="7045d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7045d-153">RELATED LINKS</span></span>

[<span data-ttu-id="7045d-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7045d-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="7045d-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7045d-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

