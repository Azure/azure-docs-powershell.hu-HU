---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353057"
---
# <span data-ttu-id="917c3-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="917c3-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="917c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="917c3-102">SYNOPSIS</span></span>
<span data-ttu-id="917c3-103">Frissíti a megadott Eseményközpontok fogyasztói csoportot.</span><span class="sxs-lookup"><span data-stu-id="917c3-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="917c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="917c3-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="917c3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="917c3-105">DESCRIPTION</span></span>
<span data-ttu-id="917c3-106">A Set-AzEventHubConsumerGroup parancsmag frissíti a megadott Event Hubs fogyasztói csoportot.</span><span class="sxs-lookup"><span data-stu-id="917c3-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="917c3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="917c3-107">EXAMPLES</span></span>

### <span data-ttu-id="917c3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="917c3-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="917c3-109">A MyConsumerGroupName fogyasztói csoport felhasználói metaadatait \` \` "Tesztelés" típusúra állítja.</span><span class="sxs-lookup"><span data-stu-id="917c3-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="917c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="917c3-110">PARAMETERS</span></span>

### <span data-ttu-id="917c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917c3-111">-DefaultProfile</span></span>
<span data-ttu-id="917c3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="917c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="917c3-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="917c3-113">-EventHub</span></span>
<span data-ttu-id="917c3-114">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="917c3-114">EventHub Name</span></span>

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

### <span data-ttu-id="917c3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="917c3-115">-Name</span></span>
<span data-ttu-id="917c3-116">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="917c3-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="917c3-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="917c3-117">-Namespace</span></span>
<span data-ttu-id="917c3-118">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="917c3-118">Namespace Name</span></span>

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

### <span data-ttu-id="917c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="917c3-120">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="917c3-120">Resource Group Name</span></span>

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

### <span data-ttu-id="917c3-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="917c3-121">-UserMetadata</span></span>
<span data-ttu-id="917c3-122">Felhasználói metaadatok a ConsumerGroup szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="917c3-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="917c3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="917c3-123">-Confirm</span></span>
<span data-ttu-id="917c3-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="917c3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="917c3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="917c3-125">-WhatIf</span></span>
<span data-ttu-id="917c3-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="917c3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="917c3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="917c3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="917c3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917c3-128">CommonParameters</span></span>
<span data-ttu-id="917c3-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="917c3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917c3-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="917c3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917c3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="917c3-131">INPUTS</span></span>

### <span data-ttu-id="917c3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="917c3-132">System.String</span></span>

## <span data-ttu-id="917c3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="917c3-133">OUTPUTS</span></span>

### <span data-ttu-id="917c3-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="917c3-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="917c3-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="917c3-135">NOTES</span></span>

## <span data-ttu-id="917c3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="917c3-136">RELATED LINKS</span></span>
