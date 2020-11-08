---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 627519cd4325e7fb9677c358146f2f8a9081151a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187451"
---
# <span data-ttu-id="734f2-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="734f2-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="734f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="734f2-102">SYNOPSIS</span></span>
<span data-ttu-id="734f2-103">Egyetlen VirtualNetworkRule hozzáadása a NetworkRuleSet a megadott névtérhez</span><span class="sxs-lookup"><span data-stu-id="734f2-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="734f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="734f2-104">SYNTAX</span></span>

### <span data-ttu-id="734f2-105">VirtualNetworkRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="734f2-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="734f2-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="734f2-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="734f2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="734f2-107">DESCRIPTION</span></span>
<span data-ttu-id="734f2-108">Egyetlen VirtualNetworkRule hozzáadása a NetworkRuleSet a megadott névtérhez</span><span class="sxs-lookup"><span data-stu-id="734f2-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="734f2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="734f2-109">EXAMPLES</span></span>

### <span data-ttu-id="734f2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="734f2-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="734f2-111">Név: alapértelmezett DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default-típus: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="734f2-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="734f2-112">Az adott névtérhez hozzáadja a megadott alhálózat-és IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) a NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="734f2-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="734f2-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="734f2-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="734f2-114">Név: alapértelmezett DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default-típus: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="734f2-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="734f2-115">A megadott névtérhez hozzáadja a NetworkRuleSet $virtualruleset 1 értéket.</span><span class="sxs-lookup"><span data-stu-id="734f2-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="734f2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="734f2-116">PARAMETERS</span></span>

### <span data-ttu-id="734f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734f2-117">-DefaultProfile</span></span>
<span data-ttu-id="734f2-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="734f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="734f2-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="734f2-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="734f2-120">Az alhálózat karja azonosítója</span><span class="sxs-lookup"><span data-stu-id="734f2-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="734f2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="734f2-121">-Name</span></span>
<span data-ttu-id="734f2-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="734f2-122">Namespace Name</span></span>

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

### <span data-ttu-id="734f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="734f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="734f2-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="734f2-124">Resource Group Name</span></span>

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

### <span data-ttu-id="734f2-125">– NetI</span><span class="sxs-lookup"><span data-stu-id="734f2-125">-SubnetId</span></span>
<span data-ttu-id="734f2-126">Alhálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="734f2-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="734f2-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="734f2-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="734f2-128">VirtualNetworkRule konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="734f2-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="734f2-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="734f2-129">-Confirm</span></span>
<span data-ttu-id="734f2-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="734f2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="734f2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="734f2-131">-WhatIf</span></span>
<span data-ttu-id="734f2-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="734f2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="734f2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="734f2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="734f2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734f2-134">CommonParameters</span></span>
<span data-ttu-id="734f2-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="734f2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="734f2-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="734f2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734f2-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="734f2-137">INPUTS</span></span>

### <span data-ttu-id="734f2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="734f2-138">System.String</span></span>

### <span data-ttu-id="734f2-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="734f2-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="734f2-140">Microsoft. Azure. Command. EventHub. models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="734f2-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="734f2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="734f2-141">OUTPUTS</span></span>

### <span data-ttu-id="734f2-142">Microsoft. Azure. Command. EventHub. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="734f2-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="734f2-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="734f2-143">NOTES</span></span>

## <span data-ttu-id="734f2-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="734f2-144">RELATED LINKS</span></span>
