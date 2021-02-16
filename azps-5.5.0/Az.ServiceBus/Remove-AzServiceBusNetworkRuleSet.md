---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 6c803f399bf88c6e4887441ec9f9bd50c058361b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150754"
---
# <span data-ttu-id="4b196-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4b196-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="4b196-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b196-102">SYNOPSIS</span></span>
<span data-ttu-id="4b196-103">A Megadott névtér NetworkRuleSet-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4b196-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="4b196-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b196-104">SYNTAX</span></span>

### <span data-ttu-id="4b196-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b196-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b196-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4b196-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b196-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b196-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b196-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b196-108">DESCRIPTION</span></span>
<span data-ttu-id="4b196-109">A Megadott névtér NetworkRuleSet-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4b196-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="4b196-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b196-110">EXAMPLES</span></span>

### <span data-ttu-id="4b196-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4b196-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="4b196-112">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="4b196-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="4b196-113">A Megadott "ServiceBus-Namespace1-1375" névtér NetworkRuleSet-ének törlése</span><span class="sxs-lookup"><span data-stu-id="4b196-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="4b196-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="4b196-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="4b196-115">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="4b196-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="4b196-116">A NetworkRuleSet törlése az InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="4b196-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="4b196-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="4b196-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="4b196-118">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="4b196-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="4b196-119">A NetworkRuleSet törlése a Namespace ResourceId (Erőforrásazonosító) használatával</span><span class="sxs-lookup"><span data-stu-id="4b196-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="4b196-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b196-120">PARAMETERS</span></span>

### <span data-ttu-id="4b196-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b196-121">-AsJob</span></span>
<span data-ttu-id="4b196-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4b196-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b196-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b196-123">-DefaultProfile</span></span>
<span data-ttu-id="4b196-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b196-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b196-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b196-125">-InputObject</span></span>
<span data-ttu-id="4b196-126">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="4b196-126">Namespace Object</span></span>

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

### <span data-ttu-id="4b196-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4b196-127">-Name</span></span>
<span data-ttu-id="4b196-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="4b196-128">Namespace Name</span></span>

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

### <span data-ttu-id="4b196-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b196-129">-PassThru</span></span>
<span data-ttu-id="4b196-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4b196-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4b196-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b196-131">-ResourceGroupName</span></span>
<span data-ttu-id="4b196-132">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4b196-132">Resource Group Name</span></span>

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

### <span data-ttu-id="4b196-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b196-133">-ResourceId</span></span>
<span data-ttu-id="4b196-134">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="4b196-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="4b196-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b196-135">-Confirm</span></span>
<span data-ttu-id="4b196-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4b196-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b196-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b196-137">-WhatIf</span></span>
<span data-ttu-id="4b196-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4b196-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b196-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b196-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b196-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b196-140">CommonParameters</span></span>
<span data-ttu-id="4b196-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b196-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4b196-142">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b196-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b196-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b196-143">INPUTS</span></span>

### <span data-ttu-id="4b196-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4b196-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="4b196-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4b196-145">System.String</span></span>

## <span data-ttu-id="4b196-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b196-146">OUTPUTS</span></span>

### <span data-ttu-id="4b196-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b196-147">System.Boolean</span></span>

## <span data-ttu-id="4b196-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b196-148">NOTES</span></span>

## <span data-ttu-id="4b196-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b196-149">RELATED LINKS</span></span>
