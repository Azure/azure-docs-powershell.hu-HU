---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: a20262e1414b8f747e638f22283aed26b5483896
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497480"
---
# <span data-ttu-id="0a8a2-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="0a8a2-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="0a8a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a8a2-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8a2-103">Új Azure-esemény rácsvonal-témakörének létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a8a2-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a8a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a8a2-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a8a2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a8a2-105">DESCRIPTION</span></span>
<span data-ttu-id="0a8a2-106">Új Azure-esemény rácsvonal-témakörének létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a8a2-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="0a8a2-107">Miután létrehozta a témát, az alkalmazás közzéteheti az eseményeket a téma végpontjának segítségével.</span><span class="sxs-lookup"><span data-stu-id="0a8a2-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="0a8a2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0a8a2-108">EXAMPLES</span></span>

### <span data-ttu-id="0a8a2-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0a8a2-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="0a8a2-110">A \` \` megadott földrajzi hely \` westus2 \` , az erőforráscsoport- \` MyResourceGroupName \` létrehoz egy esemény rácshoz tartozó téma1.</span><span class="sxs-lookup"><span data-stu-id="0a8a2-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0a8a2-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="0a8a2-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="0a8a2-112">A megadott \` \` földrajzi hely \` westus2 \` , az erőforráscsoport \` MyResourceGroupName \` a megadott címkéket a "részleg" és a "környezet" téma1 hozza létre az esemény táblázatát.</span><span class="sxs-lookup"><span data-stu-id="0a8a2-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="0a8a2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a8a2-113">PARAMETERS</span></span>

### <span data-ttu-id="0a8a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8a2-114">-DefaultProfile</span></span>
<span data-ttu-id="0a8a2-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a8a2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a8a2-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="0a8a2-116">-Location</span></span>
<span data-ttu-id="0a8a2-117">A témakör helye</span><span class="sxs-lookup"><span data-stu-id="0a8a2-117">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8a2-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a8a2-118">-Name</span></span>
<span data-ttu-id="0a8a2-119">A témakör neve.</span><span class="sxs-lookup"><span data-stu-id="0a8a2-119">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a8a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="0a8a2-121">Az az erőforráscsoport, amelyben a témakört létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="0a8a2-121">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8a2-122">-Címke</span><span class="sxs-lookup"><span data-stu-id="0a8a2-122">-Tag</span></span>
<span data-ttu-id="0a8a2-123">Hashtables, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="0a8a2-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8a2-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a8a2-124">-Confirm</span></span>
<span data-ttu-id="0a8a2-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a8a2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a8a2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a8a2-126">-WhatIf</span></span>
<span data-ttu-id="0a8a2-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a8a2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a8a2-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a8a2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a8a2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8a2-129">CommonParameters</span></span>
<span data-ttu-id="0a8a2-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a8a2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8a2-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a8a2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8a2-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a8a2-132">INPUTS</span></span>

### <span data-ttu-id="0a8a2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0a8a2-133">System.String</span></span>

### <span data-ttu-id="0a8a2-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0a8a2-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0a8a2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a8a2-135">OUTPUTS</span></span>

### <span data-ttu-id="0a8a2-136">Microsoft. Azure. Command. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="0a8a2-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="0a8a2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a8a2-137">NOTES</span></span>

## <span data-ttu-id="0a8a2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a8a2-138">RELATED LINKS</span></span>
