---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185471"
---
# <span data-ttu-id="7437c-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="7437c-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="7437c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7437c-102">SYNOPSIS</span></span>
<span data-ttu-id="7437c-103">Újra létrehoz egy Azure-esemény rácsvonal-témakörének megosztott elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="7437c-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="7437c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7437c-104">SYNTAX</span></span>

### <span data-ttu-id="7437c-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7437c-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7437c-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7437c-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7437c-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7437c-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7437c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7437c-108">DESCRIPTION</span></span>
<span data-ttu-id="7437c-109">Újra létrehoz egy Azure-esemény rácsvonal-témakörének megosztott elérési kulcsát.</span><span class="sxs-lookup"><span data-stu-id="7437c-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="7437c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7437c-110">EXAMPLES</span></span>

### <span data-ttu-id="7437c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7437c-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="7437c-112">Az \' \` \` erőforráscsoport-MyResourceGroupName az esemény rácshoz tartozó Key1 (az esemény rácsvonala \` \` ) téma1 tartozó kulcs ismételt létrehozása</span><span class="sxs-lookup"><span data-stu-id="7437c-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7437c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7437c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="7437c-114">Az \' \` \` erőforráscsoport-MyResourceGroupName az esemény rácshoz tartozó Key1 (az esemény rácsvonala \` \` ) téma1 tartozó kulcs ismételt létrehozása</span><span class="sxs-lookup"><span data-stu-id="7437c-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7437c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7437c-115">PARAMETERS</span></span>

### <span data-ttu-id="7437c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7437c-116">-DefaultProfile</span></span>
<span data-ttu-id="7437c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7437c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7437c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7437c-118">-InputObject</span></span>
<span data-ttu-id="7437c-119">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="7437c-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="7437c-120">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="7437c-120">-KeyName</span></span>
<span data-ttu-id="7437c-121">Annak a kulcsnak a neve, amelyet újra létre kell hoznia</span><span class="sxs-lookup"><span data-stu-id="7437c-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="7437c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7437c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7437c-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="7437c-123">Resource group name.</span></span>

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

### <span data-ttu-id="7437c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7437c-124">-ResourceId</span></span>
<span data-ttu-id="7437c-125">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7437c-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="7437c-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7437c-126">-TopicName</span></span>
<span data-ttu-id="7437c-127">A témakör neve.</span><span class="sxs-lookup"><span data-stu-id="7437c-127">The name of the topic.</span></span>

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

### <span data-ttu-id="7437c-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7437c-128">-Confirm</span></span>
<span data-ttu-id="7437c-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7437c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7437c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7437c-130">-WhatIf</span></span>
<span data-ttu-id="7437c-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7437c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7437c-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7437c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7437c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7437c-133">CommonParameters</span></span>
<span data-ttu-id="7437c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7437c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7437c-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7437c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7437c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7437c-136">INPUTS</span></span>

### <span data-ttu-id="7437c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7437c-137">System.String</span></span>

### <span data-ttu-id="7437c-138">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="7437c-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="7437c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7437c-139">OUTPUTS</span></span>

### <span data-ttu-id="7437c-140">Microsoft. Azure. Management. EventGrid. models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="7437c-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="7437c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7437c-141">NOTES</span></span>

## <span data-ttu-id="7437c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7437c-142">RELATED LINKS</span></span>