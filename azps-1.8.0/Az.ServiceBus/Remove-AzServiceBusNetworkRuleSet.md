---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: df8e85505a7aa62b883ecdc0536f9b3cd1352109
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669162"
---
# <span data-ttu-id="d45dd-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d45dd-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="d45dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d45dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d45dd-103">A megadott névtér NetwrokRuleSet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d45dd-103">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="d45dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d45dd-104">SYNTAX</span></span>

### <span data-ttu-id="d45dd-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d45dd-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d45dd-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d45dd-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d45dd-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d45dd-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d45dd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d45dd-108">DESCRIPTION</span></span>
<span data-ttu-id="d45dd-109">A megadott névtér NetwrokRuleSet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d45dd-109">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="d45dd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d45dd-110">EXAMPLES</span></span>

### <span data-ttu-id="d45dd-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d45dd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="d45dd-112">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default típus: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="d45dd-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="d45dd-113">Törli a NetwrokRuleSet az adott "ServiceBus-Namespace1-1375" namesapce</span><span class="sxs-lookup"><span data-stu-id="d45dd-113">Deletes the NetwrokRuleSet for the Given "ServiceBus-Namespace1-1375" namesapce</span></span> 

### <span data-ttu-id="d45dd-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="d45dd-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="d45dd-115">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="d45dd-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="d45dd-116">A NetwrokRuleSet törlése a InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="d45dd-116">Deletes the NetwrokRuleSet using InputObject</span></span> 

### <span data-ttu-id="d45dd-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="d45dd-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="d45dd-118">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="d45dd-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="d45dd-119">A NetwrokRuleSet törlése a Namepsace ResourceId használatával</span><span class="sxs-lookup"><span data-stu-id="d45dd-119">Deletes the NetwrokRuleSet using ResourceId of the Namepsace</span></span>


## <span data-ttu-id="d45dd-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d45dd-120">PARAMETERS</span></span>

### <span data-ttu-id="d45dd-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d45dd-121">-AsJob</span></span>
<span data-ttu-id="d45dd-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d45dd-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45dd-123">-DefaultProfile</span></span>
<span data-ttu-id="d45dd-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d45dd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d45dd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d45dd-125">-InputObject</span></span>
<span data-ttu-id="d45dd-126">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="d45dd-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d45dd-127">-Name</span></span>
<span data-ttu-id="d45dd-128">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="d45dd-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d45dd-129">-PassThru</span></span>
<span data-ttu-id="d45dd-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d45dd-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d45dd-131">-ResourceGroupName</span></span>
<span data-ttu-id="d45dd-132">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d45dd-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d45dd-133">-ResourceId</span></span>
<span data-ttu-id="d45dd-134">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="d45dd-134">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d45dd-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d45dd-135">-Confirm</span></span>
<span data-ttu-id="d45dd-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d45dd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d45dd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d45dd-137">-WhatIf</span></span>
<span data-ttu-id="d45dd-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d45dd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d45dd-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d45dd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d45dd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45dd-140">CommonParameters</span></span>
<span data-ttu-id="d45dd-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d45dd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d45dd-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d45dd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45dd-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d45dd-143">INPUTS</span></span>

### <span data-ttu-id="d45dd-144">Microsoft. Azure. Command. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d45dd-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="d45dd-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d45dd-145">System.String</span></span>

## <span data-ttu-id="d45dd-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d45dd-146">OUTPUTS</span></span>

### <span data-ttu-id="d45dd-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d45dd-147">System.Boolean</span></span>

## <span data-ttu-id="d45dd-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d45dd-148">NOTES</span></span>

## <span data-ttu-id="d45dd-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d45dd-149">RELATED LINKS</span></span>
