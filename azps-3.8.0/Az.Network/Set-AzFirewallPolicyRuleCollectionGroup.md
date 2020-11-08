---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8e1260a636a1be5a42888fcc6cc12cb8b228859c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012509"
---
# <span data-ttu-id="88256-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="88256-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="88256-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88256-102">SYNOPSIS</span></span>
<span data-ttu-id="88256-103">módosított Azure tűzfal házirend-gyűjtemény csoportjának mentése</span><span class="sxs-lookup"><span data-stu-id="88256-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="88256-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88256-104">SYNTAX</span></span>

### <span data-ttu-id="88256-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="88256-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88256-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88256-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88256-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88256-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88256-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88256-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88256-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="88256-109">DESCRIPTION</span></span>
<span data-ttu-id="88256-110">A **set-AzFirewallPolicyRuleCollectionGroup** parancsmag az Azure tűzfal-házirendben frissíti a szabályok begyűjtési csoportjait.</span><span class="sxs-lookup"><span data-stu-id="88256-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="88256-111">Példák</span><span class="sxs-lookup"><span data-stu-id="88256-111">EXAMPLES</span></span>

### <span data-ttu-id="88256-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="88256-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="88256-113">Ebben a példában egy szabály-gyűjteményi csoportot frissít a tűzfal házirend-$fp</span><span class="sxs-lookup"><span data-stu-id="88256-113">This example updates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="88256-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88256-114">PARAMETERS</span></span>

### <span data-ttu-id="88256-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88256-115">-DefaultProfile</span></span>
<span data-ttu-id="88256-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88256-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88256-117">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="88256-117">-FirewallPolicyName</span></span>
<span data-ttu-id="88256-118">A tűzfal-házirend neve</span><span class="sxs-lookup"><span data-stu-id="88256-118">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88256-119">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="88256-119">-FirewallPolicyObject</span></span>
<span data-ttu-id="88256-120">Tűzfal-házirend.</span><span class="sxs-lookup"><span data-stu-id="88256-120">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88256-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88256-121">-InputObject</span></span>
<span data-ttu-id="88256-122">A szabályok listája</span><span class="sxs-lookup"><span data-stu-id="88256-122">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88256-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88256-123">-Name</span></span>
<span data-ttu-id="88256-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="88256-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88256-125">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="88256-125">-Priority</span></span>
<span data-ttu-id="88256-126">A szabály csoport prioritása</span><span class="sxs-lookup"><span data-stu-id="88256-126">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88256-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88256-127">-ResourceGroupName</span></span>
<span data-ttu-id="88256-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="88256-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88256-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88256-129">-ResourceId</span></span>
<span data-ttu-id="88256-130">A szabály-összegyűjtési csoport erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="88256-130">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88256-131">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="88256-131">-RuleCollection</span></span>
<span data-ttu-id="88256-132">A szabályok gyűjteményének listája</span><span class="sxs-lookup"><span data-stu-id="88256-132">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88256-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88256-133">-Confirm</span></span>
<span data-ttu-id="88256-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88256-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88256-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88256-135">-WhatIf</span></span>
<span data-ttu-id="88256-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88256-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88256-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88256-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88256-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88256-138">CommonParameters</span></span>
<span data-ttu-id="88256-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88256-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88256-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88256-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88256-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88256-141">INPUTS</span></span>

### <span data-ttu-id="88256-142">System. String</span><span class="sxs-lookup"><span data-stu-id="88256-142">System.String</span></span>

### <span data-ttu-id="88256-143">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="88256-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="88256-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88256-144">OUTPUTS</span></span>

### <span data-ttu-id="88256-145">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="88256-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="88256-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88256-146">NOTES</span></span>

## <span data-ttu-id="88256-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88256-147">RELATED LINKS</span></span>
