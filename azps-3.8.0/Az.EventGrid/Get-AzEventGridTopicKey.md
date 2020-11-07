---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: a956e0e99db44e5f92b4d9ec772158b262434c05
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846082"
---
# <span data-ttu-id="c18a5-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="c18a5-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="c18a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c18a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c18a5-103">Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c18a5-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="c18a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c18a5-104">SYNTAX</span></span>

### <span data-ttu-id="c18a5-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c18a5-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c18a5-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c18a5-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c18a5-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c18a5-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c18a5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c18a5-108">DESCRIPTION</span></span>
<span data-ttu-id="c18a5-109">Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c18a5-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="c18a5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c18a5-110">EXAMPLES</span></span>

### <span data-ttu-id="c18a5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c18a5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="c18a5-112">Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="c18a5-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c18a5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c18a5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="c18a5-114">Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="c18a5-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c18a5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c18a5-115">PARAMETERS</span></span>

### <span data-ttu-id="c18a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c18a5-116">-DefaultProfile</span></span>
<span data-ttu-id="c18a5-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c18a5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c18a5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c18a5-118">-InputObject</span></span>
<span data-ttu-id="c18a5-119">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="c18a5-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c18a5-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c18a5-120">-Name</span></span>
<span data-ttu-id="c18a5-121">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="c18a5-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c18a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c18a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="c18a5-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c18a5-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="c18a5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c18a5-124">-ResourceId</span></span>
<span data-ttu-id="c18a5-125">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c18a5-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="c18a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c18a5-126">CommonParameters</span></span>
<span data-ttu-id="c18a5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c18a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c18a5-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c18a5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c18a5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c18a5-129">INPUTS</span></span>

### <span data-ttu-id="c18a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c18a5-130">System.String</span></span>

### <span data-ttu-id="c18a5-131">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c18a5-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="c18a5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c18a5-132">OUTPUTS</span></span>

### <span data-ttu-id="c18a5-133">Microsoft. Azure. Management. EventGrid. models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c18a5-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="c18a5-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c18a5-134">NOTES</span></span>

## <span data-ttu-id="c18a5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c18a5-135">RELATED LINKS</span></span>
