---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
ms.openlocfilehash: 2c5bf49245da7ecac0f9d4351f5a66a39a663b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502572"
---
# <span data-ttu-id="2c37f-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="2c37f-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="2c37f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c37f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c37f-103">Új esemény-hubot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2c37f-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c37f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c37f-104">SYNTAX</span></span>

### <span data-ttu-id="2c37f-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2c37f-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c37f-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2c37f-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c37f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c37f-107">DESCRIPTION</span></span>
<span data-ttu-id="2c37f-108">Az New-AzureRmEventHub parancsmag létrehoz egy új Azure esemény-hubot.</span><span class="sxs-lookup"><span data-stu-id="2c37f-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="2c37f-109">Ha a Eventhub a rögzítési Leírás tulajdonságaival szeretné létrehozni, kövesse az alábbi lépéseket (2. példa).</span><span class="sxs-lookup"><span data-stu-id="2c37f-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="2c37f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2c37f-110">EXAMPLES</span></span>

### <span data-ttu-id="2c37f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2c37f-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="2c37f-112">Egy \` MyEventHubName nevű \` , 3 napos adatmegőrzési időszakot és két partíciót tartalmazó eseményt hoz létre a \` WestUS \` helyen, az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2c37f-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2c37f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2c37f-113">Example 2</span></span>
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

<span data-ttu-id="2c37f-114">Létrehoz egy MyEventHubName nevű esemény \` \` -hubot egy 3 napos üzenet adatmegőrzési időszakmal, 2 partíciót és CaptureDescription tulajdonsággal a \` WestUS \` helyen, az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2c37f-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2c37f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c37f-115">PARAMETERS</span></span>

### <span data-ttu-id="2c37f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c37f-116">-DefaultProfile</span></span>
<span data-ttu-id="2c37f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c37f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c37f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c37f-118">-InputObject</span></span>
<span data-ttu-id="2c37f-119">EventHub beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="2c37f-119">EventHub Input object</span></span>

```yaml
Type: PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c37f-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2c37f-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="2c37f-121">Eventhub a napokban</span><span class="sxs-lookup"><span data-stu-id="2c37f-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="2c37f-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c37f-122">-Name</span></span>
<span data-ttu-id="2c37f-123">Eventhub neve</span><span class="sxs-lookup"><span data-stu-id="2c37f-123">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c37f-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2c37f-124">-Namespace</span></span>
<span data-ttu-id="2c37f-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="2c37f-125">Namespace Name</span></span>

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

### <span data-ttu-id="2c37f-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="2c37f-126">-PartitionCount</span></span>
<span data-ttu-id="2c37f-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="2c37f-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="2c37f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c37f-128">-ResourceGroupName</span></span>
<span data-ttu-id="2c37f-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2c37f-129">Resource Group Name</span></span>

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

### <span data-ttu-id="2c37f-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c37f-130">-Confirm</span></span>
<span data-ttu-id="2c37f-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c37f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c37f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c37f-132">-WhatIf</span></span>
<span data-ttu-id="2c37f-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c37f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c37f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c37f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c37f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c37f-135">CommonParameters</span></span>
<span data-ttu-id="2c37f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c37f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2c37f-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c37f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c37f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c37f-138">INPUTS</span></span>

### <span data-ttu-id="2c37f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2c37f-139">System.String</span></span>
<span data-ttu-id="2c37f-140">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes System. null ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2c37f-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="2c37f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c37f-141">OUTPUTS</span></span>

### <span data-ttu-id="2c37f-142">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2c37f-142">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>


## <span data-ttu-id="2c37f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c37f-143">NOTES</span></span>

## <span data-ttu-id="2c37f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c37f-144">RELATED LINKS</span></span>
