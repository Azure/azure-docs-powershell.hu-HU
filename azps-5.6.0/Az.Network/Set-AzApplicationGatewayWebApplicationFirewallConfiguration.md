---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 95d0e82609c2cb8bfcbbfcf57d1354d219da9f9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941049"
---
# <span data-ttu-id="fc2d4-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc2d4-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="fc2d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc2d4-102">SYNOPSIS</span></span>
<span data-ttu-id="fc2d4-103">Módosítja egy alkalmazás átjárójának WAF-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="fc2d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc2d4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc2d4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc2d4-105">DESCRIPTION</span></span>
<span data-ttu-id="fc2d4-106">A **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** parancsmag módosítja egy alkalmazás-átjáró webalkalmazás tűzfalának (WAF) konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="fc2d4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc2d4-107">EXAMPLES</span></span>

### <span data-ttu-id="fc2d4-108">1. példa: Az alkalmazás átjárójának webalkalmazás tűzfalkonfigurációjának frissítése</span><span class="sxs-lookup"><span data-stu-id="fc2d4-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="fc2d4-109">Az első parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, majd a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fc2d4-110">A második parancs engedélyezi a tűzfal konfigurációját az $AppGw-ben tárolt alkalmazás-átjáróhoz, és a tűzfal üzemmódot "Észlelés", a RuleSetType beállítást "OWASP" és a RuleSetVersion beállítást "3.0" módra állítja.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="fc2d4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc2d4-111">PARAMETERS</span></span>

### <span data-ttu-id="fc2d4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc2d4-112">-ApplicationGateway</span></span>
<span data-ttu-id="fc2d4-113">Egy alkalmazás-átjáróobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="fc2d4-114">A Get-AzApplicationGateway parancsmag használatával lekért egy alkalmazás-átjáróobjektumot.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="fc2d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc2d4-115">-DefaultProfile</span></span>
<span data-ttu-id="fc2d4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc2d4-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="fc2d4-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="fc2d4-118">A letiltott szabálycsoportok.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="fc2d4-119">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="fc2d4-119">-Enabled</span></span>
<span data-ttu-id="fc2d4-120">Azt jelzi, hogy engedélyezve van-e a webalkalmazás tűzfala.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="fc2d4-121">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="fc2d4-121">-Exclusion</span></span>
<span data-ttu-id="fc2d4-122">A kivétellisták.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="fc2d4-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="fc2d4-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="fc2d4-124">Maximális fájlfeltöltési korlát MB-ban.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="fc2d4-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="fc2d4-125">-FirewallMode</span></span>
<span data-ttu-id="fc2d4-126">A webalkalmazás tűzfalmódját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="fc2d4-127">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="fc2d4-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fc2d4-128">Észlelés</span><span class="sxs-lookup"><span data-stu-id="fc2d4-128">Detection</span></span>
- <span data-ttu-id="fc2d4-129">Megelőzés</span><span class="sxs-lookup"><span data-stu-id="fc2d4-129">Prevention</span></span>

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

### <span data-ttu-id="fc2d4-130">-MaxRequestQuestSizeInKb</span><span class="sxs-lookup"><span data-stu-id="fc2d4-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="fc2d4-131">A kérés maximális mérete KB-ban.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="fc2d4-132">-RequestCheck</span><span class="sxs-lookup"><span data-stu-id="fc2d4-132">-RequestBodyCheck</span></span>
<span data-ttu-id="fc2d4-133">Függetlenül attól, hogy a kérelem törzse be van-e jelölve.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="fc2d4-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="fc2d4-134">-RuleSetType</span></span>
<span data-ttu-id="fc2d4-135">A webalkalmazás tűzfalszabálykészletének típusa.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="fc2d4-136">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="fc2d4-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="fc2d4-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="fc2d4-137">OWASP</span></span>

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

### <span data-ttu-id="fc2d4-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="fc2d4-138">-RuleSetVersion</span></span>
<span data-ttu-id="fc2d4-139">A szabálykészlet-típus verziója.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="fc2d4-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc2d4-140">-Confirm</span></span>
<span data-ttu-id="fc2d4-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc2d4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc2d4-142">-WhatIf</span></span>
<span data-ttu-id="fc2d4-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc2d4-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc2d4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc2d4-145">CommonParameters</span></span>
<span data-ttu-id="fc2d4-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc2d4-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc2d4-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc2d4-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc2d4-148">INPUTS</span></span>

### <span data-ttu-id="fc2d4-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc2d4-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc2d4-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc2d4-150">OUTPUTS</span></span>

### <span data-ttu-id="fc2d4-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc2d4-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc2d4-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc2d4-152">NOTES</span></span>

## <span data-ttu-id="fc2d4-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc2d4-153">RELATED LINKS</span></span>

[<span data-ttu-id="fc2d4-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc2d4-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="fc2d4-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc2d4-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="fc2d4-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc2d4-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


