---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: b8027083225b774d1795d8c96132a0e031f8a51e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007894"
---
# <span data-ttu-id="316f1-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="316f1-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="316f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="316f1-102">SYNOPSIS</span></span>
<span data-ttu-id="316f1-103">Frissítse az aktuális Azure-előfizetés adott Névterének NetworkruleSet szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="316f1-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="316f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="316f1-104">SYNTAX</span></span>

### <span data-ttu-id="316f1-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="316f1-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="316f1-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="316f1-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="316f1-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="316f1-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="316f1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="316f1-108">DESCRIPTION</span></span>
<span data-ttu-id="316f1-109">Frissítse az aktuális Azure-előfizetés adott Névterének NetworkruleSet szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="316f1-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="316f1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="316f1-110">EXAMPLES</span></span>

### <span data-ttu-id="316f1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="316f1-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="316f1-112">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="316f1-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="316f1-113">A NetworkRuleSet frissítése az -IPRule és a -VirtualNetworkRule paraméterekkel</span><span class="sxs-lookup"><span data-stu-id="316f1-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="316f1-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="316f1-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="316f1-115">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="316f1-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="316f1-116">A NetworkRuleSet frissítése az -InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="316f1-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="316f1-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="316f1-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="316f1-118">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="316f1-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="316f1-119">Frissítse a NetworkRuleSetet a másik névtér -ResourceId-ével.</span><span class="sxs-lookup"><span data-stu-id="316f1-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="316f1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="316f1-120">PARAMETERS</span></span>

### <span data-ttu-id="316f1-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="316f1-121">-DefaultAction</span></span>
<span data-ttu-id="316f1-122">A NetworkRuleSet alapértelmezett művelete</span><span class="sxs-lookup"><span data-stu-id="316f1-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="316f1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316f1-123">-DefaultProfile</span></span>
<span data-ttu-id="316f1-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="316f1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316f1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="316f1-125">-InputObject</span></span>
<span data-ttu-id="316f1-126">NetworkruleSet Configuration Object</span><span class="sxs-lookup"><span data-stu-id="316f1-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="316f1-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="316f1-127">-IPRule</span></span>
<span data-ttu-id="316f1-128">Az IPRuleSet listája</span><span class="sxs-lookup"><span data-stu-id="316f1-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="316f1-129">-Name</span><span class="sxs-lookup"><span data-stu-id="316f1-129">-Name</span></span>
<span data-ttu-id="316f1-130">EventHub Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="316f1-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="316f1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316f1-131">-ResourceGroupName</span></span>
<span data-ttu-id="316f1-132">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="316f1-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="316f1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="316f1-133">-ResourceId</span></span>
<span data-ttu-id="316f1-134">A Namespace erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="316f1-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="316f1-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="316f1-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="316f1-136">Azt jelzi, hogy engedélyezve van-e a TrustedServiceAccessEnabled szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="316f1-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

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

### <span data-ttu-id="316f1-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="316f1-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="316f1-138">A VirtualNetworkRules listája</span><span class="sxs-lookup"><span data-stu-id="316f1-138">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="316f1-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="316f1-139">-Confirm</span></span>
<span data-ttu-id="316f1-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="316f1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="316f1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316f1-141">-WhatIf</span></span>
<span data-ttu-id="316f1-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="316f1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="316f1-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="316f1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="316f1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316f1-144">CommonParameters</span></span>
<span data-ttu-id="316f1-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316f1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="316f1-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316f1-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316f1-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="316f1-147">INPUTS</span></span>

### <span data-ttu-id="316f1-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="316f1-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="316f1-149">System.String</span><span class="sxs-lookup"><span data-stu-id="316f1-149">System.String</span></span>

## <span data-ttu-id="316f1-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="316f1-150">OUTPUTS</span></span>

### <span data-ttu-id="316f1-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="316f1-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="316f1-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="316f1-152">NOTES</span></span>

## <span data-ttu-id="316f1-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="316f1-153">RELATED LINKS</span></span>