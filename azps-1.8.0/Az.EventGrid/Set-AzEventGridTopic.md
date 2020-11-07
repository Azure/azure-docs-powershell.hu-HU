---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: bcba056777cd9a5eef42799b170c2dad69c8bbf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670863"
---
# <span data-ttu-id="1f5ba-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="1f5ba-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="1f5ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1f5ba-103">Az esemény rácsa téma tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="1f5ba-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="1f5ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f5ba-104">SYNTAX</span></span>

### <span data-ttu-id="1f5ba-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f5ba-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f5ba-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f5ba-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f5ba-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f5ba-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f5ba-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f5ba-108">DESCRIPTION</span></span>
<span data-ttu-id="1f5ba-109">Az esemény rácsa téma tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="1f5ba-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="1f5ba-110">Ezzel a művelettel lecserélheti az esemény rácsvonalai című témakör címkéit.</span><span class="sxs-lookup"><span data-stu-id="1f5ba-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="1f5ba-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1f5ba-111">EXAMPLES</span></span>

### <span data-ttu-id="1f5ba-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1f5ba-112">Example 1</span></span>
```
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="1f5ba-113">A \` \` \` \` "részleg" és a "környezet" kifejezésekre cseréli a címkéket a Téma1 MyResourceGroupName az esemény rácsa témakörben.</span><span class="sxs-lookup"><span data-stu-id="1f5ba-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="1f5ba-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f5ba-114">PARAMETERS</span></span>

### <span data-ttu-id="1f5ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f5ba-115">-DefaultProfile</span></span>
<span data-ttu-id="1f5ba-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1f5ba-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f5ba-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f5ba-117">-InputObject</span></span>
<span data-ttu-id="1f5ba-118">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="1f5ba-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="1f5ba-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f5ba-119">-Name</span></span>
<span data-ttu-id="1f5ba-120">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="1f5ba-120">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f5ba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f5ba-121">-ResourceGroupName</span></span>
<span data-ttu-id="1f5ba-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="1f5ba-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="1f5ba-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f5ba-123">-ResourceId</span></span>
<span data-ttu-id="1f5ba-124">EventGrid téma ResourceID.</span><span class="sxs-lookup"><span data-stu-id="1f5ba-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="1f5ba-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="1f5ba-125">-Tag</span></span>
<span data-ttu-id="1f5ba-126">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="1f5ba-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f5ba-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f5ba-127">-Confirm</span></span>
<span data-ttu-id="1f5ba-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f5ba-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f5ba-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f5ba-129">-WhatIf</span></span>
<span data-ttu-id="1f5ba-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f5ba-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f5ba-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f5ba-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f5ba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f5ba-132">CommonParameters</span></span>
<span data-ttu-id="1f5ba-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f5ba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f5ba-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f5ba-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f5ba-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f5ba-135">INPUTS</span></span>

### <span data-ttu-id="1f5ba-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1f5ba-136">System.String</span></span>

### <span data-ttu-id="1f5ba-137">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="1f5ba-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="1f5ba-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f5ba-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1f5ba-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f5ba-139">OUTPUTS</span></span>

### <span data-ttu-id="1f5ba-140">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="1f5ba-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="1f5ba-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f5ba-141">NOTES</span></span>

## <span data-ttu-id="1f5ba-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f5ba-142">RELATED LINKS</span></span>
