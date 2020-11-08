---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f769613516dbd1f94400832bd8fac0045fec198
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94023990"
---
# <span data-ttu-id="24312-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="24312-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="24312-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24312-102">SYNOPSIS</span></span>
<span data-ttu-id="24312-103">A megadott névtér NetworkruleSet frissítése az aktuális Azure-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="24312-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="24312-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24312-104">SYNTAX</span></span>

### <span data-ttu-id="24312-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24312-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24312-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="24312-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24312-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24312-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24312-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="24312-108">DESCRIPTION</span></span>
<span data-ttu-id="24312-109">A megadott névtér NetworkruleSet frissítése az aktuális Azure-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="24312-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="24312-110">Példák</span><span class="sxs-lookup"><span data-stu-id="24312-110">EXAMPLES</span></span>

### <span data-ttu-id="24312-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24312-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="24312-112">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="24312-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="24312-113">A NetworkRuleSet frissítése a-IPRule és a-VirtualNetworkRule paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="24312-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="24312-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="24312-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="24312-115">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="24312-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="24312-116">A NetworkRuleSet frissítése a-InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="24312-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="24312-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="24312-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="24312-118">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="24312-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="24312-119">Frissítse a NetworkRuleSet a másik névtér ResourceId.</span><span class="sxs-lookup"><span data-stu-id="24312-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="24312-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24312-120">PARAMETERS</span></span>

### <span data-ttu-id="24312-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="24312-121">-DefaultAction</span></span>
<span data-ttu-id="24312-122">A NetworkRuleSet alapértelmezett tevékenysége</span><span class="sxs-lookup"><span data-stu-id="24312-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="24312-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24312-123">-DefaultProfile</span></span>
<span data-ttu-id="24312-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24312-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24312-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24312-125">-InputObject</span></span>
<span data-ttu-id="24312-126">NetworkruleSet konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="24312-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="24312-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="24312-127">-IPRule</span></span>
<span data-ttu-id="24312-128">IPRuleSet listája</span><span class="sxs-lookup"><span data-stu-id="24312-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="24312-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24312-129">-Name</span></span>
<span data-ttu-id="24312-130">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="24312-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="24312-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24312-131">-ResourceGroupName</span></span>
<span data-ttu-id="24312-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="24312-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="24312-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24312-133">-ResourceId</span></span>
<span data-ttu-id="24312-134">A névtér erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="24312-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="24312-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="24312-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="24312-136">Azt jelzi, hogy engedélyezve van-e a TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="24312-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24312-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="24312-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="24312-138">VirtualNetworkRules listája</span><span class="sxs-lookup"><span data-stu-id="24312-138">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="24312-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24312-139">-Confirm</span></span>
<span data-ttu-id="24312-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24312-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24312-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24312-141">-WhatIf</span></span>
<span data-ttu-id="24312-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24312-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24312-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24312-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24312-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24312-144">CommonParameters</span></span>
<span data-ttu-id="24312-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24312-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="24312-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24312-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24312-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24312-147">INPUTS</span></span>

### <span data-ttu-id="24312-148">Microsoft. Azure. Command. EventHub. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="24312-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="24312-149">System. String</span><span class="sxs-lookup"><span data-stu-id="24312-149">System.String</span></span>

## <span data-ttu-id="24312-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24312-150">OUTPUTS</span></span>

### <span data-ttu-id="24312-151">Microsoft. Azure. Command. EventHub. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="24312-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="24312-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24312-152">NOTES</span></span>

## <span data-ttu-id="24312-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24312-153">RELATED LINKS</span></span>