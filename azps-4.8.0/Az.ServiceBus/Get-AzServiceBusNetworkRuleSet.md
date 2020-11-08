---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017624"
---
# <span data-ttu-id="8370e-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8370e-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="8370e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8370e-102">SYNOPSIS</span></span>
<span data-ttu-id="8370e-103">Az aktuális Azure-előfizetésben az esemény-hubok NetworkruleSet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8370e-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="8370e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8370e-104">SYNTAX</span></span>

### <span data-ttu-id="8370e-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8370e-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8370e-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8370e-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8370e-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8370e-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8370e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8370e-108">DESCRIPTION</span></span>
<span data-ttu-id="8370e-109">Az aktuális Azure-előfizetésben az esemény-hubok NetworkruleSet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8370e-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="8370e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8370e-110">EXAMPLES</span></span>

### <span data-ttu-id="8370e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8370e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="8370e-112">Név: alapértelmezett DefaultAction: engedélyezési azonosító:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default-típus: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="8370e-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8370e-113">A ResourceGroup és a NAMESPACE paraméterrel megtudhatja, hogy miként érheti el az esemény-hubok NetworkruleSet.</span><span class="sxs-lookup"><span data-stu-id="8370e-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="8370e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="8370e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="8370e-115">Név: alapértelmezett DefaultAction: engedélyezési azonosító:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default-típus: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="8370e-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8370e-116">Az esemény-hubok NetworkruleSet az aktuális előfizetésben található névtérrel megtudhatja.</span><span class="sxs-lookup"><span data-stu-id="8370e-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="8370e-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="8370e-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="8370e-118">Név: alapértelmezett DefaultAction: engedélyezési azonosító:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default-típus: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="8370e-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8370e-119">Az esemény-hubok NetworkruleSet a többi névtér erőforrás-azonosítójának használatával</span><span class="sxs-lookup"><span data-stu-id="8370e-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="8370e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8370e-120">PARAMETERS</span></span>

### <span data-ttu-id="8370e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8370e-121">-DefaultProfile</span></span>
<span data-ttu-id="8370e-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8370e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8370e-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8370e-123">-Namespace</span></span>
<span data-ttu-id="8370e-124">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="8370e-124">Namespace Name</span></span>

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

### <span data-ttu-id="8370e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8370e-125">-ResourceGroupName</span></span>
<span data-ttu-id="8370e-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="8370e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8370e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8370e-127">-ResourceId</span></span>
<span data-ttu-id="8370e-128">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="8370e-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="8370e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8370e-129">CommonParameters</span></span>
<span data-ttu-id="8370e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8370e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8370e-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8370e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8370e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8370e-132">INPUTS</span></span>

### <span data-ttu-id="8370e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8370e-133">System.String</span></span>

## <span data-ttu-id="8370e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8370e-134">OUTPUTS</span></span>

### <span data-ttu-id="8370e-135">Microsoft. Azure. Command. ServiceBus. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="8370e-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="8370e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8370e-136">NOTES</span></span>

## <span data-ttu-id="8370e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8370e-137">RELATED LINKS</span></span>