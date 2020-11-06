---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 34a59f0530ed036397523e3810d68175e7ee2d3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492811"
---
# <span data-ttu-id="28799-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="28799-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="28799-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28799-102">SYNOPSIS</span></span>
<span data-ttu-id="28799-103">Új fogyasztói csoportot hoz létre a megadott esemény központhoz.</span><span class="sxs-lookup"><span data-stu-id="28799-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28799-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28799-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28799-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="28799-105">DESCRIPTION</span></span>
<span data-ttu-id="28799-106">Új fogyasztói csoportot hoz létre a megadott esemény központhoz.</span><span class="sxs-lookup"><span data-stu-id="28799-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="28799-107">Példák</span><span class="sxs-lookup"><span data-stu-id="28799-107">EXAMPLES</span></span>

### <span data-ttu-id="28799-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="28799-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="28799-109">Létrehozza a fogyasztói csoport \` MyConsumerGroupName az \` esemény központi \` MyEventHubName \` , mely a névtér \` MyNamespaceName, az \` erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="28799-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="28799-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28799-110">PARAMETERS</span></span>

### <span data-ttu-id="28799-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28799-111">-DefaultProfile</span></span>
<span data-ttu-id="28799-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28799-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28799-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="28799-113">-EventHub</span></span>
<span data-ttu-id="28799-114">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="28799-114">EventHub Name</span></span>

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

### <span data-ttu-id="28799-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28799-115">-Name</span></span>
<span data-ttu-id="28799-116">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="28799-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28799-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="28799-117">-Namespace</span></span>
<span data-ttu-id="28799-118">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="28799-118">Namespace Name</span></span>

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

### <span data-ttu-id="28799-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28799-119">-ResourceGroupName</span></span>
<span data-ttu-id="28799-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="28799-120">Resource Group Name</span></span>

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

### <span data-ttu-id="28799-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="28799-121">-UserMetadata</span></span>
<span data-ttu-id="28799-122">A ConsumerGroup felhasználói metaadatai</span><span class="sxs-lookup"><span data-stu-id="28799-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28799-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28799-123">-Confirm</span></span>
<span data-ttu-id="28799-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28799-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28799-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28799-125">-WhatIf</span></span>
<span data-ttu-id="28799-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="28799-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28799-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28799-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28799-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28799-128">CommonParameters</span></span>
<span data-ttu-id="28799-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28799-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28799-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28799-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28799-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28799-131">INPUTS</span></span>

### <span data-ttu-id="28799-132">System. String</span><span class="sxs-lookup"><span data-stu-id="28799-132">System.String</span></span>

## <span data-ttu-id="28799-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28799-133">OUTPUTS</span></span>

### <span data-ttu-id="28799-134">Microsoft. Azure. Command. EventHub. models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="28799-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="28799-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28799-135">NOTES</span></span>

## <span data-ttu-id="28799-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28799-136">RELATED LINKS</span></span>
