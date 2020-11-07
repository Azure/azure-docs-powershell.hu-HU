---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 33d562d362abbdec17680c7af7e70f956ab10486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666457"
---
# <span data-ttu-id="d1ee3-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d1ee3-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="d1ee3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ee3-103">A névtér NetworkRuleSet egyetlen adott VirtualNetworkRule eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1ee3-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="d1ee3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1ee3-104">SYNTAX</span></span>

### <span data-ttu-id="d1ee3-105">VirtualNetworkRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1ee3-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1ee3-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1ee3-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1ee3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1ee3-107">DESCRIPTION</span></span>
<span data-ttu-id="d1ee3-108">A névtér NetworkRuleSet egyetlen adott VirtualNetworkRule eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1ee3-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="d1ee3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d1ee3-109">EXAMPLES</span></span>

### <span data-ttu-id="d1ee3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d1ee3-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="d1ee3-111">A névtér NetworkRuleSet egyetlen adott VirtualNetworkRule eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1ee3-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="d1ee3-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d1ee3-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="d1ee3-113">A megadott névtérhez tartozó NetworkRuleSet 1 $virtualruleset eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d1ee3-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="d1ee3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1ee3-114">PARAMETERS</span></span>

### <span data-ttu-id="d1ee3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1ee3-115">-AsJob</span></span>
<span data-ttu-id="d1ee3-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d1ee3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1ee3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ee3-117">-DefaultProfile</span></span>
<span data-ttu-id="d1ee3-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1ee3-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1ee3-119">-Name</span></span>
<span data-ttu-id="d1ee3-120">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="d1ee3-120">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ee3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1ee3-121">-PassThru</span></span>
<span data-ttu-id="d1ee3-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d1ee3-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d1ee3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1ee3-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1ee3-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="d1ee3-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ee3-125">– NetI</span><span class="sxs-lookup"><span data-stu-id="d1ee3-125">-SubnetId</span></span>
<span data-ttu-id="d1ee3-126">Alhálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d1ee3-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ee3-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="d1ee3-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="d1ee3-128">IPRule konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="d1ee3-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ee3-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1ee3-129">-Confirm</span></span>
<span data-ttu-id="d1ee3-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1ee3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1ee3-131">-WhatIf</span></span>
<span data-ttu-id="d1ee3-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1ee3-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1ee3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ee3-134">CommonParameters</span></span>
<span data-ttu-id="d1ee3-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1ee3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d1ee3-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ee3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ee3-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1ee3-137">INPUTS</span></span>

### <span data-ttu-id="d1ee3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d1ee3-138">System.String</span></span>

### <span data-ttu-id="d1ee3-139">Microsoft. Azure. Command. EventHub. models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="d1ee3-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="d1ee3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1ee3-140">OUTPUTS</span></span>

### <span data-ttu-id="d1ee3-141">Microsoft. Azure. Command. EventHub. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d1ee3-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d1ee3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1ee3-142">NOTES</span></span>

## <span data-ttu-id="d1ee3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1ee3-143">RELATED LINKS</span></span>