---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: c7519b6cf5f95f80a20f94bbae5ec097964bd01a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670340"
---
# <span data-ttu-id="73f3a-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="73f3a-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="73f3a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="73f3a-103">Tűzfal NAT-szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="73f3a-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="73f3a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73f3a-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f3a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="73f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="73f3a-106">A **New-AzFirewallNatRule** parancsmag hálózati címfordítási szabályt hoz létre az Azure tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="73f3a-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="73f3a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="73f3a-107">EXAMPLES</span></span>

### <span data-ttu-id="73f3a-108">1: szabály létrehozása az összes TCP-forgalom DNAT a 10.0.0.0/24-ből a cél 10.1.2.3:80-tól a cél 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="73f3a-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="73f3a-109">Ez a példa létrehoz egy szabályt, amely a 10.0.0.0/24-ből származó összes forgalmat DNAT a rendeltetési 10.1.2.3:80 – 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="73f3a-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="73f3a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73f3a-110">PARAMETERS</span></span>

### <span data-ttu-id="73f3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f3a-111">-DefaultProfile</span></span>
<span data-ttu-id="73f3a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73f3a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73f3a-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="73f3a-113">-Description</span></span>
<span data-ttu-id="73f3a-114">A szabály választható leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="73f3a-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="73f3a-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="73f3a-115">-DestinationAddress</span></span>
<span data-ttu-id="73f3a-116">A szabály rendeltetési címe.</span><span class="sxs-lookup"><span data-stu-id="73f3a-116">The destination addresses of the rule.</span></span>

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

### <span data-ttu-id="73f3a-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="73f3a-117">-DestinationPort</span></span>
<span data-ttu-id="73f3a-118">A szabály rendeltetési portjai</span><span class="sxs-lookup"><span data-stu-id="73f3a-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="73f3a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73f3a-119">-Name</span></span>
<span data-ttu-id="73f3a-120">A NAT-szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73f3a-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="73f3a-121">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="73f3a-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="73f3a-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="73f3a-122">-Protocol</span></span>
<span data-ttu-id="73f3a-123">Adja meg, hogy milyen típusú forgalmat szeretne szűrni a szabály.</span><span class="sxs-lookup"><span data-stu-id="73f3a-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="73f3a-124">A támogatott protokollok a TCP és az UDP.</span><span class="sxs-lookup"><span data-stu-id="73f3a-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="73f3a-125">Az "any" speciális érték, amely azt jelenti, hogy a TCP és az UDP is megfelel, de más protokollok nem.</span><span class="sxs-lookup"><span data-stu-id="73f3a-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="73f3a-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="73f3a-126">-SourceAddress</span></span>
<span data-ttu-id="73f3a-127">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="73f3a-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="73f3a-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="73f3a-128">-TranslatedAddress</span></span>
<span data-ttu-id="73f3a-129">A címfordítás kívánt eredményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73f3a-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="73f3a-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="73f3a-130">-TranslatedPort</span></span>
<span data-ttu-id="73f3a-131">A port fordításának kívánt eredményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73f3a-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="73f3a-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="73f3a-132">-Confirm</span></span>
<span data-ttu-id="73f3a-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73f3a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73f3a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f3a-134">-WhatIf</span></span>
<span data-ttu-id="73f3a-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="73f3a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73f3a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73f3a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73f3a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f3a-137">CommonParameters</span></span>
<span data-ttu-id="73f3a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73f3a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f3a-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f3a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f3a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73f3a-140">INPUTS</span></span>

### <span data-ttu-id="73f3a-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="73f3a-141">None</span></span>

## <span data-ttu-id="73f3a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73f3a-142">OUTPUTS</span></span>

### <span data-ttu-id="73f3a-143">Microsoft. Azure. commands. Network. models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="73f3a-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="73f3a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73f3a-144">NOTES</span></span>

## <span data-ttu-id="73f3a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73f3a-145">RELATED LINKS</span></span>

[<span data-ttu-id="73f3a-146">Új – AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="73f3a-146">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="73f3a-147">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="73f3a-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="73f3a-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="73f3a-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
