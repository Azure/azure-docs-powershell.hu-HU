---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: 132070183480beba14196abcf1362a29e8fa4ed2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842353"
---
# <span data-ttu-id="1b076-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1b076-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="1b076-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b076-102">SYNOPSIS</span></span>
<span data-ttu-id="1b076-103">A megadott esemény-hubok fogyasztói csoportjának részleteit kapja meg, vagy a fogyasztói csoportok listáját egy esemény központjában kapja.</span><span class="sxs-lookup"><span data-stu-id="1b076-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="1b076-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b076-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b076-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b076-105">DESCRIPTION</span></span>
<span data-ttu-id="1b076-106">A Get-AzEventHubConsumerGroup parancsmag a megadott esemény-hubok fogyasztói csoportjának részleteit, illetve az adott esemény központjának fogyasztói csoportjai listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="1b076-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="1b076-107">Ha a fogyasztói csoport neve meg van határozva, akkor a rendszer az egyetlen fogyasztói csoport részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="1b076-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="1b076-108">Ha a fogyasztói csoport neve nincs megadva, a program az adott esemény központjában lévő fogyasztói csoportok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="1b076-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="1b076-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1b076-109">EXAMPLES</span></span>

### <span data-ttu-id="1b076-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1b076-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="1b076-111">Beolvassa a fogyasztói csoport \` MyConsumerGroupName az \` esemény központi \` MyEventHubName \` , amely a névtér MyNamespaceName van az \` \` erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1b076-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1b076-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="1b076-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="1b076-113">Beolvassa a fogyasztói csoportok listáját az esemény központi \` MyEventHubName \` , amely az \` erőforráscsoport MyResourceGroupName található névtér MyNamespaceName található \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="1b076-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1b076-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b076-114">PARAMETERS</span></span>

### <span data-ttu-id="1b076-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b076-115">-DefaultProfile</span></span>
<span data-ttu-id="1b076-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b076-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b076-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="1b076-117">-EventHub</span></span>
<span data-ttu-id="1b076-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="1b076-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b076-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1b076-119">-MaxCount</span></span>
<span data-ttu-id="1b076-120">Adja meg a ConsumerGroups maximális számát.</span><span class="sxs-lookup"><span data-stu-id="1b076-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b076-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1b076-121">-Name</span></span>
<span data-ttu-id="1b076-122">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="1b076-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b076-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1b076-123">-Namespace</span></span>
<span data-ttu-id="1b076-124">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="1b076-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b076-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b076-125">-ResourceGroupName</span></span>
<span data-ttu-id="1b076-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="1b076-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b076-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b076-127">CommonParameters</span></span>
<span data-ttu-id="1b076-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b076-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b076-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b076-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b076-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b076-130">INPUTS</span></span>

### <span data-ttu-id="1b076-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1b076-131">System.String</span></span>

## <span data-ttu-id="1b076-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b076-132">OUTPUTS</span></span>

### <span data-ttu-id="1b076-133">Microsoft. Azure. Command. EventHub. models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="1b076-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="1b076-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b076-134">NOTES</span></span>

## <span data-ttu-id="1b076-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b076-135">RELATED LINKS</span></span>
