---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: a15cb222108d79544d38ce730897e03fa61066ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505048"
---
# <span data-ttu-id="9abc0-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="9abc0-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="9abc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9abc0-102">SYNOPSIS</span></span>
<span data-ttu-id="9abc0-103">Azure Event Grid esemény-előfizetés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9abc0-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9abc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9abc0-104">SYNTAX</span></span>

### <span data-ttu-id="9abc0-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9abc0-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abc0-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9abc0-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abc0-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9abc0-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abc0-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9abc0-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9abc0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9abc0-109">DESCRIPTION</span></span>
<span data-ttu-id="9abc0-110">Azure Event Grid-eseményre szóló előfizetés eltávolítása az Azure-esemény rácsvonalai témához, erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="9abc0-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="9abc0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9abc0-111">EXAMPLES</span></span>

### <span data-ttu-id="9abc0-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9abc0-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="9abc0-113">Eltávolítja az esemény-előfizetést az \` \` Azure-esemény EventSubscription1 az \` \` erőforráscsoport- \` MyResourceGroupName téma1 \` .</span><span class="sxs-lookup"><span data-stu-id="9abc0-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9abc0-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9abc0-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="9abc0-115">Eltávolítja az esemény-előfizetést \` EventSubscription1 \` egy erőforráscsoport- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9abc0-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9abc0-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="9abc0-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="9abc0-117">Eltávolítja az esemény-előfizetést \` \` az alapértelmezett Azure-előfizetésre EventSubscription1.</span><span class="sxs-lookup"><span data-stu-id="9abc0-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="9abc0-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="9abc0-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="9abc0-119">Eltávolítja az esemény-előfizetési \` EventSubscription1 az \` esemény-hub-névtérbe.</span><span class="sxs-lookup"><span data-stu-id="9abc0-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="9abc0-120">Példa 5</span><span class="sxs-lookup"><span data-stu-id="9abc0-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="9abc0-121">Eltávolítja az esemény-előfizetést az \` EventSubscription1 \` -témára.</span><span class="sxs-lookup"><span data-stu-id="9abc0-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="9abc0-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9abc0-122">PARAMETERS</span></span>

### <span data-ttu-id="9abc0-123">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9abc0-123">-EventSubscriptionName</span></span>
<span data-ttu-id="9abc0-124">Annak az esemény-előfizetésnek a neve, amelyet el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="9abc0-124">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="9abc0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9abc0-125">-InputObject</span></span>
<span data-ttu-id="9abc0-126">EventGrid EventSubscription objektum</span><span class="sxs-lookup"><span data-stu-id="9abc0-126">EventGrid EventSubscription object.</span></span>

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

### <span data-ttu-id="9abc0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9abc0-127">-PassThru</span></span>
<span data-ttu-id="9abc0-128">Az eltávolítási művelet állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="9abc0-128">Returns the status of the Remove operation.</span></span> <span data-ttu-id="9abc0-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9abc0-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9abc0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9abc0-130">-ResourceGroupName</span></span>
<span data-ttu-id="9abc0-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9abc0-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="9abc0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9abc0-132">-ResourceId</span></span>
<span data-ttu-id="9abc0-133">Annak az erőforrásnak az azonosítója, akinek az esemény-előfizetését el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="9abc0-133">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="9abc0-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="9abc0-134">-TopicName</span></span>
<span data-ttu-id="9abc0-135">Az esemény rácsvonala téma neve.</span><span class="sxs-lookup"><span data-stu-id="9abc0-135">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="9abc0-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9abc0-136">-Confirm</span></span>
<span data-ttu-id="9abc0-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9abc0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9abc0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9abc0-138">-WhatIf</span></span>
<span data-ttu-id="9abc0-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9abc0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9abc0-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9abc0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9abc0-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abc0-141">-DefaultProfile</span></span>
<span data-ttu-id="9abc0-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9abc0-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9abc0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abc0-143">CommonParameters</span></span>
<span data-ttu-id="9abc0-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9abc0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abc0-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9abc0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abc0-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9abc0-146">INPUTS</span></span>

### <span data-ttu-id="9abc0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9abc0-147">System.String</span></span>
<span data-ttu-id="9abc0-148">Microsoft. Azure. Command. EventGrid. models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="9abc0-148">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="9abc0-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9abc0-149">OUTPUTS</span></span>

### <span data-ttu-id="9abc0-150">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="9abc0-150">System.Object</span></span>

## <span data-ttu-id="9abc0-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9abc0-151">NOTES</span></span>

## <span data-ttu-id="9abc0-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9abc0-152">RELATED LINKS</span></span>

