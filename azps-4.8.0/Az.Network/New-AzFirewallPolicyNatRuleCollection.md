---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181578"
---
# <span data-ttu-id="2011e-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2011e-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="2011e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2011e-102">SYNOPSIS</span></span>
<span data-ttu-id="2011e-103">Új Azure Firewall Policy NAT-szabálygyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="2011e-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="2011e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2011e-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2011e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2011e-105">DESCRIPTION</span></span>
<span data-ttu-id="2011e-106">A **New-AzFirewallPolicyNatRuleCollection** parancsmag létrehoz egy NAT-szabályt az Azure tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="2011e-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="2011e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2011e-107">EXAMPLES</span></span>

### <span data-ttu-id="2011e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2011e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="2011e-109">Ez a példa NAT-szabályt hoz létre egy hálózati szabállyal</span><span class="sxs-lookup"><span data-stu-id="2011e-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="2011e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2011e-110">PARAMETERS</span></span>

### <span data-ttu-id="2011e-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="2011e-111">-ActionType</span></span>
<span data-ttu-id="2011e-112">A szabály típusú műveletek típusa</span><span class="sxs-lookup"><span data-stu-id="2011e-112">The type of the rule action</span></span>

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

### <span data-ttu-id="2011e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2011e-113">-DefaultProfile</span></span>
<span data-ttu-id="2011e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2011e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2011e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2011e-115">-Name</span></span>
<span data-ttu-id="2011e-116">A hálózati szabály gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="2011e-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="2011e-117">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="2011e-117">-Priority</span></span>
<span data-ttu-id="2011e-118">A szabály-gyűjtemény prioritása</span><span class="sxs-lookup"><span data-stu-id="2011e-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="2011e-119">-Szabály</span><span class="sxs-lookup"><span data-stu-id="2011e-119">-Rule</span></span>
<span data-ttu-id="2011e-120">A hálózati szabályok listája</span><span class="sxs-lookup"><span data-stu-id="2011e-120">The list of network rules</span></span>

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

### <span data-ttu-id="2011e-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="2011e-121">-TranslatedAddress</span></span>
<span data-ttu-id="2011e-122">A NAT-szabály lefordított címe</span><span class="sxs-lookup"><span data-stu-id="2011e-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="2011e-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="2011e-123">-TranslatedPort</span></span>
<span data-ttu-id="2011e-124">A NAT-szabály lefordított portja</span><span class="sxs-lookup"><span data-stu-id="2011e-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="2011e-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2011e-125">-Confirm</span></span>
<span data-ttu-id="2011e-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2011e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2011e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2011e-127">-WhatIf</span></span>
<span data-ttu-id="2011e-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2011e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2011e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2011e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2011e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2011e-130">CommonParameters</span></span>
<span data-ttu-id="2011e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2011e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2011e-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2011e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2011e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2011e-133">INPUTS</span></span>

### <span data-ttu-id="2011e-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="2011e-134">None</span></span>

## <span data-ttu-id="2011e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2011e-135">OUTPUTS</span></span>

### <span data-ttu-id="2011e-136">Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2011e-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="2011e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2011e-137">NOTES</span></span>

## <span data-ttu-id="2011e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2011e-138">RELATED LINKS</span></span>
