---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: 2a11ab0ec68ee01864f1255953121b91f1b27ebf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921177"
---
# <span data-ttu-id="5a409-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5a409-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="5a409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a409-102">SYNOPSIS</span></span>
<span data-ttu-id="5a409-103">Létrehoz egy új fogyasztói csoportot a megadott Eseményközponthoz.</span><span class="sxs-lookup"><span data-stu-id="5a409-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="5a409-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a409-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a409-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a409-105">DESCRIPTION</span></span>
<span data-ttu-id="5a409-106">Létrehoz egy új fogyasztói csoportot a megadott Eseményközponthoz.</span><span class="sxs-lookup"><span data-stu-id="5a409-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="5a409-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a409-107">EXAMPLES</span></span>

### <span data-ttu-id="5a409-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="5a409-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="5a409-109">Létrehozza a \` MyConsumerGroupName fogyasztói csoportot az Event Hub MyEventHubName nevű, a \` \` \` MyNamespaceName névterére terjed ki, a \` \` \` MyResourceGroupName \` erőforráscsoporttal.</span><span class="sxs-lookup"><span data-stu-id="5a409-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5a409-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a409-110">PARAMETERS</span></span>

### <span data-ttu-id="5a409-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a409-111">-DefaultProfile</span></span>
<span data-ttu-id="5a409-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a409-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a409-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5a409-113">-EventHub</span></span>
<span data-ttu-id="5a409-114">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="5a409-114">EventHub Name</span></span>

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

### <span data-ttu-id="5a409-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5a409-115">-Name</span></span>
<span data-ttu-id="5a409-116">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="5a409-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="5a409-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5a409-117">-Namespace</span></span>
<span data-ttu-id="5a409-118">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5a409-118">Namespace Name</span></span>

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

### <span data-ttu-id="5a409-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a409-119">-ResourceGroupName</span></span>
<span data-ttu-id="5a409-120">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5a409-120">Resource Group Name</span></span>

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

### <span data-ttu-id="5a409-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="5a409-121">-UserMetadata</span></span>
<span data-ttu-id="5a409-122">Felhasználói metaadatok a ConsumerGroup szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="5a409-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="5a409-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a409-123">-Confirm</span></span>
<span data-ttu-id="5a409-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5a409-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a409-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a409-125">-WhatIf</span></span>
<span data-ttu-id="5a409-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5a409-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a409-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a409-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a409-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a409-128">CommonParameters</span></span>
<span data-ttu-id="5a409-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a409-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a409-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a409-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a409-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a409-131">INPUTS</span></span>

### <span data-ttu-id="5a409-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5a409-132">System.String</span></span>

## <span data-ttu-id="5a409-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a409-133">OUTPUTS</span></span>

### <span data-ttu-id="5a409-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="5a409-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="5a409-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a409-135">NOTES</span></span>

## <span data-ttu-id="5a409-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a409-136">RELATED LINKS</span></span>
