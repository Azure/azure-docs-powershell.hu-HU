---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: a5f60588a0db848d0b96aa0611b8647142db2b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670028"
---
# <span data-ttu-id="8571a-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="8571a-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="8571a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8571a-102">SYNOPSIS</span></span>
<span data-ttu-id="8571a-103">Módosítja az WAF konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="8571a-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="8571a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8571a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8571a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8571a-105">DESCRIPTION</span></span>
<span data-ttu-id="8571a-106">A **set-AzApplicationGatewayWebApplicationFirewallConfiguration** parancsmag módosította az WAF webalkalmazások tűzfalának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="8571a-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="8571a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8571a-107">EXAMPLES</span></span>

### <span data-ttu-id="8571a-108">Példa 1: az alkalmazás-átjáró webalkalmazás-tűzfal konfigurációjának frissítése</span><span class="sxs-lookup"><span data-stu-id="8571a-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="8571a-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, majd a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8571a-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8571a-110">A második parancs engedélyezi az $AppGw tárolt alkalmazás-átjáró tűzfal-konfigurációját, és a tűzfal üzemmódját "észlelési" értékre állítja, RuleSetType a "OWASP" és a RuleSetVersion "3,0"-ra.</span><span class="sxs-lookup"><span data-stu-id="8571a-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="8571a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8571a-111">PARAMETERS</span></span>

### <span data-ttu-id="8571a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8571a-112">-ApplicationGateway</span></span>
<span data-ttu-id="8571a-113">Egy Application Gateway-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="8571a-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="8571a-114">Az Get-AzApplicationGateway parancsmag használatával beszerezhet egy Application Gateway-objektumot.</span><span class="sxs-lookup"><span data-stu-id="8571a-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8571a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8571a-115">-DefaultProfile</span></span>
<span data-ttu-id="8571a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8571a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8571a-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="8571a-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="8571a-118">A letiltott szabályok csoportjai.</span><span class="sxs-lookup"><span data-stu-id="8571a-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="8571a-119">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="8571a-119">-Enabled</span></span>
<span data-ttu-id="8571a-120">Azt jelzi, hogy a webalkalmazás-tűzfal engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="8571a-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="8571a-121">– Kizárás</span><span class="sxs-lookup"><span data-stu-id="8571a-121">-Exclusion</span></span>
<span data-ttu-id="8571a-122">A kizárási listák.</span><span class="sxs-lookup"><span data-stu-id="8571a-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="8571a-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="8571a-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="8571a-124">Maximális feltöltési korlát MB-ban</span><span class="sxs-lookup"><span data-stu-id="8571a-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="8571a-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="8571a-125">-FirewallMode</span></span>
<span data-ttu-id="8571a-126">A webalkalmazás-tűzfal üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8571a-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="8571a-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8571a-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8571a-128">Nyomozás</span><span class="sxs-lookup"><span data-stu-id="8571a-128">Detection</span></span>
- <span data-ttu-id="8571a-129">Megelőzés</span><span class="sxs-lookup"><span data-stu-id="8571a-129">Prevention</span></span>

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

### <span data-ttu-id="8571a-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="8571a-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="8571a-131">Maximális kérés: a szövegtörzs mérete KB-ban</span><span class="sxs-lookup"><span data-stu-id="8571a-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="8571a-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="8571a-132">-RequestBodyCheck</span></span>
<span data-ttu-id="8571a-133">Azt, hogy a kérési törzs be van-e jelölve vagy sem.</span><span class="sxs-lookup"><span data-stu-id="8571a-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="8571a-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="8571a-134">-RuleSetType</span></span>
<span data-ttu-id="8571a-135">A webalkalmazás-tűzfal szabálykészlet típusa.</span><span class="sxs-lookup"><span data-stu-id="8571a-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="8571a-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8571a-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="8571a-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="8571a-137">OWASP</span></span>

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

### <span data-ttu-id="8571a-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="8571a-138">-RuleSetVersion</span></span>
<span data-ttu-id="8571a-139">A szabálykészlet típusának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="8571a-139">The version of the rule set type.</span></span>
<span data-ttu-id="8571a-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8571a-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="8571a-141">3,0</span><span class="sxs-lookup"><span data-stu-id="8571a-141">3.0</span></span>
- <span data-ttu-id="8571a-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="8571a-142">2.2.9</span></span>

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

### <span data-ttu-id="8571a-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8571a-143">-Confirm</span></span>
<span data-ttu-id="8571a-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8571a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8571a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8571a-145">-WhatIf</span></span>
<span data-ttu-id="8571a-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8571a-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8571a-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8571a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8571a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8571a-148">CommonParameters</span></span>
<span data-ttu-id="8571a-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8571a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8571a-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8571a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8571a-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8571a-151">INPUTS</span></span>

### <span data-ttu-id="8571a-152">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8571a-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8571a-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8571a-153">OUTPUTS</span></span>

### <span data-ttu-id="8571a-154">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8571a-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8571a-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8571a-155">NOTES</span></span>

## <span data-ttu-id="8571a-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8571a-156">RELATED LINKS</span></span>

[<span data-ttu-id="8571a-157">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8571a-157">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="8571a-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="8571a-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="8571a-159">Új – AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="8571a-159">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


