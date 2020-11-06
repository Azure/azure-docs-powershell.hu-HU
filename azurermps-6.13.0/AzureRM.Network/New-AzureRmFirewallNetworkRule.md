---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494043"
---
# <span data-ttu-id="e98dc-101">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e98dc-101">New-AzureRmFirewallNetworkRule</span></span>

## <span data-ttu-id="e98dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e98dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e98dc-103">Tűzfal-hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="e98dc-103">Creates a Firewall Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e98dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e98dc-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e98dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e98dc-105">DESCRIPTION</span></span>
<span data-ttu-id="e98dc-106">A **New-AzureRmFirewallNetworkRule** parancsmag hálózati szabályt hoz létre az Azure tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="e98dc-106">The **New-AzureRmFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="e98dc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e98dc-107">EXAMPLES</span></span>

### <span data-ttu-id="e98dc-108">1: szabály létrehozása az összes TCP-forgalomhoz</span><span class="sxs-lookup"><span data-stu-id="e98dc-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="e98dc-109">Ez a példa létrehoz egy szabályt az összes TCP-forgalomhoz.</span><span class="sxs-lookup"><span data-stu-id="e98dc-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="e98dc-110">A felhasználó kikényszeríti, hogy a forgalom engedélyezett vagy elutasított-e a szabályhoz társított szabály-gyűjtemény alapján.</span><span class="sxs-lookup"><span data-stu-id="e98dc-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="e98dc-111">2: szabály létrehozása az összes TCP-forgalomra a 10.0.0.0-től a 60.1.5.0-ig: 4040</span><span class="sxs-lookup"><span data-stu-id="e98dc-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="e98dc-112">Ez a példa létrehoz egy szabályt az összes TCP-forgalomhoz a 10.0.0.0-től a 60.1.5.0-ig: 4040.</span><span class="sxs-lookup"><span data-stu-id="e98dc-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="e98dc-113">A felhasználó kikényszeríti, hogy a forgalom engedélyezett vagy elutasított-e a szabályhoz társított szabály-gyűjtemény alapján.</span><span class="sxs-lookup"><span data-stu-id="e98dc-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="e98dc-114">3: szabály létrehozása bármely forrásból az összes TCP-és ICMP-forgalomra a 10.0.0.0/16-ra</span><span class="sxs-lookup"><span data-stu-id="e98dc-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="e98dc-115">Ez a példa létrehoz egy szabályt az összes TCP-forgalomhoz a 10.0.0.0-től a 60.1.5.0-ig: 4040.</span><span class="sxs-lookup"><span data-stu-id="e98dc-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="e98dc-116">A felhasználó kikényszeríti, hogy a forgalom engedélyezett vagy elutasított-e a szabályhoz társított szabály-gyűjtemény alapján.</span><span class="sxs-lookup"><span data-stu-id="e98dc-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="e98dc-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e98dc-117">PARAMETERS</span></span>

### <span data-ttu-id="e98dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98dc-118">-DefaultProfile</span></span>
<span data-ttu-id="e98dc-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e98dc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e98dc-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e98dc-120">-Description</span></span>
<span data-ttu-id="e98dc-121">A szabály választható leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e98dc-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98dc-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e98dc-122">-DestinationAddress</span></span>
<span data-ttu-id="e98dc-123">A szabály rendeltetési címe</span><span class="sxs-lookup"><span data-stu-id="e98dc-123">The destination addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98dc-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e98dc-124">-DestinationPort</span></span>
<span data-ttu-id="e98dc-125">A szabály rendeltetési portjai</span><span class="sxs-lookup"><span data-stu-id="e98dc-125">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98dc-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e98dc-126">-Name</span></span>
<span data-ttu-id="e98dc-127">A hálózati szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e98dc-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="e98dc-128">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="e98dc-128">The name must be unique inside a rule collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98dc-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e98dc-129">-Protocol</span></span>
<span data-ttu-id="e98dc-130">Adja meg, hogy milyen típusú forgalmat szeretne szűrni a szabály.</span><span class="sxs-lookup"><span data-stu-id="e98dc-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="e98dc-131">Lehetséges értékek: TCP, UDP, ICMP és any.</span><span class="sxs-lookup"><span data-stu-id="e98dc-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98dc-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e98dc-132">-SourceAddress</span></span>
<span data-ttu-id="e98dc-133">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="e98dc-133">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98dc-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e98dc-134">-Confirm</span></span>
<span data-ttu-id="e98dc-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e98dc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e98dc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e98dc-136">-WhatIf</span></span>
<span data-ttu-id="e98dc-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e98dc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e98dc-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e98dc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e98dc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98dc-139">CommonParameters</span></span>
<span data-ttu-id="e98dc-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e98dc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98dc-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e98dc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98dc-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e98dc-142">INPUTS</span></span>

### <span data-ttu-id="e98dc-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="e98dc-143">None</span></span>
<span data-ttu-id="e98dc-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e98dc-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e98dc-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e98dc-145">OUTPUTS</span></span>

### <span data-ttu-id="e98dc-146">Microsoft. Azure. commands. Network. models. PSFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e98dc-146">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRule</span></span>

## <span data-ttu-id="e98dc-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e98dc-147">NOTES</span></span>

## <span data-ttu-id="e98dc-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e98dc-148">RELATED LINKS</span></span>

[<span data-ttu-id="e98dc-149">Új – AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e98dc-149">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)

[<span data-ttu-id="e98dc-150">Új – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e98dc-150">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="e98dc-151">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e98dc-151">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
