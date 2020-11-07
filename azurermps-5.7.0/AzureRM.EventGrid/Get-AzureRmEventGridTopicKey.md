---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 741a888287ba7fcb4a9b54c1281a6a27be5fbb0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679740"
---
# <span data-ttu-id="eb7e6-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="eb7e6-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="eb7e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7e6-103">Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eb7e6-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb7e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb7e6-104">SYNTAX</span></span>

### <span data-ttu-id="eb7e6-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb7e6-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb7e6-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb7e6-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb7e6-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb7e6-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb7e6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb7e6-108">DESCRIPTION</span></span>
<span data-ttu-id="eb7e6-109">Az események esemény rácsvonal-témához való közzétételekor használható megosztott hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eb7e6-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="eb7e6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="eb7e6-110">EXAMPLES</span></span>

### <span data-ttu-id="eb7e6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb7e6-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="eb7e6-112">Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="eb7e6-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="eb7e6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="eb7e6-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="eb7e6-114">Az téma1 MyResourceGroupName az esemény rácsa témakör megosztott hozzáférés kulcsait kapja \` \` meg \` \` .</span><span class="sxs-lookup"><span data-stu-id="eb7e6-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="eb7e6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb7e6-115">PARAMETERS</span></span>

### <span data-ttu-id="eb7e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7e6-116">-DefaultProfile</span></span>
<span data-ttu-id="eb7e6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="eb7e6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb7e6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb7e6-118">-InputObject</span></span>
<span data-ttu-id="eb7e6-119">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="eb7e6-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="eb7e6-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb7e6-120">-Name</span></span>
<span data-ttu-id="eb7e6-121">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="eb7e6-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="eb7e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb7e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="eb7e6-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="eb7e6-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="eb7e6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb7e6-124">-ResourceId</span></span>
<span data-ttu-id="eb7e6-125">Az esemény rács témakörét megadó erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="eb7e6-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="eb7e6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7e6-126">CommonParameters</span></span>
<span data-ttu-id="eb7e6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb7e6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7e6-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb7e6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7e6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb7e6-129">INPUTS</span></span>

### <span data-ttu-id="eb7e6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eb7e6-130">System.String</span></span>

## <span data-ttu-id="eb7e6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb7e6-131">OUTPUTS</span></span>

### <span data-ttu-id="eb7e6-132">Microsoft. Azure. Management. EventGrid. models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="eb7e6-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="eb7e6-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb7e6-133">NOTES</span></span>

## <span data-ttu-id="eb7e6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb7e6-134">RELATED LINKS</span></span>

