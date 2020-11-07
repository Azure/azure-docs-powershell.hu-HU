---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: ca404636f58eb3f4b4037ec05ab1822eb00b17ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666523"
---
# <span data-ttu-id="5ac29-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5ac29-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="5ac29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ac29-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac29-103">Új Azure-esemény-előfizetést hoz létre egy témakörhöz, Azure-erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5ac29-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="5ac29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ac29-104">SYNTAX</span></span>

### <span data-ttu-id="5ac29-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ac29-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ac29-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ac29-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ac29-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ac29-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ac29-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ac29-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ac29-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ac29-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ac29-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ac29-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ac29-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ac29-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ac29-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ac29-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ac29-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ac29-113">DESCRIPTION</span></span>
<span data-ttu-id="5ac29-114">Új esemény-előfizetés létrehozása Azure-esemény rácsához, támogatott Azure-erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5ac29-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="5ac29-115">Ha az aktuálisan kiválasztott Azure-előfizetéshez szeretne esemény-előfizetést létrehozni, adja meg az esemény-előfizetés nevét és a cél végpontját.</span><span class="sxs-lookup"><span data-stu-id="5ac29-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="5ac29-116">Ha eseményvezérelt előfizetést szeretne létrehozni egy erőforrás-csoporthoz, az esemény-előfizetés neve és a cél végpont mellett adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="5ac29-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="5ac29-117">Ha eseményvezérelt előfizetést szeretne létrehozni az Azure-esemény rácsához, adja meg a téma nevét is.</span><span class="sxs-lookup"><span data-stu-id="5ac29-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="5ac29-118">Ha egy támogatott Azure-erőforráshoz szeretne esemény-előfizetést létrehozni, adja meg az erőforrás teljes erőforrás-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="5ac29-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="5ac29-119">A támogatott típusok listájának megtekintéséhez futtassa az Get-AzEventGridTopicType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5ac29-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="5ac29-120">Példák</span><span class="sxs-lookup"><span data-stu-id="5ac29-120">EXAMPLES</span></span>

### <span data-ttu-id="5ac29-121">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5ac29-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5ac29-122">Új esemény-előfizetést hoz létre az \` \` Azure EventSubscription1 \` -témakör téma1 az \` erőforráscsoport \` MyResourceGroupName \` a webhook Destination végponttal https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="5ac29-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="5ac29-123">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="5ac29-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="5ac29-124">2. példa</span><span class="sxs-lookup"><span data-stu-id="5ac29-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5ac29-125">Új esemény-előfizetési \` EventSubscription1 hoz létre \` egy erőforráscsoport \` MyResourceGroupName \` a webhook-cél végponttal https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="5ac29-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="5ac29-126">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="5ac29-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="5ac29-127">3. példa</span><span class="sxs-lookup"><span data-stu-id="5ac29-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5ac29-128">Új esemény-előfizetést hoz létre \` \` az aktuálisan kijelölt Azure-előfizetéshez a EventSubscription1 végponttal https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="5ac29-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="5ac29-129">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="5ac29-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="5ac29-130">4. példa</span><span class="sxs-lookup"><span data-stu-id="5ac29-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="5ac29-131">Új esemény-előfizetést hoz létre \` \` az aktuálisan kijelölt Azure-előfizetéshez a EventSubscription1 végponttal https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="5ac29-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="5ac29-132">Ez az esemény-előfizetés adja meg az eseménytípus és a tárgy további szűrőit, és csak az adott szűrővel egyező eseményeket kézbesíti a program a cél végpontra.</span><span class="sxs-lookup"><span data-stu-id="5ac29-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="5ac29-133">Példa 5</span><span class="sxs-lookup"><span data-stu-id="5ac29-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="5ac29-134">Új esemény-előfizetést hoz létre az \` \` aktuálisan kijelölt Azure-előfizetéshez, a megadott EventSubscription1 az események céljára.</span><span class="sxs-lookup"><span data-stu-id="5ac29-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="5ac29-135">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="5ac29-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="5ac29-136">6. példa</span><span class="sxs-lookup"><span data-stu-id="5ac29-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5ac29-137">Új esemény-előfizetési \` EventSubscription1 \` hoz létre egy EventHub-névtérhez a megadott webhook-cél végponttal https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="5ac29-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="5ac29-138">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="5ac29-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="5ac29-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ac29-139">PARAMETERS</span></span>

### <span data-ttu-id="5ac29-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="5ac29-140">-AdvancedFilter</span></span>
<span data-ttu-id="5ac29-141">Speciális szűrő, amely az attribútum-alapú szűréshez használt több Hashtable-érték tömböját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ac29-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="5ac29-142">Minden Hashtable-értékhez tartozik az alábbi kulcsok-érték adatok: művelet, kulcs és érték vagy értékek.</span><span class="sxs-lookup"><span data-stu-id="5ac29-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="5ac29-143">Az operátor az alábbi értékek egyike lehet: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith, StringContains vagy.</span><span class="sxs-lookup"><span data-stu-id="5ac29-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="5ac29-144">A kulcs azt a hasznos tulajdonságot jelenti, amelyben a speciális szűrési házirendek érvényesülnek.</span><span class="sxs-lookup"><span data-stu-id="5ac29-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="5ac29-145">Végül az érték vagy az értékek az egyeztetni kívánt értékek értékét vagy halmazát jelentik.</span><span class="sxs-lookup"><span data-stu-id="5ac29-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="5ac29-146">Ez a megfelelő típusú vagy értékek tömbje lehet egyetlen érték.</span><span class="sxs-lookup"><span data-stu-id="5ac29-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="5ac29-147">Példaként a speciális szűrő paraméterek: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), ahol $AdvFilter 1 = @ {Operator = "NumberIn"; Key = "Data. Key1"; Values = @ (1; 2)} és $AdvFilter 2 = @ {operátor = "StringBringsWith"; Key = "subject"; Values = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="5ac29-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-148">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ac29-148">-DeadLetterEndpoint</span></span>
<span data-ttu-id="5ac29-149">A kézbesítetlen események tárolásához használt végpont.</span><span class="sxs-lookup"><span data-stu-id="5ac29-149">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="5ac29-150">Adja meg egy tároló blob-tároló Azure Resource ID azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="5ac29-150">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="5ac29-151">Például:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="5ac29-151">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac29-152">-DefaultProfile</span></span>
<span data-ttu-id="5ac29-153">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5ac29-153">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ac29-154">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="5ac29-154">-DomainInputObject</span></span>
<span data-ttu-id="5ac29-155">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="5ac29-155">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="5ac29-156">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="5ac29-156">-DomainName</span></span>
<span data-ttu-id="5ac29-157">Annak az eseménynek a rácsnak a neve, amelyre az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="5ac29-157">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-158">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="5ac29-158">-DomainTopicInputObject</span></span>
<span data-ttu-id="5ac29-159">EventGrid objektum</span><span class="sxs-lookup"><span data-stu-id="5ac29-159">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="5ac29-160">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="5ac29-160">-DomainTopicName</span></span>
<span data-ttu-id="5ac29-161">Annak a tartománynak a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="5ac29-161">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-162">-Végpont</span><span class="sxs-lookup"><span data-stu-id="5ac29-162">-Endpoint</span></span>
<span data-ttu-id="5ac29-163">Esemény-előfizetés cél végpontja.</span><span class="sxs-lookup"><span data-stu-id="5ac29-163">Event subscription destination endpoint.</span></span>
<span data-ttu-id="5ac29-164">Ez lehet egy webhorog URL-címe, vagy egy EventHub, tárolási várólista, hybridconnection vagy servicebusqueue Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5ac29-164">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="5ac29-165">A hibrid kapcsolat erőforrás-azonosítója például a következő:/Subscriptions/[Azure előfizetés-azonosító]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="5ac29-165">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="5ac29-166">Az esemény rácsos parancsmagjai elvégzése előtt várhatóan létrejön a cél végpont, és elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="5ac29-166">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-167">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="5ac29-167">-EndpointType</span></span>
<span data-ttu-id="5ac29-168">Végpont típusa.</span><span class="sxs-lookup"><span data-stu-id="5ac29-168">Endpoint Type.</span></span>
<span data-ttu-id="5ac29-169">Ez lehet webhook, eventhub, storagequeue, hybridconnection vagy servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="5ac29-169">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="5ac29-170">Az alapértelmezett érték a webhook.</span><span class="sxs-lookup"><span data-stu-id="5ac29-170">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-171">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5ac29-171">-EventSubscriptionName</span></span>
<span data-ttu-id="5ac29-172">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="5ac29-172">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
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

### <span data-ttu-id="5ac29-173">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="5ac29-173">-EventTtl</span></span>
<span data-ttu-id="5ac29-174">Az esemény kézbesítésének időpontja percben.</span><span class="sxs-lookup"><span data-stu-id="5ac29-174">The time in minutes for the event delivery.</span></span> <span data-ttu-id="5ac29-175">Ennek az értéknek 1 és 1440 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="5ac29-175">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-176">-Lejáratidátum</span><span class="sxs-lookup"><span data-stu-id="5ac29-176">-ExpirationDate</span></span>
<span data-ttu-id="5ac29-177">Meghatározza annak az esemény-előfizetésnek az elévülési idejét, amely után az esemény előfizetése nyugdíjba kerül.</span><span class="sxs-lookup"><span data-stu-id="5ac29-177">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-178">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="5ac29-178">-IncludedEventType</span></span>
<span data-ttu-id="5ac29-179">Szűrő, amely a szerepeltetni kívánt eseménytípus listáját adja meg. Ha nincs megadva, az összes eseménytípus szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="5ac29-179">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ac29-180">-InputObject</span></span>
<span data-ttu-id="5ac29-181">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="5ac29-181">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="5ac29-182">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="5ac29-182">-Label</span></span>
<span data-ttu-id="5ac29-183">Az esemény-előfizetés címkéi</span><span class="sxs-lookup"><span data-stu-id="5ac29-183">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-184">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="5ac29-184">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="5ac29-185">Az esemény kézbesítésének maximális száma.</span><span class="sxs-lookup"><span data-stu-id="5ac29-185">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="5ac29-186">Ennek az értéknek 1 és 30 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="5ac29-186">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-187">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac29-187">-ResourceGroupName</span></span>
<span data-ttu-id="5ac29-188">A témakör erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="5ac29-188">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-189">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ac29-189">-ResourceId</span></span>
<span data-ttu-id="5ac29-190">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="5ac29-190">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="5ac29-191">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="5ac29-191">-SubjectBeginsWith</span></span>
<span data-ttu-id="5ac29-192">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi előtaghoz tartozó eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="5ac29-192">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="5ac29-193">Ha nem adja meg, akkor az összes tárgy előtagokkal rendelkező események is szerepelni fognak.</span><span class="sxs-lookup"><span data-stu-id="5ac29-193">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-194">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="5ac29-194">-SubjectCaseSensitive</span></span>
<span data-ttu-id="5ac29-195">Szűrő: azt adja meg, hogy a tárgy mezőt a kis-és nagybetűk megkülönböztetésével kell összehasonlítani.</span><span class="sxs-lookup"><span data-stu-id="5ac29-195">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="5ac29-196">Ha nem adja meg, a program a tárgyat a kis-és nagybetűk megkülönböztetésével hasonlítja össze.</span><span class="sxs-lookup"><span data-stu-id="5ac29-196">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="5ac29-197">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="5ac29-197">-SubjectEndsWith</span></span>
<span data-ttu-id="5ac29-198">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi utótaggal egyező eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="5ac29-198">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="5ac29-199">Ha nem adja meg, a program az összes tárgyi utótaggal rendelkező eseményeket is belefoglalja.</span><span class="sxs-lookup"><span data-stu-id="5ac29-199">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac29-200">-TopicName</span><span class="sxs-lookup"><span data-stu-id="5ac29-200">-TopicName</span></span>
<span data-ttu-id="5ac29-201">Annak a témakörnek a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="5ac29-201">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="5ac29-202">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ac29-202">-Confirm</span></span>
<span data-ttu-id="5ac29-203">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ac29-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac29-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac29-204">-WhatIf</span></span>
<span data-ttu-id="5ac29-205">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ac29-205">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ac29-206">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ac29-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ac29-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac29-207">CommonParameters</span></span>
<span data-ttu-id="5ac29-208">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ac29-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac29-209">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac29-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac29-210">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac29-210">INPUTS</span></span>

### <span data-ttu-id="5ac29-211">System. String</span><span class="sxs-lookup"><span data-stu-id="5ac29-211">System.String</span></span>

### <span data-ttu-id="5ac29-212">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5ac29-212">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="5ac29-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="5ac29-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="5ac29-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="5ac29-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="5ac29-215">System. string []</span><span class="sxs-lookup"><span data-stu-id="5ac29-215">System.String[]</span></span>

### <span data-ttu-id="5ac29-216">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5ac29-216">System.Int32</span></span>

## <span data-ttu-id="5ac29-217">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac29-217">OUTPUTS</span></span>

### <span data-ttu-id="5ac29-218">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="5ac29-218">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="5ac29-219">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ac29-219">NOTES</span></span>

## <span data-ttu-id="5ac29-220">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ac29-220">RELATED LINKS</span></span>
