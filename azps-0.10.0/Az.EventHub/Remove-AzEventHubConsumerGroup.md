---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: d4443cf25790d74617a02b048ce31296e451cf95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842294"
---
# <span data-ttu-id="df13f-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="df13f-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="df13f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df13f-102">SYNOPSIS</span></span>
<span data-ttu-id="df13f-103">Törli a megadott esemény-hubok fogyasztói csoportját.</span><span class="sxs-lookup"><span data-stu-id="df13f-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="df13f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df13f-104">SYNTAX</span></span>

### <span data-ttu-id="df13f-105">ConsumergroupPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df13f-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df13f-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="df13f-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df13f-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df13f-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df13f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="df13f-108">DESCRIPTION</span></span>
<span data-ttu-id="df13f-109">A Remove-AzEventHubConsumerGroup parancsmag eltávolítja és törli a megadott fogyasztói csoportot az adott esemény központból.</span><span class="sxs-lookup"><span data-stu-id="df13f-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="df13f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="df13f-110">EXAMPLES</span></span>

### <span data-ttu-id="df13f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="df13f-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="df13f-112">Törli a fogyasztói csoport \` MyConsumerGroupName \` az esemény központi \` MyEventHubName \` , amely a \` MyNamespaceName névtérre van korlátozva \` .</span><span class="sxs-lookup"><span data-stu-id="df13f-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="df13f-113">Példa 2,1-InputObject – változó használata</span><span class="sxs-lookup"><span data-stu-id="df13f-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="df13f-114">Példa 2,2-InputObject – csővezetékek használata</span><span class="sxs-lookup"><span data-stu-id="df13f-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="df13f-115">Példa 3,1-ResourceId változó használatával</span><span class="sxs-lookup"><span data-stu-id="df13f-115">Example 3.1 - ResourceId Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="df13f-116">Példa 3,2-ResourceId karakterlánc használatával</span><span class="sxs-lookup"><span data-stu-id="df13f-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="df13f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df13f-117">PARAMETERS</span></span>

### <span data-ttu-id="df13f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df13f-118">-AsJob</span></span>
<span data-ttu-id="df13f-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="df13f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df13f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df13f-120">-DefaultProfile</span></span>
<span data-ttu-id="df13f-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df13f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df13f-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="df13f-122">-EventHub</span></span>
<span data-ttu-id="df13f-123">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="df13f-123">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df13f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df13f-124">-InputObject</span></span>
<span data-ttu-id="df13f-125">ConsumerGroup objektum</span><span class="sxs-lookup"><span data-stu-id="df13f-125">ConsumerGroup Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes
Parameter Sets: ConsumergroupInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df13f-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df13f-126">-Name</span></span>
<span data-ttu-id="df13f-127">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="df13f-127">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df13f-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="df13f-128">-Namespace</span></span>
<span data-ttu-id="df13f-129">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="df13f-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df13f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df13f-130">-PassThru</span></span>
<span data-ttu-id="df13f-131">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="df13f-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="df13f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df13f-132">-ResourceGroupName</span></span>
<span data-ttu-id="df13f-133">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="df13f-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df13f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df13f-134">-ResourceId</span></span>
<span data-ttu-id="df13f-135">ConsumerGroup erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="df13f-135">ConsumerGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df13f-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df13f-136">-Confirm</span></span>
<span data-ttu-id="df13f-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df13f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df13f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df13f-138">-WhatIf</span></span>
<span data-ttu-id="df13f-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df13f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df13f-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df13f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df13f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df13f-141">CommonParameters</span></span>
<span data-ttu-id="df13f-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df13f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df13f-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df13f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df13f-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df13f-144">INPUTS</span></span>

### <span data-ttu-id="df13f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="df13f-145">System.String</span></span>

### <span data-ttu-id="df13f-146">Microsoft. Azure. Command. EventHub. models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="df13f-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="df13f-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df13f-147">OUTPUTS</span></span>

### <span data-ttu-id="df13f-148">System. Void</span><span class="sxs-lookup"><span data-stu-id="df13f-148">System.Void</span></span>

## <span data-ttu-id="df13f-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df13f-149">NOTES</span></span>

## <span data-ttu-id="df13f-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df13f-150">RELATED LINKS</span></span>
