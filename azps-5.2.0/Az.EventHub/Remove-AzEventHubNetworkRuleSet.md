---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329261"
---
# <span data-ttu-id="79f65-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="79f65-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="79f65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79f65-102">SYNOPSIS</span></span>
<span data-ttu-id="79f65-103">A Megadott névtér NetworkRuleSet-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="79f65-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="79f65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79f65-104">SYNTAX</span></span>

### <span data-ttu-id="79f65-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79f65-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79f65-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="79f65-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79f65-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79f65-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79f65-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79f65-108">DESCRIPTION</span></span>
<span data-ttu-id="79f65-109">A Megadott névtér NetworkRuleSet-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="79f65-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="79f65-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79f65-110">EXAMPLES</span></span>

### <span data-ttu-id="79f65-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="79f65-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="79f65-112">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroups/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="79f65-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="79f65-113">Törli a NetworkRuleSet rekordot a Megadott "Eventhub-Namespace1-1375" névtérből</span><span class="sxs-lookup"><span data-stu-id="79f65-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="79f65-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="79f65-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="79f65-115">A NetworkRuleSet törlése az InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="79f65-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="79f65-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="79f65-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="79f65-117">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroups/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="79f65-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="79f65-118">A NetworkRuleSet törlése a Namespace ResourceId (Erőforrásazonosító) használatával</span><span class="sxs-lookup"><span data-stu-id="79f65-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="79f65-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79f65-119">PARAMETERS</span></span>

### <span data-ttu-id="79f65-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79f65-120">-AsJob</span></span>
<span data-ttu-id="79f65-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="79f65-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79f65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f65-122">-DefaultProfile</span></span>
<span data-ttu-id="79f65-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79f65-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79f65-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79f65-124">-InputObject</span></span>
<span data-ttu-id="79f65-125">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="79f65-125">Namespace Object</span></span>

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

### <span data-ttu-id="79f65-126">-Name</span><span class="sxs-lookup"><span data-stu-id="79f65-126">-Name</span></span>
<span data-ttu-id="79f65-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="79f65-127">Namespace Name</span></span>

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

### <span data-ttu-id="79f65-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79f65-128">-PassThru</span></span>
<span data-ttu-id="79f65-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="79f65-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="79f65-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f65-130">-ResourceGroupName</span></span>
<span data-ttu-id="79f65-131">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="79f65-131">Resource Group Name</span></span>

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

### <span data-ttu-id="79f65-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79f65-132">-ResourceId</span></span>
<span data-ttu-id="79f65-133">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="79f65-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="79f65-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79f65-134">-Confirm</span></span>
<span data-ttu-id="79f65-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="79f65-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79f65-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79f65-136">-WhatIf</span></span>
<span data-ttu-id="79f65-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="79f65-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79f65-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79f65-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79f65-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f65-139">CommonParameters</span></span>
<span data-ttu-id="79f65-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f65-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="79f65-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f65-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f65-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79f65-142">INPUTS</span></span>

### <span data-ttu-id="79f65-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="79f65-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="79f65-144">System.String</span><span class="sxs-lookup"><span data-stu-id="79f65-144">System.String</span></span>

## <span data-ttu-id="79f65-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79f65-145">OUTPUTS</span></span>

### <span data-ttu-id="79f65-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79f65-146">System.Boolean</span></span>

## <span data-ttu-id="79f65-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79f65-147">NOTES</span></span>

## <span data-ttu-id="79f65-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79f65-148">RELATED LINKS</span></span>