---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 3454a3aad2276384588c0ccc550a1b0ef6df7cfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670877"
---
# <span data-ttu-id="5757f-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="5757f-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="5757f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5757f-102">SYNOPSIS</span></span>
<span data-ttu-id="5757f-103">Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5757f-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="5757f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5757f-104">SYNTAX</span></span>

### <span data-ttu-id="5757f-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5757f-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5757f-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5757f-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5757f-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5757f-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5757f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5757f-108">DESCRIPTION</span></span>
<span data-ttu-id="5757f-109">Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5757f-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="5757f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5757f-110">EXAMPLES</span></span>

### <span data-ttu-id="5757f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5757f-111">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="5757f-112">Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="5757f-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5757f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5757f-113">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="5757f-114">Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="5757f-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5757f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5757f-115">PARAMETERS</span></span>

### <span data-ttu-id="5757f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5757f-116">-DefaultProfile</span></span>
<span data-ttu-id="5757f-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5757f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5757f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5757f-118">-InputObject</span></span>
<span data-ttu-id="5757f-119">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="5757f-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="5757f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5757f-120">-Name</span></span>
<span data-ttu-id="5757f-121">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="5757f-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="5757f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5757f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5757f-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="5757f-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="5757f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5757f-124">-ResourceId</span></span>
<span data-ttu-id="5757f-125">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5757f-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="5757f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5757f-126">CommonParameters</span></span>
<span data-ttu-id="5757f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5757f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5757f-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5757f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5757f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5757f-129">INPUTS</span></span>

### <span data-ttu-id="5757f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5757f-130">System.String</span></span>

### <span data-ttu-id="5757f-131">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5757f-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="5757f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5757f-132">OUTPUTS</span></span>

### <span data-ttu-id="5757f-133">Microsoft. Azure. Management. EventGrid. models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="5757f-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="5757f-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5757f-134">NOTES</span></span>

## <span data-ttu-id="5757f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5757f-135">RELATED LINKS</span></span>
