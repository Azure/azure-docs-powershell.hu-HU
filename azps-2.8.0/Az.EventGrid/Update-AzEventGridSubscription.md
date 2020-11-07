---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: eaf9a89a8c610d8666a356e563681accfced4a7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666505"
---
# <span data-ttu-id="29de3-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="29de3-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="29de3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29de3-102">SYNOPSIS</span></span>
<span data-ttu-id="29de3-103">Az esemény rácsa esemény-előfizetés tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="29de3-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="29de3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29de3-104">SYNTAX</span></span>

### <span data-ttu-id="29de3-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29de3-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29de3-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="29de3-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29de3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29de3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29de3-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="29de3-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29de3-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="29de3-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29de3-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="29de3-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29de3-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="29de3-111">DESCRIPTION</span></span>
<span data-ttu-id="29de3-112">Az esemény rácsa esemény-előfizetés tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="29de3-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="29de3-113">Ez a funkció a meglévő esemény-előfizetések szűrő, cél vagy címkék frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="29de3-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="29de3-114">Példák</span><span class="sxs-lookup"><span data-stu-id="29de3-114">EXAMPLES</span></span>

### <span data-ttu-id="29de3-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29de3-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="29de3-116">Frissíti az esemény-előfizetési ES1 végpontját a \` \` témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="29de3-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="29de3-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="29de3-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="29de3-118">Frissíti az esemény-előfizetési ES1 végpontját a \` \` témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="29de3-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="29de3-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="29de3-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="29de3-120">A \` \` EventHub-névtér ContosoNamespace az új végponttal \` https://requestb.in/1kxxoui1\ "és az új SubjectEndsWith-szűrő jpg-ként" ES1 frissíti az esemény-előfizetés tulajdonságait. \`\`</span><span class="sxs-lookup"><span data-stu-id="29de3-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="29de3-121">4. példa</span><span class="sxs-lookup"><span data-stu-id="29de3-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="29de3-122">Frissíti az erőforráscsoport MyResourceGroupName tartozó esemény-előfizetési \` ES1 tulajdonságait \` \` \` az új címkék $labels.</span><span class="sxs-lookup"><span data-stu-id="29de3-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="29de3-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29de3-123">PARAMETERS</span></span>

### <span data-ttu-id="29de3-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="29de3-124">-AdvancedFilter</span></span>
<span data-ttu-id="29de3-125">Speciális szűrő, amely az attribútum-alapú szűréshez használt több Hashtable-érték tömböját adja meg.</span><span class="sxs-lookup"><span data-stu-id="29de3-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="29de3-126">Minden Hashtable-értékhez tartozik az alábbi kulcsok-érték adatok: művelet, kulcs és érték vagy értékek.</span><span class="sxs-lookup"><span data-stu-id="29de3-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="29de3-127">Az operátor az alábbi értékek egyike lehet: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith, StringContains vagy.</span><span class="sxs-lookup"><span data-stu-id="29de3-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="29de3-128">A kulcs azt a hasznos tulajdonságot jelenti, amelyben a speciális szűrési házirendek érvényesülnek.</span><span class="sxs-lookup"><span data-stu-id="29de3-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="29de3-129">Végül az érték vagy az értékek az egyeztetni kívánt értékek értékét vagy halmazát jelentik.</span><span class="sxs-lookup"><span data-stu-id="29de3-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="29de3-130">Ez a megfelelő típusú vagy értékek tömbje lehet egyetlen érték.</span><span class="sxs-lookup"><span data-stu-id="29de3-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="29de3-131">Példaként a speciális szűrő paraméterek: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), ahol $AdvFilter 1 = @ {Operator = "NumberIn"; Key = "Data. Key1"; Values = @ (1; 2)} és $AdvFilter 2 = @ {operátor = "StringBringsWith"; Key = "subject"; Values = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="29de3-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="29de3-132">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="29de3-132">-DeadLetterEndpoint</span></span>
<span data-ttu-id="29de3-133">A kézbesítetlen események tárolásához használt végpont.</span><span class="sxs-lookup"><span data-stu-id="29de3-133">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="29de3-134">Adja meg egy tároló blob-tároló Azure Resource ID azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="29de3-134">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="29de3-135">Például:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="29de3-135">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="29de3-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29de3-136">-DefaultProfile</span></span>
<span data-ttu-id="29de3-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29de3-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29de3-138">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="29de3-138">-DomainName</span></span>
<span data-ttu-id="29de3-139">Annak a tartománynak a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="29de3-139">The name of the domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29de3-140">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="29de3-140">-DomainTopicName</span></span>
<span data-ttu-id="29de3-141">Annak a tartománynak a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="29de3-141">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29de3-142">-Végpont</span><span class="sxs-lookup"><span data-stu-id="29de3-142">-Endpoint</span></span>
<span data-ttu-id="29de3-143">Esemény-előfizetés cél végpontja.</span><span class="sxs-lookup"><span data-stu-id="29de3-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="29de3-144">Ez lehet egy webhorog URL-címe, vagy egy EventHub, tárolási várólista, hybridconnection vagy servicebusqueue Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="29de3-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="29de3-145">A hibrid kapcsolat erőforrás-azonosítója például a következő:/Subscriptions/[Azure előfizetés-azonosító]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="29de3-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="29de3-146">Az esemény rácsos parancsmagjai elvégzése előtt várhatóan létrejön a cél végpont, és elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="29de3-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="29de3-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="29de3-147">-EndpointType</span></span>
<span data-ttu-id="29de3-148">Végpont típusa.</span><span class="sxs-lookup"><span data-stu-id="29de3-148">Endpoint Type.</span></span>
<span data-ttu-id="29de3-149">Ez lehet webhook, eventhub, storagequeue, hybridconnection vagy servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="29de3-149">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="29de3-150">Az alapértelmezett érték a webhook.</span><span class="sxs-lookup"><span data-stu-id="29de3-150">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29de3-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="29de3-151">-EventSubscriptionName</span></span>
<span data-ttu-id="29de3-152">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="29de3-152">The name of the event subscription</span></span>

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

### <span data-ttu-id="29de3-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="29de3-153">-EventTtl</span></span>
<span data-ttu-id="29de3-154">Az esemény kézbesítésének időpontja percben.</span><span class="sxs-lookup"><span data-stu-id="29de3-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="29de3-155">Ennek az értéknek 1 és 1440 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="29de3-155">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="29de3-156">-Lejáratidátum</span><span class="sxs-lookup"><span data-stu-id="29de3-156">-ExpirationDate</span></span>
<span data-ttu-id="29de3-157">Meghatározza annak az esemény-előfizetésnek az elévülési idejét, amely után az esemény előfizetése nyugdíjba kerül.</span><span class="sxs-lookup"><span data-stu-id="29de3-157">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="29de3-158">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="29de3-158">-IncludedEventType</span></span>
<span data-ttu-id="29de3-159">Szűrő, amely a szerepeltetni kívánt eseménytípus listáját adja meg. Ha nincs megadva, az összes eseménytípus szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="29de3-159">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="29de3-160">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29de3-160">-InputObject</span></span>
<span data-ttu-id="29de3-161">EventGridSubscription objektum</span><span class="sxs-lookup"><span data-stu-id="29de3-161">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="29de3-162">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="29de3-162">-Label</span></span>
<span data-ttu-id="29de3-163">Az esemény-előfizetés címkéi</span><span class="sxs-lookup"><span data-stu-id="29de3-163">Labels for the event subscription</span></span>

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

### <span data-ttu-id="29de3-164">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="29de3-164">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="29de3-165">Az esemény kézbesítésének maximális száma.</span><span class="sxs-lookup"><span data-stu-id="29de3-165">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="29de3-166">Ennek az értéknek 1 és 30 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="29de3-166">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="29de3-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29de3-167">-ResourceGroupName</span></span>
<span data-ttu-id="29de3-168">A témakör erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="29de3-168">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29de3-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29de3-169">-ResourceId</span></span>
<span data-ttu-id="29de3-170">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetést létrehozták.</span><span class="sxs-lookup"><span data-stu-id="29de3-170">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="29de3-171">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="29de3-171">-SubjectBeginsWith</span></span>
<span data-ttu-id="29de3-172">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi előtaghoz tartozó eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="29de3-172">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="29de3-173">Ha nem adja meg, akkor az összes tárgy előtagokkal rendelkező események is szerepelni fognak.</span><span class="sxs-lookup"><span data-stu-id="29de3-173">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="29de3-174">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="29de3-174">-SubjectEndsWith</span></span>
<span data-ttu-id="29de3-175">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi utótaggal egyező eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="29de3-175">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="29de3-176">Ha nem adja meg, a program az összes tárgyi utótaggal rendelkező eseményeket is belefoglalja.</span><span class="sxs-lookup"><span data-stu-id="29de3-176">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="29de3-177">-TopicName</span><span class="sxs-lookup"><span data-stu-id="29de3-177">-TopicName</span></span>
<span data-ttu-id="29de3-178">Annak a témakörnek a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="29de3-178">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="29de3-179">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29de3-179">-Confirm</span></span>
<span data-ttu-id="29de3-180">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29de3-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29de3-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29de3-181">-WhatIf</span></span>
<span data-ttu-id="29de3-182">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29de3-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29de3-183">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29de3-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29de3-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29de3-184">CommonParameters</span></span>
<span data-ttu-id="29de3-185">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29de3-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29de3-186">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29de3-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29de3-187">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29de3-187">INPUTS</span></span>

### <span data-ttu-id="29de3-188">System. String</span><span class="sxs-lookup"><span data-stu-id="29de3-188">System.String</span></span>

### <span data-ttu-id="29de3-189">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="29de3-189">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="29de3-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29de3-190">OUTPUTS</span></span>

### <span data-ttu-id="29de3-191">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="29de3-191">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="29de3-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29de3-192">NOTES</span></span>

## <span data-ttu-id="29de3-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29de3-193">RELATED LINKS</span></span>
