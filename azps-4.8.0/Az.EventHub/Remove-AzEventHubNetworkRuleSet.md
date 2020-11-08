---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184962"
---
# <span data-ttu-id="0b136-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b136-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="0b136-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0b136-102">SYNOPSIS</span></span>
<span data-ttu-id="0b136-103">A megadott névtér NetworkRuleSet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0b136-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="0b136-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0b136-104">SYNTAX</span></span>

### <span data-ttu-id="0b136-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b136-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b136-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0b136-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b136-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b136-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b136-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0b136-108">DESCRIPTION</span></span>
<span data-ttu-id="0b136-109">A megadott névtér NetworkRuleSet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0b136-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="0b136-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0b136-110">EXAMPLES</span></span>

### <span data-ttu-id="0b136-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0b136-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="0b136-112">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="0b136-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="0b136-113">A megadott "Eventhub-Namespace1-1375" névtér NetworkRuleSet törlése</span><span class="sxs-lookup"><span data-stu-id="0b136-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="0b136-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="0b136-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="0b136-115">A NetworkRuleSet törlése a InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="0b136-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="0b136-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="0b136-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="0b136-117">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="0b136-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="0b136-118">A NetworkRuleSet törlése a névtér ResourceId használatával</span><span class="sxs-lookup"><span data-stu-id="0b136-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="0b136-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0b136-119">PARAMETERS</span></span>

### <span data-ttu-id="0b136-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b136-120">-AsJob</span></span>
<span data-ttu-id="0b136-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0b136-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b136-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b136-122">-DefaultProfile</span></span>
<span data-ttu-id="0b136-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b136-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b136-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b136-124">-InputObject</span></span>
<span data-ttu-id="0b136-125">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="0b136-125">Namespace Object</span></span>

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

### <span data-ttu-id="0b136-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0b136-126">-Name</span></span>
<span data-ttu-id="0b136-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="0b136-127">Namespace Name</span></span>

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

### <span data-ttu-id="0b136-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b136-128">-PassThru</span></span>
<span data-ttu-id="0b136-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0b136-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0b136-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b136-130">-ResourceGroupName</span></span>
<span data-ttu-id="0b136-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0b136-131">Resource Group Name</span></span>

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

### <span data-ttu-id="0b136-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b136-132">-ResourceId</span></span>
<span data-ttu-id="0b136-133">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="0b136-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="0b136-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0b136-134">-Confirm</span></span>
<span data-ttu-id="0b136-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0b136-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b136-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b136-136">-WhatIf</span></span>
<span data-ttu-id="0b136-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0b136-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b136-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0b136-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b136-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b136-139">CommonParameters</span></span>
<span data-ttu-id="0b136-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0b136-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0b136-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b136-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b136-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b136-142">INPUTS</span></span>

### <span data-ttu-id="0b136-143">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="0b136-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="0b136-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0b136-144">System.String</span></span>

## <span data-ttu-id="0b136-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b136-145">OUTPUTS</span></span>

### <span data-ttu-id="0b136-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b136-146">System.Boolean</span></span>

## <span data-ttu-id="0b136-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0b136-147">NOTES</span></span>

## <span data-ttu-id="0b136-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b136-148">RELATED LINKS</span></span>