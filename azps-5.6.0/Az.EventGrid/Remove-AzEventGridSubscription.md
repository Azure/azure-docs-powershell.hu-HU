---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 1625e3325164156b1809640c54d4b75698ae7363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938698"
---
# <span data-ttu-id="12a90-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="12a90-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="12a90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12a90-102">SYNOPSIS</span></span>
<span data-ttu-id="12a90-103">Eltávolít egy Azure Event Grid-esemény-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="12a90-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="12a90-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12a90-104">SYNTAX</span></span>

### <span data-ttu-id="12a90-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12a90-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12a90-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="12a90-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12a90-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12a90-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12a90-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12a90-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12a90-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12a90-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12a90-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12a90-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12a90-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12a90-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12a90-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="12a90-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12a90-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="12a90-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12a90-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12a90-114">DESCRIPTION</span></span>
<span data-ttu-id="12a90-115">Eltávolítja az Azure Event Grid esemény-előfizetését egy Azure Event Grid-témakör, erőforrás, Azure-előfizetés vagy erőforráscsoport esetén.</span><span class="sxs-lookup"><span data-stu-id="12a90-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="12a90-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12a90-116">EXAMPLES</span></span>

### <span data-ttu-id="12a90-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="12a90-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="12a90-118">Eltávolítja az esemény-előfizetés \` EventSubscription1-et \` egy Azure Event Grid \` topic1 témakörbe a \` \` MyResourceGroupName \` erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="12a90-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="12a90-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="12a90-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="12a90-120">Eltávolítja az esemény-előfizetés \` EventSubscription1-et \` egy \` MyResourceGroupName \` erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="12a90-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="12a90-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="12a90-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="12a90-122">Eltávolítja az esemény-előfizetés \` EventSubscription1-et \` az alapértelmezett Azure-előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="12a90-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="12a90-123">4. példa</span><span class="sxs-lookup"><span data-stu-id="12a90-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="12a90-124">Eltávolítja az esemény-előfizetés \` EventSubscription1-et \` az Eseményközpont névteréből.</span><span class="sxs-lookup"><span data-stu-id="12a90-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="12a90-125">5. példa</span><span class="sxs-lookup"><span data-stu-id="12a90-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="12a90-126">Eltávolítja az esemény-előfizetés \` EventSubscription1-et \` egy eseményrácstémára.</span><span class="sxs-lookup"><span data-stu-id="12a90-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="12a90-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12a90-127">PARAMETERS</span></span>

### <span data-ttu-id="12a90-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a90-128">-DefaultProfile</span></span>
<span data-ttu-id="12a90-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="12a90-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12a90-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="12a90-130">-DomainInputObject</span></span>
<span data-ttu-id="12a90-131">EventGrid Domain objektum.</span><span class="sxs-lookup"><span data-stu-id="12a90-131">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="12a90-132">-DomainName</span></span>
<span data-ttu-id="12a90-133">EventGrid tartománynév.</span><span class="sxs-lookup"><span data-stu-id="12a90-133">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="12a90-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="12a90-135">EventGrid domain Topic objektum.</span><span class="sxs-lookup"><span data-stu-id="12a90-135">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="12a90-136">-DomainTopicName</span></span>
<span data-ttu-id="12a90-137">EventGrid tartomány témakörének neve.</span><span class="sxs-lookup"><span data-stu-id="12a90-137">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="12a90-138">-EventSubscriptionName</span></span>
<span data-ttu-id="12a90-139">Az eltávolítható esemény-előfizetés neve.</span><span class="sxs-lookup"><span data-stu-id="12a90-139">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet, DomainNameParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12a90-140">-InputObject</span></span>
<span data-ttu-id="12a90-141">EventGrid Topic objektum.</span><span class="sxs-lookup"><span data-stu-id="12a90-141">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12a90-142">-PassThru</span></span>
<span data-ttu-id="12a90-143">Az Eltávolítás művelet állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="12a90-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="12a90-144">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="12a90-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12a90-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a90-145">-ResourceGroupName</span></span>
<span data-ttu-id="12a90-146">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="12a90-146">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12a90-147">-ResourceId</span></span>
<span data-ttu-id="12a90-148">Annak az erőforrásnak az azonosítója, amelynek az esemény-előfizetését el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="12a90-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="12a90-149">-TopicName</span></span>
<span data-ttu-id="12a90-150">Eseményrács-témakör neve.</span><span class="sxs-lookup"><span data-stu-id="12a90-150">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a90-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12a90-151">-Confirm</span></span>
<span data-ttu-id="12a90-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="12a90-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12a90-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12a90-153">-WhatIf</span></span>
<span data-ttu-id="12a90-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="12a90-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12a90-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12a90-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12a90-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a90-156">CommonParameters</span></span>
<span data-ttu-id="12a90-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a90-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a90-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12a90-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a90-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12a90-159">INPUTS</span></span>

### <span data-ttu-id="12a90-160">System.String</span><span class="sxs-lookup"><span data-stu-id="12a90-160">System.String</span></span>

### <span data-ttu-id="12a90-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="12a90-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="12a90-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="12a90-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="12a90-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="12a90-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="12a90-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12a90-164">OUTPUTS</span></span>

### <span data-ttu-id="12a90-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="12a90-165">System.Boolean</span></span>

## <span data-ttu-id="12a90-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12a90-166">NOTES</span></span>

## <span data-ttu-id="12a90-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12a90-167">RELATED LINKS</span></span>
