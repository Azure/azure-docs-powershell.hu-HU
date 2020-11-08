---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: b4cbc404139cd56e75f03c5cb19cb9b761576e39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011817"
---
# <span data-ttu-id="f91a8-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f91a8-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="f91a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f91a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f91a8-103">Új Azure tűzfal-házirend-hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="f91a8-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="f91a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f91a8-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f91a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f91a8-105">DESCRIPTION</span></span>
<span data-ttu-id="f91a8-106">A **New-AzFirewallPolicyNetworkRule** parancsmag hálózati szabályt hoz létre az Azure tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="f91a8-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="f91a8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f91a8-107">EXAMPLES</span></span>

### <span data-ttu-id="f91a8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f91a8-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="f91a8-109">Ebben a példában egy hálózati szabályt hoz létre a forráscím, a protokoll, a cél címe és a cél porttal.</span><span class="sxs-lookup"><span data-stu-id="f91a8-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="f91a8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f91a8-110">PARAMETERS</span></span>

### <span data-ttu-id="f91a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91a8-111">-DefaultProfile</span></span>
<span data-ttu-id="f91a8-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f91a8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f91a8-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f91a8-113">-Description</span></span>
<span data-ttu-id="f91a8-114">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="f91a8-114">The description of the rule</span></span>

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

### <span data-ttu-id="f91a8-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f91a8-115">-DestinationAddress</span></span>
<span data-ttu-id="f91a8-116">A szabály rendeltetési címe</span><span class="sxs-lookup"><span data-stu-id="f91a8-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="f91a8-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f91a8-117">-DestinationPort</span></span>
<span data-ttu-id="f91a8-118">A szabály rendeltetési portjai</span><span class="sxs-lookup"><span data-stu-id="f91a8-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="f91a8-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f91a8-119">-Name</span></span>
<span data-ttu-id="f91a8-120">A hálózati szabály neve</span><span class="sxs-lookup"><span data-stu-id="f91a8-120">The name of the Network Rule</span></span>

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

### <span data-ttu-id="f91a8-121">-Protokollok</span><span class="sxs-lookup"><span data-stu-id="f91a8-121">-Protocols</span></span>
<span data-ttu-id="f91a8-122">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="f91a8-122">The protocols of the rule</span></span>

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

### <span data-ttu-id="f91a8-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="f91a8-123">-SourceAddress</span></span>
<span data-ttu-id="f91a8-124">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="f91a8-124">The source addresses of the rule</span></span>

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

### <span data-ttu-id="f91a8-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f91a8-125">-Confirm</span></span>
<span data-ttu-id="f91a8-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f91a8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f91a8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f91a8-127">-WhatIf</span></span>
<span data-ttu-id="f91a8-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f91a8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f91a8-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f91a8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f91a8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91a8-130">CommonParameters</span></span>
<span data-ttu-id="f91a8-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f91a8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91a8-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f91a8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91a8-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f91a8-133">INPUTS</span></span>

### <span data-ttu-id="f91a8-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="f91a8-134">None</span></span>

## <span data-ttu-id="f91a8-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f91a8-135">OUTPUTS</span></span>

### <span data-ttu-id="f91a8-136">Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f91a8-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="f91a8-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f91a8-137">NOTES</span></span>

## <span data-ttu-id="f91a8-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f91a8-138">RELATED LINKS</span></span>
