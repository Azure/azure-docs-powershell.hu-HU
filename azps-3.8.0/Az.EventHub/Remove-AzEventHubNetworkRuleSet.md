---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845586"
---
# <span data-ttu-id="b9b0d-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9b0d-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="b9b0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b0d-103">A megadott névtér NetworkRuleSet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b9b0d-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="b9b0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9b0d-104">SYNTAX</span></span>

### <span data-ttu-id="b9b0d-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9b0d-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b0d-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b9b0d-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b0d-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9b0d-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b0d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9b0d-108">DESCRIPTION</span></span>
<span data-ttu-id="b9b0d-109">A megadott névtér NetworkRuleSet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b9b0d-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="b9b0d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b9b0d-110">EXAMPLES</span></span>

### <span data-ttu-id="b9b0d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b9b0d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="b9b0d-112">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="b9b0d-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="b9b0d-113">A megadott "Eventhub-Namespace1-1375" névtér NetworkRuleSet törlése</span><span class="sxs-lookup"><span data-stu-id="b9b0d-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="b9b0d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="b9b0d-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="b9b0d-115">A NetworkRuleSet törlése a InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="b9b0d-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="b9b0d-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="b9b0d-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="b9b0d-117">Név: alapértelmezett DefaultAction: Engedélyezés azonosító:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default típus: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="b9b0d-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="b9b0d-118">A NetworkRuleSet törlése a névtér ResourceId használatával</span><span class="sxs-lookup"><span data-stu-id="b9b0d-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="b9b0d-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9b0d-119">PARAMETERS</span></span>

### <span data-ttu-id="b9b0d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9b0d-120">-AsJob</span></span>
<span data-ttu-id="b9b0d-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b9b0d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9b0d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b0d-122">-DefaultProfile</span></span>
<span data-ttu-id="b9b0d-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9b0d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9b0d-124">-InputObject</span></span>
<span data-ttu-id="b9b0d-125">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="b9b0d-125">Namespace Object</span></span>

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

### <span data-ttu-id="b9b0d-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9b0d-126">-Name</span></span>
<span data-ttu-id="b9b0d-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="b9b0d-127">Namespace Name</span></span>

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

### <span data-ttu-id="b9b0d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9b0d-128">-PassThru</span></span>
<span data-ttu-id="b9b0d-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b9b0d-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b9b0d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b0d-130">-ResourceGroupName</span></span>
<span data-ttu-id="b9b0d-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b9b0d-131">Resource Group Name</span></span>

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

### <span data-ttu-id="b9b0d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9b0d-132">-ResourceId</span></span>
<span data-ttu-id="b9b0d-133">Namespace Resource id</span><span class="sxs-lookup"><span data-stu-id="b9b0d-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="b9b0d-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9b0d-134">-Confirm</span></span>
<span data-ttu-id="b9b0d-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b0d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b0d-136">-WhatIf</span></span>
<span data-ttu-id="b9b0d-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b0d-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b0d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b0d-139">CommonParameters</span></span>
<span data-ttu-id="b9b0d-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9b0d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b9b0d-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9b0d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b0d-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9b0d-142">INPUTS</span></span>

### <span data-ttu-id="b9b0d-143">Microsoft. Azure. Command. EventHub. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b9b0d-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="b9b0d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b9b0d-144">System.String</span></span>

## <span data-ttu-id="b9b0d-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9b0d-145">OUTPUTS</span></span>

### <span data-ttu-id="b9b0d-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9b0d-146">System.Boolean</span></span>

## <span data-ttu-id="b9b0d-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9b0d-147">NOTES</span></span>

## <span data-ttu-id="b9b0d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9b0d-148">RELATED LINKS</span></span>