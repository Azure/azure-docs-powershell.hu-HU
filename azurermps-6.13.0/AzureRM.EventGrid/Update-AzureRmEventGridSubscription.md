---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: d036ba2df289b0b2f84430f01000632a887ec20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680368"
---
# <span data-ttu-id="3b10d-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3b10d-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="3b10d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b10d-102">SYNOPSIS</span></span>
<span data-ttu-id="3b10d-103">Az esemény rácsa esemény-előfizetés tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="3b10d-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b10d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b10d-104">SYNTAX</span></span>

### <span data-ttu-id="3b10d-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b10d-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b10d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b10d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b10d-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3b10d-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b10d-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b10d-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b10d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b10d-109">DESCRIPTION</span></span>
<span data-ttu-id="3b10d-110">Az esemény rácsa esemény-előfizetés tulajdonságainak frissítése</span><span class="sxs-lookup"><span data-stu-id="3b10d-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="3b10d-111">Ez a funkció a meglévő esemény-előfizetések szűrő, cél vagy címkék frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="3b10d-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="3b10d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="3b10d-112">EXAMPLES</span></span>

### <span data-ttu-id="3b10d-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b10d-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="3b10d-114">Frissíti az esemény-előfizetési ES1 végpontját a \` \` témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="3b10d-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="3b10d-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="3b10d-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="3b10d-116">Frissíti az esemény-előfizetési ES1 végpontját a \` \` témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="3b10d-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="3b10d-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="3b10d-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="3b10d-118">A \` \` EventHub-névtér ContosoNamespace az új végponttal \` https://requestb.in/1kxxoui1\ "és az új SubjectEndsWith-szűrő jpg-ként" ES1 frissíti az esemény-előfizetés tulajdonságait. \`\`</span><span class="sxs-lookup"><span data-stu-id="3b10d-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="3b10d-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="3b10d-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="3b10d-120">Frissíti az erőforráscsoport MyResourceGroupName tartozó esemény-előfizetési \` ES1 tulajdonságait \` \` \` az új címkék $labels.</span><span class="sxs-lookup"><span data-stu-id="3b10d-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="3b10d-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b10d-121">PARAMETERS</span></span>

### <span data-ttu-id="3b10d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b10d-122">-DefaultProfile</span></span>
<span data-ttu-id="3b10d-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b10d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b10d-124">-Végpont</span><span class="sxs-lookup"><span data-stu-id="3b10d-124">-Endpoint</span></span>
<span data-ttu-id="3b10d-125">Esemény-előfizetés cél végpontja.</span><span class="sxs-lookup"><span data-stu-id="3b10d-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="3b10d-126">Ez lehet egy webhorog URL-címe vagy egy EventHub Azure erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3b10d-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

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

### <span data-ttu-id="3b10d-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="3b10d-127">-EndpointType</span></span>
<span data-ttu-id="3b10d-128">Végpont típusa.</span><span class="sxs-lookup"><span data-stu-id="3b10d-128">Endpoint Type.</span></span>
<span data-ttu-id="3b10d-129">Ez lehet webhook vagy eventhub</span><span class="sxs-lookup"><span data-stu-id="3b10d-129">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b10d-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3b10d-130">-EventSubscriptionName</span></span>
<span data-ttu-id="3b10d-131">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="3b10d-131">The name of the event subscription</span></span>

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

### <span data-ttu-id="3b10d-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="3b10d-132">-IncludedEventType</span></span>
<span data-ttu-id="3b10d-133">Szűrő, amely a szerepeltetni kívánt eseménytípus listáját adja meg. Ha nincs megadva, az összes eseménytípus szerepelni fog.</span><span class="sxs-lookup"><span data-stu-id="3b10d-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="3b10d-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b10d-134">-InputObject</span></span>
<span data-ttu-id="3b10d-135">EventGridSubscription objektum</span><span class="sxs-lookup"><span data-stu-id="3b10d-135">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b10d-136">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="3b10d-136">-Label</span></span>
<span data-ttu-id="3b10d-137">Az esemény-előfizetés címkéi</span><span class="sxs-lookup"><span data-stu-id="3b10d-137">Labels for the event subscription</span></span>

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

### <span data-ttu-id="3b10d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b10d-138">-ResourceGroupName</span></span>
<span data-ttu-id="3b10d-139">A témakör erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="3b10d-139">The resource group of the topic.</span></span>

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

### <span data-ttu-id="3b10d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b10d-140">-ResourceId</span></span>
<span data-ttu-id="3b10d-141">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetést létrehozták.</span><span class="sxs-lookup"><span data-stu-id="3b10d-141">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="3b10d-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="3b10d-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="3b10d-143">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi előtaghoz tartozó eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="3b10d-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="3b10d-144">Ha nem adja meg, akkor az összes tárgy előtagokkal rendelkező események is szerepelni fognak.</span><span class="sxs-lookup"><span data-stu-id="3b10d-144">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="3b10d-145">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="3b10d-145">-SubjectEndsWith</span></span>
<span data-ttu-id="3b10d-146">Szűrő, amely azt adja meg, hogy a program csak a megadott tárgyi utótaggal egyező eseményeket fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="3b10d-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="3b10d-147">Ha nem adja meg, a program az összes tárgyi utótaggal rendelkező eseményeket is belefoglalja.</span><span class="sxs-lookup"><span data-stu-id="3b10d-147">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="3b10d-148">-TopicName</span><span class="sxs-lookup"><span data-stu-id="3b10d-148">-TopicName</span></span>
<span data-ttu-id="3b10d-149">Annak a témakörnek a neve, amelyhez az esemény-előfizetést létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="3b10d-149">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="3b10d-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b10d-150">-Confirm</span></span>
<span data-ttu-id="3b10d-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b10d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b10d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b10d-152">-WhatIf</span></span>
<span data-ttu-id="3b10d-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b10d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b10d-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b10d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b10d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b10d-155">CommonParameters</span></span>
<span data-ttu-id="3b10d-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b10d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b10d-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b10d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b10d-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b10d-158">INPUTS</span></span>

### <span data-ttu-id="3b10d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="3b10d-159">System.String</span></span>

### <span data-ttu-id="3b10d-160">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="3b10d-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>
<span data-ttu-id="3b10d-161">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3b10d-161">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3b10d-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b10d-162">OUTPUTS</span></span>

### <span data-ttu-id="3b10d-163">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="3b10d-163">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="3b10d-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b10d-164">NOTES</span></span>

## <span data-ttu-id="3b10d-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b10d-165">RELATED LINKS</span></span>
