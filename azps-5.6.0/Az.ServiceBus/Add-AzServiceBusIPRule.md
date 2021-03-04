---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: e0450df003b474cae57319d5450423af58f4d3eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926410"
---
# <span data-ttu-id="301d6-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="301d6-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="301d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="301d6-102">SYNOPSIS</span></span>
<span data-ttu-id="301d6-103">Egyetlen IP-szabály hozzáadása a megadott Namespace NetworkRuleSet-hez</span><span class="sxs-lookup"><span data-stu-id="301d6-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="301d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="301d6-104">SYNTAX</span></span>

### <span data-ttu-id="301d6-105">IPRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="301d6-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301d6-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="301d6-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="301d6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="301d6-107">DESCRIPTION</span></span>
<span data-ttu-id="301d6-108">Egyetlen IP-szabály hozzáadása a megadott Namespace NetworkRuleSet-hez</span><span class="sxs-lookup"><span data-stu-id="301d6-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="301d6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="301d6-109">EXAMPLES</span></span>

### <span data-ttu-id="301d6-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="301d6-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="301d6-111">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetRules:</span><span class="sxs-lookup"><span data-stu-id="301d6-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="301d6-112">adja hozzá az IPRule tartományt az IpMask "11.22.33.44" és az Action Allow névtérhez.</span><span class="sxs-lookup"><span data-stu-id="301d6-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="301d6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="301d6-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="301d6-114">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetRules:</span><span class="sxs-lookup"><span data-stu-id="301d6-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="301d6-115">adja hozzá az IPRule tartományt az IpMask "11.22.33.44" és az Action Allow névtérhez.</span><span class="sxs-lookup"><span data-stu-id="301d6-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="301d6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="301d6-116">PARAMETERS</span></span>

### <span data-ttu-id="301d6-117">-Művelet</span><span class="sxs-lookup"><span data-stu-id="301d6-117">-Action</span></span>
<span data-ttu-id="301d6-118">Az IP-szűrési művelet</span><span class="sxs-lookup"><span data-stu-id="301d6-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301d6-119">-DefaultProfile</span></span>
<span data-ttu-id="301d6-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="301d6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="301d6-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="301d6-121">-IpMask</span></span>
<span data-ttu-id="301d6-122">Alhálózati erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="301d6-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301d6-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="301d6-123">-IpRuleObject</span></span>
<span data-ttu-id="301d6-124">Hozzáadható IPRule konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="301d6-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="301d6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="301d6-125">-Name</span></span>
<span data-ttu-id="301d6-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="301d6-126">Namespace Name</span></span>

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

### <span data-ttu-id="301d6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301d6-127">-ResourceGroupName</span></span>
<span data-ttu-id="301d6-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="301d6-128">Resource Group Name</span></span>

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

### <span data-ttu-id="301d6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="301d6-129">-Confirm</span></span>
<span data-ttu-id="301d6-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="301d6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301d6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301d6-131">-WhatIf</span></span>
<span data-ttu-id="301d6-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="301d6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301d6-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="301d6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301d6-134">CommonParameters</span></span>
<span data-ttu-id="301d6-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="301d6-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="301d6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301d6-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="301d6-137">INPUTS</span></span>

### <span data-ttu-id="301d6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="301d6-138">System.String</span></span>

### <span data-ttu-id="301d6-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="301d6-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="301d6-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="301d6-140">OUTPUTS</span></span>

### <span data-ttu-id="301d6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="301d6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="301d6-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="301d6-142">NOTES</span></span>

## <span data-ttu-id="301d6-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="301d6-143">RELATED LINKS</span></span>