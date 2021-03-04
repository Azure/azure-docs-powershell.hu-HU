---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 7d13febefe06ed1c290a0f95cbfda39dea353426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931577"
---
# <span data-ttu-id="42181-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="42181-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="42181-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42181-102">SYNOPSIS</span></span>
<span data-ttu-id="42181-103">WaF-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="42181-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="42181-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="42181-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42181-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="42181-105">DESCRIPTION</span></span>
<span data-ttu-id="42181-106">A **New-AzApplicationGatewayWebApplicationFirewallConfiguration parancsmag** létrehoz egy webalkalmazás tűzfalát (WAF) egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="42181-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="42181-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="42181-107">EXAMPLES</span></span>

### <span data-ttu-id="42181-108">1. példa: Webalkalmazás tűzfal-konfigurációjának létrehozása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="42181-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="42181-109">Az első parancs létrehoz egy új letiltott szabálycsoport-konfigurációt a "REQUEST-942-APPLICATION-ATTACK-SQLI" nevű szabálycsoporthoz, a 942130-as és a 942140-es szabály letiltva.</span><span class="sxs-lookup"><span data-stu-id="42181-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="42181-110">A második parancs egy másik letiltott szabálycsoport-konfigurációt hoz létre a "REQUEST-921-PROTOCOL-ATTACK" nevű szabálycsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="42181-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="42181-111">Konkrét szabályokat nem ad át a rendszer, így a szabálycsoport összes szabálya le lesz tiltva.</span><span class="sxs-lookup"><span data-stu-id="42181-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="42181-112">Az utolsó parancs ezután létrehoz egy, a $disabledRuleGroup 1-ben és a $disabledRuleGroup 2-ben konfigurált tűzfalszabályokat letiltó waf konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="42181-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="42181-113">Az új WAF-konfigurációt a rendszer a $firewallConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="42181-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="42181-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42181-114">PARAMETERS</span></span>

### <span data-ttu-id="42181-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42181-115">-DefaultProfile</span></span>
<span data-ttu-id="42181-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42181-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42181-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="42181-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="42181-118">A letiltott szabálycsoportok.</span><span class="sxs-lookup"><span data-stu-id="42181-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="42181-119">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="42181-119">-Enabled</span></span>
<span data-ttu-id="42181-120">Azt jelzi, hogy engedélyezve van-e a waf.</span><span class="sxs-lookup"><span data-stu-id="42181-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="42181-121">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="42181-121">-Exclusion</span></span>
<span data-ttu-id="42181-122">A kivétellisták.</span><span class="sxs-lookup"><span data-stu-id="42181-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="42181-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="42181-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="42181-124">Maximális fájlfeltöltési korlát MB-ban.</span><span class="sxs-lookup"><span data-stu-id="42181-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="42181-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="42181-125">-FirewallMode</span></span>
<span data-ttu-id="42181-126">A webalkalmazás tűzfalmódját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="42181-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="42181-127">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="42181-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42181-128">Észlelés</span><span class="sxs-lookup"><span data-stu-id="42181-128">Detection</span></span>
- <span data-ttu-id="42181-129">Megelőzés</span><span class="sxs-lookup"><span data-stu-id="42181-129">Prevention</span></span>

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

### <span data-ttu-id="42181-130">-MaxRequestQuestSizeInKb</span><span class="sxs-lookup"><span data-stu-id="42181-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="42181-131">A kérés maximális mérete KB-ban.</span><span class="sxs-lookup"><span data-stu-id="42181-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="42181-132">-RequestCheck</span><span class="sxs-lookup"><span data-stu-id="42181-132">-RequestBodyCheck</span></span>
<span data-ttu-id="42181-133">Függetlenül attól, hogy a kérelem törzse be van-e jelölve.</span><span class="sxs-lookup"><span data-stu-id="42181-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="42181-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="42181-134">-RuleSetType</span></span>
<span data-ttu-id="42181-135">A webalkalmazás tűzfalszabálykészletének típusa.</span><span class="sxs-lookup"><span data-stu-id="42181-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="42181-136">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="42181-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="42181-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="42181-137">OWASP</span></span>

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

### <span data-ttu-id="42181-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="42181-138">-RuleSetVersion</span></span>
<span data-ttu-id="42181-139">A szabálykészlet-típus verziója.</span><span class="sxs-lookup"><span data-stu-id="42181-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="42181-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42181-140">-Confirm</span></span>
<span data-ttu-id="42181-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="42181-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42181-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42181-142">-WhatIf</span></span>
<span data-ttu-id="42181-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="42181-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42181-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="42181-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42181-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42181-145">CommonParameters</span></span>
<span data-ttu-id="42181-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42181-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42181-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42181-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42181-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42181-148">INPUTS</span></span>

### <span data-ttu-id="42181-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="42181-149">None</span></span>

## <span data-ttu-id="42181-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42181-150">OUTPUTS</span></span>

### <span data-ttu-id="42181-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="42181-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="42181-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="42181-152">NOTES</span></span>

## <span data-ttu-id="42181-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42181-153">RELATED LINKS</span></span>

[<span data-ttu-id="42181-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="42181-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="42181-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="42181-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


