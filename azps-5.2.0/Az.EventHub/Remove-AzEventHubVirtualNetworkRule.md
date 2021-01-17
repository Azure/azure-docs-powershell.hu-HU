---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 68aa2d4d0d5ba29cdb2c8ddf86d49c6be1280c88
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353081"
---
# <span data-ttu-id="a4ee7-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a4ee7-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="a4ee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ee7-103">A Namespace NetworkRuleSet egyetlen megadott VirtualNetworkRule-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a4ee7-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="a4ee7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a4ee7-104">SYNTAX</span></span>

### <span data-ttu-id="a4ee7-105">VirtualNetworkRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4ee7-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4ee7-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4ee7-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4ee7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a4ee7-107">DESCRIPTION</span></span>
<span data-ttu-id="a4ee7-108">A Namespace NetworkRuleSet egyetlen megadott VirtualNetworkRule-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a4ee7-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="a4ee7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a4ee7-109">EXAMPLES</span></span>

### <span data-ttu-id="a4ee7-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a4ee7-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="a4ee7-111">A Namespace NetworkRuleSet egyetlen megadott VirtualNetworkRule-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a4ee7-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="a4ee7-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="a4ee7-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="a4ee7-113">A $virtualruleset NetworkRuleSet 1-es 1-es ének eltávolítása a megadott Névtérből</span><span class="sxs-lookup"><span data-stu-id="a4ee7-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="a4ee7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4ee7-114">PARAMETERS</span></span>

### <span data-ttu-id="a4ee7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4ee7-115">-AsJob</span></span>
<span data-ttu-id="a4ee7-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a4ee7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4ee7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ee7-117">-DefaultProfile</span></span>
<span data-ttu-id="a4ee7-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4ee7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ee7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a4ee7-119">-Name</span></span>
<span data-ttu-id="a4ee7-120">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a4ee7-120">Namespace Name</span></span>

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

### <span data-ttu-id="a4ee7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4ee7-121">-PassThru</span></span>
<span data-ttu-id="a4ee7-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a4ee7-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a4ee7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ee7-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4ee7-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a4ee7-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a4ee7-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a4ee7-125">-SubnetId</span></span>
<span data-ttu-id="a4ee7-126">Alhálózati erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="a4ee7-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="a4ee7-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="a4ee7-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="a4ee7-128">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="a4ee7-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="a4ee7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4ee7-129">-Confirm</span></span>
<span data-ttu-id="a4ee7-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a4ee7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ee7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ee7-131">-WhatIf</span></span>
<span data-ttu-id="a4ee7-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a4ee7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ee7-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4ee7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ee7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ee7-134">CommonParameters</span></span>
<span data-ttu-id="a4ee7-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ee7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a4ee7-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ee7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ee7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4ee7-137">INPUTS</span></span>

### <span data-ttu-id="a4ee7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a4ee7-138">System.String</span></span>

### <span data-ttu-id="a4ee7-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="a4ee7-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="a4ee7-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4ee7-140">OUTPUTS</span></span>

### <span data-ttu-id="a4ee7-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a4ee7-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="a4ee7-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a4ee7-142">NOTES</span></span>

## <span data-ttu-id="a4ee7-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4ee7-143">RELATED LINKS</span></span>