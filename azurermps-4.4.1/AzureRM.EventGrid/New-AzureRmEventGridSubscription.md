---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: ed2855571ccd3ce10a8a41fd72f5e14fde7bba16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505063"
---
# <span data-ttu-id="a2beb-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a2beb-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="a2beb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2beb-102">SYNOPSIS</span></span>
<span data-ttu-id="a2beb-103">Új Azure-esemény-előfizetést hoz létre egy témakörhöz, Azure-erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="a2beb-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2beb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2beb-104">SYNTAX</span></span>

### <span data-ttu-id="a2beb-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2beb-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2beb-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2beb-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2beb-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2beb-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2beb-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2beb-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2beb-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2beb-109">DESCRIPTION</span></span>
<span data-ttu-id="a2beb-110">Új esemény-előfizetés létrehozása Azure-esemény rácsához, támogatott Azure-erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="a2beb-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="a2beb-111">Ha az aktuálisan kiválasztott Azure-előfizetéshez szeretne esemény-előfizetést létrehozni, adja meg az esemény-előfizetés nevét és a cél végpontját.</span><span class="sxs-lookup"><span data-stu-id="a2beb-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="a2beb-112">Ha eseményvezérelt előfizetést szeretne létrehozni egy erőforrás-csoporthoz, az esemény-előfizetés neve és a cél végpont mellett adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="a2beb-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="a2beb-113">Ha eseményvezérelt előfizetést szeretne létrehozni az Azure-esemény rácsához, adja meg a téma nevét is.</span><span class="sxs-lookup"><span data-stu-id="a2beb-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="a2beb-114">Ha egy támogatott Azure-erőforráshoz szeretne esemény-előfizetést létrehozni, adja meg az erőforrás teljes erőforrás-AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="a2beb-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="a2beb-115">A támogatott típusok listájának megtekintéséhez futtassa az Get-AzureRmEventGridTopicType parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a2beb-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="a2beb-116">Példák</span><span class="sxs-lookup"><span data-stu-id="a2beb-116">EXAMPLES</span></span>

### <span data-ttu-id="a2beb-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2beb-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a2beb-118">Új esemény-előfizetést hoz létre az \` \` Azure EventSubscription1 \` -témakör téma1 az \` erőforráscsoport \` MyResourceGroupName \` a webhook Destination végponttal https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="a2beb-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="a2beb-119">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="a2beb-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="a2beb-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="a2beb-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a2beb-121">Új esemény-előfizetési \` EventSubscription1 hoz létre \` egy erőforráscsoport \` MyResourceGroupName \` a webhook-cél végponttal https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="a2beb-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="a2beb-122">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="a2beb-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="a2beb-123">3. példa</span><span class="sxs-lookup"><span data-stu-id="a2beb-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a2beb-124">Új esemény-előfizetést hoz létre \` \` az aktuálisan kijelölt Azure-előfizetéshez a EventSubscription1 végponttal https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="a2beb-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="a2beb-125">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="a2beb-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="a2beb-126">4. példa</span><span class="sxs-lookup"><span data-stu-id="a2beb-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="a2beb-127">Új esemény-előfizetést hoz létre \` \` az aktuálisan kijelölt Azure-előfizetéshez a EventSubscription1 végponttal https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="a2beb-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="a2beb-128">Ez az esemény-előfizetés adja meg az eseménytípus és a tárgy további szűrőit, és csak az adott szűrővel egyező eseményeket kézbesíti a program a cél végpontra.</span><span class="sxs-lookup"><span data-stu-id="a2beb-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="a2beb-129">Példa 5</span><span class="sxs-lookup"><span data-stu-id="a2beb-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="a2beb-130">Új esemény-előfizetést hoz létre az \` \` aktuálisan kijelölt Azure-előfizetéshez, a megadott EventSubscription1 az események céljára.</span><span class="sxs-lookup"><span data-stu-id="a2beb-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="a2beb-131">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="a2beb-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="a2beb-132">6. példa</span><span class="sxs-lookup"><span data-stu-id="a2beb-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a2beb-133">Új esemény-előfizetési \` EventSubscription1 \` hoz létre egy EventHub-névtérhez a megadott webhhok cél végponttal https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="a2beb-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="a2beb-134">Ez az esemény-előfizetés az alapértelmezett szűrőket használja.</span><span class="sxs-lookup"><span data-stu-id="a2beb-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="a2beb-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2beb-135">PARAMETERS</span></span>

### <span data-ttu-id="a2beb-136">-Végpont</span><span class="sxs-lookup"><span data-stu-id="a2beb-136">-Endpoint</span></span>
<span data-ttu-id="a2beb-137">Esemény-előfizetés cél végpontja.</span><span class="sxs-lookup"><span data-stu-id="a2beb-137">Event subscription destination endpoint.</span></span>
<span data-ttu-id="a2beb-138">Ez lehet egy webhorog URL-címe vagy egy EventHub Azure erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2beb-138">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2beb-139">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a2beb-139">-EndpointType</span></span>
<span data-ttu-id="a2beb-140">Végpont típusa.</span><span class="sxs-lookup"><span data-stu-id="a2beb-140">Endpoint Type.</span></span>
<span data-ttu-id="a2beb-141">Ez lehet webhook vagy eventhub</span><span class="sxs-lookup"><span data-stu-id="a2beb-141">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2beb-142">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a2beb-142">-EventSubscriptionName</span></span>
<span data-ttu-id="a2beb-143">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="a2beb-143">The name of the event subscription</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2beb-144">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="a2beb-144">-IncludedEventType</span></span>
<span data-ttu-id="a2beb-145">Szűrő, amely a szerepeltetni kívánt eseménytípus listáját adja meg. Ha nincs megadva, az összes eseménytípus szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="a2beb-145">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2beb-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2beb-146">-InputObject</span></span>
<span data-ttu-id="a2beb-147">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="a2beb-147">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2beb-148">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="a2beb-148">-Label</span></span>
<span data-ttu-id="a2beb-149">Az esemény-előfizetés címkéi</span><span class="sxs-lookup"><span data-stu-id="a2beb-149">Labels for the event subscription</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2beb-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2beb-150">-ResourceGroupName</span></span>
<span data-ttu-id="a2beb-151">A témakör erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="a2beb-151">The resource group of the topic.</span></span>

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

### <span data-ttu-id="a2beb-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2beb-152">-ResourceId</span></span>
<span data-ttu-id="a2beb-153">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="a2beb-153">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="a2beb-154">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="a2beb-154">-SubjectBeginsWith</span></span>
<span data-ttu-id="a2beb-155">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi előtaghoz tartozó eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="a2beb-155">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="a2beb-156">Ha nem adja meg, akkor az összes tárgy előtagokkal rendelkező események is szerepelni fognak.</span><span class="sxs-lookup"><span data-stu-id="a2beb-156">If not specified, events with all subject prefixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2beb-157">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="a2beb-157">-SubjectCaseSensitive</span></span>
<span data-ttu-id="a2beb-158">Szűrő: azt adja meg, hogy a tárgy mezőt a kis-és nagybetűk megkülönböztetésével kell összehasonlítani.</span><span class="sxs-lookup"><span data-stu-id="a2beb-158">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="a2beb-159">Ha nem adja meg, a program a tárgyat a kis-és nagybetűk megkülönböztetésével hasonlítja össze.</span><span class="sxs-lookup"><span data-stu-id="a2beb-159">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="a2beb-160">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="a2beb-160">-SubjectEndsWith</span></span>
<span data-ttu-id="a2beb-161">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi utótaggal egyező eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="a2beb-161">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="a2beb-162">Ha nem adja meg, a program az összes tárgyi utótaggal rendelkező eseményeket is belefoglalja.</span><span class="sxs-lookup"><span data-stu-id="a2beb-162">If not specified, events with all subject suffixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2beb-163">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a2beb-163">-TopicName</span></span>
<span data-ttu-id="a2beb-164">Annak a témakörnek a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="a2beb-164">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="a2beb-165">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a2beb-165">-Confirm</span></span>
<span data-ttu-id="a2beb-166">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a2beb-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2beb-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2beb-167">-WhatIf</span></span>
<span data-ttu-id="a2beb-168">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a2beb-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2beb-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2beb-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2beb-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2beb-170">-DefaultProfile</span></span>
<span data-ttu-id="a2beb-171">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2beb-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2beb-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2beb-172">CommonParameters</span></span>
<span data-ttu-id="a2beb-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2beb-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2beb-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2beb-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2beb-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2beb-175">INPUTS</span></span>

### <span data-ttu-id="a2beb-176">System. String</span><span class="sxs-lookup"><span data-stu-id="a2beb-176">System.String</span></span>
<span data-ttu-id="a2beb-177">Microsoft. Azure. Command. EventGrid. models. PSTopic System. Management. Automation. SwitchParameter System. string []</span><span class="sxs-lookup"><span data-stu-id="a2beb-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic System.Management.Automation.SwitchParameter System.String[]</span></span>

## <span data-ttu-id="a2beb-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2beb-178">OUTPUTS</span></span>

### <span data-ttu-id="a2beb-179">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a2beb-179">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a2beb-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2beb-180">NOTES</span></span>

## <span data-ttu-id="a2beb-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2beb-181">RELATED LINKS</span></span>

