---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386916"
---
# <span data-ttu-id="a2522-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a2522-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="a2522-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2522-102">SYNOPSIS</span></span>
<span data-ttu-id="a2522-103">A Megadott névtér NetworkRuleSet-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a2522-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="a2522-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2522-104">SYNTAX</span></span>

### <span data-ttu-id="a2522-105">NetworkRuleSetPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2522-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2522-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2522-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2522-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2522-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2522-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2522-108">DESCRIPTION</span></span>
<span data-ttu-id="a2522-109">A Megadott névtér NetworkRuleSet-ének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a2522-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="a2522-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2522-110">EXAMPLES</span></span>

### <span data-ttu-id="a2522-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a2522-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="a2522-112">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroups/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="a2522-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="a2522-113">Törli a NetworkRuleSet rekordot a Megadott "Eventhub-Namespace1-1375" névtérből</span><span class="sxs-lookup"><span data-stu-id="a2522-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="a2522-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="a2522-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="a2522-115">A NetworkRuleSet törlése az InputObject használatával</span><span class="sxs-lookup"><span data-stu-id="a2522-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="a2522-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="a2522-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="a2522-117">Név: alapértelmezett DefaultAction: Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroups/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="a2522-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="a2522-118">A NetworkRuleSet törlése a Namespace ResourceId (Erőforrásazonosító) használatával</span><span class="sxs-lookup"><span data-stu-id="a2522-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="a2522-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2522-119">PARAMETERS</span></span>

### <span data-ttu-id="a2522-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2522-120">-AsJob</span></span>
<span data-ttu-id="a2522-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a2522-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2522-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2522-122">-DefaultProfile</span></span>
<span data-ttu-id="a2522-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2522-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2522-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2522-124">-InputObject</span></span>
<span data-ttu-id="a2522-125">Namespace objektum</span><span class="sxs-lookup"><span data-stu-id="a2522-125">Namespace Object</span></span>

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

### <span data-ttu-id="a2522-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a2522-126">-Name</span></span>
<span data-ttu-id="a2522-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a2522-127">Namespace Name</span></span>

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

### <span data-ttu-id="a2522-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2522-128">-PassThru</span></span>
<span data-ttu-id="a2522-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a2522-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a2522-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2522-130">-ResourceGroupName</span></span>
<span data-ttu-id="a2522-131">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a2522-131">Resource Group Name</span></span>

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

### <span data-ttu-id="a2522-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2522-132">-ResourceId</span></span>
<span data-ttu-id="a2522-133">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="a2522-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="a2522-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2522-134">-Confirm</span></span>
<span data-ttu-id="a2522-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2522-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2522-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2522-136">-WhatIf</span></span>
<span data-ttu-id="a2522-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2522-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2522-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2522-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2522-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2522-139">CommonParameters</span></span>
<span data-ttu-id="a2522-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2522-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a2522-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2522-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2522-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2522-142">INPUTS</span></span>

### <span data-ttu-id="a2522-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a2522-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="a2522-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a2522-144">System.String</span></span>

## <span data-ttu-id="a2522-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2522-145">OUTPUTS</span></span>

### <span data-ttu-id="a2522-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2522-146">System.Boolean</span></span>

## <span data-ttu-id="a2522-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2522-147">NOTES</span></span>

## <span data-ttu-id="a2522-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2522-148">RELATED LINKS</span></span>