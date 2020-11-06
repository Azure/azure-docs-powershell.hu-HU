---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 743928771fdba7ed17fe2643cf9e92ae7c2d9860
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492282"
---
# <span data-ttu-id="72032-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="72032-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="72032-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72032-102">SYNOPSIS</span></span>
<span data-ttu-id="72032-103">Frissíti a megadott esemény-hubok fogyasztói csoportját.</span><span class="sxs-lookup"><span data-stu-id="72032-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72032-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72032-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72032-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72032-105">DESCRIPTION</span></span>
<span data-ttu-id="72032-106">A Set-AzureRmEventHubConsumerGroup parancsmag frissíti a megadott esemény-hubok fogyasztói csoportját.</span><span class="sxs-lookup"><span data-stu-id="72032-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="72032-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72032-107">EXAMPLES</span></span>

### <span data-ttu-id="72032-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="72032-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="72032-109">A fogyasztói csoport MyConsumerGroupName felhasználói metaadatait a \` \` "tesztelés" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="72032-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="72032-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72032-110">PARAMETERS</span></span>

### <span data-ttu-id="72032-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72032-111">-DefaultProfile</span></span>
<span data-ttu-id="72032-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72032-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72032-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="72032-113">-EventHub</span></span>
<span data-ttu-id="72032-114">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="72032-114">EventHub Name</span></span>

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

### <span data-ttu-id="72032-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72032-115">-Name</span></span>
<span data-ttu-id="72032-116">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="72032-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="72032-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="72032-117">-Namespace</span></span>
<span data-ttu-id="72032-118">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="72032-118">Namespace Name</span></span>

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

### <span data-ttu-id="72032-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72032-119">-ResourceGroupName</span></span>
<span data-ttu-id="72032-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="72032-120">Resource Group Name</span></span>

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

### <span data-ttu-id="72032-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="72032-121">-UserMetadata</span></span>
<span data-ttu-id="72032-122">A ConsumerGroup felhasználói metaadatai</span><span class="sxs-lookup"><span data-stu-id="72032-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="72032-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72032-123">-Confirm</span></span>
<span data-ttu-id="72032-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72032-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72032-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72032-125">-WhatIf</span></span>
<span data-ttu-id="72032-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72032-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72032-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72032-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72032-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72032-128">CommonParameters</span></span>
<span data-ttu-id="72032-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72032-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="72032-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72032-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72032-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72032-131">INPUTS</span></span>

### <span data-ttu-id="72032-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72032-132">System.String</span></span>


## <span data-ttu-id="72032-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72032-133">OUTPUTS</span></span>

### <span data-ttu-id="72032-134">Microsoft. Azure. Command. EventHub. models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="72032-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="72032-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72032-135">NOTES</span></span>

## <span data-ttu-id="72032-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72032-136">RELATED LINKS</span></span>
