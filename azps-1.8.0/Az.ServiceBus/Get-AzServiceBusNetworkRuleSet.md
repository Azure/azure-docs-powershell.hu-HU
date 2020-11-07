---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: d200d342bfa16fb0b2864e0196dc9648b4aa7fcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669202"
---
# <span data-ttu-id="f984b-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f984b-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="f984b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f984b-102">SYNOPSIS</span></span>
<span data-ttu-id="f984b-103">Az aktuális Azure-előfizetésben az esemény-hubok NetwrokruleSet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f984b-103">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="f984b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f984b-104">SYNTAX</span></span>

### <span data-ttu-id="f984b-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f984b-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f984b-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f984b-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f984b-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f984b-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f984b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f984b-108">DESCRIPTION</span></span>
<span data-ttu-id="f984b-109">Az aktuális Azure-előfizetésben az esemény-hubok NetwrokruleSet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f984b-109">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="f984b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f984b-110">EXAMPLES</span></span>

### <span data-ttu-id="f984b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f984b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="f984b-112">Név: alapértelmezett DefaultAction: engedélyezési azonosító:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default-típus: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="f984b-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="f984b-113">A ResourceGroup és a Namesape paraméterrel megtudhatja, hogy hol található az esemény-hubok NetwrokruleSet a névtérben.</span><span class="sxs-lookup"><span data-stu-id="f984b-113">Get the details of Event Hubs NetwrokruleSet of namespace using ResourceGroup and Namesape parameters.</span></span> 

### <span data-ttu-id="f984b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="f984b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="f984b-115">Név: alapértelmezett DefaultAction: engedélyezési azonosító:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default-típus: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="f984b-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="f984b-116">Az esemény-hubok NetwrokruleSet az aktuális előfizetésben található névtérrel megtudhatja.</span><span class="sxs-lookup"><span data-stu-id="f984b-116">Get the details of Event Hubs NetwrokruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="f984b-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="f984b-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="f984b-118">Név: alapértelmezett DefaultAction: engedélyezési azonosító:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default-típus: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="f984b-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="f984b-119">Az esemény-hubok NetwrokruleSet a többi névtér erőforrás-azonosítójának használatával</span><span class="sxs-lookup"><span data-stu-id="f984b-119">Get the details of Event Hubs NetwrokruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="f984b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f984b-120">PARAMETERS</span></span>

### <span data-ttu-id="f984b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f984b-121">-DefaultProfile</span></span>
<span data-ttu-id="f984b-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f984b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f984b-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f984b-123">-Namespace</span></span>
<span data-ttu-id="f984b-124">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f984b-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f984b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f984b-125">-ResourceGroupName</span></span>
<span data-ttu-id="f984b-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f984b-126">Resource Group Name</span></span>

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

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f984b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f984b-127">-ResourceId</span></span>
<span data-ttu-id="f984b-128">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="f984b-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="f984b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f984b-129">CommonParameters</span></span>
<span data-ttu-id="f984b-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f984b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f984b-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f984b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f984b-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f984b-132">INPUTS</span></span>

### <span data-ttu-id="f984b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f984b-133">System.String</span></span>

## <span data-ttu-id="f984b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f984b-134">OUTPUTS</span></span>

### <span data-ttu-id="f984b-135">Microsoft. Azure. Command. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="f984b-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="f984b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f984b-136">NOTES</span></span>

## <span data-ttu-id="f984b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f984b-137">RELATED LINKS</span></span>