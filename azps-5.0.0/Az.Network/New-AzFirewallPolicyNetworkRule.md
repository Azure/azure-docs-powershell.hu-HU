---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194029"
---
# <span data-ttu-id="f4ffc-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f4ffc-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="f4ffc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ffc-103">Új Azure tűzfal-házirend-hálózati szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="f4ffc-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="f4ffc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4ffc-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ffc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="f4ffc-106">A **New-AzFirewallPolicyNetworkRule** parancsmag hálózati szabályt hoz létre az Azure tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="f4ffc-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="f4ffc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f4ffc-107">EXAMPLES</span></span>

### <span data-ttu-id="f4ffc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4ffc-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="f4ffc-109">Ebben a példában egy hálózati szabályt hoz létre a forráscím, a protokoll, a cél címe és a cél porttal.</span><span class="sxs-lookup"><span data-stu-id="f4ffc-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="f4ffc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4ffc-110">PARAMETERS</span></span>

### <span data-ttu-id="f4ffc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ffc-111">-DefaultProfile</span></span>
<span data-ttu-id="f4ffc-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4ffc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4ffc-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f4ffc-113">-Description</span></span>
<span data-ttu-id="f4ffc-114">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="f4ffc-114">The description of the rule</span></span>

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

### <span data-ttu-id="f4ffc-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f4ffc-115">-DestinationAddress</span></span>
<span data-ttu-id="f4ffc-116">A szabály rendeltetési címe</span><span class="sxs-lookup"><span data-stu-id="f4ffc-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="f4ffc-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="f4ffc-117">-DestinationFqdn</span></span>
<span data-ttu-id="f4ffc-118">A szabály cél FQDN-je</span><span class="sxs-lookup"><span data-stu-id="f4ffc-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="f4ffc-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="f4ffc-119">-DestinationIpGroup</span></span>
<span data-ttu-id="f4ffc-120">A szabály rendeltetési ipgroups</span><span class="sxs-lookup"><span data-stu-id="f4ffc-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="f4ffc-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f4ffc-121">-DestinationPort</span></span>
<span data-ttu-id="f4ffc-122">A szabály rendeltetési portjai</span><span class="sxs-lookup"><span data-stu-id="f4ffc-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="f4ffc-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4ffc-123">-Name</span></span>
<span data-ttu-id="f4ffc-124">A hálózati szabály neve</span><span class="sxs-lookup"><span data-stu-id="f4ffc-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="f4ffc-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f4ffc-125">-Protocol</span></span>
<span data-ttu-id="f4ffc-126">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="f4ffc-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="f4ffc-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="f4ffc-127">-SourceAddress</span></span>
<span data-ttu-id="f4ffc-128">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="f4ffc-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="f4ffc-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="f4ffc-129">-SourceIpGroup</span></span>
<span data-ttu-id="f4ffc-130">A szabály forrás ipgroups</span><span class="sxs-lookup"><span data-stu-id="f4ffc-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="f4ffc-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4ffc-131">-Confirm</span></span>
<span data-ttu-id="f4ffc-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4ffc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ffc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ffc-133">-WhatIf</span></span>
<span data-ttu-id="f4ffc-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4ffc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4ffc-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4ffc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ffc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ffc-136">CommonParameters</span></span>
<span data-ttu-id="f4ffc-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4ffc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ffc-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4ffc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ffc-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4ffc-139">INPUTS</span></span>

### <span data-ttu-id="f4ffc-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="f4ffc-140">None</span></span>

## <span data-ttu-id="f4ffc-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4ffc-141">OUTPUTS</span></span>

### <span data-ttu-id="f4ffc-142">Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f4ffc-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="f4ffc-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4ffc-143">NOTES</span></span>

## <span data-ttu-id="f4ffc-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4ffc-144">RELATED LINKS</span></span>
