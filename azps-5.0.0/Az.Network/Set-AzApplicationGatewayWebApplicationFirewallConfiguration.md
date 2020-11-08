---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9b5e618fc4b4be02614d872bfa5bcdabd2b0fec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187941"
---
# <span data-ttu-id="37c88-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="37c88-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="37c88-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37c88-102">SYNOPSIS</span></span>
<span data-ttu-id="37c88-103">Módosítja az WAF konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="37c88-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="37c88-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37c88-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37c88-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="37c88-105">DESCRIPTION</span></span>
<span data-ttu-id="37c88-106">A **set-AzApplicationGatewayWebApplicationFirewallConfiguration** parancsmag módosította az WAF webalkalmazások tűzfalának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="37c88-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="37c88-107">Példák</span><span class="sxs-lookup"><span data-stu-id="37c88-107">EXAMPLES</span></span>

### <span data-ttu-id="37c88-108">Példa 1: az alkalmazás-átjáró webalkalmazás-tűzfal konfigurációjának frissítése</span><span class="sxs-lookup"><span data-stu-id="37c88-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="37c88-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, majd a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="37c88-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="37c88-110">A második parancs engedélyezi az $AppGw tárolt alkalmazás-átjáró tűzfal-konfigurációját, és a tűzfal üzemmódját "észlelési" értékre állítja, RuleSetType a "OWASP" és a RuleSetVersion "3,0"-ra.</span><span class="sxs-lookup"><span data-stu-id="37c88-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="37c88-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37c88-111">PARAMETERS</span></span>

### <span data-ttu-id="37c88-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37c88-112">-ApplicationGateway</span></span>
<span data-ttu-id="37c88-113">Egy Application Gateway-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="37c88-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="37c88-114">Az Get-AzApplicationGateway parancsmag használatával beszerezhet egy Application Gateway-objektumot.</span><span class="sxs-lookup"><span data-stu-id="37c88-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="37c88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c88-115">-DefaultProfile</span></span>
<span data-ttu-id="37c88-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37c88-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37c88-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="37c88-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="37c88-118">A letiltott szabályok csoportjai.</span><span class="sxs-lookup"><span data-stu-id="37c88-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="37c88-119">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="37c88-119">-Enabled</span></span>
<span data-ttu-id="37c88-120">Azt jelzi, hogy a webalkalmazás-tűzfal engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="37c88-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="37c88-121">– Kizárás</span><span class="sxs-lookup"><span data-stu-id="37c88-121">-Exclusion</span></span>
<span data-ttu-id="37c88-122">A kizárási listák.</span><span class="sxs-lookup"><span data-stu-id="37c88-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="37c88-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="37c88-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="37c88-124">Maximális feltöltési korlát MB-ban</span><span class="sxs-lookup"><span data-stu-id="37c88-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="37c88-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="37c88-125">-FirewallMode</span></span>
<span data-ttu-id="37c88-126">A webalkalmazás-tűzfal üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="37c88-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="37c88-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="37c88-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37c88-128">Nyomozás</span><span class="sxs-lookup"><span data-stu-id="37c88-128">Detection</span></span>
- <span data-ttu-id="37c88-129">Megelőzés</span><span class="sxs-lookup"><span data-stu-id="37c88-129">Prevention</span></span>

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

### <span data-ttu-id="37c88-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="37c88-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="37c88-131">Maximális kérés: a szövegtörzs mérete KB-ban</span><span class="sxs-lookup"><span data-stu-id="37c88-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="37c88-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="37c88-132">-RequestBodyCheck</span></span>
<span data-ttu-id="37c88-133">Azt, hogy a kérési törzs be van-e jelölve vagy sem.</span><span class="sxs-lookup"><span data-stu-id="37c88-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="37c88-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="37c88-134">-RuleSetType</span></span>
<span data-ttu-id="37c88-135">A webalkalmazás-tűzfal szabálykészlet típusa.</span><span class="sxs-lookup"><span data-stu-id="37c88-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="37c88-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="37c88-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="37c88-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="37c88-137">OWASP</span></span>

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

### <span data-ttu-id="37c88-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="37c88-138">-RuleSetVersion</span></span>
<span data-ttu-id="37c88-139">A szabálykészlet típusának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="37c88-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="37c88-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="37c88-140">-Confirm</span></span>
<span data-ttu-id="37c88-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="37c88-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c88-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c88-142">-WhatIf</span></span>
<span data-ttu-id="37c88-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="37c88-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37c88-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37c88-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c88-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c88-145">CommonParameters</span></span>
<span data-ttu-id="37c88-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37c88-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c88-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c88-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c88-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37c88-148">INPUTS</span></span>

### <span data-ttu-id="37c88-149">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37c88-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37c88-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37c88-150">OUTPUTS</span></span>

### <span data-ttu-id="37c88-151">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37c88-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37c88-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37c88-152">NOTES</span></span>

## <span data-ttu-id="37c88-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37c88-153">RELATED LINKS</span></span>

[<span data-ttu-id="37c88-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37c88-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="37c88-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="37c88-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="37c88-156">Új – AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="37c88-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


