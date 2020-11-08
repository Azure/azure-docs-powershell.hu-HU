---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: eec7294a15217be85b4c2248dac6506d54c2e6aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184971"
---
# <span data-ttu-id="c05b9-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="c05b9-101">New-AzEventHub</span></span>

## <span data-ttu-id="c05b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c05b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c05b9-103">Új esemény-hubot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c05b9-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="c05b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c05b9-104">SYNTAX</span></span>

### <span data-ttu-id="c05b9-105">EventhubPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c05b9-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c05b9-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c05b9-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c05b9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c05b9-107">DESCRIPTION</span></span>
<span data-ttu-id="c05b9-108">Az New-AzEventHub parancsmag létrehoz egy új Azure esemény-hubot.</span><span class="sxs-lookup"><span data-stu-id="c05b9-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="c05b9-109">Ha a Eventhub a rögzítési Leírás tulajdonságaival szeretné létrehozni, kövesse az alábbi lépéseket (2. példa).</span><span class="sxs-lookup"><span data-stu-id="c05b9-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="c05b9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c05b9-110">EXAMPLES</span></span>

### <span data-ttu-id="c05b9-111">Példa 1: – új EventHub létrehozása</span><span class="sxs-lookup"><span data-stu-id="c05b9-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="c05b9-112">Egy \` MyEventHubName nevű \` , 3 napos adatmegőrzési időszakot és két partíciót tartalmazó eseményt hoz létre a \` WestUS \` helyen, az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c05b9-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c05b9-113">2. példa: a Eventhub frissítése "CaptureDescription"</span><span class="sxs-lookup"><span data-stu-id="c05b9-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="c05b9-114">Létrehoz egy MyEventHubName nevű esemény \` \` -hubot egy 3 napos üzenet adatmegőrzési időszakmal, 2 partíciót és CaptureDescription tulajdonsággal a \` WestUS \` helyen, az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c05b9-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c05b9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c05b9-115">PARAMETERS</span></span>

### <span data-ttu-id="c05b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05b9-116">-DefaultProfile</span></span>
<span data-ttu-id="c05b9-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c05b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c05b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c05b9-118">-InputObject</span></span>
<span data-ttu-id="c05b9-119">EventHub beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="c05b9-119">EventHub Input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05b9-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c05b9-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="c05b9-121">Eventhub a napokban</span><span class="sxs-lookup"><span data-stu-id="c05b9-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05b9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c05b9-122">-Name</span></span>
<span data-ttu-id="c05b9-123">Eventhub neve</span><span class="sxs-lookup"><span data-stu-id="c05b9-123">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05b9-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c05b9-124">-Namespace</span></span>
<span data-ttu-id="c05b9-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="c05b9-125">Namespace Name</span></span>

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

### <span data-ttu-id="c05b9-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="c05b9-126">-PartitionCount</span></span>
<span data-ttu-id="c05b9-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="c05b9-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05b9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05b9-128">-ResourceGroupName</span></span>
<span data-ttu-id="c05b9-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c05b9-129">Resource Group Name</span></span>

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

### <span data-ttu-id="c05b9-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c05b9-130">-Confirm</span></span>
<span data-ttu-id="c05b9-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c05b9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c05b9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c05b9-132">-WhatIf</span></span>
<span data-ttu-id="c05b9-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c05b9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c05b9-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c05b9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c05b9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05b9-135">CommonParameters</span></span>
<span data-ttu-id="c05b9-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c05b9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05b9-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c05b9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05b9-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c05b9-138">INPUTS</span></span>

### <span data-ttu-id="c05b9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c05b9-139">System.String</span></span>

### <span data-ttu-id="c05b9-140">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="c05b9-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="c05b9-141">System. null ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c05b9-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c05b9-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c05b9-142">OUTPUTS</span></span>

### <span data-ttu-id="c05b9-143">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="c05b9-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="c05b9-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c05b9-144">NOTES</span></span>

## <span data-ttu-id="c05b9-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c05b9-145">RELATED LINKS</span></span>
