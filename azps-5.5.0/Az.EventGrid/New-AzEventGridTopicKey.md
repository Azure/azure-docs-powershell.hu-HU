---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155723"
---
# <span data-ttu-id="029de-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="029de-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="029de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="029de-102">SYNOPSIS</span></span>
<span data-ttu-id="029de-103">Az Azure Event Grid-témakör megosztott hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="029de-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="029de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="029de-104">SYNTAX</span></span>

### <span data-ttu-id="029de-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="029de-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="029de-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="029de-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="029de-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="029de-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="029de-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="029de-108">DESCRIPTION</span></span>
<span data-ttu-id="029de-109">Az Azure Event Grid-témakör megosztott hozzáférési kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="029de-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="029de-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="029de-110">EXAMPLES</span></span>

### <span data-ttu-id="029de-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="029de-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="029de-112">A \' \` \` \` MyResourceGroupName erőforráscsoport Eseményrács témakör1 kulcskulcs1\\ kulcsának újragenerálásával. \`</span><span class="sxs-lookup"><span data-stu-id="029de-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="029de-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="029de-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="029de-114">A \' \` \` \` MyResourceGroupName erőforráscsoport Eseményrács témakör1 kulcskulcs1\\ kulcsának újragenerálásával. \`</span><span class="sxs-lookup"><span data-stu-id="029de-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="029de-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="029de-115">PARAMETERS</span></span>

### <span data-ttu-id="029de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="029de-116">-DefaultProfile</span></span>
<span data-ttu-id="029de-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="029de-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="029de-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="029de-118">-InputObject</span></span>
<span data-ttu-id="029de-119">EventGrid Topic objektum.</span><span class="sxs-lookup"><span data-stu-id="029de-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="029de-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="029de-120">-KeyName</span></span>
<span data-ttu-id="029de-121">Az újragenerálható kulcs neve</span><span class="sxs-lookup"><span data-stu-id="029de-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="029de-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="029de-122">-ResourceGroupName</span></span>
<span data-ttu-id="029de-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="029de-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="029de-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="029de-124">-ResourceId</span></span>
<span data-ttu-id="029de-125">Az Eseményrács témakört képviselő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="029de-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="029de-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="029de-126">-TopicName</span></span>
<span data-ttu-id="029de-127">A témakör neve.</span><span class="sxs-lookup"><span data-stu-id="029de-127">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="029de-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="029de-128">-Confirm</span></span>
<span data-ttu-id="029de-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="029de-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="029de-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="029de-130">-WhatIf</span></span>
<span data-ttu-id="029de-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="029de-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="029de-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="029de-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="029de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="029de-133">CommonParameters</span></span>
<span data-ttu-id="029de-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="029de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="029de-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="029de-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="029de-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="029de-136">INPUTS</span></span>

### <span data-ttu-id="029de-137">System.String</span><span class="sxs-lookup"><span data-stu-id="029de-137">System.String</span></span>

### <span data-ttu-id="029de-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="029de-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="029de-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="029de-139">OUTPUTS</span></span>

### <span data-ttu-id="029de-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="029de-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="029de-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="029de-141">NOTES</span></span>

## <span data-ttu-id="029de-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="029de-142">RELATED LINKS</span></span>
