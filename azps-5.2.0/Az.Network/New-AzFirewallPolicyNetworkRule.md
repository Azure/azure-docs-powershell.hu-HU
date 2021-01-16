---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327091"
---
# <span data-ttu-id="314eb-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="314eb-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="314eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="314eb-102">SYNOPSIS</span></span>
<span data-ttu-id="314eb-103">Új Azure firewall policy network rule</span><span class="sxs-lookup"><span data-stu-id="314eb-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="314eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="314eb-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="314eb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="314eb-105">DESCRIPTION</span></span>
<span data-ttu-id="314eb-106">A **New-AzFirewallPolicyNetworkRule** parancsmag létrehoz egy hálózati szabályt az Azure tűzfal házirendjére.</span><span class="sxs-lookup"><span data-stu-id="314eb-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="314eb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="314eb-107">EXAMPLES</span></span>

### <span data-ttu-id="314eb-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="314eb-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="314eb-109">Ebben a példában egy hálózati szabályt hoz létre a forráscím, a protokoll, a célcím és a célportport alapján.</span><span class="sxs-lookup"><span data-stu-id="314eb-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="314eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="314eb-110">PARAMETERS</span></span>

### <span data-ttu-id="314eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314eb-111">-DefaultProfile</span></span>
<span data-ttu-id="314eb-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="314eb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="314eb-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="314eb-113">-Description</span></span>
<span data-ttu-id="314eb-114">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="314eb-114">The description of the rule</span></span>

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

### <span data-ttu-id="314eb-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="314eb-115">-DestinationAddress</span></span>
<span data-ttu-id="314eb-116">A szabály célcíme</span><span class="sxs-lookup"><span data-stu-id="314eb-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="314eb-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="314eb-117">-DestinationFqdn</span></span>
<span data-ttu-id="314eb-118">A szabály cél teljes tartományának tartománya</span><span class="sxs-lookup"><span data-stu-id="314eb-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="314eb-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="314eb-119">-DestinationIpGroup</span></span>
<span data-ttu-id="314eb-120">A szabály cél ip-csoportjai</span><span class="sxs-lookup"><span data-stu-id="314eb-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="314eb-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="314eb-121">-DestinationPort</span></span>
<span data-ttu-id="314eb-122">A szabály célportjai</span><span class="sxs-lookup"><span data-stu-id="314eb-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="314eb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="314eb-123">-Name</span></span>
<span data-ttu-id="314eb-124">A hálózati szabály neve</span><span class="sxs-lookup"><span data-stu-id="314eb-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="314eb-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="314eb-125">-Protocol</span></span>
<span data-ttu-id="314eb-126">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="314eb-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="314eb-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="314eb-127">-SourceAddress</span></span>
<span data-ttu-id="314eb-128">A szabály forráscíme</span><span class="sxs-lookup"><span data-stu-id="314eb-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="314eb-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="314eb-129">-SourceIpGroup</span></span>
<span data-ttu-id="314eb-130">A szabály forrás IP-csoportjai</span><span class="sxs-lookup"><span data-stu-id="314eb-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="314eb-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="314eb-131">-Confirm</span></span>
<span data-ttu-id="314eb-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="314eb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="314eb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="314eb-133">-WhatIf</span></span>
<span data-ttu-id="314eb-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="314eb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="314eb-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="314eb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="314eb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314eb-136">CommonParameters</span></span>
<span data-ttu-id="314eb-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="314eb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314eb-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="314eb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314eb-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="314eb-139">INPUTS</span></span>

### <span data-ttu-id="314eb-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="314eb-140">None</span></span>

## <span data-ttu-id="314eb-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="314eb-141">OUTPUTS</span></span>

### <span data-ttu-id="314eb-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="314eb-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="314eb-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="314eb-143">NOTES</span></span>

## <span data-ttu-id="314eb-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="314eb-144">RELATED LINKS</span></span>
