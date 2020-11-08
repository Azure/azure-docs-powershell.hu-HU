---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180523"
---
# <span data-ttu-id="ce4be-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce4be-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="ce4be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce4be-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4be-103">Új Azure tűzfal-házirend-hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="ce4be-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="ce4be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce4be-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce4be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce4be-105">DESCRIPTION</span></span>
<span data-ttu-id="ce4be-106">A **New-AzFirewallPolicyNetworkRule** parancsmag hálózati szabályt hoz létre az Azure tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="ce4be-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="ce4be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ce4be-107">EXAMPLES</span></span>

### <span data-ttu-id="ce4be-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ce4be-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="ce4be-109">Ebben a példában egy hálózati szabályt hoz létre a forráscím, a protokoll, a cél címe és a cél porttal.</span><span class="sxs-lookup"><span data-stu-id="ce4be-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="ce4be-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce4be-110">PARAMETERS</span></span>

### <span data-ttu-id="ce4be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4be-111">-DefaultProfile</span></span>
<span data-ttu-id="ce4be-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce4be-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce4be-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ce4be-113">-Description</span></span>
<span data-ttu-id="ce4be-114">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="ce4be-114">The description of the rule</span></span>

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

### <span data-ttu-id="ce4be-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ce4be-115">-DestinationAddress</span></span>
<span data-ttu-id="ce4be-116">A szabály rendeltetési címe</span><span class="sxs-lookup"><span data-stu-id="ce4be-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="ce4be-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="ce4be-117">-DestinationFqdn</span></span>
<span data-ttu-id="ce4be-118">A szabály cél FQDN-je</span><span class="sxs-lookup"><span data-stu-id="ce4be-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="ce4be-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="ce4be-119">-DestinationIpGroup</span></span>
<span data-ttu-id="ce4be-120">A szabály rendeltetési ipgroups</span><span class="sxs-lookup"><span data-stu-id="ce4be-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="ce4be-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ce4be-121">-DestinationPort</span></span>
<span data-ttu-id="ce4be-122">A szabály rendeltetési portjai</span><span class="sxs-lookup"><span data-stu-id="ce4be-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="ce4be-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce4be-123">-Name</span></span>
<span data-ttu-id="ce4be-124">A hálózati szabály neve</span><span class="sxs-lookup"><span data-stu-id="ce4be-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="ce4be-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ce4be-125">-Protocol</span></span>
<span data-ttu-id="ce4be-126">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="ce4be-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="ce4be-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="ce4be-127">-SourceAddress</span></span>
<span data-ttu-id="ce4be-128">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="ce4be-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="ce4be-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="ce4be-129">-SourceIpGroup</span></span>
<span data-ttu-id="ce4be-130">A szabály forrás ipgroups</span><span class="sxs-lookup"><span data-stu-id="ce4be-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="ce4be-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce4be-131">-Confirm</span></span>
<span data-ttu-id="ce4be-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce4be-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce4be-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce4be-133">-WhatIf</span></span>
<span data-ttu-id="ce4be-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce4be-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce4be-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce4be-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce4be-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4be-136">CommonParameters</span></span>
<span data-ttu-id="ce4be-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce4be-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4be-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ce4be-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4be-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce4be-139">INPUTS</span></span>

### <span data-ttu-id="ce4be-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="ce4be-140">None</span></span>

## <span data-ttu-id="ce4be-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce4be-141">OUTPUTS</span></span>

### <span data-ttu-id="ce4be-142">Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce4be-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="ce4be-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce4be-143">NOTES</span></span>

## <span data-ttu-id="ce4be-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce4be-144">RELATED LINKS</span></span>
