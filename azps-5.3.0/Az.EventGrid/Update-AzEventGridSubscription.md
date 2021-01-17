---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376737"
---
# <span data-ttu-id="b76cb-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b76cb-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="b76cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b76cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b76cb-103">Frissítse egy Eseményrács esemény-előfizetés tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b76cb-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="b76cb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b76cb-104">SYNTAX</span></span>

### <span data-ttu-id="b76cb-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b76cb-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b76cb-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b76cb-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b76cb-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b76cb-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b76cb-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b76cb-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b76cb-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b76cb-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b76cb-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b76cb-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b76cb-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b76cb-111">DESCRIPTION</span></span>
<span data-ttu-id="b76cb-112">Frissítse egy Eseményrács esemény-előfizetés tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b76cb-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="b76cb-113">Ezzel frissítheti egy meglévő esemény-előfizetés szűrőit, célhelyét vagy címkéit.</span><span class="sxs-lookup"><span data-stu-id="b76cb-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="b76cb-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b76cb-114">EXAMPLES</span></span>

### <span data-ttu-id="b76cb-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="b76cb-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="b76cb-116">Frissíti az esemény-előfizetés ES1 végpontját \` \` a \` \` \` MyResourceGroupName erőforráscsoport Témakör1 témaköréhez: \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="b76cb-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="b76cb-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="b76cb-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="b76cb-118">Frissíti az esemény-előfizetés ES1 végpontját \` \` a \` \` \` MyResourceGroupName erőforráscsoport Témakör1 témaköréhez: \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="b76cb-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="b76cb-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="b76cb-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="b76cb-120">Frissíti az esemény-előfizetés ES1 tulajdonságát az EventHub névtér ContosoNamespace számára az új végponttal " és az új \` \` \` https://requestb.in/1kxxoui1\ SubjectEndsWith \` szűrővel jpg formátumban\`</span><span class="sxs-lookup"><span data-stu-id="b76cb-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="b76cb-121">4. példa</span><span class="sxs-lookup"><span data-stu-id="b76cb-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="b76cb-122">Frissíti a \` \` \` MyResourceGroupName erőforráscsoport es1 esemény-előfizetésének tulajdonságait az új \` $labels.</span><span class="sxs-lookup"><span data-stu-id="b76cb-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="b76cb-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b76cb-123">PARAMETERS</span></span>

### <span data-ttu-id="b76cb-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="b76cb-124">-AdvancedFilter</span></span>
<span data-ttu-id="b76cb-125">Speciális szűrő, amely több, attribútumalapú szűréshez használt hashtable értékeket tartalmazó tömböt ad meg.</span><span class="sxs-lookup"><span data-stu-id="b76cb-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="b76cb-126">Minden egyes hashtable érték a következő kulcsérték-információkkal rendelkezik: Művelet, Kulcs és Érték vagy Értékek.</span><span class="sxs-lookup"><span data-stu-id="b76cb-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="b76cb-127">Az operátor a következő értékek egyike lehet: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith vagy StringContains.</span><span class="sxs-lookup"><span data-stu-id="b76cb-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="b76cb-128">A kulcs azt a betöltési tulajdonságot jelöli, amelyben a speciális szűrési házirendek vannak alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="b76cb-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="b76cb-129">Végül az Érték vagy az Értékek az egyezéshez megadott értéket vagy értékhalmazt jelentik.</span><span class="sxs-lookup"><span data-stu-id="b76cb-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="b76cb-130">Ez lehet a megfelelő típus egyetlen értéke vagy egy értéktömb.</span><span class="sxs-lookup"><span data-stu-id="b76cb-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="b76cb-131">Példa az irányított szűrés paramétereire: $AdvancedFilters=@($AdvFilter 1; $AdvFilter 2), ahol $AdvFilter 1=@{operátor="NumberIn"; key="Data.Key1"; Values=@(1,2)} és $AdvFilter 2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1";"SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="b76cb-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="b76cb-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="b76cb-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="b76cb-133">Az Azure Active Directory (AAD) alkalmazásazonosítója vagy Uri a kézbesítési kérelmekben a szállító jogkivonatként szereplő hozzáférési jogkivonat lekérése érdekében. Csak webhook mint célhely esetén alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="b76cb-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="b76cb-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="b76cb-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="b76cb-135">Az Azure Active Directory (AAD) bérlőazonosítója, amely a kézbesítési kérelmekben a szállító jogkivonatként szereplő hozzáférési jogkivonatot fogja kapni. Csak webhook mint célhely esetén alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="b76cb-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="b76cb-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="b76cb-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="b76cb-137">A kézbesítetlen események tárolásához használt végpont.</span><span class="sxs-lookup"><span data-stu-id="b76cb-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="b76cb-138">Adja meg egy tár blobtárolójának Azure-erőforrás-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="b76cb-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="b76cb-139">Például: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="b76cb-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="b76cb-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76cb-140">-DefaultProfile</span></span>
<span data-ttu-id="b76cb-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b76cb-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76cb-142">-DomainName</span><span class="sxs-lookup"><span data-stu-id="b76cb-142">-DomainName</span></span>
<span data-ttu-id="b76cb-143">Annak a tartománynak a neve, amelyhez létre kell hozatni az esemény-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b76cb-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="b76cb-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="b76cb-144">-DomainTopicName</span></span>
<span data-ttu-id="b76cb-145">Annak a tartománytémakörnek a neve, amelyhez létre kell hozatni az esemény-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b76cb-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="b76cb-146">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="b76cb-146">-Endpoint</span></span>
<span data-ttu-id="b76cb-147">Esemény-előfizetés cél végpontja.</span><span class="sxs-lookup"><span data-stu-id="b76cb-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="b76cb-148">Ez lehet egy webhook URL-cím vagy egy EventHub-erőforrás Azure-erőforrásazonosítója, társor, hibrid összekapcsolás vagy szolgáltatásbusqueue.</span><span class="sxs-lookup"><span data-stu-id="b76cb-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="b76cb-149">A hibrid kapcsolat erőforrás-azonosítója például a következő űrlapot veszi fel: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="b76cb-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="b76cb-150">Az Eseményrács parancsmagok végrehajtása előtt várhatóan létre lesz hozva és használható lesz a cél végpont.</span><span class="sxs-lookup"><span data-stu-id="b76cb-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="b76cb-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="b76cb-151">-EndpointType</span></span>
<span data-ttu-id="b76cb-152">Végpont típusa.</span><span class="sxs-lookup"><span data-stu-id="b76cb-152">Endpoint Type.</span></span>
<span data-ttu-id="b76cb-153">Ez lehet webhook, eventhub, storagequeue, hybridconnection vagy servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="b76cb-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="b76cb-154">Az alapértelmezett érték a webhook.</span><span class="sxs-lookup"><span data-stu-id="b76cb-154">Default value is webhook.</span></span>

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

### <span data-ttu-id="b76cb-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b76cb-155">-EventSubscriptionName</span></span>
<span data-ttu-id="b76cb-156">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="b76cb-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="b76cb-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="b76cb-157">-EventTtl</span></span>
<span data-ttu-id="b76cb-158">Az esemény kézbesítési ideje percek alatt.</span><span class="sxs-lookup"><span data-stu-id="b76cb-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="b76cb-159">Ennek az értéknek 1 és 1440 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b76cb-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="b76cb-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="b76cb-160">-ExpirationDate</span></span>
<span data-ttu-id="b76cb-161">Az esemény-előfizetés lejárati DateTime-ját határozza meg, amely után az esemény-előfizetés kivezetve lesz.</span><span class="sxs-lookup"><span data-stu-id="b76cb-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="b76cb-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="b76cb-162">-IncludedEventType</span></span>
<span data-ttu-id="b76cb-163">Szűrő, amely megadja a szerepeltethető eseménytípusok listáját. Ha nincs megadva, az összes eseménytípus szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="b76cb-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="b76cb-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b76cb-164">-InputObject</span></span>
<span data-ttu-id="b76cb-165">EventGridSubscription objektum.</span><span class="sxs-lookup"><span data-stu-id="b76cb-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="b76cb-166">-Label</span><span class="sxs-lookup"><span data-stu-id="b76cb-166">-Label</span></span>
<span data-ttu-id="b76cb-167">Az esemény-előfizetés címkéi</span><span class="sxs-lookup"><span data-stu-id="b76cb-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="b76cb-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="b76cb-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="b76cb-169">Az esemény kézbesítésére irányuló kísérletek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="b76cb-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="b76cb-170">Ennek az értéknek 1 és 30 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b76cb-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="b76cb-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="b76cb-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="b76cb-172">Egy kötegben az események maximális száma.</span><span class="sxs-lookup"><span data-stu-id="b76cb-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="b76cb-173">Ennek az értéknek 1 és 5000 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b76cb-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="b76cb-174">Ez a paraméter csak akkor érvényes, ha az Endpint típusa csak webhook.</span><span class="sxs-lookup"><span data-stu-id="b76cb-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="b76cb-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="b76cb-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="b76cb-176">Az előnyben részesített köteg mérete kilobájtban.</span><span class="sxs-lookup"><span data-stu-id="b76cb-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="b76cb-177">Ennek az értéknek 1 és 1024 között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b76cb-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="b76cb-178">Ez a paraméter csak akkor érvényes, ha az Endpint típusa csak webhook.</span><span class="sxs-lookup"><span data-stu-id="b76cb-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="b76cb-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b76cb-179">-ResourceGroupName</span></span>
<span data-ttu-id="b76cb-180">A témakör erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="b76cb-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="b76cb-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b76cb-181">-ResourceId</span></span>
<span data-ttu-id="b76cb-182">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetést létrehozta.</span><span class="sxs-lookup"><span data-stu-id="b76cb-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="b76cb-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="b76cb-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="b76cb-184">Szűrő, amely meghatározza, hogy csak a megadott tárgyelőtagnak megfelelő eseményeket tartalmazza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="b76cb-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="b76cb-185">Ha nincs megadva, az összes tárgyelőtaggal megadott esemény szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="b76cb-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="b76cb-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="b76cb-186">-SubjectEndsWith</span></span>
<span data-ttu-id="b76cb-187">Szűrő, amely meghatározza, hogy csak a megadott tárgy utótaggal megegyező eseményeket tartalmazza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="b76cb-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="b76cb-188">Ha nincs megadva, akkor az összes tárgy utótaggal megadott esemény szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="b76cb-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="b76cb-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="b76cb-189">-TopicName</span></span>
<span data-ttu-id="b76cb-190">Annak a témakörnek a neve, amelyhez létre kell hozatni az esemény-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b76cb-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="b76cb-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b76cb-191">-Confirm</span></span>
<span data-ttu-id="b76cb-192">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b76cb-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b76cb-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b76cb-193">-WhatIf</span></span>
<span data-ttu-id="b76cb-194">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b76cb-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b76cb-195">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b76cb-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b76cb-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76cb-196">CommonParameters</span></span>
<span data-ttu-id="b76cb-197">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76cb-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76cb-198">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b76cb-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76cb-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b76cb-199">INPUTS</span></span>

### <span data-ttu-id="b76cb-200">System.String</span><span class="sxs-lookup"><span data-stu-id="b76cb-200">System.String</span></span>

### <span data-ttu-id="b76cb-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="b76cb-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="b76cb-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b76cb-202">OUTPUTS</span></span>

### <span data-ttu-id="b76cb-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="b76cb-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="b76cb-204">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b76cb-204">NOTES</span></span>

## <span data-ttu-id="b76cb-205">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b76cb-205">RELATED LINKS</span></span>
