---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 656e010a05ce1272355f689be8513ecadd330e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505019"
---
# <span data-ttu-id="f298e-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="f298e-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="f298e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f298e-102">SYNOPSIS</span></span>
<span data-ttu-id="f298e-103">Új esemény-hubot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f298e-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f298e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f298e-104">SYNTAX</span></span>

### <span data-ttu-id="f298e-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f298e-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f298e-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f298e-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f298e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f298e-107">DESCRIPTION</span></span>
<span data-ttu-id="f298e-108">Az New-AzureRmEventHub parancsmag létrehoz egy új Azure esemény-hubot.</span><span class="sxs-lookup"><span data-stu-id="f298e-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="f298e-109">Ha a Eventhub a rögzítési Leírás tulajdonságaival szeretné létrehozni, kövesse az alábbi lépéseket (2. példa).</span><span class="sxs-lookup"><span data-stu-id="f298e-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 


## <span data-ttu-id="f298e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f298e-110">EXAMPLES</span></span>

### <span data-ttu-id="f298e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f298e-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="f298e-112">Egy \` MyEventHubName nevű \` , 3 napos adatmegőrzési időszakot és két partíciót tartalmazó eseményt hoz létre a \` WestUS \` helyen, az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f298e-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f298e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f298e-113">Example 2</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="f298e-114">Létrehoz egy MyEventHubName nevű esemény \` \` -hubot egy 3 napos üzenet adatmegőrzési időszakmal, 2 partíciót és CaptureDescription tulajdonsággal a \` WestUS \` helyen, az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f298e-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f298e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f298e-115">PARAMETERS</span></span>

### <span data-ttu-id="f298e-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="f298e-116">-Location</span></span>
<span data-ttu-id="f298e-117">Namespace földrajzi helye.</span><span class="sxs-lookup"><span data-stu-id="f298e-117">Namespace geographic location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f298e-118">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f298e-118">-MessageRetentionInDays</span></span>
<span data-ttu-id="f298e-119">Esemény-hubok: az üzenet retenciós ideje napokban.</span><span class="sxs-lookup"><span data-stu-id="f298e-119">Event Hubs message retention time in days.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f298e-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="f298e-120">-PartitionCount</span></span>
<span data-ttu-id="f298e-121">A partíciók száma az esemény központban.</span><span class="sxs-lookup"><span data-stu-id="f298e-121">Number of partitions in the Event Hub.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f298e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f298e-122">-ResourceGroupName</span></span>
<span data-ttu-id="f298e-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f298e-123">Resource group name.</span></span>

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

### <span data-ttu-id="f298e-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f298e-124">-Confirm</span></span>
<span data-ttu-id="f298e-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f298e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f298e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f298e-126">-WhatIf</span></span>
<span data-ttu-id="f298e-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f298e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f298e-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f298e-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f298e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f298e-129">-InputObject</span></span>
<span data-ttu-id="f298e-130">EventHub bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="f298e-130">EventHub Input object.</span></span>

```yaml
Type: EventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f298e-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f298e-131">-Name</span></span>
<span data-ttu-id="f298e-132">Eventhub neve</span><span class="sxs-lookup"><span data-stu-id="f298e-132">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f298e-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f298e-133">-Namespace</span></span>
<span data-ttu-id="f298e-134">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f298e-134">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="f298e-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f298e-135">INPUTS</span></span>

### <span data-ttu-id="f298e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f298e-136">System.String</span></span>

## <span data-ttu-id="f298e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f298e-137">OUTPUTS</span></span>

### <span data-ttu-id="f298e-138">Microsoft. Azure. Command. EventHub. models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f298e-138">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="f298e-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f298e-139">NOTES</span></span>

## <span data-ttu-id="f298e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f298e-140">RELATED LINKS</span></span>

