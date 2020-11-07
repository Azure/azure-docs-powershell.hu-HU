---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 60074271c37097e266e0c8e2ca1e4ee2a35e577d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842373"
---
# <span data-ttu-id="011ab-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="011ab-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="011ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="011ab-102">SYNOPSIS</span></span>
<span data-ttu-id="011ab-103">Egyetlen IP-szabály felvétele a megadott névtér NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="011ab-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="011ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="011ab-104">SYNTAX</span></span>

### <span data-ttu-id="011ab-105">IPRulePropertiesParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="011ab-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="011ab-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="011ab-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="011ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="011ab-107">DESCRIPTION</span></span>
<span data-ttu-id="011ab-108">Egyetlen IP-szabály felvétele a megadott névtér NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="011ab-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="011ab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="011ab-109">EXAMPLES</span></span>

### <span data-ttu-id="011ab-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="011ab-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="011ab-111">Név: alapértelmezett DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default-típus: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="011ab-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="011ab-112">vegye fel a IPRule a IpMask "11.22.33.44", és engedélyezze az adott névtérhez tartozó műveletek használatát.</span><span class="sxs-lookup"><span data-stu-id="011ab-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="011ab-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="011ab-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="011ab-114">Név: alapértelmezett DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default-típus: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="011ab-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="011ab-115">vegye fel a IPRule a IpMask "11.22.33.44", és engedélyezze az adott névtérhez tartozó műveletek használatát.</span><span class="sxs-lookup"><span data-stu-id="011ab-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="011ab-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="011ab-116">PARAMETERS</span></span>

### <span data-ttu-id="011ab-117">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="011ab-117">-Action</span></span>
<span data-ttu-id="011ab-118">Az IP-szűrési műveletek</span><span class="sxs-lookup"><span data-stu-id="011ab-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="011ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="011ab-119">-DefaultProfile</span></span>
<span data-ttu-id="011ab-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="011ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="011ab-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="011ab-121">-IpMask</span></span>
<span data-ttu-id="011ab-122">Alhálózati erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="011ab-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="011ab-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="011ab-123">-IpRuleObject</span></span>
<span data-ttu-id="011ab-124">Hozzáadni kívánt IPRule-konfigurációs objektum</span><span class="sxs-lookup"><span data-stu-id="011ab-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="011ab-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="011ab-125">-Name</span></span>
<span data-ttu-id="011ab-126">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="011ab-126">Namespace Name</span></span>

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

### <span data-ttu-id="011ab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="011ab-127">-ResourceGroupName</span></span>
<span data-ttu-id="011ab-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="011ab-128">Resource Group Name</span></span>

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

### <span data-ttu-id="011ab-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="011ab-129">-Confirm</span></span>
<span data-ttu-id="011ab-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="011ab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="011ab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="011ab-131">-WhatIf</span></span>
<span data-ttu-id="011ab-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="011ab-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="011ab-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="011ab-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="011ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011ab-134">CommonParameters</span></span>
<span data-ttu-id="011ab-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="011ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="011ab-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="011ab-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011ab-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="011ab-137">INPUTS</span></span>

### <span data-ttu-id="011ab-138">System. String</span><span class="sxs-lookup"><span data-stu-id="011ab-138">System.String</span></span>

### <span data-ttu-id="011ab-139">Microsoft. Azure. Command. EventHub. models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="011ab-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="011ab-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="011ab-140">OUTPUTS</span></span>

### <span data-ttu-id="011ab-141">Microsoft. Azure. Command. EventHub. models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="011ab-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="011ab-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="011ab-142">NOTES</span></span>

## <span data-ttu-id="011ab-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="011ab-143">RELATED LINKS</span></span>
