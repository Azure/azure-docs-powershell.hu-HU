---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: edccb9bf46a75c8a9f6fe0c577a87e13d11a2ba9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010933"
---
# <span data-ttu-id="ea719-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="ea719-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="ea719-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea719-102">SYNOPSIS</span></span>
<span data-ttu-id="ea719-103">Az esemény rácsa téma tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="ea719-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="ea719-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea719-104">SYNTAX</span></span>

### <span data-ttu-id="ea719-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea719-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea719-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea719-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea719-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea719-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea719-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea719-108">DESCRIPTION</span></span>
<span data-ttu-id="ea719-109">Az esemény rácsa téma tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="ea719-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="ea719-110">Ezzel a művelettel lecserélheti az esemény rácsvonalai című témakör címkéit.</span><span class="sxs-lookup"><span data-stu-id="ea719-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="ea719-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ea719-111">EXAMPLES</span></span>

### <span data-ttu-id="ea719-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ea719-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="ea719-113">A \` \` \` \` "részleg" és a "környezet" kifejezésekre cseréli a címkéket a Téma1 MyResourceGroupName az esemény rácsa témakörben.</span><span class="sxs-lookup"><span data-stu-id="ea719-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="ea719-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea719-114">PARAMETERS</span></span>

### <span data-ttu-id="ea719-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea719-115">-DefaultProfile</span></span>
<span data-ttu-id="ea719-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ea719-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea719-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea719-117">-InputObject</span></span>
<span data-ttu-id="ea719-118">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="ea719-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ea719-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea719-119">-Name</span></span>
<span data-ttu-id="ea719-120">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="ea719-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="ea719-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea719-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea719-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ea719-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea719-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea719-123">-ResourceId</span></span>
<span data-ttu-id="ea719-124">EventGrid téma ResourceID.</span><span class="sxs-lookup"><span data-stu-id="ea719-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="ea719-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="ea719-125">-Tag</span></span>
<span data-ttu-id="ea719-126">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ea719-126">Hashtables which represents resource Tag.</span></span>

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

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea719-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea719-127">-Confirm</span></span>
<span data-ttu-id="ea719-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea719-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea719-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea719-129">-WhatIf</span></span>
<span data-ttu-id="ea719-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ea719-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea719-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea719-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea719-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea719-132">CommonParameters</span></span>
<span data-ttu-id="ea719-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea719-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea719-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea719-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea719-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea719-135">INPUTS</span></span>

### <span data-ttu-id="ea719-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ea719-136">System.String</span></span>

### <span data-ttu-id="ea719-137">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ea719-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="ea719-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ea719-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ea719-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea719-139">OUTPUTS</span></span>

### <span data-ttu-id="ea719-140">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ea719-140">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="ea719-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea719-141">NOTES</span></span>

## <span data-ttu-id="ea719-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea719-142">RELATED LINKS</span></span>
