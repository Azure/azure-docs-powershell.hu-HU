---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: a6f821f094594fb00863f5dce2134f6702cfa8e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502592"
---
# <span data-ttu-id="acbf2-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="acbf2-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="acbf2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="acbf2-102">SYNOPSIS</span></span>
<span data-ttu-id="acbf2-103">Beolvassa az esemény előfizetésének részleteit, vagy megkapja az aktuális Azure-előfizetésben az összes esemény-előfizetés listáját.</span><span class="sxs-lookup"><span data-stu-id="acbf2-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acbf2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="acbf2-104">SYNTAX</span></span>

### <span data-ttu-id="acbf2-105">EventSubscriptionTopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="acbf2-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acbf2-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="acbf2-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acbf2-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="acbf2-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acbf2-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="acbf2-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="acbf2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="acbf2-109">DESCRIPTION</span></span>
<span data-ttu-id="acbf2-110">A Get-AzureRmEventGridSubscription parancsmag a megadott esemény rácsra szóló előfizetésének részleteire, illetve az aktuális Azure-előfizetésben vagy az erőforráscsoport-előfizetések listájára kerül.</span><span class="sxs-lookup"><span data-stu-id="acbf2-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="acbf2-111">Ha az esemény-előfizetés neve meg van határozva, az egyetlen eseményből álló rácsra szóló előfizetés adatait adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="acbf2-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="acbf2-112">Ha az esemény-előfizetés neve nincs megadva, a program az esemény-előfizetések listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="acbf2-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="acbf2-113">Példák</span><span class="sxs-lookup"><span data-stu-id="acbf2-113">EXAMPLES</span></span>

### <span data-ttu-id="acbf2-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="acbf2-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="acbf2-115">A \` EventSubscription1 \` \` téma1 \` az erőforráscsoport MyResourceGroupName című témakörben létrehozott esemény- \` előfizetési adatok részleteit kapja meg \` .</span><span class="sxs-lookup"><span data-stu-id="acbf2-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="acbf2-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="acbf2-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="acbf2-117">A \` \` téma1 az erőforráscsoport MyResourceGroupName, a teljes végpont URL-EventSubscription1 létrehozott esemény-előfizetési adatok részleteit kapja \` \` \` \` meg, ha ez egy webhorogon alapuló esemény előfizetése.</span><span class="sxs-lookup"><span data-stu-id="acbf2-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="acbf2-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="acbf2-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="acbf2-119">Ebben a témakörben megtalálhatja az \` erőforráscsoport-MyResourceGroupName létrehozott téma1-előfizetések listáját \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="acbf2-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="acbf2-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="acbf2-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="acbf2-121">A EventSubscription1 MyResourceGroupName létrehozott esemény-előfizetési adatok részleteit kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="acbf2-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="acbf2-122">Példa 5</span><span class="sxs-lookup"><span data-stu-id="acbf2-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="acbf2-123">Az \` \` aktuálisan kijelölt Azure-előfizetéshez létrehozott EventSubscription1-előfizetés részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="acbf2-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="acbf2-124">6. példa</span><span class="sxs-lookup"><span data-stu-id="acbf2-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="acbf2-125">Megkapja az erőforráscsoport MyResourceGroupName létrehozott összes globális esemény-előfizetés listáját \` \` .</span><span class="sxs-lookup"><span data-stu-id="acbf2-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="acbf2-126">7. példa</span><span class="sxs-lookup"><span data-stu-id="acbf2-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="acbf2-127">Az aktuálisan kijelölt Azure-előfizetésből létrehozott összes globális esemény-előfizetés listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="acbf2-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="acbf2-128">8. példa</span><span class="sxs-lookup"><span data-stu-id="acbf2-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="acbf2-129">A megadott hely westus2 az erőforráscsoport MyResourceGroupName létrehozott összes regionális esemény-előfizetésből álló listát kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="acbf2-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="acbf2-130">Példa 9</span><span class="sxs-lookup"><span data-stu-id="acbf2-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="acbf2-131">A megadott EventHub-névtérhez létrehozott összes esemény-előfizetés listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="acbf2-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="acbf2-132">10. példa</span><span class="sxs-lookup"><span data-stu-id="acbf2-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="acbf2-133">A megadott helyen lévő adott témakörhöz (EventHub-névterekhez) létrehozott összes esemény-előfizetés listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="acbf2-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="acbf2-134">Példa 11</span><span class="sxs-lookup"><span data-stu-id="acbf2-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="acbf2-135">Az adott erőforráscsoport számára létrehozott összes esemény-előfizetés listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="acbf2-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="acbf2-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="acbf2-136">PARAMETERS</span></span>

### <span data-ttu-id="acbf2-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbf2-137">-DefaultProfile</span></span>
<span data-ttu-id="acbf2-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="acbf2-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbf2-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="acbf2-139">-EventSubscriptionName</span></span>
<span data-ttu-id="acbf2-140">Az esemény-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="acbf2-140">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf2-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="acbf2-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="acbf2-142">Adja meg az esemény-előfizetés célhelyének teljes URL-címét.</span><span class="sxs-lookup"><span data-stu-id="acbf2-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbf2-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acbf2-143">-InputObject</span></span>
<span data-ttu-id="acbf2-144">EventGrid-esemény előfizetési objektuma.</span><span class="sxs-lookup"><span data-stu-id="acbf2-144">EventGrid Event Subscription object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf2-145">-Hely</span><span class="sxs-lookup"><span data-stu-id="acbf2-145">-Location</span></span>
<span data-ttu-id="acbf2-146">Helyre</span><span class="sxs-lookup"><span data-stu-id="acbf2-146">Location</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf2-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acbf2-147">-ResourceGroupName</span></span>
<span data-ttu-id="acbf2-148">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="acbf2-148">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf2-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acbf2-149">-ResourceId</span></span>
<span data-ttu-id="acbf2-150">Annak az erőforrásnak az azonosítója, amelyhez az esemény-előfizetéseket létrehozták.</span><span class="sxs-lookup"><span data-stu-id="acbf2-150">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf2-151">-TopicName</span><span class="sxs-lookup"><span data-stu-id="acbf2-151">-TopicName</span></span>
<span data-ttu-id="acbf2-152">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="acbf2-152">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf2-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="acbf2-153">-TopicTypeName</span></span>
<span data-ttu-id="acbf2-154">TopicType neve</span><span class="sxs-lookup"><span data-stu-id="acbf2-154">TopicType name</span></span>

```yaml
Type: String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acbf2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbf2-155">CommonParameters</span></span>
<span data-ttu-id="acbf2-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="acbf2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbf2-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acbf2-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbf2-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="acbf2-158">INPUTS</span></span>

### <span data-ttu-id="acbf2-159">System. String</span><span class="sxs-lookup"><span data-stu-id="acbf2-159">System.String</span></span>
<span data-ttu-id="acbf2-160">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="acbf2-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="acbf2-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acbf2-161">OUTPUTS</span></span>

### <span data-ttu-id="acbf2-162">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="acbf2-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>
<span data-ttu-id="acbf2-163">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventGrid. models. PSEventSubscriptionListInstance, Microsoft. Azure. commands. EventGrid, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="acbf2-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscriptionListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="acbf2-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="acbf2-164">NOTES</span></span>

## <span data-ttu-id="acbf2-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acbf2-165">RELATED LINKS</span></span>

