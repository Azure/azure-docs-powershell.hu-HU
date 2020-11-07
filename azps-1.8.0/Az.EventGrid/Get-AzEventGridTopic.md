---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 23004583a08dbcf5ef8785b62d0457b6b6ee0897
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670878"
---
# <span data-ttu-id="a3b06-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="a3b06-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="a3b06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3b06-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b06-103">Az aktuális Azure-előfizetésből kinyeri az esemény rácsvonalait ismertető témakör részleteit</span><span class="sxs-lookup"><span data-stu-id="a3b06-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="a3b06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3b06-104">SYNTAX</span></span>

### <span data-ttu-id="a3b06-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3b06-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3b06-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b06-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3b06-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b06-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3b06-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3b06-108">DESCRIPTION</span></span>
<span data-ttu-id="a3b06-109">A Get-AzEventGridTopic parancsmag az aktuális Azure-előfizetésből származó adott esemény rácsvonalait ismerteti, vagy az aktuális Azure-előfizetésben lévő összes esemény rácsos témakörének listáját.</span><span class="sxs-lookup"><span data-stu-id="a3b06-109">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="a3b06-110">Ha a téma neve meg van határozva, az egyetlen esemény rácsa témakör részleteit adja vissza a program.</span><span class="sxs-lookup"><span data-stu-id="a3b06-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="a3b06-111">Ha a téma neve nincs megadva, a program a témakörök listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="a3b06-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="a3b06-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a3b06-112">EXAMPLES</span></span>

### <span data-ttu-id="a3b06-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a3b06-113">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="a3b06-114">Az téma1 MyResourceGroupName az esemény rácsa témakör részleteit kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="a3b06-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a3b06-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="a3b06-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="a3b06-116">Az téma1 MyResourceGroupName az esemény rácsa témakör részleteit kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="a3b06-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a3b06-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="a3b06-117">Example 3</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="a3b06-118">Az erőforráscsoportok MyResourceGroupName az esemény Rácsával kapcsolatos témakörök felsorolása \` \` .</span><span class="sxs-lookup"><span data-stu-id="a3b06-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a3b06-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="a3b06-119">Example 4</span></span>
```
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="a3b06-120">Az előfizetésben szereplő összes esemény rácsvonal-témakörének listázása</span><span class="sxs-lookup"><span data-stu-id="a3b06-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="a3b06-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3b06-121">PARAMETERS</span></span>

### <span data-ttu-id="a3b06-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b06-122">-DefaultProfile</span></span>
<span data-ttu-id="a3b06-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a3b06-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3b06-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3b06-124">-Name</span></span>
<span data-ttu-id="a3b06-125">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="a3b06-125">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="a3b06-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b06-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3b06-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a3b06-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="a3b06-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3b06-128">-ResourceId</span></span>
<span data-ttu-id="a3b06-129">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a3b06-129">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="a3b06-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b06-130">CommonParameters</span></span>
<span data-ttu-id="a3b06-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3b06-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b06-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3b06-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b06-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3b06-133">INPUTS</span></span>

### <span data-ttu-id="a3b06-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a3b06-134">System.String</span></span>

## <span data-ttu-id="a3b06-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3b06-135">OUTPUTS</span></span>

### <span data-ttu-id="a3b06-136">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a3b06-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="a3b06-137">Microsoft. Azure. Command. EventGrid. models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="a3b06-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="a3b06-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3b06-138">NOTES</span></span>

## <span data-ttu-id="a3b06-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3b06-139">RELATED LINKS</span></span>
