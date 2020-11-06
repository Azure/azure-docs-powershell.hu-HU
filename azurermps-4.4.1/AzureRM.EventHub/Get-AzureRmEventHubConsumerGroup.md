---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505028"
---
# <span data-ttu-id="ac2c2-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ac2c2-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="ac2c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ac2c2-103">A megadott esemény-hubok fogyasztói csoportjának részleteit kapja meg, vagy a fogyasztói csoportok listáját egy esemény központjában kapja.</span><span class="sxs-lookup"><span data-stu-id="ac2c2-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac2c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac2c2-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## <span data-ttu-id="ac2c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac2c2-105">DESCRIPTION</span></span>
<span data-ttu-id="ac2c2-106">A Get-AzureRmEventHubConsumerGroup parancsmag a megadott esemény-hubok fogyasztói csoportjának részleteit, illetve az adott esemény központjának fogyasztói csoportjai listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="ac2c2-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="ac2c2-107">Ha a fogyasztói csoport neve meg van határozva, akkor a rendszer az egyetlen fogyasztói csoport részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ac2c2-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="ac2c2-108">Ha a fogyasztói csoport neve nincs megadva, a program az adott esemény központjában lévő fogyasztói csoportok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ac2c2-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="ac2c2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ac2c2-109">EXAMPLES</span></span>

### <span data-ttu-id="ac2c2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac2c2-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="ac2c2-111">Beolvassa a fogyasztói csoport \` MyConsumerGroupName az \` esemény központi \` MyEventHubName \` , amely a névtér MyNamespaceName van az \` \` erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ac2c2-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ac2c2-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="ac2c2-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="ac2c2-113">Beolvassa a fogyasztói csoportok listáját az esemény központi \` MyEventHubName \` , amely az \` erőforráscsoport MyResourceGroupName található névtér MyNamespaceName található \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="ac2c2-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ac2c2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac2c2-114">PARAMETERS</span></span>

### <span data-ttu-id="ac2c2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac2c2-115">-ResourceGroupName</span></span>
<span data-ttu-id="ac2c2-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ac2c2-116">Resource group name.</span></span>

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

### <span data-ttu-id="ac2c2-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ac2c2-117">-EventHub</span></span>
<span data-ttu-id="ac2c2-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="ac2c2-118">EventHub Name.</span></span>

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

### <span data-ttu-id="ac2c2-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac2c2-119">-Name</span></span>
<span data-ttu-id="ac2c2-120">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="ac2c2-120">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac2c2-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ac2c2-121">-Namespace</span></span>
<span data-ttu-id="ac2c2-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ac2c2-122">Namespace Name.</span></span>

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

## <span data-ttu-id="ac2c2-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac2c2-123">INPUTS</span></span>

### <span data-ttu-id="ac2c2-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ac2c2-124">System.String</span></span>

## <span data-ttu-id="ac2c2-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac2c2-125">OUTPUTS</span></span>

### <span data-ttu-id="ac2c2-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. ConsumerGroupAttributes, Microsoft. Azure. commands. EventHub, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ac2c2-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ac2c2-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac2c2-127">NOTES</span></span>

## <span data-ttu-id="ac2c2-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac2c2-128">RELATED LINKS</span></span>

