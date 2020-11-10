---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 44441fa364c43242a7a4454ccdf62f920cb321e5
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395424"
---
# <span data-ttu-id="7e7d6-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7e7d6-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="7e7d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e7d6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7d6-103">Új Azure-esemény-előfizetést hoz létre egy témakörhöz, Azure-erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="7e7d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e7d6-104">SYNTAX</span></span>

### <span data-ttu-id="7e7d6-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e7d6-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e7d6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e7d6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e7d6-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e7d6-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e7d6-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e7d6-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e7d6-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e7d6-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e7d6-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e7d6-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e7d6-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e7d6-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e7d6-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e7d6-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [-EndpointType <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e7d6-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e7d6-113">DESCRIPTION</span></span>
<span data-ttu-id="7e7d6-114">Új esemény-előfizetés létrehozása Azure-esemény rácsához, támogatott Azure-erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="7e7d6-115">Ha az aktuálisan kiválasztott Azure-előfizetéshez szeretne esemény-előfizetést létrehozni, adja meg az esemény-előfizetés nevét és a cél végpontját.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="7e7d6-116">Ha eseményvezérelt előfizetést szeretne létrehozni egy erőforrás-csoporthoz, az esemény-előfizetés neve és a cél végpont mellett adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="7e7d6-117">Ha eseményvezérelt előfizetést szeretne létrehozni az Azure-esemény rácsához, adja meg a téma nevét is.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="7e7d6-118">Ha egy támogatott Azure-erőforráshoz szeretne esemény-előfizetést létrehozni, adja meg az erőforrás teljes erőforrás-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="7e7d6-119">A támogatott típusok listájának megtekintéséhez futtassa az Get-AzEventGridTopicType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="7e7d6-120">Példák</span><span class="sxs-lookup"><span data-stu-id="7e7d6-120">EXAMPLES</span></span>

### <span data-ttu-id="7e7d6-121">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7e7d6-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7e7d6-122">Új esemény-előfizetést hoz létre az \` \` Azure EventSubscription1 \` -témakör téma1 az \` erőforráscsoport \` MyResourceGroupName \` a webhook Destination végponttal `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="7e7d6-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="7e7d6-123">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="7e7d6-124">2. példa</span><span class="sxs-lookup"><span data-stu-id="7e7d6-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7e7d6-125">Új esemény-előfizetési \` EventSubscription1 hoz létre \` egy erőforráscsoport \` MyResourceGroupName \` a webhook-cél végponttal `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="7e7d6-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="7e7d6-126">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="7e7d6-127">3. példa</span><span class="sxs-lookup"><span data-stu-id="7e7d6-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7e7d6-128">Új esemény-előfizetést hoz létre \` \` az aktuálisan kijelölt Azure-előfizetéshez a EventSubscription1 végponttal `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="7e7d6-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="7e7d6-129">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="7e7d6-130">4. példa</span><span class="sxs-lookup"><span data-stu-id="7e7d6-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="7e7d6-131">Új esemény-előfizetést hoz létre \` \` az aktuálisan kijelölt Azure-előfizetéshez a EventSubscription1 végponttal `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="7e7d6-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="7e7d6-132">Ez az esemény-előfizetés adja meg az eseménytípus és a tárgy további szűrőit, és csak az adott szűrővel egyező eseményeket kézbesíti a program a cél végpontra.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="7e7d6-133">Példa 5</span><span class="sxs-lookup"><span data-stu-id="7e7d6-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="7e7d6-134">Új esemény-előfizetést hoz létre az \` \` aktuálisan kijelölt Azure-előfizetéshez, a megadott EventSubscription1 az események céljára.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="7e7d6-135">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="7e7d6-136">6. példa</span><span class="sxs-lookup"><span data-stu-id="7e7d6-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="7e7d6-137">Új esemény-előfizetési \` EventSubscription1 \` hoz létre egy EventHub-névtérhez a megadott webhook-cél végponttal `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="7e7d6-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="7e7d6-138">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="7e7d6-139">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e7d6-139">PARAMETERS</span></span>

### <span data-ttu-id="7e7d6-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="7e7d6-140">-AdvancedFilter</span></span>
<span data-ttu-id="7e7d6-141">Speciális szűrő, amely az attribútum-alapú szűréshez használt több Hashtable-érték tömböját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="7e7d6-142">Minden Hashtable-értékhez tartozik az alábbi kulcsok-érték adatok: művelet, kulcs és érték vagy értékek.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="7e7d6-143">Az operátor az alábbi értékek egyike lehet: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith, StringContains vagy.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="7e7d6-144">A kulcs azt a hasznos tulajdonságot jelenti, amelyben a speciális szűrési házirendek érvényesülnek.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="7e7d6-145">Végül az érték vagy az értékek az egyeztetni kívánt értékek értékét vagy halmazát jelentik.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="7e7d6-146">Ez a megfelelő típusú vagy értékek tömbje lehet egyetlen érték.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="7e7d6-147">Példaként a speciális szűrő paraméterek: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), ahol $AdvFilter 1 = @ {Operator = "NumberIn"; Key = "Data. Key1"; Values = @ (1; 2)} és $AdvFilter 2 = @ {operátor = "StringBringsWith"; Key = "subject"; Values = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="7e7d6-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="7e7d6-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="7e7d6-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="7e7d6-149">Az Azure Active Directory-(AAD-) alkalmazásspecifikus azonosító vagy URI a kézbesítési kérelmekben szereplő birtokosi jogkivonatként való részvételhez. Csak célhelyként használható.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7d6-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="7e7d6-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="7e7d6-151">Az Azure Active Directory (AAD) bérlői azonosítója a kézbesítési kérésekben szereplő birtokosi jogkivonatként szerepeltetni kívánt hozzáférési jogkivonat beszerzéséhez. Csak célhelyként használható.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7d6-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e7d6-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="7e7d6-153">A kézbesítetlen események tárolásához használt végpont.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="7e7d6-154">Adja meg egy tároló blob-tároló Azure Resource ID azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="7e7d6-155">Például:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="7e7d6-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="7e7d6-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7d6-156">-DefaultProfile</span></span>
<span data-ttu-id="7e7d6-157">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7e7d6-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e7d6-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="7e7d6-158">-DeliverySchema</span></span>
<span data-ttu-id="7e7d6-159">Az eseményeknek a célhelyre való kézbesítéséhez használandó séma.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="7e7d6-160">A lehetséges értékek a következők: eventgridschema, CustomInputSchema vagy cloudeventv01schema.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="7e7d6-161">Az alapértelmezett érték a CustomInputSchema.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-161">Default value is CustomInputSchema.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

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
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7d6-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="7e7d6-162">-DomainInputObject</span></span>
<span data-ttu-id="7e7d6-163">EventGrid tartomány objektuma.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="7e7d6-164">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="7e7d6-164">-DomainName</span></span>
<span data-ttu-id="7e7d6-165">Annak az eseménynek a rácsnak a neve, amelyre az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="7e7d6-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="7e7d6-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="7e7d6-167">EventGrid objektum</span><span class="sxs-lookup"><span data-stu-id="7e7d6-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="7e7d6-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="7e7d6-168">-DomainTopicName</span></span>
<span data-ttu-id="7e7d6-169">Annak a tartománynak a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-169">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="7e7d6-170">-Végpont</span><span class="sxs-lookup"><span data-stu-id="7e7d6-170">-Endpoint</span></span>
<span data-ttu-id="7e7d6-171">Esemény-előfizetés cél végpontja.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="7e7d6-172">Ez lehet egy webhorog URL-címe, vagy egy EventHub, tárolási várólista, hybridconnection vagy servicebusqueue Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="7e7d6-173">A hibrid kapcsolat erőforrás-azonosítója például a következő:/Subscriptions/[Azure előfizetés-azonosító]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="7e7d6-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="7e7d6-174">Az esemény rácsos parancsmagjai elvégzése előtt várhatóan létrejön a cél végpont, és elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="7e7d6-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="7e7d6-175">-EndpointType</span></span>
<span data-ttu-id="7e7d6-176">Végpont típusa.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-176">Endpoint Type.</span></span>
<span data-ttu-id="7e7d6-177">Ez lehet webhook, eventhub, storagequeue, hybridconnection vagy servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="7e7d6-178">Az alapértelmezett érték a webhook.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-178">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

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
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7d6-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7e7d6-179">-EventSubscriptionName</span></span>
<span data-ttu-id="7e7d6-180">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="7e7d6-180">The name of the event subscription</span></span>

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

### <span data-ttu-id="7e7d6-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="7e7d6-181">-EventTtl</span></span>
<span data-ttu-id="7e7d6-182">Az esemény kézbesítésének időpontja percben.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="7e7d6-183">Ennek az értéknek 1 és 1440 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="7e7d6-183">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="7e7d6-184">-Lejáratidátum</span><span class="sxs-lookup"><span data-stu-id="7e7d6-184">-ExpirationDate</span></span>
<span data-ttu-id="7e7d6-185">Meghatározza annak az esemény-előfizetésnek az elévülési idejét, amely után az esemény előfizetése nyugdíjba kerül.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="7e7d6-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="7e7d6-186">-IncludedEventType</span></span>
<span data-ttu-id="7e7d6-187">Szűrő, amely a szerepeltetni kívánt eseménytípus listáját adja meg. Ha nincs megadva, az összes eseménytípus szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7d6-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e7d6-188">-InputObject</span></span>
<span data-ttu-id="7e7d6-189">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="7e7d6-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="7e7d6-190">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="7e7d6-190">-Label</span></span>
<span data-ttu-id="7e7d6-191">Az esemény-előfizetés címkéi</span><span class="sxs-lookup"><span data-stu-id="7e7d6-191">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7d6-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="7e7d6-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="7e7d6-193">Az esemény kézbesítésének maximális száma.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="7e7d6-194">Ennek az értéknek 1 és 30 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="7e7d6-194">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="7e7d6-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="7e7d6-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="7e7d6-196">Az események maximális száma egy kötegben.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="7e7d6-197">Ennek az értéknek 1 és 5000 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="7e7d6-198">Ez a paraméter akkor érvényes, ha a Endpint típusa csak webhook-típus.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-198">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="7e7d6-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="7e7d6-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="7e7d6-200">Az előnyben részesített köteg mérete kilobájtban.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="7e7d6-201">Ennek az értéknek 1 és 1024 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="7e7d6-202">Ez a paraméter akkor érvényes, ha a Endpint típusa csak webhook-típus.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-202">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="7e7d6-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e7d6-203">-ResourceGroupName</span></span>
<span data-ttu-id="7e7d6-204">A témakör erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-204">The resource group of the topic.</span></span>

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

### <span data-ttu-id="7e7d6-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e7d6-205">-ResourceId</span></span>
<span data-ttu-id="7e7d6-206">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="7e7d6-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="7e7d6-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="7e7d6-208">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi előtaghoz tartozó eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="7e7d6-209">Ha nem adja meg, akkor az összes tárgy előtagokkal rendelkező események is szerepelni fognak.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-209">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="7e7d6-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="7e7d6-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="7e7d6-211">Szűrő: azt adja meg, hogy a tárgy mezőt a kis-és nagybetűk megkülönböztetésével kell összehasonlítani.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="7e7d6-212">Ha nem adja meg, a program a tárgyat a kis-és nagybetűk megkülönböztetésével hasonlítja össze.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="7e7d6-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="7e7d6-213">-SubjectEndsWith</span></span>
<span data-ttu-id="7e7d6-214">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi utótaggal egyező eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="7e7d6-215">Ha nem adja meg, a program az összes tárgyi utótaggal rendelkező eseményeket is belefoglalja.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-215">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="7e7d6-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7e7d6-216">-TopicName</span></span>
<span data-ttu-id="7e7d6-217">Annak a témakörnek a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="7e7d6-218">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e7d6-218">-Confirm</span></span>
<span data-ttu-id="7e7d6-219">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e7d6-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e7d6-220">-WhatIf</span></span>
<span data-ttu-id="7e7d6-221">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e7d6-222">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e7d6-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7d6-223">CommonParameters</span></span>
<span data-ttu-id="7e7d6-224">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e7d6-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7d6-225">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7e7d6-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7d6-226">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e7d6-226">INPUTS</span></span>

### <span data-ttu-id="7e7d6-227">System. String</span><span class="sxs-lookup"><span data-stu-id="7e7d6-227">System.String</span></span>

### <span data-ttu-id="7e7d6-228">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="7e7d6-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="7e7d6-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="7e7d6-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="7e7d6-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7e7d6-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="7e7d6-231">System. string []</span><span class="sxs-lookup"><span data-stu-id="7e7d6-231">System.String[]</span></span>

### <span data-ttu-id="7e7d6-232">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7e7d6-232">System.Int32</span></span>

## <span data-ttu-id="7e7d6-233">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e7d6-233">OUTPUTS</span></span>

### <span data-ttu-id="7e7d6-234">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="7e7d6-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="7e7d6-235">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e7d6-235">NOTES</span></span>

## <span data-ttu-id="7e7d6-236">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e7d6-236">RELATED LINKS</span></span>
