---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 31c066ce97502c43c9e93bdaf532ee63e701a18f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845134"
---
# <span data-ttu-id="46a9e-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="46a9e-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="46a9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="46a9e-103">Tűzfal-hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="46a9e-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="46a9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46a9e-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a9e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="46a9e-105">DESCRIPTION</span></span>
<span data-ttu-id="46a9e-106">A **New-AzFirewallNetworkRule** parancsmag hálózati szabályt hoz létre az Azure tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="46a9e-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="46a9e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="46a9e-107">EXAMPLES</span></span>

### <span data-ttu-id="46a9e-108">1: szabály létrehozása az összes TCP-forgalomhoz</span><span class="sxs-lookup"><span data-stu-id="46a9e-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="46a9e-109">Ez a példa létrehoz egy szabályt az összes TCP-forgalomhoz.</span><span class="sxs-lookup"><span data-stu-id="46a9e-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="46a9e-110">A felhasználó kikényszeríti, hogy a forgalom engedélyezett vagy elutasított-e a szabályhoz társított szabály-gyűjtemény alapján.</span><span class="sxs-lookup"><span data-stu-id="46a9e-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="46a9e-111">2: szabály létrehozása az összes TCP-forgalomra a 10.0.0.0-től a 60.1.5.0-ig: 4040</span><span class="sxs-lookup"><span data-stu-id="46a9e-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="46a9e-112">Ez a példa létrehoz egy szabályt az összes TCP-forgalomhoz a 10.0.0.0-től a 60.1.5.0-ig: 4040.</span><span class="sxs-lookup"><span data-stu-id="46a9e-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="46a9e-113">A felhasználó kikényszeríti, hogy a forgalom engedélyezett vagy elutasított-e a szabályhoz társított szabály-gyűjtemény alapján.</span><span class="sxs-lookup"><span data-stu-id="46a9e-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="46a9e-114">3: szabály létrehozása bármely forrásból az összes TCP-és ICMP-forgalomra a 10.0.0.0/16-ra</span><span class="sxs-lookup"><span data-stu-id="46a9e-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="46a9e-115">Ez a példa létrehoz egy szabályt az összes TCP-forgalomhoz a 10.0.0.0-től a 60.1.5.0-ig: 4040.</span><span class="sxs-lookup"><span data-stu-id="46a9e-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="46a9e-116">A felhasználó kikényszeríti, hogy a forgalom engedélyezett vagy elutasított-e a szabályhoz társított szabály-gyűjtemény alapján.</span><span class="sxs-lookup"><span data-stu-id="46a9e-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="46a9e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46a9e-117">PARAMETERS</span></span>

### <span data-ttu-id="46a9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a9e-118">-DefaultProfile</span></span>
<span data-ttu-id="46a9e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46a9e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46a9e-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="46a9e-120">-Description</span></span>
<span data-ttu-id="46a9e-121">A szabály választható leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="46a9e-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="46a9e-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="46a9e-122">-DestinationAddress</span></span>
<span data-ttu-id="46a9e-123">A szabály rendeltetési címe</span><span class="sxs-lookup"><span data-stu-id="46a9e-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="46a9e-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="46a9e-124">-DestinationFqdn</span></span>
<span data-ttu-id="46a9e-125">A szabály cél FQDN-je</span><span class="sxs-lookup"><span data-stu-id="46a9e-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="46a9e-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="46a9e-126">-DestinationIpGroup</span></span>
<span data-ttu-id="46a9e-127">A szabály rendeltetési ipgroup</span><span class="sxs-lookup"><span data-stu-id="46a9e-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="46a9e-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="46a9e-128">-DestinationPort</span></span>
<span data-ttu-id="46a9e-129">A szabály rendeltetési portjai</span><span class="sxs-lookup"><span data-stu-id="46a9e-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="46a9e-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46a9e-130">-Name</span></span>
<span data-ttu-id="46a9e-131">A hálózati szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46a9e-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="46a9e-132">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="46a9e-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="46a9e-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="46a9e-133">-Protocol</span></span>
<span data-ttu-id="46a9e-134">Adja meg, hogy milyen típusú forgalmat szeretne szűrni a szabály.</span><span class="sxs-lookup"><span data-stu-id="46a9e-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="46a9e-135">Lehetséges értékek: TCP, UDP, ICMP és any.</span><span class="sxs-lookup"><span data-stu-id="46a9e-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a9e-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="46a9e-136">-SourceAddress</span></span>
<span data-ttu-id="46a9e-137">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="46a9e-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="46a9e-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="46a9e-138">-SourceIpGroup</span></span>
<span data-ttu-id="46a9e-139">A szabály forrás ipgroup</span><span class="sxs-lookup"><span data-stu-id="46a9e-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="46a9e-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46a9e-140">-Confirm</span></span>
<span data-ttu-id="46a9e-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46a9e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a9e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a9e-142">-WhatIf</span></span>
<span data-ttu-id="46a9e-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46a9e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a9e-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46a9e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a9e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a9e-145">CommonParameters</span></span>
<span data-ttu-id="46a9e-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46a9e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a9e-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a9e-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a9e-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46a9e-148">INPUTS</span></span>

### <span data-ttu-id="46a9e-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="46a9e-149">None</span></span>

## <span data-ttu-id="46a9e-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46a9e-150">OUTPUTS</span></span>

### <span data-ttu-id="46a9e-151">Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="46a9e-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="46a9e-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46a9e-152">NOTES</span></span>

## <span data-ttu-id="46a9e-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46a9e-153">RELATED LINKS</span></span>

[<span data-ttu-id="46a9e-154">Új – AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="46a9e-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="46a9e-155">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="46a9e-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="46a9e-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="46a9e-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
