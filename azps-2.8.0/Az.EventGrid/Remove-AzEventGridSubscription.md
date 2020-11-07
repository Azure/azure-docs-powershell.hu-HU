---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 2e2abe03d0df4ccf662f99945c45e837669a1de9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666512"
---
# <span data-ttu-id="83f8b-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="83f8b-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="83f8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="83f8b-103">Azure Event Grid esemény-előfizetés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="83f8b-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="83f8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83f8b-104">SYNTAX</span></span>

### <span data-ttu-id="83f8b-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83f8b-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f8b-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="83f8b-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f8b-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83f8b-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f8b-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83f8b-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f8b-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83f8b-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f8b-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="83f8b-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83f8b-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="83f8b-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f8b-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="83f8b-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f8b-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="83f8b-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83f8b-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="83f8b-114">DESCRIPTION</span></span>
<span data-ttu-id="83f8b-115">Azure Event Grid-eseményre szóló előfizetés eltávolítása az Azure-esemény rácsvonalai témához, erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="83f8b-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="83f8b-116">Példák</span><span class="sxs-lookup"><span data-stu-id="83f8b-116">EXAMPLES</span></span>

### <span data-ttu-id="83f8b-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="83f8b-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="83f8b-118">Eltávolítja az esemény-előfizetést az \` \` Azure-esemény EventSubscription1 az \` \` erőforráscsoport- \` MyResourceGroupName téma1 \` .</span><span class="sxs-lookup"><span data-stu-id="83f8b-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="83f8b-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="83f8b-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="83f8b-120">Eltávolítja az esemény-előfizetést \` EventSubscription1 \` egy erőforráscsoport- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="83f8b-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="83f8b-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="83f8b-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="83f8b-122">Eltávolítja az esemény-előfizetést \` \` az alapértelmezett Azure-előfizetésre EventSubscription1.</span><span class="sxs-lookup"><span data-stu-id="83f8b-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="83f8b-123">4. példa</span><span class="sxs-lookup"><span data-stu-id="83f8b-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="83f8b-124">Eltávolítja az esemény-előfizetési \` EventSubscription1 az \` esemény-hub-névtérbe.</span><span class="sxs-lookup"><span data-stu-id="83f8b-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="83f8b-125">Példa 5</span><span class="sxs-lookup"><span data-stu-id="83f8b-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="83f8b-126">Eltávolítja az esemény-előfizetést az \` EventSubscription1 \` -témára.</span><span class="sxs-lookup"><span data-stu-id="83f8b-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="83f8b-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83f8b-127">PARAMETERS</span></span>

### <span data-ttu-id="83f8b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f8b-128">-DefaultProfile</span></span>
<span data-ttu-id="83f8b-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="83f8b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83f8b-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="83f8b-130">-DomainInputObject</span></span>
<span data-ttu-id="83f8b-131">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="83f8b-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="83f8b-132">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="83f8b-132">-DomainName</span></span>
<span data-ttu-id="83f8b-133">EventGrid-tartomány neve.</span><span class="sxs-lookup"><span data-stu-id="83f8b-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="83f8b-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="83f8b-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="83f8b-135">EventGrid objektum</span><span class="sxs-lookup"><span data-stu-id="83f8b-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="83f8b-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="83f8b-136">-DomainTopicName</span></span>
<span data-ttu-id="83f8b-137">EventGrid a tartomány témájának nevét.</span><span class="sxs-lookup"><span data-stu-id="83f8b-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="83f8b-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="83f8b-138">-EventSubscriptionName</span></span>
<span data-ttu-id="83f8b-139">Annak az esemény-előfizetésnek a neve, amelyet el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="83f8b-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="83f8b-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83f8b-140">-InputObject</span></span>
<span data-ttu-id="83f8b-141">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="83f8b-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="83f8b-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83f8b-142">-PassThru</span></span>
<span data-ttu-id="83f8b-143">Az eltávolítási művelet állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="83f8b-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="83f8b-144">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="83f8b-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83f8b-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f8b-145">-ResourceGroupName</span></span>
<span data-ttu-id="83f8b-146">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="83f8b-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="83f8b-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83f8b-147">-ResourceId</span></span>
<span data-ttu-id="83f8b-148">Annak az erőforrásnak az azonosítója, akinek az esemény-előfizetését el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="83f8b-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="83f8b-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="83f8b-149">-TopicName</span></span>
<span data-ttu-id="83f8b-150">Az esemény rácsvonala téma neve.</span><span class="sxs-lookup"><span data-stu-id="83f8b-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="83f8b-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83f8b-151">-Confirm</span></span>
<span data-ttu-id="83f8b-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83f8b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f8b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f8b-153">-WhatIf</span></span>
<span data-ttu-id="83f8b-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83f8b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83f8b-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83f8b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f8b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f8b-156">CommonParameters</span></span>
<span data-ttu-id="83f8b-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83f8b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f8b-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83f8b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f8b-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83f8b-159">INPUTS</span></span>

### <span data-ttu-id="83f8b-160">System. String</span><span class="sxs-lookup"><span data-stu-id="83f8b-160">System.String</span></span>

### <span data-ttu-id="83f8b-161">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="83f8b-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="83f8b-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="83f8b-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="83f8b-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="83f8b-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="83f8b-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83f8b-164">OUTPUTS</span></span>

### <span data-ttu-id="83f8b-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83f8b-165">System.Boolean</span></span>

## <span data-ttu-id="83f8b-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83f8b-166">NOTES</span></span>

## <span data-ttu-id="83f8b-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83f8b-167">RELATED LINKS</span></span>
