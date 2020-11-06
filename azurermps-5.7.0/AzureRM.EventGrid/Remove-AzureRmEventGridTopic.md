---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: aa9ef35ec0571628eb209163e91c9415706b57a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495371"
---
# <span data-ttu-id="ef3ec-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="ef3ec-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="ef3ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ef3ec-103">Azure-esemény rácsvonal-témakörének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ef3ec-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef3ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef3ec-104">SYNTAX</span></span>

### <span data-ttu-id="ef3ec-105">TopicNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef3ec-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3ec-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef3ec-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3ec-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef3ec-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef3ec-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef3ec-108">DESCRIPTION</span></span>
<span data-ttu-id="ef3ec-109">Azure-esemény rácsvonal-témakörének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ef3ec-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="ef3ec-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ef3ec-110">EXAMPLES</span></span>

### <span data-ttu-id="ef3ec-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ef3ec-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="ef3ec-112">Eltávolítja az esemény rács témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ef3ec-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ef3ec-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ef3ec-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="ef3ec-114">Eltávolítja az esemény rács témakör \` téma1 \` az erőforráscsoport \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ef3ec-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ef3ec-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef3ec-115">PARAMETERS</span></span>

### <span data-ttu-id="ef3ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef3ec-116">-DefaultProfile</span></span>
<span data-ttu-id="ef3ec-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ef3ec-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef3ec-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef3ec-118">-InputObject</span></span>
<span data-ttu-id="ef3ec-119">EventGrid-téma objektuma</span><span class="sxs-lookup"><span data-stu-id="ef3ec-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ef3ec-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef3ec-120">-Name</span></span>
<span data-ttu-id="ef3ec-121">EventGrid a téma neve</span><span class="sxs-lookup"><span data-stu-id="ef3ec-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="ef3ec-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef3ec-122">-PassThru</span></span>
<span data-ttu-id="ef3ec-123">Az eltávolítási művelet állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ef3ec-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="ef3ec-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ef3ec-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef3ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef3ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef3ec-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ef3ec-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="ef3ec-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef3ec-127">-ResourceId</span></span>
<span data-ttu-id="ef3ec-128">EventGrid téma ResourceID.</span><span class="sxs-lookup"><span data-stu-id="ef3ec-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef3ec-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef3ec-129">-Confirm</span></span>
<span data-ttu-id="ef3ec-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef3ec-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef3ec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef3ec-131">-WhatIf</span></span>
<span data-ttu-id="ef3ec-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef3ec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef3ec-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef3ec-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef3ec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef3ec-134">CommonParameters</span></span>
<span data-ttu-id="ef3ec-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef3ec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef3ec-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef3ec-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef3ec-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef3ec-137">INPUTS</span></span>

### <span data-ttu-id="ef3ec-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ef3ec-138">System.String</span></span>
<span data-ttu-id="ef3ec-139">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ef3ec-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="ef3ec-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef3ec-140">OUTPUTS</span></span>

### <span data-ttu-id="ef3ec-141">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="ef3ec-141">System.Object</span></span>

## <span data-ttu-id="ef3ec-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef3ec-142">NOTES</span></span>

## <span data-ttu-id="ef3ec-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef3ec-143">RELATED LINKS</span></span>

