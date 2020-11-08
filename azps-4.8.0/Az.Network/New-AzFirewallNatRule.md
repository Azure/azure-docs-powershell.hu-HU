---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184850"
---
# <span data-ttu-id="cf89b-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="cf89b-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="cf89b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf89b-102">SYNOPSIS</span></span>
<span data-ttu-id="cf89b-103">Tűzfal NAT-szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cf89b-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="cf89b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf89b-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf89b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf89b-105">DESCRIPTION</span></span>
<span data-ttu-id="cf89b-106">A **New-AzFirewallNatRule** parancsmag hálózati címfordítási szabályt hoz létre az Azure tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="cf89b-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="cf89b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cf89b-107">EXAMPLES</span></span>

### <span data-ttu-id="cf89b-108">1. példa: szabály létrehozása az összes TCP-forgalom DNAT a 10.0.0.0/24 szolgáltatónál a cél 10.1.2.3:80-tól a cél 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="cf89b-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="cf89b-109">Ez a példa létrehoz egy szabályt, amely a 10.0.0.0/24-ből származó összes forgalmat DNAT a rendeltetési 10.1.2.3:80 – 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="cf89b-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="cf89b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf89b-110">PARAMETERS</span></span>

### <span data-ttu-id="cf89b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf89b-111">-DefaultProfile</span></span>
<span data-ttu-id="cf89b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf89b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf89b-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="cf89b-113">-Description</span></span>
<span data-ttu-id="cf89b-114">A szabály választható leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf89b-114">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf89b-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="cf89b-115">-DestinationAddress</span></span>
<span data-ttu-id="cf89b-116">A szabály rendeltetési címe</span><span class="sxs-lookup"><span data-stu-id="cf89b-116">The destination addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf89b-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="cf89b-117">-DestinationPort</span></span>
<span data-ttu-id="cf89b-118">A szabály rendeltetési portjai</span><span class="sxs-lookup"><span data-stu-id="cf89b-118">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf89b-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf89b-119">-Name</span></span>
<span data-ttu-id="cf89b-120">A NAT-szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf89b-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="cf89b-121">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="cf89b-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="cf89b-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="cf89b-122">-Protocol</span></span>
<span data-ttu-id="cf89b-123">Adja meg, hogy milyen típusú forgalmat szeretne szűrni a szabály.</span><span class="sxs-lookup"><span data-stu-id="cf89b-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="cf89b-124">A támogatott protokollok a TCP és az UDP.</span><span class="sxs-lookup"><span data-stu-id="cf89b-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="cf89b-125">Az "any" speciális érték, amely azt jelenti, hogy a TCP és az UDP is megfelel, de más protokollok nem.</span><span class="sxs-lookup"><span data-stu-id="cf89b-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf89b-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="cf89b-126">-SourceAddress</span></span>
<span data-ttu-id="cf89b-127">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="cf89b-127">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf89b-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="cf89b-128">-SourceIpGroup</span></span>
<span data-ttu-id="cf89b-129">A szabály forrás ipgroup</span><span class="sxs-lookup"><span data-stu-id="cf89b-129">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf89b-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="cf89b-130">-TranslatedAddress</span></span>
<span data-ttu-id="cf89b-131">A címfordítás kívánt eredményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf89b-131">Specifies the desired result of the address translation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf89b-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="cf89b-132">-TranslatedFqdn</span></span>
<span data-ttu-id="cf89b-133">A CÍMFORDÍTÁSi szabály lefordított FQDN-je</span><span class="sxs-lookup"><span data-stu-id="cf89b-133">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf89b-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="cf89b-134">-TranslatedPort</span></span>
<span data-ttu-id="cf89b-135">A port fordításának kívánt eredményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf89b-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="cf89b-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf89b-136">-Confirm</span></span>
<span data-ttu-id="cf89b-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf89b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf89b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf89b-138">-WhatIf</span></span>
<span data-ttu-id="cf89b-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf89b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf89b-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf89b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf89b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf89b-141">CommonParameters</span></span>
<span data-ttu-id="cf89b-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf89b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf89b-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf89b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf89b-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf89b-144">INPUTS</span></span>

### <span data-ttu-id="cf89b-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="cf89b-145">None</span></span>

## <span data-ttu-id="cf89b-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf89b-146">OUTPUTS</span></span>

### <span data-ttu-id="cf89b-147">Microsoft. Azure. commands. Network. models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="cf89b-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="cf89b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf89b-148">NOTES</span></span>

## <span data-ttu-id="cf89b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf89b-149">RELATED LINKS</span></span>

[<span data-ttu-id="cf89b-150">Új – AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="cf89b-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="cf89b-151">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cf89b-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="cf89b-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cf89b-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
