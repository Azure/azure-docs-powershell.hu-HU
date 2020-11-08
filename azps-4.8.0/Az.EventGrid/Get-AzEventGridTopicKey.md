---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025349"
---
# <span data-ttu-id="e87a1-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="e87a1-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="e87a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e87a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e87a1-103">Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e87a1-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="e87a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e87a1-104">SYNTAX</span></span>

### <span data-ttu-id="e87a1-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e87a1-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e87a1-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e87a1-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e87a1-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e87a1-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e87a1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e87a1-108">DESCRIPTION</span></span>
<span data-ttu-id="e87a1-109">Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e87a1-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="e87a1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e87a1-110">EXAMPLES</span></span>

### <span data-ttu-id="e87a1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e87a1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="e87a1-112">Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="e87a1-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e87a1-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e87a1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="e87a1-114">Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="e87a1-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e87a1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e87a1-115">PARAMETERS</span></span>

### <span data-ttu-id="e87a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e87a1-116">-DefaultProfile</span></span>
<span data-ttu-id="e87a1-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e87a1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e87a1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e87a1-118">-InputObject</span></span>
<span data-ttu-id="e87a1-119">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="e87a1-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="e87a1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e87a1-120">-Name</span></span>
<span data-ttu-id="e87a1-121">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="e87a1-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="e87a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e87a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="e87a1-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e87a1-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="e87a1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e87a1-124">-ResourceId</span></span>
<span data-ttu-id="e87a1-125">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e87a1-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="e87a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e87a1-126">CommonParameters</span></span>
<span data-ttu-id="e87a1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e87a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e87a1-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e87a1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e87a1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e87a1-129">INPUTS</span></span>

### <span data-ttu-id="e87a1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e87a1-130">System.String</span></span>

### <span data-ttu-id="e87a1-131">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="e87a1-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="e87a1-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e87a1-132">OUTPUTS</span></span>

### <span data-ttu-id="e87a1-133">Microsoft. Azure. Management. EventGrid. models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="e87a1-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="e87a1-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e87a1-134">NOTES</span></span>

## <span data-ttu-id="e87a1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e87a1-135">RELATED LINKS</span></span>
