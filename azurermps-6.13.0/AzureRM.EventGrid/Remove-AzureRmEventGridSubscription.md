---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: 82d386fb0834db3de03d5692ad8b7a241b6eed90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497475"
---
# <span data-ttu-id="b9b2c-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b9b2c-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="b9b2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b2c-103">Azure Event Grid esemény-előfizetés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9b2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9b2c-104">SYNTAX</span></span>

### <span data-ttu-id="b9b2c-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9b2c-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b2c-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9b2c-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b2c-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b9b2c-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b2c-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9b2c-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9b2c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9b2c-109">DESCRIPTION</span></span>
<span data-ttu-id="b9b2c-110">Azure Event Grid-eseményre szóló előfizetés eltávolítása az Azure-esemény rácsvonalai témához, erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="b9b2c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b9b2c-111">EXAMPLES</span></span>

### <span data-ttu-id="b9b2c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b9b2c-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b9b2c-113">Eltávolítja az esemény-előfizetést az \` \` Azure-esemény EventSubscription1 az \` \` erőforráscsoport- \` MyResourceGroupName téma1 \` .</span><span class="sxs-lookup"><span data-stu-id="b9b2c-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b9b2c-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="b9b2c-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b9b2c-115">Eltávolítja az esemény-előfizetést \` EventSubscription1 \` egy erőforráscsoport- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b9b2c-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b9b2c-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="b9b2c-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b9b2c-117">Eltávolítja az esemény-előfizetést \` \` az alapértelmezett Azure-előfizetésre EventSubscription1.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="b9b2c-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="b9b2c-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b9b2c-119">Eltávolítja az esemény-előfizetési \` EventSubscription1 az \` esemény-hub-névtérbe.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="b9b2c-120">Példa 5</span><span class="sxs-lookup"><span data-stu-id="b9b2c-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b9b2c-121">Eltávolítja az esemény-előfizetést az \` EventSubscription1 \` -témára.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="b9b2c-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9b2c-122">PARAMETERS</span></span>

### <span data-ttu-id="b9b2c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b2c-123">-DefaultProfile</span></span>
<span data-ttu-id="b9b2c-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b9b2c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9b2c-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b9b2c-125">-EventSubscriptionName</span></span>
<span data-ttu-id="b9b2c-126">Annak az esemény-előfizetésnek a neve, amelyet el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-126">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
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

### <span data-ttu-id="b9b2c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9b2c-127">-InputObject</span></span>
<span data-ttu-id="b9b2c-128">EventGrid EventSubscription objektum</span><span class="sxs-lookup"><span data-stu-id="b9b2c-128">EventGrid EventSubscription object.</span></span>

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

### <span data-ttu-id="b9b2c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9b2c-129">-PassThru</span></span>
<span data-ttu-id="b9b2c-130">Az eltávolítási művelet állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="b9b2c-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b9b2c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b2c-132">-ResourceGroupName</span></span>
<span data-ttu-id="b9b2c-133">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-133">Resource Group Name.</span></span>

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
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b2c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9b2c-134">-ResourceId</span></span>
<span data-ttu-id="b9b2c-135">Annak az erőforrásnak az azonosítója, akinek az esemény-előfizetését el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="b9b2c-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="b9b2c-136">-TopicName</span></span>
<span data-ttu-id="b9b2c-137">Az esemény rácsvonala téma neve.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-137">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b2c-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9b2c-138">-Confirm</span></span>
<span data-ttu-id="b9b2c-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b2c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b2c-140">-WhatIf</span></span>
<span data-ttu-id="b9b2c-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b2c-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9b2c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b2c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b2c-143">CommonParameters</span></span>
<span data-ttu-id="b9b2c-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9b2c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b2c-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9b2c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b2c-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9b2c-146">INPUTS</span></span>

### <span data-ttu-id="b9b2c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b9b2c-147">System.String</span></span>

### <span data-ttu-id="b9b2c-148">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="b9b2c-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="b9b2c-149">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9b2c-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b9b2c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9b2c-150">OUTPUTS</span></span>

### <span data-ttu-id="b9b2c-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9b2c-151">System.Boolean</span></span>

## <span data-ttu-id="b9b2c-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9b2c-152">NOTES</span></span>

## <span data-ttu-id="b9b2c-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9b2c-153">RELATED LINKS</span></span>
