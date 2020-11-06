---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
ms.openlocfilehash: 0bad5133dd57ec0bee88949fbc9536a6389d6112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498308"
---
# <span data-ttu-id="d9b64-101">New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="d9b64-101">New-AzureRmFirewallNatRule</span></span>

## <span data-ttu-id="d9b64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9b64-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b64-103">Tűzfal NAT-szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d9b64-103">Creates a Firewall NAT Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9b64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9b64-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9b64-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9b64-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b64-106">A **New-AzureRmFirewallNatRule** parancsmag hálózati címfordítási szabályt hoz létre az Azure tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="d9b64-106">The **New-AzureRmFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="d9b64-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d9b64-107">EXAMPLES</span></span>

### <span data-ttu-id="d9b64-108">1: szabály létrehozása az összes TCP-forgalom DNAT a 10.0.0.0/24-ből a cél 10.1.2.3:80-tól a cél 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="d9b64-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzureRmFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="d9b64-109">Ez a példa létrehoz egy szabályt, amely a 10.0.0.0/24-ből származó összes forgalmat DNAT a rendeltetési 10.1.2.3:80 – 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="d9b64-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="d9b64-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9b64-110">PARAMETERS</span></span>

### <span data-ttu-id="d9b64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b64-111">-DefaultProfile</span></span>
<span data-ttu-id="d9b64-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9b64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9b64-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="d9b64-113">-Description</span></span>
<span data-ttu-id="d9b64-114">A szabály választható leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9b64-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="d9b64-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d9b64-115">-DestinationAddress</span></span>
<span data-ttu-id="d9b64-116">A szabály rendeltetési címe.</span><span class="sxs-lookup"><span data-stu-id="d9b64-116">The destination addresses of the rule.</span></span>

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

### <span data-ttu-id="d9b64-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d9b64-117">-DestinationPort</span></span>
<span data-ttu-id="d9b64-118">A szabály rendeltetési portjai</span><span class="sxs-lookup"><span data-stu-id="d9b64-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="d9b64-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9b64-119">-Name</span></span>
<span data-ttu-id="d9b64-120">A NAT-szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9b64-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="d9b64-121">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="d9b64-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="d9b64-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d9b64-122">-Protocol</span></span>
<span data-ttu-id="d9b64-123">Adja meg, hogy milyen típusú forgalmat szeretne szűrni a szabály.</span><span class="sxs-lookup"><span data-stu-id="d9b64-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="d9b64-124">A támogatott protokollok a TCP és az UDP.</span><span class="sxs-lookup"><span data-stu-id="d9b64-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="d9b64-125">Az "any" speciális érték, amely azt jelenti, hogy a TCP és az UDP is megfelel, de más protokollok nem.</span><span class="sxs-lookup"><span data-stu-id="d9b64-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9b64-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d9b64-126">-SourceAddress</span></span>
<span data-ttu-id="d9b64-127">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="d9b64-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="d9b64-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="d9b64-128">-TranslatedAddress</span></span>
<span data-ttu-id="d9b64-129">A címfordítás kívánt eredményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9b64-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="d9b64-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="d9b64-130">-TranslatedPort</span></span>
<span data-ttu-id="d9b64-131">A port fordításának kívánt eredményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d9b64-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="d9b64-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d9b64-132">-Confirm</span></span>
<span data-ttu-id="d9b64-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d9b64-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b64-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b64-134">-WhatIf</span></span>
<span data-ttu-id="d9b64-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d9b64-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9b64-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9b64-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b64-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b64-137">CommonParameters</span></span>
<span data-ttu-id="d9b64-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9b64-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b64-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b64-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b64-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9b64-140">INPUTS</span></span>

### <span data-ttu-id="d9b64-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="d9b64-141">None</span></span>
<span data-ttu-id="d9b64-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d9b64-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9b64-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9b64-143">OUTPUTS</span></span>

### <span data-ttu-id="d9b64-144">Microsoft. Azure. commands. Network. models. PSFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="d9b64-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRule</span></span>

## <span data-ttu-id="d9b64-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9b64-145">NOTES</span></span>

## <span data-ttu-id="d9b64-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9b64-146">RELATED LINKS</span></span>

[<span data-ttu-id="d9b64-147">Új – AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d9b64-147">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="d9b64-148">Új – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d9b64-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="d9b64-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d9b64-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
