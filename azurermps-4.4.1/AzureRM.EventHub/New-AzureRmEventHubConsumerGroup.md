---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680565"
---
# <span data-ttu-id="0bc80-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0bc80-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="0bc80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0bc80-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc80-103">Új fogyasztói csoportot hoz létre a megadott esemény központhoz.</span><span class="sxs-lookup"><span data-stu-id="0bc80-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bc80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0bc80-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0bc80-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0bc80-105">DESCRIPTION</span></span>
<span data-ttu-id="0bc80-106">Az New-AzureRmEventHubConsumerGroup parancsmag létrehoz egy új fogyasztói csoportot a megadott esemény központhoz.</span><span class="sxs-lookup"><span data-stu-id="0bc80-106">The New-AzureRmEventHubConsumerGroup cmdlet creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="0bc80-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0bc80-107">EXAMPLES</span></span>

### <span data-ttu-id="0bc80-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0bc80-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="0bc80-109">Létrehozza a fogyasztói csoport \` MyConsumerGroupName az \` esemény központi \` MyEventHubName \` , mely a névtér \` MyNamespaceName, az \` erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0bc80-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0bc80-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0bc80-110">PARAMETERS</span></span>

### <span data-ttu-id="0bc80-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc80-111">-ResourceGroupName</span></span>
<span data-ttu-id="0bc80-112">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="0bc80-112">Resource group name.</span></span>

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

### <span data-ttu-id="0bc80-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="0bc80-113">-UserMetadata</span></span>
<span data-ttu-id="0bc80-114">A fogyasztói csoport felhasználói metaadatai.</span><span class="sxs-lookup"><span data-stu-id="0bc80-114">User metadata for the consumer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc80-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0bc80-115">-Confirm</span></span>
<span data-ttu-id="0bc80-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0bc80-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bc80-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bc80-117">-WhatIf</span></span>
<span data-ttu-id="0bc80-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0bc80-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bc80-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0bc80-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bc80-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="0bc80-120">-EventHub</span></span>
<span data-ttu-id="0bc80-121">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="0bc80-121">EventHub Name.</span></span>

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

### <span data-ttu-id="0bc80-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0bc80-122">-Name</span></span>
<span data-ttu-id="0bc80-123">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="0bc80-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="0bc80-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0bc80-124">-Namespace</span></span>
<span data-ttu-id="0bc80-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="0bc80-125">Namespace Name.</span></span>

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

## <span data-ttu-id="0bc80-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bc80-126">INPUTS</span></span>

### <span data-ttu-id="0bc80-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0bc80-127">System.String</span></span>

## <span data-ttu-id="0bc80-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bc80-128">OUTPUTS</span></span>

### <span data-ttu-id="0bc80-129">Microsoft. Azure. Command. EventHub. models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="0bc80-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="0bc80-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0bc80-130">NOTES</span></span>

## <span data-ttu-id="0bc80-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bc80-131">RELATED LINKS</span></span>

