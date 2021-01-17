---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: fc108c633b70cc1eed32bcc0574ad25109a065fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469882"
---
# <span data-ttu-id="506a9-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="506a9-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="506a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="506a9-102">SYNOPSIS</span></span>
<span data-ttu-id="506a9-103">Lekérte egy adott Eseményközpont fogyasztói csoportjának adatait, vagy lekérte egy fogyasztói csoportok listáját az Eseményközpontban.</span><span class="sxs-lookup"><span data-stu-id="506a9-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="506a9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="506a9-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="506a9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="506a9-105">DESCRIPTION</span></span>
<span data-ttu-id="506a9-106">A Get-AzEventHubConsumerGroup parancsmag vagy egy megadott Event Hubs fogyasztói csoport adatait, vagy egy adott eseményközpont fogyasztói csoportjainak listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="506a9-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="506a9-107">Ha meg van biztosítanak egy fogyasztói csoport nevét, egyetlen fogyasztói csoport adatait is visszaadja a szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="506a9-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="506a9-108">Ha nincs megadva egy fogyasztói csoport neve, a megadott Eseményközpontban visszaadja a fogyasztói csoportok listáját.</span><span class="sxs-lookup"><span data-stu-id="506a9-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="506a9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="506a9-109">EXAMPLES</span></span>

### <span data-ttu-id="506a9-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="506a9-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="506a9-111">A MyConsumerGroupName fogyasztói csoportot beveszi az Event Hub MyEventHubName eseményközpontba, amely a MyNamespaceName nevű névtérben létezik a \` \` \` \` \` \` \` MyResourceGroupName \` erőforráscsoporttal.</span><span class="sxs-lookup"><span data-stu-id="506a9-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="506a9-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="506a9-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="506a9-113">A \` \` \` \` \` MyResourceGroupName erőforráscsoport myResourceGroupName nevű erőforráscsoportjával a MyNamespaceName névterében található, az Event Hub MyEventHubName nevű fogyasztói csoportjainak listáját \` tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="506a9-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="506a9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="506a9-114">PARAMETERS</span></span>

### <span data-ttu-id="506a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506a9-115">-DefaultProfile</span></span>
<span data-ttu-id="506a9-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="506a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="506a9-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="506a9-117">-EventHub</span></span>
<span data-ttu-id="506a9-118">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="506a9-118">EventHub Name</span></span>

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

### <span data-ttu-id="506a9-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="506a9-119">-MaxCount</span></span>
<span data-ttu-id="506a9-120">Határozza meg, hogy legfeljebb hány ConsumerGroups csoportot kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="506a9-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="506a9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="506a9-121">-Name</span></span>
<span data-ttu-id="506a9-122">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="506a9-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="506a9-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="506a9-123">-Namespace</span></span>
<span data-ttu-id="506a9-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="506a9-124">Namespace Name</span></span>

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

### <span data-ttu-id="506a9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="506a9-125">-ResourceGroupName</span></span>
<span data-ttu-id="506a9-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="506a9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="506a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506a9-127">CommonParameters</span></span>
<span data-ttu-id="506a9-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="506a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506a9-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="506a9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506a9-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="506a9-130">INPUTS</span></span>

### <span data-ttu-id="506a9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="506a9-131">System.String</span></span>

## <span data-ttu-id="506a9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="506a9-132">OUTPUTS</span></span>

### <span data-ttu-id="506a9-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="506a9-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="506a9-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="506a9-134">NOTES</span></span>

## <span data-ttu-id="506a9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="506a9-135">RELATED LINKS</span></span>
