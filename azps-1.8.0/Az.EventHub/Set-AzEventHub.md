---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: ad7d4a1cefaadf3f1c2f12b9ef3a1b516c3813fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670815"
---
# <span data-ttu-id="faef1-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="faef1-101">Set-AzEventHub</span></span>

## <span data-ttu-id="faef1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="faef1-102">SYNOPSIS</span></span>
<span data-ttu-id="faef1-103">Frissíti a megadott esemény hub-ot.</span><span class="sxs-lookup"><span data-stu-id="faef1-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="faef1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="faef1-104">SYNTAX</span></span>

### <span data-ttu-id="faef1-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="faef1-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="faef1-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="faef1-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faef1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="faef1-107">DESCRIPTION</span></span>
<span data-ttu-id="faef1-108">A Set-AzEventHub parancsmag frissíti a megadott esemény központi verziójának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="faef1-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="faef1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="faef1-109">EXAMPLES</span></span>

### <span data-ttu-id="faef1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="faef1-110">Example 1</span></span>
<span data-ttu-id="faef1-111">Ha frissíteni szeretné a Eventhub a rögzítési Leírás tulajdonságaival, kövesse az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="faef1-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="faef1-112">Frissíti a \` \` MyCreatedEventHub objektum által képviselt \` MyEventHubName \` , amelyben az üzenet adatmegőrzési időszaka 4 napra, a partíciók száma 2 és a CaptureDescription tulajdonságra van állítva</span><span class="sxs-lookup"><span data-stu-id="faef1-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="faef1-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="faef1-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="faef1-114">Frissíti a \` \` MyCreatedEventHub objektum által reprezentált esemény \` -hub MyEventHubName, az \` üzenet adatmegőrzési időszakát 4 napra, a partíciók számát pedig 2 értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="faef1-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="faef1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="faef1-115">PARAMETERS</span></span>

### <span data-ttu-id="faef1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faef1-116">-DefaultProfile</span></span>
<span data-ttu-id="faef1-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="faef1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faef1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faef1-118">-InputObject</span></span>
<span data-ttu-id="faef1-119">EventHub objektum</span><span class="sxs-lookup"><span data-stu-id="faef1-119">EventHub object</span></span>

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

### <span data-ttu-id="faef1-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="faef1-120">-messageRetentionInDays</span></span>
<span data-ttu-id="faef1-121">Eventhub a napokban</span><span class="sxs-lookup"><span data-stu-id="faef1-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="faef1-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="faef1-122">-Name</span></span>
<span data-ttu-id="faef1-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="faef1-123">Namespace Name</span></span>

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

### <span data-ttu-id="faef1-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="faef1-124">-Namespace</span></span>
<span data-ttu-id="faef1-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="faef1-125">Namespace Name</span></span>

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

### <span data-ttu-id="faef1-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="faef1-126">-partitionCount</span></span>
<span data-ttu-id="faef1-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="faef1-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="faef1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faef1-128">-ResourceGroupName</span></span>
<span data-ttu-id="faef1-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="faef1-129">Resource Group Name</span></span>

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

### <span data-ttu-id="faef1-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="faef1-130">-Confirm</span></span>
<span data-ttu-id="faef1-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="faef1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faef1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faef1-132">-WhatIf</span></span>
<span data-ttu-id="faef1-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="faef1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faef1-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="faef1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faef1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faef1-135">CommonParameters</span></span>
<span data-ttu-id="faef1-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="faef1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faef1-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faef1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faef1-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="faef1-138">INPUTS</span></span>

### <span data-ttu-id="faef1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="faef1-139">System.String</span></span>

### <span data-ttu-id="faef1-140">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="faef1-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="faef1-141">System. null ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="faef1-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="faef1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="faef1-142">OUTPUTS</span></span>

### <span data-ttu-id="faef1-143">Microsoft. Azure. Command. EventHub. models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="faef1-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="faef1-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="faef1-144">NOTES</span></span>

## <span data-ttu-id="faef1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="faef1-145">RELATED LINKS</span></span>
