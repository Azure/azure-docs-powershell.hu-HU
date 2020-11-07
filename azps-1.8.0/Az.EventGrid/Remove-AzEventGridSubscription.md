---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: fd872830f82f1d75f0b3c5f60ba6b129d7edd6f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670866"
---
# <span data-ttu-id="2c5b8-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2c5b8-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="2c5b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c5b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c5b8-103">Azure Event Grid esemény-előfizetés eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="2c5b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c5b8-104">SYNTAX</span></span>

### <span data-ttu-id="2c5b8-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c5b8-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c5b8-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c5b8-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c5b8-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c5b8-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c5b8-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c5b8-108">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c5b8-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c5b8-109">DESCRIPTION</span></span>
<span data-ttu-id="2c5b8-110">Azure Event Grid-eseményre szóló előfizetés eltávolítása az Azure-esemény rácsvonalai témához, erőforráshoz, Azure-előfizetéshez vagy erőforrás-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="2c5b8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2c5b8-111">EXAMPLES</span></span>

### <span data-ttu-id="2c5b8-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2c5b8-112">Example 1</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2c5b8-113">Eltávolítja az esemény-előfizetést az \` \` Azure-esemény EventSubscription1 az \` \` erőforráscsoport- \` MyResourceGroupName téma1 \` .</span><span class="sxs-lookup"><span data-stu-id="2c5b8-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2c5b8-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="2c5b8-114">Example 2</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2c5b8-115">Eltávolítja az esemény-előfizetést \` EventSubscription1 \` egy erőforráscsoport- \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2c5b8-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2c5b8-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="2c5b8-116">Example 3</span></span>
```
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2c5b8-117">Eltávolítja az esemény-előfizetést \` \` az alapértelmezett Azure-előfizetésre EventSubscription1.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="2c5b8-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="2c5b8-118">Example 4</span></span>
```
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2c5b8-119">Eltávolítja az esemény-előfizetési \` EventSubscription1 az \` esemény-hub-névtérbe.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="2c5b8-120">Példa 5</span><span class="sxs-lookup"><span data-stu-id="2c5b8-120">Example 5</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2c5b8-121">Eltávolítja az esemény-előfizetést az \` EventSubscription1 \` -témára.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="2c5b8-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c5b8-122">PARAMETERS</span></span>

### <span data-ttu-id="2c5b8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c5b8-123">-DefaultProfile</span></span>
<span data-ttu-id="2c5b8-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2c5b8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c5b8-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2c5b8-125">-EventSubscriptionName</span></span>
<span data-ttu-id="2c5b8-126">Annak az esemény-előfizetésnek a neve, amelyet el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-126">Name of the event subscription that needs to be removed.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c5b8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c5b8-127">-InputObject</span></span>
<span data-ttu-id="2c5b8-128">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="2c5b8-128">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="2c5b8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c5b8-129">-PassThru</span></span>
<span data-ttu-id="2c5b8-130">Az eltávolítási művelet állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="2c5b8-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c5b8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c5b8-132">-ResourceGroupName</span></span>
<span data-ttu-id="2c5b8-133">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="2c5b8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c5b8-134">-ResourceId</span></span>
<span data-ttu-id="2c5b8-135">Annak az erőforrásnak az azonosítója, akinek az esemény-előfizetését el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="2c5b8-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="2c5b8-136">-TopicName</span></span>
<span data-ttu-id="2c5b8-137">Az esemény rácsvonala téma neve.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-137">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="2c5b8-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c5b8-138">-Confirm</span></span>
<span data-ttu-id="2c5b8-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c5b8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c5b8-140">-WhatIf</span></span>
<span data-ttu-id="2c5b8-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c5b8-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c5b8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c5b8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5b8-143">CommonParameters</span></span>
<span data-ttu-id="2c5b8-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c5b8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5b8-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c5b8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5b8-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c5b8-146">INPUTS</span></span>

### <span data-ttu-id="2c5b8-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2c5b8-147">System.String</span></span>

### <span data-ttu-id="2c5b8-148">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="2c5b8-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="2c5b8-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c5b8-149">OUTPUTS</span></span>

### <span data-ttu-id="2c5b8-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c5b8-150">System.Boolean</span></span>

## <span data-ttu-id="2c5b8-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c5b8-151">NOTES</span></span>

## <span data-ttu-id="2c5b8-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c5b8-152">RELATED LINKS</span></span>
