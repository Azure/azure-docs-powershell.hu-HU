---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: c887aab15e0874357ec32d9c815a9a9b1dd1227a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666477"
---
# <span data-ttu-id="e02df-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e02df-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="e02df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e02df-102">SYNOPSIS</span></span>
<span data-ttu-id="e02df-103">Új fogyasztói csoportot hoz létre a megadott esemény központhoz.</span><span class="sxs-lookup"><span data-stu-id="e02df-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="e02df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e02df-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e02df-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e02df-105">DESCRIPTION</span></span>
<span data-ttu-id="e02df-106">Új fogyasztói csoportot hoz létre a megadott esemény központhoz.</span><span class="sxs-lookup"><span data-stu-id="e02df-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="e02df-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e02df-107">EXAMPLES</span></span>

### <span data-ttu-id="e02df-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e02df-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="e02df-109">Létrehozza a fogyasztói csoport \` MyConsumerGroupName az \` esemény központi \` MyEventHubName \` , mely a névtér \` MyNamespaceName, az \` erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e02df-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e02df-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e02df-110">PARAMETERS</span></span>

### <span data-ttu-id="e02df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02df-111">-DefaultProfile</span></span>
<span data-ttu-id="e02df-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e02df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02df-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e02df-113">-EventHub</span></span>
<span data-ttu-id="e02df-114">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="e02df-114">EventHub Name</span></span>

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

### <span data-ttu-id="e02df-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e02df-115">-Name</span></span>
<span data-ttu-id="e02df-116">ConsumerGroup neve</span><span class="sxs-lookup"><span data-stu-id="e02df-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="e02df-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e02df-117">-Namespace</span></span>
<span data-ttu-id="e02df-118">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="e02df-118">Namespace Name</span></span>

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

### <span data-ttu-id="e02df-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02df-119">-ResourceGroupName</span></span>
<span data-ttu-id="e02df-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e02df-120">Resource Group Name</span></span>

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

### <span data-ttu-id="e02df-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="e02df-121">-UserMetadata</span></span>
<span data-ttu-id="e02df-122">A ConsumerGroup felhasználói metaadatai</span><span class="sxs-lookup"><span data-stu-id="e02df-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="e02df-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e02df-123">-Confirm</span></span>
<span data-ttu-id="e02df-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e02df-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e02df-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e02df-125">-WhatIf</span></span>
<span data-ttu-id="e02df-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e02df-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e02df-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e02df-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e02df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02df-128">CommonParameters</span></span>
<span data-ttu-id="e02df-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e02df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02df-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e02df-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02df-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e02df-131">INPUTS</span></span>

### <span data-ttu-id="e02df-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e02df-132">System.String</span></span>

## <span data-ttu-id="e02df-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e02df-133">OUTPUTS</span></span>

### <span data-ttu-id="e02df-134">Microsoft. Azure. Command. EventHub. models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="e02df-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="e02df-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e02df-135">NOTES</span></span>

## <span data-ttu-id="e02df-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e02df-136">RELATED LINKS</span></span>
