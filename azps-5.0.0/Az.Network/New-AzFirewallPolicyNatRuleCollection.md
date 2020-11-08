---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187275"
---
# <span data-ttu-id="45ad2-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="45ad2-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="45ad2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="45ad2-103">Új Azure Firewall Policy NAT-szabálygyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="45ad2-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="45ad2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45ad2-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45ad2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="45ad2-106">A **New-AzFirewallPolicyNatRuleCollection** parancsmag létrehoz egy NAT-szabályt az Azure tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="45ad2-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="45ad2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45ad2-107">EXAMPLES</span></span>

### <span data-ttu-id="45ad2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45ad2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="45ad2-109">Ez a példa NAT-szabályt hoz létre egy hálózati szabállyal</span><span class="sxs-lookup"><span data-stu-id="45ad2-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="45ad2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45ad2-110">PARAMETERS</span></span>

### <span data-ttu-id="45ad2-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="45ad2-111">-ActionType</span></span>
<span data-ttu-id="45ad2-112">A szabály típusú műveletek típusa</span><span class="sxs-lookup"><span data-stu-id="45ad2-112">The type of the rule action</span></span>

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

### <span data-ttu-id="45ad2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ad2-113">-DefaultProfile</span></span>
<span data-ttu-id="45ad2-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45ad2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45ad2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45ad2-115">-Name</span></span>
<span data-ttu-id="45ad2-116">A hálózati szabály gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="45ad2-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="45ad2-117">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="45ad2-117">-Priority</span></span>
<span data-ttu-id="45ad2-118">A szabály-gyűjtemény prioritása</span><span class="sxs-lookup"><span data-stu-id="45ad2-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="45ad2-119">-Szabály</span><span class="sxs-lookup"><span data-stu-id="45ad2-119">-Rule</span></span>
<span data-ttu-id="45ad2-120">A hálózati szabályok listája</span><span class="sxs-lookup"><span data-stu-id="45ad2-120">The list of network rules</span></span>

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

### <span data-ttu-id="45ad2-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="45ad2-121">-TranslatedAddress</span></span>
<span data-ttu-id="45ad2-122">A NAT-szabály lefordított címe</span><span class="sxs-lookup"><span data-stu-id="45ad2-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="45ad2-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="45ad2-123">-TranslatedPort</span></span>
<span data-ttu-id="45ad2-124">A NAT-szabály lefordított portja</span><span class="sxs-lookup"><span data-stu-id="45ad2-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="45ad2-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45ad2-125">-Confirm</span></span>
<span data-ttu-id="45ad2-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45ad2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ad2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ad2-127">-WhatIf</span></span>
<span data-ttu-id="45ad2-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45ad2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45ad2-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45ad2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ad2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ad2-130">CommonParameters</span></span>
<span data-ttu-id="45ad2-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45ad2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ad2-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="45ad2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ad2-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45ad2-133">INPUTS</span></span>

### <span data-ttu-id="45ad2-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="45ad2-134">None</span></span>

## <span data-ttu-id="45ad2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45ad2-135">OUTPUTS</span></span>

### <span data-ttu-id="45ad2-136">Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="45ad2-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="45ad2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45ad2-137">NOTES</span></span>

## <span data-ttu-id="45ad2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45ad2-138">RELATED LINKS</span></span>
