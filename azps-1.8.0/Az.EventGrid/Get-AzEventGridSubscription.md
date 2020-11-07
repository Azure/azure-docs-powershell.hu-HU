---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670880"
---
# <span data-ttu-id="a9718-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a9718-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="a9718-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9718-102">SYNOPSIS</span></span>
<span data-ttu-id="a9718-103">Beolvassa az esemény előfizetésének részleteit, vagy megkapja az aktuális Azure-előfizetésben az összes esemény-előfizetés listáját.</span><span class="sxs-lookup"><span data-stu-id="a9718-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="a9718-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9718-104">SYNTAX</span></span>

### <span data-ttu-id="a9718-105">EventSubscriptionTopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9718-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9718-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9718-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9718-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9718-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9718-108">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9718-108">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9718-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9718-109">DESCRIPTION</span></span>
<span data-ttu-id="a9718-110">A Get-AzEventGridSubscription parancsmag a megadott esemény rácsra szóló előfizetésének részleteire, illetve az aktuális Azure-előfizetésben vagy az erőforráscsoport-előfizetések listájára kerül.</span><span class="sxs-lookup"><span data-stu-id="a9718-110">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="a9718-111">Ha az esemény-előfizetés neve meg van határozva, az egyetlen eseményből álló rácsra szóló előfizetés adatait adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a9718-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="a9718-112">Ha az esemény-előfizetés neve nincs megadva, a program az esemény-előfizetések listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="a9718-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="a9718-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a9718-113">EXAMPLES</span></span>

### <span data-ttu-id="a9718-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a9718-114">Example 1</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9718-115">A \` EventSubscription1 \` \` téma1 \` az erőforráscsoport MyResourceGroupName című témakörben létrehozott esemény- \` előfizetési adatok részleteit kapja meg \` .</span><span class="sxs-lookup"><span data-stu-id="a9718-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a9718-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="a9718-116">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="a9718-117">A \` \` téma1 az erőforráscsoport MyResourceGroupName, a teljes végpont URL-EventSubscription1 létrehozott esemény-előfizetési adatok részleteit kapja \` \` \` \` meg, ha ez egy webhorogon alapuló esemény előfizetése.</span><span class="sxs-lookup"><span data-stu-id="a9718-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="a9718-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="a9718-118">Example 3</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="a9718-119">Ebben a témakörben megtalálhatja az \` erőforráscsoport-MyResourceGroupName létrehozott téma1-előfizetések listáját \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="a9718-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a9718-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="a9718-120">Example 4</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9718-121">A EventSubscription1 MyResourceGroupName létrehozott esemény-előfizetési adatok részleteit kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="a9718-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a9718-122">Példa 5</span><span class="sxs-lookup"><span data-stu-id="a9718-122">Example 5</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a9718-123">Az \` \` aktuálisan kijelölt Azure-előfizetéshez létrehozott EventSubscription1-előfizetés részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a9718-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="a9718-124">6. példa</span><span class="sxs-lookup"><span data-stu-id="a9718-124">Example 6</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a9718-125">Megkapja az erőforráscsoport MyResourceGroupName létrehozott összes globális esemény-előfizetés listáját \` \` .</span><span class="sxs-lookup"><span data-stu-id="a9718-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a9718-126">7. példa</span><span class="sxs-lookup"><span data-stu-id="a9718-126">Example 7</span></span>
```
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="a9718-127">Az aktuálisan kijelölt Azure-előfizetésből létrehozott összes globális esemény-előfizetés listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a9718-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="a9718-128">8. példa</span><span class="sxs-lookup"><span data-stu-id="a9718-128">Example 8</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="a9718-129">A megadott hely westus2 az erőforráscsoport MyResourceGroupName létrehozott összes regionális esemény-előfizetésből álló listát kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="a9718-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="a9718-130">Példa 9</span><span class="sxs-lookup"><span data-stu-id="a9718-130">Example 9</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="a9718-131">A megadott EventHub-névtérhez létrehozott összes esemény-előfizetés listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a9718-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="a9718-132">10. példa</span><span class="sxs-lookup"><span data-stu-id="a9718-132">Example 10</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="a9718-133">A megadott helyen lévő adott témakörhöz (EventHub-névterekhez) létrehozott összes esemény-előfizetés listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9718-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="a9718-134">Példa 11</span><span class="sxs-lookup"><span data-stu-id="a9718-134">Example 11</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a9718-135">Az adott erőforráscsoport számára létrehozott összes esemény-előfizetés listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="a9718-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="a9718-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9718-136">PARAMETERS</span></span>

### <span data-ttu-id="a9718-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9718-137">-DefaultProfile</span></span>
<span data-ttu-id="a9718-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a9718-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9718-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a9718-139">-EventSubscriptionName</span></span>
<span data-ttu-id="a9718-140">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="a9718-140">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9718-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="a9718-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="a9718-142">Adja meg az esemény-előfizetés célhelyének teljes URL-címét.</span><span class="sxs-lookup"><span data-stu-id="a9718-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9718-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9718-143">-InputObject</span></span>
<span data-ttu-id="a9718-144">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="a9718-144">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a9718-145">-Hely</span><span class="sxs-lookup"><span data-stu-id="a9718-145">-Location</span></span>
<span data-ttu-id="a9718-146">Helyre</span><span class="sxs-lookup"><span data-stu-id="a9718-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9718-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9718-147">-ResourceGroupName</span></span>
<span data-ttu-id="a9718-148">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a9718-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9718-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9718-149">-ResourceId</span></span>
<span data-ttu-id="a9718-150">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetéseket létrehozták.</span><span class="sxs-lookup"><span data-stu-id="a9718-150">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9718-151">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a9718-151">-TopicName</span></span>
<span data-ttu-id="a9718-152">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="a9718-152">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9718-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="a9718-153">-TopicTypeName</span></span>
<span data-ttu-id="a9718-154">TopicType neve</span><span class="sxs-lookup"><span data-stu-id="a9718-154">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9718-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9718-155">CommonParameters</span></span>
<span data-ttu-id="a9718-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9718-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9718-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9718-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9718-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9718-158">INPUTS</span></span>

### <span data-ttu-id="a9718-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a9718-159">System.String</span></span>

### <span data-ttu-id="a9718-160">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a9718-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a9718-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9718-161">OUTPUTS</span></span>

### <span data-ttu-id="a9718-162">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a9718-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a9718-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9718-163">NOTES</span></span>

## <span data-ttu-id="a9718-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9718-164">RELATED LINKS</span></span>
