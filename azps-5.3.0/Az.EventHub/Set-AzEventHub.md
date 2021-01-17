---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: a5a1f0bbe0f353014047e795c467a645e244f125
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386915"
---
# <span data-ttu-id="ad617-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="ad617-101">Set-AzEventHub</span></span>

## <span data-ttu-id="ad617-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad617-102">SYNOPSIS</span></span>
<span data-ttu-id="ad617-103">Frissíti a megadott eseményközpontot.</span><span class="sxs-lookup"><span data-stu-id="ad617-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="ad617-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad617-104">SYNTAX</span></span>

### <span data-ttu-id="ad617-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ad617-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad617-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ad617-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad617-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad617-107">DESCRIPTION</span></span>
<span data-ttu-id="ad617-108">A Set-AzEventHub parancsmag frissíti a megadott Eseményközpont tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="ad617-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="ad617-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad617-109">EXAMPLES</span></span>

### <span data-ttu-id="ad617-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ad617-110">Example 1</span></span>
<span data-ttu-id="ad617-111">Ha frissítenie kell az Eventhubot a Leírás rögzítése tulajdonsággal, kérjük, kövesse az alábbi lépéseket.</span><span class="sxs-lookup"><span data-stu-id="ad617-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

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

<span data-ttu-id="ad617-112">Frissíti a \` MyCreatedEventHub objektum által képviselt Event Hub MyEventHubName eseményközpontot, az üzenetmegőrzési időszakot 4 napra, a partíciók számát 2-re és \` \` a \` CaptureDescription tulajdonságokra.</span><span class="sxs-lookup"><span data-stu-id="ad617-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="ad617-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ad617-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="ad617-114">Frissíti a \` MyCreatedEventHub objektum által képviselt Event Hub MyEventHubName eseményközpontot, az üzenetmegőrzési időszakot 4 napra, a partíciók számát \` \` pedig \` 2-re.</span><span class="sxs-lookup"><span data-stu-id="ad617-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="ad617-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad617-115">PARAMETERS</span></span>

### <span data-ttu-id="ad617-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad617-116">-DefaultProfile</span></span>
<span data-ttu-id="ad617-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad617-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad617-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad617-118">-InputObject</span></span>
<span data-ttu-id="ad617-119">EventHub objektum</span><span class="sxs-lookup"><span data-stu-id="ad617-119">EventHub object</span></span>

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

### <span data-ttu-id="ad617-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ad617-120">-messageRetentionInDays</span></span>
<span data-ttu-id="ad617-121">Eventhub Message Retention In Days</span><span class="sxs-lookup"><span data-stu-id="ad617-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="ad617-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ad617-122">-Name</span></span>
<span data-ttu-id="ad617-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ad617-123">Namespace Name</span></span>

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

### <span data-ttu-id="ad617-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ad617-124">-Namespace</span></span>
<span data-ttu-id="ad617-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ad617-125">Namespace Name</span></span>

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

### <span data-ttu-id="ad617-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="ad617-126">-partitionCount</span></span>
<span data-ttu-id="ad617-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="ad617-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="ad617-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad617-128">-ResourceGroupName</span></span>
<span data-ttu-id="ad617-129">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ad617-129">Resource Group Name</span></span>

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

### <span data-ttu-id="ad617-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad617-130">-Confirm</span></span>
<span data-ttu-id="ad617-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ad617-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad617-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad617-132">-WhatIf</span></span>
<span data-ttu-id="ad617-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ad617-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad617-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad617-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad617-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad617-135">CommonParameters</span></span>
<span data-ttu-id="ad617-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad617-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad617-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad617-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad617-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad617-138">INPUTS</span></span>

### <span data-ttu-id="ad617-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ad617-139">System.String</span></span>

### <span data-ttu-id="ad617-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="ad617-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="ad617-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ad617-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ad617-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad617-142">OUTPUTS</span></span>

### <span data-ttu-id="ad617-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="ad617-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="ad617-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad617-144">NOTES</span></span>

## <span data-ttu-id="ad617-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad617-145">RELATED LINKS</span></span>
