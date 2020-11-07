---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: fd925829248c7f11f047de90ddc2bc0b57f51b71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849554"
---
# <span data-ttu-id="f3c72-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c72-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="f3c72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3c72-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c72-103">Módosítja az WAF konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f3c72-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3c72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3c72-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3c72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3c72-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c72-106">A **set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** parancsmag módosította az WAF webalkalmazások tűzfalának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f3c72-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="f3c72-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f3c72-107">EXAMPLES</span></span>

### <span data-ttu-id="f3c72-108">Példa 1: az alkalmazás-átjáró webalkalmazás-tűzfal konfigurációjának frissítése</span><span class="sxs-lookup"><span data-stu-id="f3c72-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="f3c72-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, majd a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f3c72-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f3c72-110">A második parancs engedélyezi az $AppGw tárolt alkalmazás-átjáró tűzfal-konfigurációját, és a tűzfal üzemmódját "észlelési" értékre állítja, RuleSetType a "OWASP" és a RuleSetVersion "3,0"-ra.</span><span class="sxs-lookup"><span data-stu-id="f3c72-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="f3c72-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3c72-111">PARAMETERS</span></span>

### <span data-ttu-id="f3c72-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3c72-112">-ApplicationGateway</span></span>
<span data-ttu-id="f3c72-113">Egy Application Gateway-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f3c72-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="f3c72-114">Az Get-AzureRmApplicationGateway parancsmag használatával beszerezhet egy Application Gateway-objektumot.</span><span class="sxs-lookup"><span data-stu-id="f3c72-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c72-115">-DefaultProfile</span></span>
<span data-ttu-id="f3c72-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3c72-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3c72-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="f3c72-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="f3c72-118">A letiltott szabályok csoportjai.</span><span class="sxs-lookup"><span data-stu-id="f3c72-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="f3c72-119">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="f3c72-119">-Enabled</span></span>
<span data-ttu-id="f3c72-120">Azt jelzi, hogy a webalkalmazás-tűzfal engedélyezve van-e.</span><span class="sxs-lookup"><span data-stu-id="f3c72-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="f3c72-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="f3c72-121">-FirewallMode</span></span>
<span data-ttu-id="f3c72-122">A webalkalmazás-tűzfal üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3c72-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="f3c72-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f3c72-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3c72-124">Nyomozás</span><span class="sxs-lookup"><span data-stu-id="f3c72-124">Detection</span></span>
- <span data-ttu-id="f3c72-125">Megelőzés</span><span class="sxs-lookup"><span data-stu-id="f3c72-125">Prevention</span></span>

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

### <span data-ttu-id="f3c72-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="f3c72-126">-RuleSetType</span></span>
<span data-ttu-id="f3c72-127">A webalkalmazás-tűzfal szabálykészlet típusa.</span><span class="sxs-lookup"><span data-stu-id="f3c72-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="f3c72-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f3c72-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="f3c72-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="f3c72-129">OWASP</span></span>

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

### <span data-ttu-id="f3c72-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="f3c72-130">-RuleSetVersion</span></span>
<span data-ttu-id="f3c72-131">A szabálykészlet típusának verziószáma.</span><span class="sxs-lookup"><span data-stu-id="f3c72-131">The version of the rule set type.</span></span>
<span data-ttu-id="f3c72-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f3c72-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="f3c72-133">3,0</span><span class="sxs-lookup"><span data-stu-id="f3c72-133">3.0</span></span>
- <span data-ttu-id="f3c72-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="f3c72-134">2.2.9</span></span>

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

### <span data-ttu-id="f3c72-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3c72-135">-Confirm</span></span>
<span data-ttu-id="f3c72-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3c72-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c72-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c72-137">-WhatIf</span></span>
<span data-ttu-id="f3c72-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3c72-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3c72-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3c72-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c72-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c72-140">CommonParameters</span></span>
<span data-ttu-id="f3c72-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3c72-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c72-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c72-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c72-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3c72-143">INPUTS</span></span>

### <span data-ttu-id="f3c72-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3c72-144">PSApplicationGateway</span></span>
<span data-ttu-id="f3c72-145">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f3c72-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="f3c72-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3c72-146">OUTPUTS</span></span>

### <span data-ttu-id="f3c72-147">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3c72-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f3c72-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3c72-148">NOTES</span></span>

## <span data-ttu-id="f3c72-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3c72-149">RELATED LINKS</span></span>

[<span data-ttu-id="f3c72-150">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3c72-150">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="f3c72-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c72-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="f3c72-152">Új – AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c72-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


