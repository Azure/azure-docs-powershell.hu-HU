---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 2ff36708ba9b8303c8b8763146c81ee4e4d8b209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500043"
---
# <span data-ttu-id="7c187-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="7c187-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="7c187-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c187-102">SYNOPSIS</span></span>
<span data-ttu-id="7c187-103">Frissíti a megadott esemény hub-ot.</span><span class="sxs-lookup"><span data-stu-id="7c187-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c187-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c187-104">SYNTAX</span></span>

### <span data-ttu-id="7c187-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c187-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7c187-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="7c187-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7c187-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c187-107">DESCRIPTION</span></span>
<span data-ttu-id="7c187-108">A Set-AzureRmEventHub parancsmag frissíti a megadott esemény központi verziójának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="7c187-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="7c187-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7c187-109">EXAMPLES</span></span>

### <span data-ttu-id="7c187-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7c187-110">Example 1</span></span>
<span data-ttu-id="7c187-111">Ha frissíteni szeretné a Eventhub a rögzítési Leírás tulajdonságaival, kövesse az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="7c187-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="7c187-112">Frissíti a \` \` MyCreatedEventHub objektum által képviselt \` MyEventHubName \` , amelyben az üzenet adatmegőrzési időszaka 4 napra, a partíciók száma 2 és a CaptureDescription tulajdonságra van állítva</span><span class="sxs-lookup"><span data-stu-id="7c187-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="7c187-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7c187-113">Example 2</span></span>

```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="7c187-114">Frissíti a \` \` MyCreatedEventHub objektum által reprezentált esemény \` -hub MyEventHubName, az \` üzenet adatmegőrzési időszakát 4 napra, a partíciók számát pedig 2 értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="7c187-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="7c187-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c187-115">PARAMETERS</span></span>

### <span data-ttu-id="7c187-116">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7c187-116">-messageRetentionInDays</span></span>
<span data-ttu-id="7c187-117">Az esemény központi üzenetének adatmegőrzési időszaka napokban.</span><span class="sxs-lookup"><span data-stu-id="7c187-117">Event Hub message retention period, in days.</span></span>

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

### <span data-ttu-id="7c187-118">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="7c187-118">-partitionCount</span></span>
<span data-ttu-id="7c187-119">A partíciók száma az esemény központban.</span><span class="sxs-lookup"><span data-stu-id="7c187-119">Number of partitions on this Event Hub.</span></span>

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

### <span data-ttu-id="7c187-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c187-120">-ResourceGroupName</span></span>
<span data-ttu-id="7c187-121">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7c187-121">Resource group name.</span></span>

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

### <span data-ttu-id="7c187-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7c187-122">-Confirm</span></span>
<span data-ttu-id="7c187-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c187-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c187-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c187-124">-WhatIf</span></span>
<span data-ttu-id="7c187-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7c187-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c187-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c187-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c187-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c187-127">-InputObject</span></span>
<span data-ttu-id="7c187-128">EventHub objektum</span><span class="sxs-lookup"><span data-stu-id="7c187-128">EventHub object.</span></span>

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

### <span data-ttu-id="7c187-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7c187-129">-Name</span></span>
<span data-ttu-id="7c187-130">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="7c187-130">Namespace Name.</span></span>

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

### <span data-ttu-id="7c187-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7c187-131">-Namespace</span></span>
<span data-ttu-id="7c187-132">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="7c187-132">Namespace Name.</span></span>

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

## <span data-ttu-id="7c187-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c187-133">INPUTS</span></span>

### <span data-ttu-id="7c187-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7c187-134">System.String</span></span>

## <span data-ttu-id="7c187-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c187-135">OUTPUTS</span></span>

### <span data-ttu-id="7c187-136">Microsoft. Azure. Command. EventHub. models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="7c187-136">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="7c187-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c187-137">NOTES</span></span>

## <span data-ttu-id="7c187-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c187-138">RELATED LINKS</span></span>

