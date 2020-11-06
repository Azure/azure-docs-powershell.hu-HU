---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 8ea4fc7674af247ffded2c6c4317f07a831adf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501868"
---
# <span data-ttu-id="9ccf4-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="9ccf4-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="9ccf4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ccf4-102">SYNOPSIS</span></span>
<span data-ttu-id="9ccf4-103">Az aktuális Azure-előfizetésből kinyeri az esemény rácsvonalait ismertető témakör részleteit</span><span class="sxs-lookup"><span data-stu-id="9ccf4-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ccf4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ccf4-104">SYNTAX</span></span>

### <span data-ttu-id="9ccf4-105">ResourceGroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ccf4-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ccf4-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ccf4-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ccf4-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ccf4-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ccf4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ccf4-108">DESCRIPTION</span></span>
<span data-ttu-id="9ccf4-109">A Get-AzureRmEventGridTopic parancsmag az aktuális Azure-előfizetésből származó adott esemény rácsvonalait ismerteti, vagy az aktuális Azure-előfizetésben lévő összes esemény rácsos témakörének listáját.</span><span class="sxs-lookup"><span data-stu-id="9ccf4-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="9ccf4-110">Ha a téma neve meg van határozva, az egyetlen esemény rácsa témakör részleteit adja vissza a program.</span><span class="sxs-lookup"><span data-stu-id="9ccf4-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="9ccf4-111">Ha a téma neve nincs megadva, a program a témakörök listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="9ccf4-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="9ccf4-112">Példák</span><span class="sxs-lookup"><span data-stu-id="9ccf4-112">EXAMPLES</span></span>

### <span data-ttu-id="9ccf4-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ccf4-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="9ccf4-114">Az téma1 MyResourceGroupName az esemény rácsa témakör részleteit kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="9ccf4-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9ccf4-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="9ccf4-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="9ccf4-116">Az téma1 MyResourceGroupName az esemény rácsa témakör részleteit kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="9ccf4-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9ccf4-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="9ccf4-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="9ccf4-118">Az erőforráscsoportok MyResourceGroupName az esemény Rácsával kapcsolatos témakörök felsorolása \` \` .</span><span class="sxs-lookup"><span data-stu-id="9ccf4-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9ccf4-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="9ccf4-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="9ccf4-120">Az előfizetésben szereplő összes esemény rácsvonal-témakörének listázása</span><span class="sxs-lookup"><span data-stu-id="9ccf4-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="9ccf4-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ccf4-121">PARAMETERS</span></span>

### <span data-ttu-id="9ccf4-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ccf4-122">-Name</span></span>
<span data-ttu-id="9ccf4-123">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="9ccf4-123">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="9ccf4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ccf4-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ccf4-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9ccf4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9ccf4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ccf4-126">-ResourceId</span></span>
<span data-ttu-id="9ccf4-127">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9ccf4-127">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="9ccf4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ccf4-128">-DefaultProfile</span></span>
<span data-ttu-id="9ccf4-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ccf4-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ccf4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ccf4-130">CommonParameters</span></span>
<span data-ttu-id="9ccf4-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ccf4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ccf4-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ccf4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ccf4-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ccf4-133">INPUTS</span></span>

### <span data-ttu-id="9ccf4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9ccf4-134">System.String</span></span>
<span data-ttu-id="9ccf4-135">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="9ccf4-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="9ccf4-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ccf4-136">OUTPUTS</span></span>

### <span data-ttu-id="9ccf4-137">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="9ccf4-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="9ccf4-138">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. EventGrid. models. PSTopicListInstance, Microsoft. Azure. commands. EventGrid, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9ccf4-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9ccf4-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ccf4-139">NOTES</span></span>

## <span data-ttu-id="9ccf4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ccf4-140">RELATED LINKS</span></span>

