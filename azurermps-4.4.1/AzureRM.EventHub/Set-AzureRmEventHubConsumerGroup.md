---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c871036c6f3113bd40e17fb5bbc201fa6297573c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501864"
---
# <span data-ttu-id="94fa9-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="94fa9-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="94fa9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="94fa9-103">Frissíti a megadott esemény-hubok fogyasztói csoportját.</span><span class="sxs-lookup"><span data-stu-id="94fa9-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94fa9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94fa9-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="94fa9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="94fa9-106">A Set-AzureRmEventHubConsumerGroup parancsmag frissíti a megadott esemény-hubok fogyasztói csoportját.</span><span class="sxs-lookup"><span data-stu-id="94fa9-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="94fa9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="94fa9-107">EXAMPLES</span></span>

### <span data-ttu-id="94fa9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94fa9-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="94fa9-109">A fogyasztói csoport MyConsumerGroupName felhasználói metaadatait a \` \` "tesztelés" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="94fa9-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="94fa9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94fa9-110">PARAMETERS</span></span>

### <span data-ttu-id="94fa9-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94fa9-111">-ResourceGroupName</span></span>
<span data-ttu-id="94fa9-112">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="94fa9-112">Resource group name.</span></span>

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

### <span data-ttu-id="94fa9-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="94fa9-113">-UserMetadata</span></span>
<span data-ttu-id="94fa9-114">A fogyasztói csoport felhasználói metaadatai (nem kötelező).</span><span class="sxs-lookup"><span data-stu-id="94fa9-114">User metadata for the consumer group (optional).</span></span>

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

### <span data-ttu-id="94fa9-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94fa9-115">-Confirm</span></span>
<span data-ttu-id="94fa9-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94fa9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94fa9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94fa9-117">-WhatIf</span></span>
<span data-ttu-id="94fa9-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94fa9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94fa9-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94fa9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94fa9-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="94fa9-120">-EventHub</span></span>
<span data-ttu-id="94fa9-121">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="94fa9-121">EventHub Name.</span></span>

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

### <span data-ttu-id="94fa9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94fa9-122">-Name</span></span>
<span data-ttu-id="94fa9-123">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="94fa9-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="94fa9-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="94fa9-124">-Namespace</span></span>
<span data-ttu-id="94fa9-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="94fa9-125">Namespace Name.</span></span>

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

## <span data-ttu-id="94fa9-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94fa9-126">INPUTS</span></span>

### <span data-ttu-id="94fa9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="94fa9-127">System.String</span></span>

## <span data-ttu-id="94fa9-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94fa9-128">OUTPUTS</span></span>

### <span data-ttu-id="94fa9-129">Microsoft. Azure. Command. EventHub. models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="94fa9-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="94fa9-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94fa9-130">NOTES</span></span>

## <span data-ttu-id="94fa9-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94fa9-131">RELATED LINKS</span></span>

