---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 445d20453b9f3d99e4ff5c72e118b287f0a83898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502588"
---
# <span data-ttu-id="0c40e-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0c40e-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="0c40e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c40e-102">SYNOPSIS</span></span>
<span data-ttu-id="0c40e-103">A megadott esemény-hubok fogyasztói csoportjának részleteit kapja meg, vagy a fogyasztói csoportok listáját egy esemény központjában kapja.</span><span class="sxs-lookup"><span data-stu-id="0c40e-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c40e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c40e-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c40e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c40e-105">DESCRIPTION</span></span>
<span data-ttu-id="0c40e-106">A Get-AzureRmEventHubConsumerGroup parancsmag a megadott esemény-hubok fogyasztói csoportjának részleteit, illetve az adott esemény központjának fogyasztói csoportjai listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="0c40e-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="0c40e-107">Ha a fogyasztói csoport neve meg van határozva, akkor a rendszer az egyetlen fogyasztói csoport részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0c40e-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="0c40e-108">Ha a fogyasztói csoport neve nincs megadva, a program az adott esemény központjában lévő fogyasztói csoportok listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0c40e-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="0c40e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0c40e-109">EXAMPLES</span></span>

### <span data-ttu-id="0c40e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0c40e-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="0c40e-111">Beolvassa a fogyasztói csoport \` MyConsumerGroupName az \` esemény központi \` MyEventHubName \` , amely a névtér MyNamespaceName van az \` \` erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="0c40e-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0c40e-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0c40e-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="0c40e-113">Beolvassa a fogyasztói csoportok listáját az esemény központi \` MyEventHubName \` , amely az \` erőforráscsoport MyResourceGroupName található névtér MyNamespaceName található \` \` \` .</span><span class="sxs-lookup"><span data-stu-id="0c40e-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0c40e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c40e-114">PARAMETERS</span></span>

### <span data-ttu-id="0c40e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c40e-115">-DefaultProfile</span></span>
<span data-ttu-id="0c40e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c40e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c40e-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="0c40e-117">-EventHub</span></span>
<span data-ttu-id="0c40e-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="0c40e-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c40e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c40e-119">-Name</span></span>
<span data-ttu-id="0c40e-120">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="0c40e-120">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c40e-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0c40e-121">-Namespace</span></span>
<span data-ttu-id="0c40e-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="0c40e-122">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c40e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c40e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c40e-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0c40e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0c40e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c40e-125">CommonParameters</span></span>
<span data-ttu-id="0c40e-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c40e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0c40e-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c40e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c40e-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c40e-128">INPUTS</span></span>

### <span data-ttu-id="0c40e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0c40e-129">System.String</span></span>


## <span data-ttu-id="0c40e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c40e-130">OUTPUTS</span></span>

### <span data-ttu-id="0c40e-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventHub. models. PSConsumerGroupAttributes, Microsoft. Azure. commands. EventHub, Version = 0.5.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0c40e-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="0c40e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c40e-132">NOTES</span></span>

## <span data-ttu-id="0c40e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c40e-133">RELATED LINKS</span></span>
