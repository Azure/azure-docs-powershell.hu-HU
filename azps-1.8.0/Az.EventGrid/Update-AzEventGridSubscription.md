---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: a5aee2c8df132a4218ece171453e04d1224f7adc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670862"
---
# <span data-ttu-id="68fab-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="68fab-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="68fab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68fab-102">SYNOPSIS</span></span>
<span data-ttu-id="68fab-103">Az esemény rácsa esemény-előfizetés tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="68fab-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="68fab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68fab-104">SYNTAX</span></span>

### <span data-ttu-id="68fab-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="68fab-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68fab-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="68fab-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68fab-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68fab-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68fab-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="68fab-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68fab-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="68fab-109">DESCRIPTION</span></span>
<span data-ttu-id="68fab-110">Az esemény rácsa esemény-előfizetés tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="68fab-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="68fab-111">Ez a funkció a meglévő esemény-előfizetések szűrő, cél vagy címkék frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="68fab-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="68fab-112">Példák</span><span class="sxs-lookup"><span data-stu-id="68fab-112">EXAMPLES</span></span>

### <span data-ttu-id="68fab-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="68fab-113">Example 1</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="68fab-114">Frissíti az esemény-előfizetési ES1 végpontját a \` \` témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="68fab-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="68fab-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="68fab-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="68fab-116">Frissíti az esemény-előfizetési ES1 végpontját a \` \` témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="68fab-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="68fab-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="68fab-117">Example 3</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="68fab-118">A \` \` EventHub-névtér ContosoNamespace az új végponttal \` https://requestb.in/1kxxoui1\ "és az új SubjectEndsWith-szűrő jpg-ként" ES1 frissíti az esemény-előfizetés tulajdonságait. \`\`</span><span class="sxs-lookup"><span data-stu-id="68fab-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="68fab-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="68fab-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="68fab-120">Frissíti az erőforráscsoport MyResourceGroupName tartozó esemény-előfizetési \` ES1 tulajdonságait \` \` \` az új címkék $labels.</span><span class="sxs-lookup"><span data-stu-id="68fab-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="68fab-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68fab-121">PARAMETERS</span></span>

### <span data-ttu-id="68fab-122">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="68fab-122">-DeadLetterEndpoint</span></span>
<span data-ttu-id="68fab-123">A kézbesítetlen események tárolásához használt végpont.</span><span class="sxs-lookup"><span data-stu-id="68fab-123">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="68fab-124">Adja meg egy tároló blob-tároló Azure Resource ID azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="68fab-124">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="68fab-125">Például:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="68fab-125">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fab-126">-DefaultProfile</span></span>
<span data-ttu-id="68fab-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68fab-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68fab-128">-Végpont</span><span class="sxs-lookup"><span data-stu-id="68fab-128">-Endpoint</span></span>
<span data-ttu-id="68fab-129">Esemény-előfizetés cél végpontja.</span><span class="sxs-lookup"><span data-stu-id="68fab-129">Event subscription destination endpoint.</span></span>
<span data-ttu-id="68fab-130">Ez lehet egy webhorog URL-címe, vagy egy EventHub, tárolási várólista vagy hybridconnection Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="68fab-130">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="68fab-131">A hibrid kapcsolat erőforrás-azonosítója például a következő:/Subscriptions/[Azure előfizetés-azonosító]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="68fab-131">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="68fab-132">Az esemény rácsos parancsmagjai elvégzése előtt várhatóan létrejön a cél végpont, és elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="68fab-132">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-133">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="68fab-133">-EndpointType</span></span>
<span data-ttu-id="68fab-134">Végpont típusa.</span><span class="sxs-lookup"><span data-stu-id="68fab-134">Endpoint Type.</span></span>
<span data-ttu-id="68fab-135">Ez lehet a webhook, a eventhub, a storagequeue vagy a hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="68fab-135">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="68fab-136">Az alapértelmezett érték a webhook.</span><span class="sxs-lookup"><span data-stu-id="68fab-136">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="68fab-137">-EventSubscriptionName</span></span>
<span data-ttu-id="68fab-138">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="68fab-138">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-139">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="68fab-139">-EventTtl</span></span>
<span data-ttu-id="68fab-140">Az esemény kézbesítésének időpontja percben.</span><span class="sxs-lookup"><span data-stu-id="68fab-140">The time in minutes for the event delivery.</span></span> <span data-ttu-id="68fab-141">Ennek az értéknek 1 és 1440 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="68fab-141">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-142">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="68fab-142">-IncludedEventType</span></span>
<span data-ttu-id="68fab-143">Szűrő, amely a szerepeltetni kívánt eseménytípus listáját adja meg. Ha nincs megadva, az összes eseménytípus szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="68fab-143">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68fab-144">-InputObject</span></span>
<span data-ttu-id="68fab-145">EventGridSubscription objektum</span><span class="sxs-lookup"><span data-stu-id="68fab-145">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-146">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="68fab-146">-Label</span></span>
<span data-ttu-id="68fab-147">Az esemény-előfizetés címkéi</span><span class="sxs-lookup"><span data-stu-id="68fab-147">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-148">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="68fab-148">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="68fab-149">Az esemény kézbesítésének maximális száma.</span><span class="sxs-lookup"><span data-stu-id="68fab-149">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="68fab-150">Ennek az értéknek 1 és 30 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="68fab-150">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68fab-151">-ResourceGroupName</span></span>
<span data-ttu-id="68fab-152">A témakör erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="68fab-152">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68fab-153">-ResourceId</span></span>
<span data-ttu-id="68fab-154">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetést létrehozták.</span><span class="sxs-lookup"><span data-stu-id="68fab-154">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="68fab-155">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="68fab-155">-SubjectBeginsWith</span></span>
<span data-ttu-id="68fab-156">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi előtaghoz tartozó eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="68fab-156">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="68fab-157">Ha nem adja meg, akkor az összes tárgy előtagokkal rendelkező események is szerepelni fognak.</span><span class="sxs-lookup"><span data-stu-id="68fab-157">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-158">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="68fab-158">-SubjectEndsWith</span></span>
<span data-ttu-id="68fab-159">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi utótaggal egyező eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="68fab-159">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="68fab-160">Ha nem adja meg, a program az összes tárgyi utótaggal rendelkező eseményeket is belefoglalja.</span><span class="sxs-lookup"><span data-stu-id="68fab-160">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-161">-TopicName</span><span class="sxs-lookup"><span data-stu-id="68fab-161">-TopicName</span></span>
<span data-ttu-id="68fab-162">Annak a témakörnek a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="68fab-162">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68fab-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68fab-163">-Confirm</span></span>
<span data-ttu-id="68fab-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68fab-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68fab-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68fab-165">-WhatIf</span></span>
<span data-ttu-id="68fab-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68fab-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68fab-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68fab-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68fab-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fab-168">CommonParameters</span></span>
<span data-ttu-id="68fab-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68fab-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fab-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68fab-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fab-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68fab-171">INPUTS</span></span>

### <span data-ttu-id="68fab-172">System. String</span><span class="sxs-lookup"><span data-stu-id="68fab-172">System.String</span></span>

### <span data-ttu-id="68fab-173">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="68fab-173">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="68fab-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68fab-174">OUTPUTS</span></span>

### <span data-ttu-id="68fab-175">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="68fab-175">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="68fab-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68fab-176">NOTES</span></span>

## <span data-ttu-id="68fab-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68fab-177">RELATED LINKS</span></span>
