---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 9465ad8d6f66b62da8b224ab635ca45fed1a8ca1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838790"
---
# <span data-ttu-id="24a66-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="24a66-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="24a66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24a66-102">SYNOPSIS</span></span>
<span data-ttu-id="24a66-103">A megadott névtér NetworkruleSet frissítése az aktuális Azure-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="24a66-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="24a66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24a66-104">SYNTAX</span></span>

### <span data-ttu-id="24a66-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24a66-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24a66-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="24a66-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24a66-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24a66-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24a66-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="24a66-108">DESCRIPTION</span></span>
<span data-ttu-id="24a66-109">A megadott névtér NetwrokruleSet frissítése az aktuális Azure-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="24a66-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="24a66-110">Példák</span><span class="sxs-lookup"><span data-stu-id="24a66-110">EXAMPLES</span></span>

### <span data-ttu-id="24a66-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24a66-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="24a66-112">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default típus: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="24a66-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="24a66-113">A NetworkRuleSet frissítése a-IPRule és a-VirtualNetworkRule paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="24a66-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="24a66-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="24a66-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="24a66-115">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default típus: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="24a66-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="24a66-116">A NetworkRuleSet frissítése a-InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="24a66-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="24a66-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="24a66-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="24a66-118">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default típus: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, allow, 3.3.3.3, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="24a66-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="24a66-119">Frissítse a NetworkRuleSet a másik névtér ResourceId.</span><span class="sxs-lookup"><span data-stu-id="24a66-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="24a66-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24a66-120">PARAMETERS</span></span>

### <span data-ttu-id="24a66-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="24a66-121">-DefaultAction</span></span>
<span data-ttu-id="24a66-122">A NetworkRuleSet alapértelmezett tevékenysége</span><span class="sxs-lookup"><span data-stu-id="24a66-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="24a66-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a66-123">-DefaultProfile</span></span>
<span data-ttu-id="24a66-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24a66-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24a66-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24a66-125">-InputObject</span></span>
<span data-ttu-id="24a66-126">NetworkruleSet konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="24a66-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24a66-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="24a66-127">-IPRule</span></span>
<span data-ttu-id="24a66-128">IPRuleSet listája</span><span class="sxs-lookup"><span data-stu-id="24a66-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a66-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24a66-129">-Name</span></span>
<span data-ttu-id="24a66-130">EventHub-névtér neve</span><span class="sxs-lookup"><span data-stu-id="24a66-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="24a66-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a66-131">-ResourceGroupName</span></span>
<span data-ttu-id="24a66-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="24a66-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="24a66-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24a66-133">-ResourceId</span></span>
<span data-ttu-id="24a66-134">A névtér erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="24a66-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="24a66-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="24a66-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="24a66-136">VirtualNetworkRules listája</span><span class="sxs-lookup"><span data-stu-id="24a66-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a66-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24a66-137">-Confirm</span></span>
<span data-ttu-id="24a66-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24a66-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24a66-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24a66-139">-WhatIf</span></span>
<span data-ttu-id="24a66-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24a66-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24a66-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24a66-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24a66-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a66-142">CommonParameters</span></span>
<span data-ttu-id="24a66-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24a66-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="24a66-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a66-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a66-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a66-145">INPUTS</span></span>

### <span data-ttu-id="24a66-146">Microsoft. Azure. Command. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="24a66-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="24a66-147">System. String</span><span class="sxs-lookup"><span data-stu-id="24a66-147">System.String</span></span>

## <span data-ttu-id="24a66-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24a66-148">OUTPUTS</span></span>

### <span data-ttu-id="24a66-149">Microsoft. Azure. Command. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="24a66-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="24a66-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24a66-150">NOTES</span></span>

## <span data-ttu-id="24a66-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24a66-151">RELATED LINKS</span></span>