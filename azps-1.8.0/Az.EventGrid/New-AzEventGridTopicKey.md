---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: 8532e8411f474f769a4e9686ef89bf499f4f0272
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670865"
---
# <span data-ttu-id="450d7-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="450d7-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="450d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="450d7-102">SYNOPSIS</span></span>
<span data-ttu-id="450d7-103">Újra létrehoz egy Azure-esemény rácsvonal-témakörének megosztott elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="450d7-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="450d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="450d7-104">SYNTAX</span></span>

### <span data-ttu-id="450d7-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="450d7-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="450d7-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="450d7-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="450d7-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="450d7-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="450d7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="450d7-108">DESCRIPTION</span></span>
<span data-ttu-id="450d7-109">Újra létrehoz egy Azure-esemény rácsvonal-témakörének megosztott elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="450d7-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="450d7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="450d7-110">EXAMPLES</span></span>

### <span data-ttu-id="450d7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="450d7-111">Example 1</span></span>
```
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="450d7-112">Az \' \` \` erőforráscsoport-MyResourceGroupName az esemény rácshoz tartozó Key1 (az esemény rácsvonala \` \` ) téma1 tartozó kulcs ismételt létrehozása</span><span class="sxs-lookup"><span data-stu-id="450d7-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="450d7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="450d7-113">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="450d7-114">Az \' \` \` erőforráscsoport-MyResourceGroupName az esemény rácshoz tartozó Key1 (az esemény rácsvonala \` \` ) téma1 tartozó kulcs ismételt létrehozása</span><span class="sxs-lookup"><span data-stu-id="450d7-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="450d7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="450d7-115">PARAMETERS</span></span>

### <span data-ttu-id="450d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450d7-116">-DefaultProfile</span></span>
<span data-ttu-id="450d7-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="450d7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="450d7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="450d7-118">-InputObject</span></span>
<span data-ttu-id="450d7-119">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="450d7-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="450d7-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="450d7-120">-KeyName</span></span>
<span data-ttu-id="450d7-121">Annak a kulcsnak a neve, amelyet újra létre kell hoznia</span><span class="sxs-lookup"><span data-stu-id="450d7-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="450d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="450d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="450d7-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="450d7-123">Resource group name.</span></span>

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

### <span data-ttu-id="450d7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="450d7-124">-ResourceId</span></span>
<span data-ttu-id="450d7-125">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="450d7-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="450d7-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="450d7-126">-TopicName</span></span>
<span data-ttu-id="450d7-127">A témakör neve.</span><span class="sxs-lookup"><span data-stu-id="450d7-127">The name of the topic.</span></span>

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

### <span data-ttu-id="450d7-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="450d7-128">-Confirm</span></span>
<span data-ttu-id="450d7-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="450d7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="450d7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450d7-130">-WhatIf</span></span>
<span data-ttu-id="450d7-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="450d7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="450d7-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="450d7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="450d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450d7-133">CommonParameters</span></span>
<span data-ttu-id="450d7-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="450d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450d7-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="450d7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450d7-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="450d7-136">INPUTS</span></span>

### <span data-ttu-id="450d7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="450d7-137">System.String</span></span>

### <span data-ttu-id="450d7-138">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="450d7-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="450d7-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="450d7-139">OUTPUTS</span></span>

### <span data-ttu-id="450d7-140">Microsoft. Azure. Management. EventGrid. models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="450d7-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="450d7-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="450d7-141">NOTES</span></span>

## <span data-ttu-id="450d7-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="450d7-142">RELATED LINKS</span></span>
