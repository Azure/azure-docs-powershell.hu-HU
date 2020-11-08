---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187453"
---
# <span data-ttu-id="3a538-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3a538-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="3a538-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a538-102">SYNOPSIS</span></span>
<span data-ttu-id="3a538-103">Az esemény rácsa esemény-előfizetés tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="3a538-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="3a538-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a538-104">SYNTAX</span></span>

### <span data-ttu-id="3a538-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a538-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a538-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a538-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a538-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a538-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a538-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a538-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a538-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a538-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a538-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a538-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a538-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a538-111">DESCRIPTION</span></span>
<span data-ttu-id="3a538-112">Az esemény rácsa esemény-előfizetés tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="3a538-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="3a538-113">Ez a funkció a meglévő esemény-előfizetések szűrő, cél vagy címkék frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="3a538-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="3a538-114">Példák</span><span class="sxs-lookup"><span data-stu-id="3a538-114">EXAMPLES</span></span>

### <span data-ttu-id="3a538-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3a538-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="3a538-116">Frissíti az esemény-előfizetési ES1 végpontját a \` \` témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="3a538-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="3a538-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="3a538-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="3a538-118">Frissíti az esemény-előfizetési ES1 végpontját a \` \` témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="3a538-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="3a538-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="3a538-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="3a538-120">A \` \` EventHub-névtér ContosoNamespace az új végponttal \` https://requestb.in/1kxxoui1\ "és az új SubjectEndsWith-szűrő jpg-ként" ES1 frissíti az esemény-előfizetés tulajdonságait. \`\`</span><span class="sxs-lookup"><span data-stu-id="3a538-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="3a538-121">4. példa</span><span class="sxs-lookup"><span data-stu-id="3a538-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="3a538-122">Frissíti az erőforráscsoport MyResourceGroupName tartozó esemény-előfizetési \` ES1 tulajdonságait \` \` \` az új címkék $labels.</span><span class="sxs-lookup"><span data-stu-id="3a538-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="3a538-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a538-123">PARAMETERS</span></span>

### <span data-ttu-id="3a538-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="3a538-124">-AdvancedFilter</span></span>
<span data-ttu-id="3a538-125">Speciális szűrő, amely az attribútum-alapú szűréshez használt több Hashtable-érték tömböját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a538-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="3a538-126">Minden Hashtable-értékhez tartozik az alábbi kulcsok-érték adatok: művelet, kulcs és érték vagy értékek.</span><span class="sxs-lookup"><span data-stu-id="3a538-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="3a538-127">Az operátor az alábbi értékek egyike lehet: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith, StringContains vagy.</span><span class="sxs-lookup"><span data-stu-id="3a538-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="3a538-128">A kulcs azt a hasznos tulajdonságot jelenti, amelyben a speciális szűrési házirendek érvényesülnek.</span><span class="sxs-lookup"><span data-stu-id="3a538-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="3a538-129">Végül az érték vagy az értékek az egyeztetni kívánt értékek értékét vagy halmazát jelentik.</span><span class="sxs-lookup"><span data-stu-id="3a538-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="3a538-130">Ez a megfelelő típusú vagy értékek tömbje lehet egyetlen érték.</span><span class="sxs-lookup"><span data-stu-id="3a538-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="3a538-131">Példaként a speciális szűrő paraméterek: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), ahol $AdvFilter 1 = @ {Operator = "NumberIn"; Key = "Data. Key1"; Values = @ (1; 2)} és $AdvFilter 2 = @ {operátor = "StringBeginsWith"; Key = "subject"; Values = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="3a538-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="3a538-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="3a538-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="3a538-133">Az Azure Active Directory-(AAD-) alkalmazásspecifikus azonosító vagy URI a kézbesítési kérelmekben szereplő birtokosi jogkivonatként való részvételhez. Csak célhelyként használható.</span><span class="sxs-lookup"><span data-stu-id="3a538-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a538-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="3a538-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="3a538-135">Az Azure Active Directory (AAD) bérlői azonosítója a kézbesítési kérésekben szereplő birtokosi jogkivonatként szerepeltetni kívánt hozzáférési jogkivonat beszerzéséhez. Csak célhelyként használható.</span><span class="sxs-lookup"><span data-stu-id="3a538-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a538-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a538-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="3a538-137">A kézbesítetlen események tárolásához használt végpont.</span><span class="sxs-lookup"><span data-stu-id="3a538-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="3a538-138">Adja meg egy tároló blob-tároló Azure Resource ID azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="3a538-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="3a538-139">Például:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="3a538-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="3a538-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a538-140">-DefaultProfile</span></span>
<span data-ttu-id="3a538-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a538-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a538-142">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="3a538-142">-DomainName</span></span>
<span data-ttu-id="3a538-143">Annak a tartománynak a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="3a538-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="3a538-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="3a538-144">-DomainTopicName</span></span>
<span data-ttu-id="3a538-145">Annak a tartománynak a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="3a538-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="3a538-146">-Végpont</span><span class="sxs-lookup"><span data-stu-id="3a538-146">-Endpoint</span></span>
<span data-ttu-id="3a538-147">Esemény-előfizetés cél végpontja.</span><span class="sxs-lookup"><span data-stu-id="3a538-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="3a538-148">Ez lehet egy webhorog URL-címe, vagy egy EventHub, tárolási várólista, hybridconnection vagy servicebusqueue Azure Resource ID azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3a538-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="3a538-149">A hibrid kapcsolat erőforrás-azonosítója például a következő:/Subscriptions/[Azure előfizetés-azonosító]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="3a538-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="3a538-150">Az esemény rácsos parancsmagjai elvégzése előtt várhatóan létrejön a cél végpont, és elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="3a538-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="3a538-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="3a538-151">-EndpointType</span></span>
<span data-ttu-id="3a538-152">Végpont típusa.</span><span class="sxs-lookup"><span data-stu-id="3a538-152">Endpoint Type.</span></span>
<span data-ttu-id="3a538-153">Ez lehet webhook, eventhub, storagequeue, hybridconnection vagy servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="3a538-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="3a538-154">Az alapértelmezett érték a webhook.</span><span class="sxs-lookup"><span data-stu-id="3a538-154">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a538-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3a538-155">-EventSubscriptionName</span></span>
<span data-ttu-id="3a538-156">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="3a538-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="3a538-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="3a538-157">-EventTtl</span></span>
<span data-ttu-id="3a538-158">Az esemény kézbesítésének időpontja percben.</span><span class="sxs-lookup"><span data-stu-id="3a538-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="3a538-159">Ennek az értéknek 1 és 1440 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="3a538-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="3a538-160">-Lejáratidátum</span><span class="sxs-lookup"><span data-stu-id="3a538-160">-ExpirationDate</span></span>
<span data-ttu-id="3a538-161">Meghatározza annak az esemény-előfizetésnek az elévülési idejét, amely után az esemény előfizetése nyugdíjba kerül.</span><span class="sxs-lookup"><span data-stu-id="3a538-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="3a538-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="3a538-162">-IncludedEventType</span></span>
<span data-ttu-id="3a538-163">Szűrő, amely a szerepeltetni kívánt eseménytípus listáját adja meg. Ha nincs megadva, az összes eseménytípus szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="3a538-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="3a538-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a538-164">-InputObject</span></span>
<span data-ttu-id="3a538-165">EventGridSubscription objektum</span><span class="sxs-lookup"><span data-stu-id="3a538-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="3a538-166">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="3a538-166">-Label</span></span>
<span data-ttu-id="3a538-167">Az esemény-előfizetés címkéi</span><span class="sxs-lookup"><span data-stu-id="3a538-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="3a538-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="3a538-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="3a538-169">Az esemény kézbesítésének maximális száma.</span><span class="sxs-lookup"><span data-stu-id="3a538-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="3a538-170">Ennek az értéknek 1 és 30 között kell lennie</span><span class="sxs-lookup"><span data-stu-id="3a538-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="3a538-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="3a538-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="3a538-172">Az események maximális száma egy kötegben.</span><span class="sxs-lookup"><span data-stu-id="3a538-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="3a538-173">Ennek az értéknek 1 és 5000 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3a538-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="3a538-174">Ez a paraméter akkor érvényes, ha a Endpint típusa csak webhook-típus.</span><span class="sxs-lookup"><span data-stu-id="3a538-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="3a538-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="3a538-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="3a538-176">Az előnyben részesített köteg mérete kilobájtban.</span><span class="sxs-lookup"><span data-stu-id="3a538-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="3a538-177">Ennek az értéknek 1 és 1024 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3a538-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="3a538-178">Ez a paraméter akkor érvényes, ha a Endpint típusa csak webhook-típus.</span><span class="sxs-lookup"><span data-stu-id="3a538-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="3a538-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a538-179">-ResourceGroupName</span></span>
<span data-ttu-id="3a538-180">A témakör erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="3a538-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="3a538-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a538-181">-ResourceId</span></span>
<span data-ttu-id="3a538-182">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetést létrehozták.</span><span class="sxs-lookup"><span data-stu-id="3a538-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="3a538-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="3a538-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="3a538-184">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi előtaghoz tartozó eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="3a538-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="3a538-185">Ha nem adja meg, akkor az összes tárgy előtagokkal rendelkező események is szerepelni fognak.</span><span class="sxs-lookup"><span data-stu-id="3a538-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="3a538-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="3a538-186">-SubjectEndsWith</span></span>
<span data-ttu-id="3a538-187">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi utótaggal egyező eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="3a538-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="3a538-188">Ha nem adja meg, a program az összes tárgyi utótaggal rendelkező eseményeket is belefoglalja.</span><span class="sxs-lookup"><span data-stu-id="3a538-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="3a538-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="3a538-189">-TopicName</span></span>
<span data-ttu-id="3a538-190">Annak a témakörnek a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="3a538-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="3a538-191">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3a538-191">-Confirm</span></span>
<span data-ttu-id="3a538-192">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3a538-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a538-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a538-193">-WhatIf</span></span>
<span data-ttu-id="3a538-194">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3a538-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a538-195">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a538-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a538-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a538-196">CommonParameters</span></span>
<span data-ttu-id="3a538-197">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a538-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a538-198">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a538-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a538-199">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a538-199">INPUTS</span></span>

### <span data-ttu-id="3a538-200">System. String</span><span class="sxs-lookup"><span data-stu-id="3a538-200">System.String</span></span>

### <span data-ttu-id="3a538-201">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="3a538-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="3a538-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a538-202">OUTPUTS</span></span>

### <span data-ttu-id="3a538-203">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="3a538-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="3a538-204">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a538-204">NOTES</span></span>

## <span data-ttu-id="3a538-205">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a538-205">RELATED LINKS</span></span>
