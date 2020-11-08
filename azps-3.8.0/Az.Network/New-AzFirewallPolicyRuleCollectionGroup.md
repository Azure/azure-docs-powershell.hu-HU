---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011812"
---
# <span data-ttu-id="c0a35-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="c0a35-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="c0a35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0a35-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a35-103">Új Azure Firewall Policy Rule Collection-csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0a35-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="c0a35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0a35-104">SYNTAX</span></span>

### <span data-ttu-id="c0a35-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0a35-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0a35-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0a35-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0a35-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0a35-107">DESCRIPTION</span></span>
<span data-ttu-id="c0a35-108">A **New-AzFirewallPolicyRuleCollectionGroup** parancsmag létrehoz egy szabály-összegyűjtési csoportot egy Azure tűzfal-házirendben.</span><span class="sxs-lookup"><span data-stu-id="c0a35-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="c0a35-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c0a35-109">EXAMPLES</span></span>

### <span data-ttu-id="c0a35-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c0a35-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="c0a35-111">Ez a példa egy szabály-összegyűjtési csoportot hoz létre a tűzfal házirendjében $fp</span><span class="sxs-lookup"><span data-stu-id="c0a35-111">This example creates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="c0a35-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0a35-112">PARAMETERS</span></span>

### <span data-ttu-id="c0a35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a35-113">-DefaultProfile</span></span>
<span data-ttu-id="c0a35-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0a35-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0a35-115">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="c0a35-115">-FirewallPolicyName</span></span>
<span data-ttu-id="c0a35-116">A tűzfal-házirend neve</span><span class="sxs-lookup"><span data-stu-id="c0a35-116">The name of the firewall policy</span></span>

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

### <span data-ttu-id="c0a35-117">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="c0a35-117">-FirewallPolicyObject</span></span>
<span data-ttu-id="c0a35-118">Tűzfal-házirend.</span><span class="sxs-lookup"><span data-stu-id="c0a35-118">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a35-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0a35-119">-Name</span></span>
<span data-ttu-id="c0a35-120">A szabály csoport neve</span><span class="sxs-lookup"><span data-stu-id="c0a35-120">The name of the Rule Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a35-121">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="c0a35-121">-Priority</span></span>
<span data-ttu-id="c0a35-122">A szabály csoport prioritása</span><span class="sxs-lookup"><span data-stu-id="c0a35-122">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a35-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0a35-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0a35-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c0a35-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a35-125">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="c0a35-125">-RuleCollection</span></span>
<span data-ttu-id="c0a35-126">A szabályok listája</span><span class="sxs-lookup"><span data-stu-id="c0a35-126">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a35-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0a35-127">-Confirm</span></span>
<span data-ttu-id="c0a35-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0a35-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0a35-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0a35-129">-WhatIf</span></span>
<span data-ttu-id="c0a35-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0a35-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0a35-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0a35-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0a35-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a35-132">CommonParameters</span></span>
<span data-ttu-id="c0a35-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0a35-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a35-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c0a35-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a35-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0a35-135">INPUTS</span></span>

### <span data-ttu-id="c0a35-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c0a35-136">System.String</span></span>

### <span data-ttu-id="c0a35-137">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c0a35-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="c0a35-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0a35-138">OUTPUTS</span></span>

### <span data-ttu-id="c0a35-139">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="c0a35-139">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="c0a35-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0a35-140">NOTES</span></span>

## <span data-ttu-id="c0a35-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0a35-141">RELATED LINKS</span></span>
