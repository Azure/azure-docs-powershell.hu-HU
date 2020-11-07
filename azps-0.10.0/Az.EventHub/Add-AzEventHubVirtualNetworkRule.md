---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 37f13534095341895a4fc3b4c1c9feb9e5e911be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842369"
---
# <span data-ttu-id="891a1-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="891a1-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="891a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="891a1-102">SYNOPSIS</span></span>
<span data-ttu-id="891a1-103">Egyetlen VirtualNetworkRule hozzáadása a NetworkRuleSet a megadott névtérhez</span><span class="sxs-lookup"><span data-stu-id="891a1-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="891a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="891a1-104">SYNTAX</span></span>

### <span data-ttu-id="891a1-105">VirtualNetworkRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="891a1-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="891a1-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="891a1-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="891a1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="891a1-107">DESCRIPTION</span></span>
<span data-ttu-id="891a1-108">Egyetlen VirtualNetworkRule hozzáadása a NetworkRuleSet a megadott névtérhez</span><span class="sxs-lookup"><span data-stu-id="891a1-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="891a1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="891a1-109">EXAMPLES</span></span>

### <span data-ttu-id="891a1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="891a1-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="891a1-111">Név: alapértelmezett DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default-típus: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="891a1-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="891a1-112">Az adott névtérhez hozzáadja a megadott alhálózat-és IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) a NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="891a1-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="891a1-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="891a1-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="891a1-114">Név: alapértelmezett DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default-típus: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="891a1-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="891a1-115">A megadott névtérhez hozzáadja a NetworkRuleSet $virtualruleset 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="891a1-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="891a1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="891a1-116">PARAMETERS</span></span>

### <span data-ttu-id="891a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="891a1-117">-DefaultProfile</span></span>
<span data-ttu-id="891a1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="891a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891a1-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="891a1-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="891a1-120">Az alhálózat karja azonosítója</span><span class="sxs-lookup"><span data-stu-id="891a1-120">ARM ID of Subnet</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891a1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="891a1-121">-Name</span></span>
<span data-ttu-id="891a1-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="891a1-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="891a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="891a1-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="891a1-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a1-125">– NetI</span><span class="sxs-lookup"><span data-stu-id="891a1-125">-SubnetId</span></span>
<span data-ttu-id="891a1-126">Alhálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="891a1-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="891a1-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="891a1-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="891a1-128">VirtualNetworkRule konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="891a1-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="891a1-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="891a1-129">-Confirm</span></span>
<span data-ttu-id="891a1-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="891a1-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891a1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="891a1-131">-WhatIf</span></span>
<span data-ttu-id="891a1-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="891a1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="891a1-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="891a1-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891a1-134">CommonParameters</span></span>
<span data-ttu-id="891a1-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="891a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="891a1-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="891a1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891a1-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="891a1-137">INPUTS</span></span>

### <span data-ttu-id="891a1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="891a1-138">System.String</span></span>

### <span data-ttu-id="891a1-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="891a1-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="891a1-140">Microsoft. Azure. Command. EventHub. models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="891a1-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="891a1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="891a1-141">OUTPUTS</span></span>

### <span data-ttu-id="891a1-142">Microsoft. Azure. Command. EventHub. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="891a1-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="891a1-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="891a1-143">NOTES</span></span>

## <span data-ttu-id="891a1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="891a1-144">RELATED LINKS</span></span>
