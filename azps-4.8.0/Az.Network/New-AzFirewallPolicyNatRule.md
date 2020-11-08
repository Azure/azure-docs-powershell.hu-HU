---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024613"
---
# <span data-ttu-id="3de8c-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="3de8c-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="3de8c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3de8c-102">SYNOPSIS</span></span>
<span data-ttu-id="3de8c-103">Új Azure tűzfal-házirend létrehozása NAT-szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="3de8c-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="3de8c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3de8c-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3de8c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3de8c-105">DESCRIPTION</span></span>
<span data-ttu-id="3de8c-106">A **New-AzFirewallPolicyNatRule** parancsmag hálózati címfordítási szabályt hoz létre az Azure tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="3de8c-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="3de8c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3de8c-107">EXAMPLES</span></span>

### <span data-ttu-id="3de8c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3de8c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="3de8c-109">Ez a példa NAT-szabályt hoz létre a forráscím, a protokoll, a célcím, a célport, a lefordított cím és a lefordított port beállítással.</span><span class="sxs-lookup"><span data-stu-id="3de8c-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="3de8c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3de8c-110">PARAMETERS</span></span>

### <span data-ttu-id="3de8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de8c-111">-DefaultProfile</span></span>
<span data-ttu-id="3de8c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3de8c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3de8c-113">-Name</span></span>
<span data-ttu-id="3de8c-114">A NAT-szabály gyűjteményének neve</span><span class="sxs-lookup"><span data-stu-id="3de8c-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="3de8c-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="3de8c-115">-Description</span></span>
<span data-ttu-id="3de8c-116">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="3de8c-116">The description of the rule</span></span>

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

### <span data-ttu-id="3de8c-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="3de8c-117">-DestinationAddress</span></span>
<span data-ttu-id="3de8c-118">A szabály rendeltetési címe.</span><span class="sxs-lookup"><span data-stu-id="3de8c-118">The destination addresses of the rule.</span></span> <span data-ttu-id="3de8c-119">Ehhez a tűzfal nyilvános IP-címének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3de8c-119">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8c-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3de8c-120">-DestinationPort</span></span>
<span data-ttu-id="3de8c-121">A szabály rendeltetési portjai</span><span class="sxs-lookup"><span data-stu-id="3de8c-121">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8c-122">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="3de8c-122">-Protocols</span></span>
<span data-ttu-id="3de8c-123">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="3de8c-123">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8c-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="3de8c-124">-SourceAddress</span></span>
<span data-ttu-id="3de8c-125">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="3de8c-125">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8c-126">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="3de8c-126">-SourceIpGroup</span></span>
<span data-ttu-id="3de8c-127">A szabály forrás ipgroups</span><span class="sxs-lookup"><span data-stu-id="3de8c-127">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8c-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="3de8c-128">-TranslatedAddress</span></span>
<span data-ttu-id="3de8c-129">A NAT-szabály lefordított címe</span><span class="sxs-lookup"><span data-stu-id="3de8c-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="3de8c-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="3de8c-130">-TranslatedPort</span></span>
<span data-ttu-id="3de8c-131">A NAT-szabály lefordított portja</span><span class="sxs-lookup"><span data-stu-id="3de8c-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="3de8c-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3de8c-132">-Confirm</span></span>
<span data-ttu-id="3de8c-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3de8c-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de8c-134">-WhatIf</span></span>
<span data-ttu-id="3de8c-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3de8c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de8c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3de8c-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de8c-137">CommonParameters</span></span>
<span data-ttu-id="3de8c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3de8c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de8c-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3de8c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de8c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3de8c-140">INPUTS</span></span>

### <span data-ttu-id="3de8c-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="3de8c-141">None</span></span>

## <span data-ttu-id="3de8c-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3de8c-142">OUTPUTS</span></span>

### <span data-ttu-id="3de8c-143">Microsoft. Azure. commands. Network. models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="3de8c-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="3de8c-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3de8c-144">NOTES</span></span>

## <span data-ttu-id="3de8c-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3de8c-145">RELATED LINKS</span></span>
