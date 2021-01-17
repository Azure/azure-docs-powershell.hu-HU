---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: 3ff1f64bf65a4474dc9f47aa6bd419c442b49698
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479685"
---
# <span data-ttu-id="03117-101">Add-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="03117-101">Add-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="03117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03117-102">SYNOPSIS</span></span>
<span data-ttu-id="03117-103">Egyetlen VirtualNetworkRule hozzáadása a NetworkRuleSethez a megadott Névtérhez</span><span class="sxs-lookup"><span data-stu-id="03117-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="03117-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03117-104">SYNTAX</span></span>

### <span data-ttu-id="03117-105">VirtualNetworkRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03117-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03117-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03117-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03117-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03117-107">DESCRIPTION</span></span>
<span data-ttu-id="03117-108">Egyetlen VirtualNetworkRule hozzáadása a NetworkRuleSethez a megadott Névtérhez</span><span class="sxs-lookup"><span data-stu-id="03117-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="03117-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03117-109">EXAMPLES</span></span>

### <span data-ttu-id="03117-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="03117-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```
<span data-ttu-id="03117-111">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="03117-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="03117-112">A megadott Alhálózat és IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) hozzáadása a NetworkRuleSethez a megadott Névtérhez</span><span class="sxs-lookup"><span data-stu-id="03117-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="03117-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="03117-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```
<span data-ttu-id="03117-114">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="03117-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="03117-115">A $virtualruleset 1 hozzáadása a NetworkRuleSethez a megadott Névtérhez</span><span class="sxs-lookup"><span data-stu-id="03117-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="03117-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03117-116">PARAMETERS</span></span>

### <span data-ttu-id="03117-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03117-117">-DefaultProfile</span></span>
<span data-ttu-id="03117-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03117-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03117-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="03117-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="03117-120">ARM alhálózat azonosítója</span><span class="sxs-lookup"><span data-stu-id="03117-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="03117-121">-Name</span><span class="sxs-lookup"><span data-stu-id="03117-121">-Name</span></span>
<span data-ttu-id="03117-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="03117-122">Namespace Name</span></span>

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

### <span data-ttu-id="03117-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03117-123">-ResourceGroupName</span></span>
<span data-ttu-id="03117-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="03117-124">Resource Group Name</span></span>

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

### <span data-ttu-id="03117-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="03117-125">-SubnetId</span></span>
<span data-ttu-id="03117-126">Alhálózati erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="03117-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="03117-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="03117-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="03117-128">VirtualNetworkRule konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="03117-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03117-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03117-129">-Confirm</span></span>
<span data-ttu-id="03117-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03117-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03117-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03117-131">-WhatIf</span></span>
<span data-ttu-id="03117-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03117-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03117-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03117-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03117-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03117-134">CommonParameters</span></span>
<span data-ttu-id="03117-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03117-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="03117-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03117-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03117-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03117-137">INPUTS</span></span>

### <span data-ttu-id="03117-138">System.String</span><span class="sxs-lookup"><span data-stu-id="03117-138">System.String</span></span>

### <span data-ttu-id="03117-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="03117-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="03117-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="03117-140">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="03117-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03117-141">OUTPUTS</span></span>

### <span data-ttu-id="03117-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="03117-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="03117-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03117-143">NOTES</span></span>

## <span data-ttu-id="03117-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03117-144">RELATED LINKS</span></span>