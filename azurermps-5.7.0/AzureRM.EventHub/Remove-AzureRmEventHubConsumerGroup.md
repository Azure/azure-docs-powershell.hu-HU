---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 5b88ce6edc92cb6483b8d6df95599fcea854f805
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496588"
---
# <span data-ttu-id="4058b-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4058b-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="4058b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4058b-102">SYNOPSIS</span></span>
<span data-ttu-id="4058b-103">Törli a megadott esemény-hubok fogyasztói csoportját.</span><span class="sxs-lookup"><span data-stu-id="4058b-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4058b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4058b-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4058b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4058b-105">DESCRIPTION</span></span>
<span data-ttu-id="4058b-106">A Remove-AzureRmEventHubConsumerGroup parancsmag eltávolítja és törli a megadott fogyasztói csoportot az adott esemény központból.</span><span class="sxs-lookup"><span data-stu-id="4058b-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="4058b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4058b-107">EXAMPLES</span></span>

### <span data-ttu-id="4058b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4058b-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="4058b-109">Törli a fogyasztói csoport \` MyConsumerGroupName \` az esemény központi \` MyEventHubName \` , amely a \` MyNamespaceName névtérre van korlátozva \` .</span><span class="sxs-lookup"><span data-stu-id="4058b-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="4058b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4058b-110">PARAMETERS</span></span>

### <span data-ttu-id="4058b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4058b-111">-DefaultProfile</span></span>
<span data-ttu-id="4058b-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4058b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4058b-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4058b-113">-EventHub</span></span>
<span data-ttu-id="4058b-114">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="4058b-114">EventHub Name</span></span>

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

### <span data-ttu-id="4058b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4058b-115">-Name</span></span>
<span data-ttu-id="4058b-116">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="4058b-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="4058b-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4058b-117">-Namespace</span></span>
<span data-ttu-id="4058b-118">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="4058b-118">Namespace Name</span></span>

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

### <span data-ttu-id="4058b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4058b-119">-ResourceGroupName</span></span>
<span data-ttu-id="4058b-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4058b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="4058b-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4058b-121">-Confirm</span></span>
<span data-ttu-id="4058b-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4058b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4058b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4058b-123">-WhatIf</span></span>
<span data-ttu-id="4058b-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4058b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4058b-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4058b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4058b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4058b-126">CommonParameters</span></span>
<span data-ttu-id="4058b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4058b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4058b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4058b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4058b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4058b-129">INPUTS</span></span>

### <span data-ttu-id="4058b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4058b-130">System.String</span></span>


## <span data-ttu-id="4058b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4058b-131">OUTPUTS</span></span>

### <span data-ttu-id="4058b-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="4058b-132">System.Object</span></span>

## <span data-ttu-id="4058b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4058b-133">NOTES</span></span>

## <span data-ttu-id="4058b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4058b-134">RELATED LINKS</span></span>
