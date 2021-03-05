---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 6b01211b7efa20983f868c7e70e54be02d5ad5c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001558"
---
# <span data-ttu-id="b45cc-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="b45cc-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="b45cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b45cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b45cc-103">Egyetlen IP-szabály hozzáadása a megadott Namespace NetworkRuleSet-hez</span><span class="sxs-lookup"><span data-stu-id="b45cc-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="b45cc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b45cc-104">SYNTAX</span></span>

### <span data-ttu-id="b45cc-105">IPRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b45cc-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b45cc-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b45cc-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b45cc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b45cc-107">DESCRIPTION</span></span>
<span data-ttu-id="b45cc-108">Egyetlen IP-szabály hozzáadása a megadott Namespace NetworkRuleSet-hez</span><span class="sxs-lookup"><span data-stu-id="b45cc-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="b45cc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b45cc-109">EXAMPLES</span></span>

### <span data-ttu-id="b45cc-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b45cc-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="b45cc-111">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetRules:</span><span class="sxs-lookup"><span data-stu-id="b45cc-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="b45cc-112">adja hozzá az IPRule tartományt az IpMask "11.22.33.44" és az Action Allow (Művelet engedélyezése) névtérhez.</span><span class="sxs-lookup"><span data-stu-id="b45cc-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="b45cc-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b45cc-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="b45cc-114">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetRules:</span><span class="sxs-lookup"><span data-stu-id="b45cc-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="b45cc-115">adja hozzá az IPRule tartományt az IpMask "11.22.33.44" és az Action Allow (Művelet engedélyezése) névtérhez.</span><span class="sxs-lookup"><span data-stu-id="b45cc-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="b45cc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b45cc-116">PARAMETERS</span></span>

### <span data-ttu-id="b45cc-117">-Művelet</span><span class="sxs-lookup"><span data-stu-id="b45cc-117">-Action</span></span>
<span data-ttu-id="b45cc-118">Az IP-szűrési művelet</span><span class="sxs-lookup"><span data-stu-id="b45cc-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="b45cc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b45cc-119">-DefaultProfile</span></span>
<span data-ttu-id="b45cc-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b45cc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b45cc-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="b45cc-121">-IpMask</span></span>
<span data-ttu-id="b45cc-122">Alhálózati erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="b45cc-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="b45cc-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="b45cc-123">-IpRuleObject</span></span>
<span data-ttu-id="b45cc-124">Hozzáadható IPRule konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="b45cc-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b45cc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b45cc-125">-Name</span></span>
<span data-ttu-id="b45cc-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="b45cc-126">Namespace Name</span></span>

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

### <span data-ttu-id="b45cc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b45cc-127">-ResourceGroupName</span></span>
<span data-ttu-id="b45cc-128">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b45cc-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b45cc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b45cc-129">-Confirm</span></span>
<span data-ttu-id="b45cc-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b45cc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b45cc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b45cc-131">-WhatIf</span></span>
<span data-ttu-id="b45cc-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b45cc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b45cc-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b45cc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b45cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b45cc-134">CommonParameters</span></span>
<span data-ttu-id="b45cc-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b45cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b45cc-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b45cc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b45cc-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b45cc-137">INPUTS</span></span>

### <span data-ttu-id="b45cc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b45cc-138">System.String</span></span>

### <span data-ttu-id="b45cc-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="b45cc-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="b45cc-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b45cc-140">OUTPUTS</span></span>

### <span data-ttu-id="b45cc-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="b45cc-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="b45cc-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b45cc-142">NOTES</span></span>

## <span data-ttu-id="b45cc-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b45cc-143">RELATED LINKS</span></span>
