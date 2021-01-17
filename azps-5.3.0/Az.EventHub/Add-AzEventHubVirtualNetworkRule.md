---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 627519cd4325e7fb9677c358146f2f8a9081151a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376710"
---
# <span data-ttu-id="24c86-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="24c86-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="24c86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24c86-102">SYNOPSIS</span></span>
<span data-ttu-id="24c86-103">Egyetlen VirtualNetworkRule hozzáadása a NetworkRuleSethez a megadott Névtérhez</span><span class="sxs-lookup"><span data-stu-id="24c86-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="24c86-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="24c86-104">SYNTAX</span></span>

### <span data-ttu-id="24c86-105">VirtualNetworkRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24c86-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24c86-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24c86-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24c86-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="24c86-107">DESCRIPTION</span></span>
<span data-ttu-id="24c86-108">Egyetlen VirtualNetworkRule hozzáadása a NetworkRuleSethez a megadott Névtérhez</span><span class="sxs-lookup"><span data-stu-id="24c86-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="24c86-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="24c86-109">EXAMPLES</span></span>

### <span data-ttu-id="24c86-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="24c86-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="24c86-111">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="24c86-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="24c86-112">A megadott Alhálózat és IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) hozzáadása a NetworkRuleSethez a megadott Névtérhez</span><span class="sxs-lookup"><span data-stu-id="24c86-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="24c86-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="24c86-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="24c86-114">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="24c86-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="24c86-115">A $virtualruleset 1 hozzáadása a NetworkRuleSethez a megadott Névtérhez</span><span class="sxs-lookup"><span data-stu-id="24c86-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="24c86-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24c86-116">PARAMETERS</span></span>

### <span data-ttu-id="24c86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c86-117">-DefaultProfile</span></span>
<span data-ttu-id="24c86-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24c86-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24c86-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="24c86-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="24c86-120">ARM alhálózat azonosítója</span><span class="sxs-lookup"><span data-stu-id="24c86-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="24c86-121">-Name</span><span class="sxs-lookup"><span data-stu-id="24c86-121">-Name</span></span>
<span data-ttu-id="24c86-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="24c86-122">Namespace Name</span></span>

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

### <span data-ttu-id="24c86-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c86-123">-ResourceGroupName</span></span>
<span data-ttu-id="24c86-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="24c86-124">Resource Group Name</span></span>

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

### <span data-ttu-id="24c86-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="24c86-125">-SubnetId</span></span>
<span data-ttu-id="24c86-126">Alhálózati erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="24c86-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="24c86-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="24c86-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="24c86-128">VirtualNetworkRule konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="24c86-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="24c86-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24c86-129">-Confirm</span></span>
<span data-ttu-id="24c86-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="24c86-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c86-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c86-131">-WhatIf</span></span>
<span data-ttu-id="24c86-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="24c86-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24c86-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24c86-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c86-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c86-134">CommonParameters</span></span>
<span data-ttu-id="24c86-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c86-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="24c86-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c86-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c86-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24c86-137">INPUTS</span></span>

### <span data-ttu-id="24c86-138">System.String</span><span class="sxs-lookup"><span data-stu-id="24c86-138">System.String</span></span>

### <span data-ttu-id="24c86-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="24c86-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="24c86-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="24c86-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="24c86-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24c86-141">OUTPUTS</span></span>

### <span data-ttu-id="24c86-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="24c86-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="24c86-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="24c86-143">NOTES</span></span>

## <span data-ttu-id="24c86-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24c86-144">RELATED LINKS</span></span>
