---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 4dd93dec5aad6fe0e77e92e44884c687d5841e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922818"
---
# <span data-ttu-id="abdf7-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="abdf7-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="abdf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abdf7-102">SYNOPSIS</span></span>
<span data-ttu-id="abdf7-103">Új Azure tűzfal házirend nat szabálygyűjteményének létrehozása</span><span class="sxs-lookup"><span data-stu-id="abdf7-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="abdf7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="abdf7-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abdf7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="abdf7-105">DESCRIPTION</span></span>
<span data-ttu-id="abdf7-106">A **New-AzFirewallPolicyNatRuleCollection** parancsmag létrehoz egy Nat-szabálygyűjteményt egy Azure tűzfalházi házirendhez.</span><span class="sxs-lookup"><span data-stu-id="abdf7-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="abdf7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="abdf7-107">EXAMPLES</span></span>

### <span data-ttu-id="abdf7-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="abdf7-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="abdf7-109">Ebben a példában hálózati s szabálygyűjteményt hoz létre</span><span class="sxs-lookup"><span data-stu-id="abdf7-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="abdf7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abdf7-110">PARAMETERS</span></span>

### <span data-ttu-id="abdf7-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="abdf7-111">-ActionType</span></span>
<span data-ttu-id="abdf7-112">A szabály-művelet típusa</span><span class="sxs-lookup"><span data-stu-id="abdf7-112">The type of the rule action</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Dnat

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abdf7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abdf7-113">-DefaultProfile</span></span>
<span data-ttu-id="abdf7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abdf7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abdf7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="abdf7-115">-Name</span></span>
<span data-ttu-id="abdf7-116">A hálózati szabálygyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="abdf7-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="abdf7-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="abdf7-117">-Priority</span></span>
<span data-ttu-id="abdf7-118">A szabálygyűjtemény prioritása</span><span class="sxs-lookup"><span data-stu-id="abdf7-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abdf7-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="abdf7-119">-Rule</span></span>
<span data-ttu-id="abdf7-120">A hálózati szabályok listája</span><span class="sxs-lookup"><span data-stu-id="abdf7-120">The list of network rules</span></span>

```yaml
Type: PSAzureFirewallPolicyNetworkRule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abdf7-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="abdf7-121">-TranslatedAddress</span></span>
<span data-ttu-id="abdf7-122">A NAT-szabály lefordított címe</span><span class="sxs-lookup"><span data-stu-id="abdf7-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="abdf7-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="abdf7-123">-TranslatedPort</span></span>
<span data-ttu-id="abdf7-124">A NAT-szabály lefordított portja</span><span class="sxs-lookup"><span data-stu-id="abdf7-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="abdf7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abdf7-125">-Confirm</span></span>
<span data-ttu-id="abdf7-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="abdf7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abdf7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abdf7-127">-WhatIf</span></span>
<span data-ttu-id="abdf7-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="abdf7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abdf7-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abdf7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abdf7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abdf7-130">CommonParameters</span></span>
<span data-ttu-id="abdf7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abdf7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abdf7-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abdf7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abdf7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="abdf7-133">INPUTS</span></span>

### <span data-ttu-id="abdf7-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="abdf7-134">None</span></span>

## <span data-ttu-id="abdf7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abdf7-135">OUTPUTS</span></span>

### <span data-ttu-id="abdf7-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="abdf7-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="abdf7-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="abdf7-137">NOTES</span></span>

## <span data-ttu-id="abdf7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abdf7-138">RELATED LINKS</span></span>
