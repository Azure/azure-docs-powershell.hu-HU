---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187460"
---
# <span data-ttu-id="923c4-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="923c4-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="923c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="923c4-102">SYNOPSIS</span></span>
<span data-ttu-id="923c4-103">Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="923c4-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="923c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="923c4-104">SYNTAX</span></span>

### <span data-ttu-id="923c4-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="923c4-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="923c4-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="923c4-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="923c4-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="923c4-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="923c4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="923c4-108">DESCRIPTION</span></span>
<span data-ttu-id="923c4-109">Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="923c4-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="923c4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="923c4-110">EXAMPLES</span></span>

### <span data-ttu-id="923c4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="923c4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="923c4-112">Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="923c4-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="923c4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="923c4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="923c4-114">Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="923c4-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="923c4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="923c4-115">PARAMETERS</span></span>

### <span data-ttu-id="923c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923c4-116">-DefaultProfile</span></span>
<span data-ttu-id="923c4-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="923c4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="923c4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="923c4-118">-InputObject</span></span>
<span data-ttu-id="923c4-119">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="923c4-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="923c4-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="923c4-120">-Name</span></span>
<span data-ttu-id="923c4-121">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="923c4-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="923c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="923c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="923c4-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="923c4-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="923c4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="923c4-124">-ResourceId</span></span>
<span data-ttu-id="923c4-125">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="923c4-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="923c4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923c4-126">CommonParameters</span></span>
<span data-ttu-id="923c4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="923c4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923c4-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="923c4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923c4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="923c4-129">INPUTS</span></span>

### <span data-ttu-id="923c4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="923c4-130">System.String</span></span>

### <span data-ttu-id="923c4-131">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="923c4-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="923c4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="923c4-132">OUTPUTS</span></span>

### <span data-ttu-id="923c4-133">Microsoft. Azure. Management. EventGrid. models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="923c4-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="923c4-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="923c4-134">NOTES</span></span>

## <span data-ttu-id="923c4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="923c4-135">RELATED LINKS</span></span>
