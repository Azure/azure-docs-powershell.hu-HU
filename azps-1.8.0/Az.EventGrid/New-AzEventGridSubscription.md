---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 1c0391fa266e498c717bc4eb43bd92ab93be508f
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395186"
---
# <span data-ttu-id="86783-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="86783-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="86783-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86783-102">SYNOPSIS</span></span>
<span data-ttu-id="86783-103">Új Azure-esemény-előfizetést hoz létre egy témakörhöz, Azure-erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="86783-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="86783-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86783-104">SYNTAX</span></span>

### <span data-ttu-id="86783-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86783-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86783-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="86783-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86783-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86783-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86783-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="86783-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86783-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="86783-109">DESCRIPTION</span></span>
<span data-ttu-id="86783-110">Új esemény-előfizetés létrehozása Azure-esemény rácsához, támogatott Azure-erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="86783-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="86783-111">Ha az aktuálisan kiválasztott Azure-előfizetéshez szeretne esemény-előfizetést létrehozni, adja meg az esemény-előfizetés nevét és a cél végpontját.</span><span class="sxs-lookup"><span data-stu-id="86783-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="86783-112">Ha eseményvezérelt előfizetést szeretne létrehozni egy erőforrás-csoporthoz, az esemény-előfizetés neve és a cél végpont mellett adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="86783-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="86783-113">Ha eseményvezérelt előfizetést szeretne létrehozni az Azure-esemény rácsához, adja meg a téma nevét is.</span><span class="sxs-lookup"><span data-stu-id="86783-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="86783-114">Ha egy támogatott Azure-erőforráshoz szeretne esemény-előfizetést létrehozni, adja meg az erőforrás teljes erőforrás-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="86783-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="86783-115">A támogatott típusok listájának megtekintéséhez futtassa az Get-AzEventGridTopicType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="86783-115">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="86783-116">Példák</span><span class="sxs-lookup"><span data-stu-id="86783-116">EXAMPLES</span></span>

### <span data-ttu-id="86783-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="86783-117">Example 1</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="86783-118">Új esemény-előfizetést hoz létre az \` \` Azure EventSubscription1 \` -témakör téma1 az \` erőforráscsoport \` MyResourceGroupName \` a webhook Destination végponttal `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="86783-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="86783-119">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="86783-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="86783-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="86783-120">Example 2</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="86783-121">Új esemény-előfizetési \` EventSubscription1 hoz létre \` egy erőforráscsoport \` MyResourceGroupName \` a webhook-cél végponttal `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="86783-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="86783-122">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="86783-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="86783-123">3. példa</span><span class="sxs-lookup"><span data-stu-id="86783-123">Example 3</span></span>
```
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="86783-124">Új esemény-előfizetést hoz létre \` \` az aktuálisan kijelölt Azure-előfizetéshez a EventSubscription1 végponttal `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="86783-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="86783-125">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="86783-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="86783-126">4. példa</span><span class="sxs-lookup"><span data-stu-id="86783-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="86783-127">Új esemény-előfizetést hoz létre \` \` az aktuálisan kijelölt Azure-előfizetéshez a EventSubscription1 végponttal `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="86783-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="86783-128">Ez az esemény-előfizetés adja meg az eseménytípus és a tárgy további szűrőit, és csak az adott szűrővel egyező eseményeket kézbesíti a program a cél végpontra.</span><span class="sxs-lookup"><span data-stu-id="86783-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="86783-129">Példa 5</span><span class="sxs-lookup"><span data-stu-id="86783-129">Example 5</span></span>
```
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="86783-130">Új esemény-előfizetést hoz létre az \` \` aktuálisan kijelölt Azure-előfizetéshez, a megadott EventSubscription1 az események céljára.</span><span class="sxs-lookup"><span data-stu-id="86783-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="86783-131">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="86783-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="86783-132">6. példa</span><span class="sxs-lookup"><span data-stu-id="86783-132">Example 6</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="86783-133">Új esemény-előfizetési \` EventSubscription1 \` hoz létre egy EventHub-névtérhez a megadott webhook-cél végponttal `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="86783-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="86783-134">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="86783-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="86783-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86783-135">PARAMETERS</span></span>

### <span data-ttu-id="86783-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="86783-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="86783-137">A kézbesítetlen események tárolásához használt végpont.</span><span class="sxs-lookup"><span data-stu-id="86783-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="86783-138">Adja meg egy tároló blob-tároló Azure Resource ID azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="86783-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="86783-139">Például:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="86783-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86783-140">-DefaultProfile</span></span>
<span data-ttu-id="86783-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="86783-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86783-142">-Végpont</span><span class="sxs-lookup"><span data-stu-id="86783-142">-Endpoint</span></span>
<span data-ttu-id="86783-143">Esemény-előfizetés cél végpontja.</span><span class="sxs-lookup"><span data-stu-id="86783-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="86783-144">Ez lehet egy webhorog URL-címe, vagy egy EventHub, tárolási várólista vagy hybridconnection Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="86783-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="86783-145">A hibrid kapcsolat erőforrás-azonosítója például a következő:/Subscriptions/[Azure előfizetés-azonosító]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="86783-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="86783-146">Az esemény rácsos parancsmagjai elvégzése előtt várhatóan létrejön a cél végpont, és elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="86783-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="86783-147">-EndpointType</span></span>
<span data-ttu-id="86783-148">Végpont típusa.</span><span class="sxs-lookup"><span data-stu-id="86783-148">Endpoint Type.</span></span>
<span data-ttu-id="86783-149">Ez lehet a webhook, a eventhub, a storagequeue vagy a hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="86783-149">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="86783-150">Az alapértelmezett érték a webhook.</span><span class="sxs-lookup"><span data-stu-id="86783-150">Default value is webhook.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="86783-151">-EventSubscriptionName</span></span>
<span data-ttu-id="86783-152">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="86783-152">The name of the event subscription</span></span>

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

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="86783-153">-EventTtl</span></span>
<span data-ttu-id="86783-154">Az esemény kézbesítésének időpontja percben.</span><span class="sxs-lookup"><span data-stu-id="86783-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="86783-155">Ennek az értéknek 1 és 1440 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="86783-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-156">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="86783-156">-IncludedEventType</span></span>
<span data-ttu-id="86783-157">Szűrő, amely a szerepeltetni kívánt eseménytípus listáját adja meg. Ha nincs megadva, az összes eseménytípus szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="86783-157">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86783-158">-InputObject</span></span>
<span data-ttu-id="86783-159">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="86783-159">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="86783-160">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="86783-160">-Label</span></span>
<span data-ttu-id="86783-161">Az esemény-előfizetés címkéi</span><span class="sxs-lookup"><span data-stu-id="86783-161">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-162">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="86783-162">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="86783-163">Az esemény kézbesítésének maximális száma.</span><span class="sxs-lookup"><span data-stu-id="86783-163">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="86783-164">Ennek az értéknek 1 és 30 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="86783-164">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86783-165">-ResourceGroupName</span></span>
<span data-ttu-id="86783-166">A témakör erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="86783-166">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86783-167">-ResourceId</span></span>
<span data-ttu-id="86783-168">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="86783-168">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="86783-169">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="86783-169">-SubjectBeginsWith</span></span>
<span data-ttu-id="86783-170">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi előtaghoz tartozó eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="86783-170">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="86783-171">Ha nem adja meg, akkor az összes tárgy előtagokkal rendelkező események is szerepelni fognak.</span><span class="sxs-lookup"><span data-stu-id="86783-171">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-172">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="86783-172">-SubjectCaseSensitive</span></span>
<span data-ttu-id="86783-173">Szűrő: azt adja meg, hogy a tárgy mezőt a kis-és nagybetűk megkülönböztetésével kell összehasonlítani.</span><span class="sxs-lookup"><span data-stu-id="86783-173">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="86783-174">Ha nem adja meg, a program a tárgyat a kis-és nagybetűk megkülönböztetésével hasonlítja össze.</span><span class="sxs-lookup"><span data-stu-id="86783-174">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="86783-175">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="86783-175">-SubjectEndsWith</span></span>
<span data-ttu-id="86783-176">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi utótaggal egyező eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="86783-176">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="86783-177">Ha nem adja meg, a program az összes tárgyi utótaggal rendelkező eseményeket is belefoglalja.</span><span class="sxs-lookup"><span data-stu-id="86783-177">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-178">-TopicName</span><span class="sxs-lookup"><span data-stu-id="86783-178">-TopicName</span></span>
<span data-ttu-id="86783-179">Annak a témakörnek a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="86783-179">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86783-180">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86783-180">-Confirm</span></span>
<span data-ttu-id="86783-181">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86783-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86783-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86783-182">-WhatIf</span></span>
<span data-ttu-id="86783-183">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86783-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86783-184">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86783-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86783-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86783-185">CommonParameters</span></span>
<span data-ttu-id="86783-186">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86783-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86783-187">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86783-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86783-188">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86783-188">INPUTS</span></span>

### <span data-ttu-id="86783-189">System. String</span><span class="sxs-lookup"><span data-stu-id="86783-189">System.String</span></span>

### <span data-ttu-id="86783-190">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="86783-190">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="86783-191">System. string []</span><span class="sxs-lookup"><span data-stu-id="86783-191">System.String[]</span></span>

## <span data-ttu-id="86783-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86783-192">OUTPUTS</span></span>

### <span data-ttu-id="86783-193">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="86783-193">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="86783-194">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86783-194">NOTES</span></span>

## <span data-ttu-id="86783-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86783-195">RELATED LINKS</span></span>
