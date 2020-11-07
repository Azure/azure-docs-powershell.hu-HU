---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 205dc883f8f6e0481f88438137ca45ad7a99c4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672939"
---
# <span data-ttu-id="0560c-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0560c-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="0560c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0560c-102">SYNOPSIS</span></span>
<span data-ttu-id="0560c-103">A megadott esemény-hubok fogyasztói csoportjának részleteit kapja meg, vagy a fogyasztói csoportok listáját egy esemény központjában kapja.</span><span class="sxs-lookup"><span data-stu-id="0560c-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0560c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0560c-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0560c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0560c-105">DESCRIPTION</span></span>
<span data-ttu-id="0560c-106">A Get-AzureRmEventHubConsumerGroup parancsmag a megadott esemény-hubok fogyasztói csoportjának részleteit, illetve az adott esemény központjának fogyasztói csoportjai listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="0560c-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="0560c-107">Ha a fogyasztói csoport neve meg van határozva, akkor a rendszer az egyetlen fogyasztói csoport részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0560c-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="0560c-108">Ha a fogyasztói csoport neve nincs megadva, a program az adott esemény központjában lévő fogyasztói csoportok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0560c-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="0560c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0560c-109">EXAMPLES</span></span>

### <span data-ttu-id="0560c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0560c-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="0560c-111">Beolvassa a fogyasztói csoport \` MyConsumerGroupName az \` esemény központi \` MyEventHubName \` , amely a névtér MyNamespaceName van az \` \` erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0560c-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0560c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0560c-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="0560c-113">Beolvassa a fogyasztói csoportok listáját az esemény központi \` MyEventHubName \` , amely az \` erőforráscsoport MyResourceGroupName található névtér MyNamespaceName található \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="0560c-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0560c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0560c-114">PARAMETERS</span></span>

### <span data-ttu-id="0560c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0560c-115">-DefaultProfile</span></span>
<span data-ttu-id="0560c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0560c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0560c-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="0560c-117">-EventHub</span></span>
<span data-ttu-id="0560c-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="0560c-118">EventHub Name</span></span>

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

### <span data-ttu-id="0560c-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0560c-119">-MaxCount</span></span>
<span data-ttu-id="0560c-120">Adja meg a ConsumerGroups maximális számát.</span><span class="sxs-lookup"><span data-stu-id="0560c-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="0560c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0560c-121">-Name</span></span>
<span data-ttu-id="0560c-122">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="0560c-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="0560c-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0560c-123">-Namespace</span></span>
<span data-ttu-id="0560c-124">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="0560c-124">Namespace Name</span></span>

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

### <span data-ttu-id="0560c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0560c-125">-ResourceGroupName</span></span>
<span data-ttu-id="0560c-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0560c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0560c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0560c-127">CommonParameters</span></span>
<span data-ttu-id="0560c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0560c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0560c-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0560c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0560c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0560c-130">INPUTS</span></span>

### <span data-ttu-id="0560c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0560c-131">System.String</span></span>

## <span data-ttu-id="0560c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0560c-132">OUTPUTS</span></span>

### <span data-ttu-id="0560c-133">Microsoft. Azure. Command. EventHub. models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="0560c-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="0560c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0560c-134">NOTES</span></span>

## <span data-ttu-id="0560c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0560c-135">RELATED LINKS</span></span>
