---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: a9447c745ddf60c4a2adcb2a55c824b65d96efd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679734"
---
# <span data-ttu-id="3431d-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3431d-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="3431d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3431d-102">SYNOPSIS</span></span>
<span data-ttu-id="3431d-103">Új fogyasztói csoportot hoz létre a megadott esemény központhoz.</span><span class="sxs-lookup"><span data-stu-id="3431d-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3431d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3431d-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3431d-105">Példák</span><span class="sxs-lookup"><span data-stu-id="3431d-105">EXAMPLES</span></span>

### <span data-ttu-id="3431d-106">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3431d-106">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="3431d-107">Létrehozza a fogyasztói csoport \` MyConsumerGroupName az \` esemény központi \` MyEventHubName \` , mely a névtér \` MyNamespaceName, az \` erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="3431d-107">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3431d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3431d-108">PARAMETERS</span></span>

### <span data-ttu-id="3431d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3431d-109">-DefaultProfile</span></span>
<span data-ttu-id="3431d-110">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3431d-110">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3431d-111">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3431d-111">-EventHub</span></span>
<span data-ttu-id="3431d-112">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="3431d-112">EventHub Name</span></span>

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

### <span data-ttu-id="3431d-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3431d-113">-Name</span></span>
<span data-ttu-id="3431d-114">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="3431d-114">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3431d-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3431d-115">-Namespace</span></span>
<span data-ttu-id="3431d-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="3431d-116">Namespace Name</span></span>

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

### <span data-ttu-id="3431d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3431d-117">-ResourceGroupName</span></span>
<span data-ttu-id="3431d-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="3431d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="3431d-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="3431d-119">-UserMetadata</span></span>
<span data-ttu-id="3431d-120">A ConsumerGroup felhasználói metaadatai</span><span class="sxs-lookup"><span data-stu-id="3431d-120">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="3431d-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3431d-121">-Confirm</span></span>
<span data-ttu-id="3431d-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3431d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3431d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3431d-123">-WhatIf</span></span>
<span data-ttu-id="3431d-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3431d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3431d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3431d-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3431d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3431d-126">CommonParameters</span></span>
<span data-ttu-id="3431d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3431d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3431d-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3431d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3431d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3431d-129">INPUTS</span></span>

### <span data-ttu-id="3431d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3431d-130">System.String</span></span>


## <span data-ttu-id="3431d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3431d-131">OUTPUTS</span></span>

### <span data-ttu-id="3431d-132">Microsoft. Azure. Command. EventHub. models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="3431d-132">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="3431d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3431d-133">NOTES</span></span>

## <span data-ttu-id="3431d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3431d-134">RELATED LINKS</span></span>
