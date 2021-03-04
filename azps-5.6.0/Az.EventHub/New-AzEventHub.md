---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: 366bb4879b2db8bbb4a4335442a4abc6f07a5221
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921202"
---
# <span data-ttu-id="3ec30-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="3ec30-101">New-AzEventHub</span></span>

## <span data-ttu-id="3ec30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ec30-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec30-103">Létrehoz egy új eseményközpontot.</span><span class="sxs-lookup"><span data-stu-id="3ec30-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="3ec30-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3ec30-104">SYNTAX</span></span>

### <span data-ttu-id="3ec30-105">EventhubPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ec30-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ec30-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3ec30-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ec30-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3ec30-107">DESCRIPTION</span></span>
<span data-ttu-id="3ec30-108">A New-AzEventHub parancsmag létrehoz egy új Azure Event Hubot.</span><span class="sxs-lookup"><span data-stu-id="3ec30-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="3ec30-109">Az Eventhub létrehozásához a Leírás rögzítése tulajdonsággal, kérjük, kövesse az alábbi lépéseket (2. példa).</span><span class="sxs-lookup"><span data-stu-id="3ec30-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="3ec30-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3ec30-110">EXAMPLES</span></span>

### <span data-ttu-id="3ec30-111">1. példa: Új EventHub létrehozása</span><span class="sxs-lookup"><span data-stu-id="3ec30-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="3ec30-112">Létrehoz egy MyEventHubName nevű eseményközpontot egy 3 napos üzenetmegőrzési időtartammal és két partícióval a \` \` \` WestUS-helyen, a \` \` MyResourceGroupName \` erőforráscsoporttal.</span><span class="sxs-lookup"><span data-stu-id="3ec30-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3ec30-113">2. példa: Az Eventhub frissítése a "CaptureDescription" névvel</span><span class="sxs-lookup"><span data-stu-id="3ec30-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
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

<span data-ttu-id="3ec30-114">Létrehozza a MyEventHubName nevű eseményközpontot egy 3 napos üzenetmegőrzési időtartammal, 2 partícióval és CaptureDescription tulajdonsággal a \` \` \` WestUS-helyen, a \` \` MyResourceGroupName \` erőforráscsoporttal.</span><span class="sxs-lookup"><span data-stu-id="3ec30-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3ec30-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ec30-115">PARAMETERS</span></span>

### <span data-ttu-id="3ec30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec30-116">-DefaultProfile</span></span>
<span data-ttu-id="3ec30-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ec30-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ec30-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ec30-118">-InputObject</span></span>
<span data-ttu-id="3ec30-119">EventHub Input objektum</span><span class="sxs-lookup"><span data-stu-id="3ec30-119">EventHub Input object</span></span>

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

### <span data-ttu-id="3ec30-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3ec30-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="3ec30-121">Eventhub Message Retention In Days</span><span class="sxs-lookup"><span data-stu-id="3ec30-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="3ec30-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3ec30-122">-Name</span></span>
<span data-ttu-id="3ec30-123">Eventhub Name</span><span class="sxs-lookup"><span data-stu-id="3ec30-123">Eventhub Name</span></span>

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

### <span data-ttu-id="3ec30-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3ec30-124">-Namespace</span></span>
<span data-ttu-id="3ec30-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3ec30-125">Namespace Name</span></span>

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

### <span data-ttu-id="3ec30-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="3ec30-126">-PartitionCount</span></span>
<span data-ttu-id="3ec30-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="3ec30-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="3ec30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ec30-128">-ResourceGroupName</span></span>
<span data-ttu-id="3ec30-129">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3ec30-129">Resource Group Name</span></span>

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

### <span data-ttu-id="3ec30-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ec30-130">-Confirm</span></span>
<span data-ttu-id="3ec30-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3ec30-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ec30-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ec30-132">-WhatIf</span></span>
<span data-ttu-id="3ec30-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3ec30-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ec30-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ec30-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ec30-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec30-135">CommonParameters</span></span>
<span data-ttu-id="3ec30-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec30-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec30-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ec30-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec30-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ec30-138">INPUTS</span></span>

### <span data-ttu-id="3ec30-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3ec30-139">System.String</span></span>

### <span data-ttu-id="3ec30-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3ec30-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="3ec30-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3ec30-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3ec30-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ec30-142">OUTPUTS</span></span>

### <span data-ttu-id="3ec30-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3ec30-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="3ec30-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3ec30-144">NOTES</span></span>

## <span data-ttu-id="3ec30-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ec30-145">RELATED LINKS</span></span>
