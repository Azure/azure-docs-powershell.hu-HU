---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c8684e9af0bca55dca52f336a458f4c428ca67a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500048"
---
# <span data-ttu-id="792e8-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="792e8-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="792e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="792e8-102">SYNOPSIS</span></span>
<span data-ttu-id="792e8-103">Törli a megadott esemény-hubok fogyasztói csoportját.</span><span class="sxs-lookup"><span data-stu-id="792e8-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="792e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="792e8-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="792e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="792e8-105">DESCRIPTION</span></span>
<span data-ttu-id="792e8-106">A Remove-AzureRmEventHubConsumerGroup parancsmag eltávolítja és törli a megadott fogyasztói csoportot az adott esemény központból.</span><span class="sxs-lookup"><span data-stu-id="792e8-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="792e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="792e8-107">EXAMPLES</span></span>

### <span data-ttu-id="792e8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="792e8-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="792e8-109">Törli a fogyasztói csoport \` MyConsumerGroupName \` az esemény központi \` MyEventHubName \` , amely a \` MyNamespaceName névtérre van korlátozva \` .</span><span class="sxs-lookup"><span data-stu-id="792e8-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="792e8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="792e8-110">PARAMETERS</span></span>

### <span data-ttu-id="792e8-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="792e8-111">-ResourceGroupName</span></span>
<span data-ttu-id="792e8-112">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="792e8-112">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792e8-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="792e8-113">-Confirm</span></span>
<span data-ttu-id="792e8-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="792e8-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e8-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="792e8-115">-WhatIf</span></span>
<span data-ttu-id="792e8-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="792e8-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="792e8-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="792e8-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="792e8-118">-EventHub</span><span class="sxs-lookup"><span data-stu-id="792e8-118">-EventHub</span></span>
<span data-ttu-id="792e8-119">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="792e8-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792e8-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="792e8-120">-Name</span></span>
<span data-ttu-id="792e8-121">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="792e8-121">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="792e8-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="792e8-122">-Namespace</span></span>
<span data-ttu-id="792e8-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="792e8-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="792e8-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="792e8-124">INPUTS</span></span>

### <span data-ttu-id="792e8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="792e8-125">System.String</span></span>

## <span data-ttu-id="792e8-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="792e8-126">OUTPUTS</span></span>

### <span data-ttu-id="792e8-127">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="792e8-127">System.Object</span></span>

## <span data-ttu-id="792e8-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="792e8-128">NOTES</span></span>

## <span data-ttu-id="792e8-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="792e8-129">RELATED LINKS</span></span>

