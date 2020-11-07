---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 3ad94696ea10d791ebe2930b6c054e00b9e69d18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666458"
---
# <span data-ttu-id="ff2bc-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff2bc-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="ff2bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff2bc-103">A megadott névtér NetworkRuleSet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ff2bc-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="ff2bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff2bc-104">SYNTAX</span></span>

### <span data-ttu-id="ff2bc-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff2bc-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff2bc-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ff2bc-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff2bc-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff2bc-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff2bc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff2bc-108">DESCRIPTION</span></span>
<span data-ttu-id="ff2bc-109">A megadott névtér NetworkRuleSet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ff2bc-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="ff2bc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ff2bc-110">EXAMPLES</span></span>

### <span data-ttu-id="ff2bc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ff2bc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="ff2bc-112">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="ff2bc-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="ff2bc-113">A megadott "Eventhub-Namespace1-1375" névtér NetworkRuleSet törlése</span><span class="sxs-lookup"><span data-stu-id="ff2bc-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="ff2bc-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="ff2bc-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="ff2bc-115">A NetworkRuleSet törlése a InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="ff2bc-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="ff2bc-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="ff2bc-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="ff2bc-117">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="ff2bc-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="ff2bc-118">A NetworkRuleSet törlése a névtér ResourceId használatával</span><span class="sxs-lookup"><span data-stu-id="ff2bc-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="ff2bc-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff2bc-119">PARAMETERS</span></span>

### <span data-ttu-id="ff2bc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff2bc-120">-AsJob</span></span>
<span data-ttu-id="ff2bc-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ff2bc-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff2bc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2bc-122">-DefaultProfile</span></span>
<span data-ttu-id="ff2bc-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff2bc-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff2bc-124">-InputObject</span></span>
<span data-ttu-id="ff2bc-125">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="ff2bc-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff2bc-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff2bc-126">-Name</span></span>
<span data-ttu-id="ff2bc-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ff2bc-127">Namespace Name</span></span>

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

### <span data-ttu-id="ff2bc-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff2bc-128">-PassThru</span></span>
<span data-ttu-id="ff2bc-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ff2bc-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ff2bc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff2bc-130">-ResourceGroupName</span></span>
<span data-ttu-id="ff2bc-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ff2bc-131">Resource Group Name</span></span>

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

### <span data-ttu-id="ff2bc-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff2bc-132">-ResourceId</span></span>
<span data-ttu-id="ff2bc-133">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="ff2bc-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="ff2bc-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff2bc-134">-Confirm</span></span>
<span data-ttu-id="ff2bc-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff2bc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff2bc-136">-WhatIf</span></span>
<span data-ttu-id="ff2bc-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff2bc-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff2bc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2bc-139">CommonParameters</span></span>
<span data-ttu-id="ff2bc-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff2bc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ff2bc-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff2bc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2bc-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff2bc-142">INPUTS</span></span>

### <span data-ttu-id="ff2bc-143">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ff2bc-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="ff2bc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ff2bc-144">System.String</span></span>

## <span data-ttu-id="ff2bc-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff2bc-145">OUTPUTS</span></span>

### <span data-ttu-id="ff2bc-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff2bc-146">System.Boolean</span></span>

## <span data-ttu-id="ff2bc-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff2bc-147">NOTES</span></span>

## <span data-ttu-id="ff2bc-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff2bc-148">RELATED LINKS</span></span>