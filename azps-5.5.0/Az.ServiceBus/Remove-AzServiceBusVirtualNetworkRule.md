---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: d72c7e1ebfdd7543740ea8fafeb62861f4394093
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168818"
---
# <span data-ttu-id="d34d6-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d34d6-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="d34d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d34d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d34d6-103">Eltávolítja a Namespace NetworkRuleSet virtualnetworkRule-ét</span><span class="sxs-lookup"><span data-stu-id="d34d6-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="d34d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d34d6-104">SYNTAX</span></span>

### <span data-ttu-id="d34d6-105">VirtualNetworkRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d34d6-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d34d6-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d34d6-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d34d6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d34d6-107">DESCRIPTION</span></span>
<span data-ttu-id="d34d6-108">A Namespace NetworkRuleSet egyetlen megadott VirtualNetworkRule-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d34d6-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="d34d6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d34d6-109">EXAMPLES</span></span>

### <span data-ttu-id="d34d6-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d34d6-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="d34d6-111">Eltávolítja a Namespace NetworkRuleSet virtualnetworkRule-ét</span><span class="sxs-lookup"><span data-stu-id="d34d6-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="d34d6-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d34d6-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="d34d6-113">A networkruleSet $virtualruleset 1-ének eltávolítása a megadott Namespace névtérből</span><span class="sxs-lookup"><span data-stu-id="d34d6-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="d34d6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d34d6-114">PARAMETERS</span></span>

### <span data-ttu-id="d34d6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d34d6-115">-AsJob</span></span>
<span data-ttu-id="d34d6-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d34d6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d34d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34d6-117">-DefaultProfile</span></span>
<span data-ttu-id="d34d6-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d34d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d34d6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d34d6-119">-Name</span></span>
<span data-ttu-id="d34d6-120">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d34d6-120">Namespace Name</span></span>

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

### <span data-ttu-id="d34d6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d34d6-121">-PassThru</span></span>
<span data-ttu-id="d34d6-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d34d6-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d34d6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34d6-123">-ResourceGroupName</span></span>
<span data-ttu-id="d34d6-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d34d6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="d34d6-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d34d6-125">-SubnetId</span></span>
<span data-ttu-id="d34d6-126">Alhálózati erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="d34d6-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="d34d6-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="d34d6-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="d34d6-128">IPRule Configuration Object</span><span class="sxs-lookup"><span data-stu-id="d34d6-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d34d6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d34d6-129">-Confirm</span></span>
<span data-ttu-id="d34d6-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d34d6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d34d6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d34d6-131">-WhatIf</span></span>
<span data-ttu-id="d34d6-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d34d6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d34d6-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d34d6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d34d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34d6-134">CommonParameters</span></span>
<span data-ttu-id="d34d6-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d34d6-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d34d6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34d6-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d34d6-137">INPUTS</span></span>

### <span data-ttu-id="d34d6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d34d6-138">System.String</span></span>

### <span data-ttu-id="d34d6-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="d34d6-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="d34d6-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d34d6-140">OUTPUTS</span></span>

### <span data-ttu-id="d34d6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d34d6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d34d6-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d34d6-142">NOTES</span></span>

## <span data-ttu-id="d34d6-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d34d6-143">RELATED LINKS</span></span>
