---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9d66a6824cf2c84ed0414681a4d89bf3de8f31dd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844002"
---
# <span data-ttu-id="ed0cf-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed0cf-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="ed0cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0cf-103">A megadott névtér NetworkruleSet frissítése az aktuális Azure-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="ed0cf-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ed0cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed0cf-104">SYNTAX</span></span>

### <span data-ttu-id="ed0cf-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed0cf-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed0cf-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed0cf-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed0cf-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed0cf-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed0cf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed0cf-108">DESCRIPTION</span></span>
<span data-ttu-id="ed0cf-109">A megadott névtér NetworkruleSet frissítése az aktuális Azure-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="ed0cf-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ed0cf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ed0cf-110">EXAMPLES</span></span>

### <span data-ttu-id="ed0cf-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ed0cf-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="ed0cf-112">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="ed0cf-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="ed0cf-113">A NetworkRuleSet frissítése a-IPRule és a-VirtualNetworkRule paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="ed0cf-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="ed0cf-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="ed0cf-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="ed0cf-115">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="ed0cf-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="ed0cf-116">A NetworkRuleSet frissítése a-InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="ed0cf-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="ed0cf-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="ed0cf-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="ed0cf-118">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="ed0cf-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="ed0cf-119">Frissítse a NetworkRuleSet a másik névtér ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ed0cf-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="ed0cf-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed0cf-120">PARAMETERS</span></span>

### <span data-ttu-id="ed0cf-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="ed0cf-121">-DefaultAction</span></span>
<span data-ttu-id="ed0cf-122">A NetworkRuleSet alapértelmezett tevékenysége</span><span class="sxs-lookup"><span data-stu-id="ed0cf-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0cf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0cf-123">-DefaultProfile</span></span>
<span data-ttu-id="ed0cf-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed0cf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed0cf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed0cf-125">-InputObject</span></span>
<span data-ttu-id="ed0cf-126">NetworkruleSet konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="ed0cf-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0cf-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="ed0cf-127">-IPRule</span></span>
<span data-ttu-id="ed0cf-128">IPRuleSet listája</span><span class="sxs-lookup"><span data-stu-id="ed0cf-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0cf-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed0cf-129">-Name</span></span>
<span data-ttu-id="ed0cf-130">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="ed0cf-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0cf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed0cf-131">-ResourceGroupName</span></span>
<span data-ttu-id="ed0cf-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ed0cf-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0cf-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed0cf-133">-ResourceId</span></span>
<span data-ttu-id="ed0cf-134">A névtér erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ed0cf-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0cf-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed0cf-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="ed0cf-136">VirtualNetworkRules listája</span><span class="sxs-lookup"><span data-stu-id="ed0cf-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0cf-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed0cf-137">-Confirm</span></span>
<span data-ttu-id="ed0cf-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed0cf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed0cf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed0cf-139">-WhatIf</span></span>
<span data-ttu-id="ed0cf-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed0cf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed0cf-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed0cf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed0cf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0cf-142">CommonParameters</span></span>
<span data-ttu-id="ed0cf-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed0cf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ed0cf-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed0cf-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0cf-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed0cf-145">INPUTS</span></span>

### <span data-ttu-id="ed0cf-146">Microsoft. Azure. Command. EventHub. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ed0cf-146">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="ed0cf-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ed0cf-147">System.String</span></span>

## <span data-ttu-id="ed0cf-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed0cf-148">OUTPUTS</span></span>

### <span data-ttu-id="ed0cf-149">Microsoft. Azure. Command. EventHub. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ed0cf-149">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ed0cf-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed0cf-150">NOTES</span></span>

## <span data-ttu-id="ed0cf-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed0cf-151">RELATED LINKS</span></span>