---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: f84464d366ae84cf0a83ecc616a80b90475af8d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155667"
---
# <span data-ttu-id="da6b9-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="da6b9-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="da6b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="da6b9-103">Törli a megadott Eseményközpontok fogyasztói csoportot.</span><span class="sxs-lookup"><span data-stu-id="da6b9-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="da6b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da6b9-104">SYNTAX</span></span>

### <span data-ttu-id="da6b9-105">ConsumergroupPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da6b9-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da6b9-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="da6b9-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da6b9-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da6b9-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da6b9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da6b9-108">DESCRIPTION</span></span>
<span data-ttu-id="da6b9-109">A Remove-AzEventHubConsumerGroup parancsmag eltávolítja és törli a megadott fogyasztói csoportot az adott Eseményközpontból.</span><span class="sxs-lookup"><span data-stu-id="da6b9-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="da6b9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da6b9-110">EXAMPLES</span></span>

### <span data-ttu-id="da6b9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="da6b9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="da6b9-112">Törli a \` MyConsumerGroupName fogyasztói csoportot a MyEventHubName eseményközpontból, amely a \` \` \` \` MyNamespaceName \` névtérre terjed ki.</span><span class="sxs-lookup"><span data-stu-id="da6b9-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="da6b9-113">2. példa: InputObject – Változó használata</span><span class="sxs-lookup"><span data-stu-id="da6b9-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="da6b9-114">3. példa: InputObject – Piping használata</span><span class="sxs-lookup"><span data-stu-id="da6b9-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="da6b9-115">4. példa: Erőforrásazonosító változó használatával</span><span class="sxs-lookup"><span data-stu-id="da6b9-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="da6b9-116">5. példa: ResourceId using string</span><span class="sxs-lookup"><span data-stu-id="da6b9-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="da6b9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da6b9-117">PARAMETERS</span></span>

### <span data-ttu-id="da6b9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da6b9-118">-AsJob</span></span>
<span data-ttu-id="da6b9-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="da6b9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da6b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da6b9-120">-DefaultProfile</span></span>
<span data-ttu-id="da6b9-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da6b9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da6b9-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="da6b9-122">-EventHub</span></span>
<span data-ttu-id="da6b9-123">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="da6b9-123">EventHub Name</span></span>

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

### <span data-ttu-id="da6b9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da6b9-124">-InputObject</span></span>
<span data-ttu-id="da6b9-125">ConsumerGroup objektum</span><span class="sxs-lookup"><span data-stu-id="da6b9-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="da6b9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="da6b9-126">-Name</span></span>
<span data-ttu-id="da6b9-127">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="da6b9-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="da6b9-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="da6b9-128">-Namespace</span></span>
<span data-ttu-id="da6b9-129">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="da6b9-129">Namespace Name</span></span>

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

### <span data-ttu-id="da6b9-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da6b9-130">-PassThru</span></span>
<span data-ttu-id="da6b9-131">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="da6b9-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="da6b9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da6b9-132">-ResourceGroupName</span></span>
<span data-ttu-id="da6b9-133">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="da6b9-133">Resource Group Name</span></span>

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

### <span data-ttu-id="da6b9-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da6b9-134">-ResourceId</span></span>
<span data-ttu-id="da6b9-135">ConsumerGroup Resource Id</span><span class="sxs-lookup"><span data-stu-id="da6b9-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="da6b9-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da6b9-136">-Confirm</span></span>
<span data-ttu-id="da6b9-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="da6b9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da6b9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da6b9-138">-WhatIf</span></span>
<span data-ttu-id="da6b9-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="da6b9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da6b9-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da6b9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da6b9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da6b9-141">CommonParameters</span></span>
<span data-ttu-id="da6b9-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da6b9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da6b9-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da6b9-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da6b9-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da6b9-144">INPUTS</span></span>

### <span data-ttu-id="da6b9-145">System.String</span><span class="sxs-lookup"><span data-stu-id="da6b9-145">System.String</span></span>

### <span data-ttu-id="da6b9-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="da6b9-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="da6b9-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da6b9-147">OUTPUTS</span></span>

### <span data-ttu-id="da6b9-148">System.Void</span><span class="sxs-lookup"><span data-stu-id="da6b9-148">System.Void</span></span>

## <span data-ttu-id="da6b9-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da6b9-149">NOTES</span></span>

## <span data-ttu-id="da6b9-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da6b9-150">RELATED LINKS</span></span>
