---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: c6a975ee5071ff3f31ae3daa0e6e9bf6ed9a42ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495376"
---
# <span data-ttu-id="2f027-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="2f027-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="2f027-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f027-102">SYNOPSIS</span></span>
<span data-ttu-id="2f027-103">Az esemény rácsa téma tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="2f027-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f027-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f027-104">SYNTAX</span></span>

### <span data-ttu-id="2f027-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f027-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f027-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f027-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f027-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f027-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f027-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f027-108">DESCRIPTION</span></span>
<span data-ttu-id="2f027-109">Az esemény rácsa téma tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="2f027-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="2f027-110">Ezzel a művelettel lecserélheti az esemény rácsvonalai című témakör címkéit.</span><span class="sxs-lookup"><span data-stu-id="2f027-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="2f027-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2f027-111">EXAMPLES</span></span>

### <span data-ttu-id="2f027-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f027-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="2f027-113">A \` \` \` \` "részleg" és a "környezet" kifejezésekre cseréli a címkéket a Téma1 MyResourceGroupName az esemény rácsa témakörben.</span><span class="sxs-lookup"><span data-stu-id="2f027-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="2f027-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f027-114">PARAMETERS</span></span>

### <span data-ttu-id="2f027-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f027-115">-DefaultProfile</span></span>
<span data-ttu-id="2f027-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2f027-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f027-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f027-117">-InputObject</span></span>
<span data-ttu-id="2f027-118">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="2f027-118">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f027-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f027-119">-Name</span></span>
<span data-ttu-id="2f027-120">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="2f027-120">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f027-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f027-121">-ResourceGroupName</span></span>
<span data-ttu-id="2f027-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="2f027-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f027-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f027-123">-ResourceId</span></span>
<span data-ttu-id="2f027-124">EventGrid téma ResourceID.</span><span class="sxs-lookup"><span data-stu-id="2f027-124">EventGrid Topic ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f027-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="2f027-125">-Tag</span></span>
<span data-ttu-id="2f027-126">Hashtables, amely az erőforrás címkét jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2f027-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f027-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f027-127">-Confirm</span></span>
<span data-ttu-id="2f027-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f027-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f027-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f027-129">-WhatIf</span></span>
<span data-ttu-id="2f027-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f027-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f027-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f027-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f027-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f027-132">CommonParameters</span></span>
<span data-ttu-id="2f027-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f027-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f027-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f027-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f027-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f027-135">INPUTS</span></span>

### <span data-ttu-id="2f027-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2f027-136">System.String</span></span>
<span data-ttu-id="2f027-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2f027-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2f027-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f027-138">OUTPUTS</span></span>

### <span data-ttu-id="2f027-139">Microsoft. Azure. Management. EventGrid. models. topic</span><span class="sxs-lookup"><span data-stu-id="2f027-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="2f027-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f027-140">NOTES</span></span>

## <span data-ttu-id="2f027-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f027-141">RELATED LINKS</span></span>

